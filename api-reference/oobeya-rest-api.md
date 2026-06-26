---
description: >-
  Enable secure, programmatic access to your Software Engineering Intelligence
  Platform. Automate analyses, synchronize integrations, and retrieve metrics.
---

# Oobeya REST API

Oobeya provides a secure REST API that allows you to programmatically access and manage data across your **Software Engineering Intelligence Platform**.\
You can automate processes, synchronize integrations, trigger analyses, and extract metrics for custom dashboards or reporting.

***

### 1. Overview

The **Oobeya REST API v1** exposes endpoints to manage organizations, users, teams, analyses, deployments, reports, and more.

Each endpoint follows REST principles and returns data in **JSON** format.

{% hint style="info" %}
All requests must be made over **HTTPS**.\
Your API key or bearer token must be included in the header for every request.
{% endhint %}

**To access Swagger docs in Oobeya directly**, go to&#x20;

```
{OOBEYA_BASE_URL}/apis/docs/swagger-ui/index.html
```

***

### 2. Base URL

```
{OOBEYA_BASE_URL}
```

Example:

```
https://mycompany.oobeya.io
https://oobeya.mycompany.com
```

***

### 3. Authentication

Oobeya supports two authentication mechanisms:

<table><thead><tr><th width="146.3560791015625">Method</th><th width="374.6915283203125">Header</th><th>Description</th></tr></thead><tbody><tr><td>API Key</td><td><code>Oobeya-API-Key: &#x3C;your_api_key></code></td><td>Used for integrations and service-to-service access</td></tr><tr><td>Bearer Token</td><td><code>Authorization: Bearer &#x3C;your_jwt_token></code></td><td>Used for authenticated user sessions</td></tr></tbody></table>

**Example:**

```bash
curl -X GET "{OOBEYA_BASE_URL}/apis/v1/users" \
  -H "Oobeya-API-Key: <your_api_key>"
```

***

### 4. Endpoint Groups

#### 4.1. Organization Level

<table><thead><tr><th width="125.32440185546875">Method</th><th>Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>GET</code></td><td><code>/apis/v1/organization-level</code></td><td>Retrieve organization levels</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/organization-level</code></td><td>Create a new organization level</td></tr><tr><td><code>PUT</code></td><td><code>/apis/v1/organization-level/{id}</code></td><td>Update an existing organization level</td></tr></tbody></table>

**Example:**

```bash
curl -X POST "{OOBEYA_BASE_URL}/apis/v1/organization-level" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Division",
    "level": 2,
    "leadRoles": [
      { "key": "ENG_LEAD", "label": "Engineering Lead" }
    ]
  }'
```

***

#### 4.2. Users

<table><thead><tr><th width="141.55303955078125">Method</th><th width="263.49072265625">Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>GET</code></td><td><code>/apis/v1/users</code></td><td>List users with pagination</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/users</code></td><td>Create a new user</td></tr><tr><td><code>PUT</code></td><td><code>/apis/v1/users</code></td><td>Update user information</td></tr><tr><td><code>GET</code></td><td><code>/apis/v1/users/{id}</code></td><td>Retrieve a specific user</td></tr><tr><td><code>DELETE</code></td><td><code>/apis/v1/users/{id}</code></td><td>Delete a user</td></tr></tbody></table>

**Example: Create a User**

```bash
curl -X POST "{OOBEYA_BASE_URL}/apis/v1/users" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Josh",
    "surname": "Long",
    "username": "josh.long",
    "email": "josh.long@oobeya.io",
    "userType": "DB",
    "companyRole": "DEVELOPER",
    "hireDate": "2024-08-17T00:00:00+03:00"
  }'
```

***

#### 4.3. Teams

<table><thead><tr><th width="149.76910400390625">Method</th><th>Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>GET</code></td><td><code>/apis/v1/teams</code></td><td>List all teams with pagination</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/teams</code></td><td>Create a new team</td></tr><tr><td><code>PUT</code></td><td><code>/apis/v1/teams</code></td><td>Update an existing team</td></tr><tr><td><code>PATCH</code></td><td><code>/apis/v1/teams/{team-id-or-name}</code></td><td>Partially update a team</td></tr><tr><td><code>GET</code></td><td><code>/apis/v1/teams/all</code></td><td>Retrieve all teams</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/teams/trigger-analysis</code></td><td>Trigger Git &#x26; DORA analysis for selected teams</td></tr></tbody></table>

**Example: Trigger Analysis**

```bash
curl -X POST "{OOBEYA_BASE_URL}/apis/v1/teams/trigger-analysis" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{
    "teamIds": ["team-123"],
    "trigger": { "git": true, "pullRequest": true, "deployment": true }
  }'
```

***

#### 4.4. Git Analysis

Track repository data, pull requests, and DORA metrics.

<table><thead><tr><th width="147.41937255859375">Method</th><th>Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>GET</code></td><td><code>/apis/v1/analysis</code></td><td>List Git analyses</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/analysis</code></td><td>Create a new analysis</td></tr><tr><td><code>DELETE</code></td><td><code>/apis/v1/analysis/{analysisId}</code></td><td>Delete an analysis</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/analysis/trigger-all-dora-analyses</code></td><td>Trigger bulk DORA analyses</td></tr><tr><td><code>GET</code></td><td><code>/apis/v1/analysis/dora-summary-metrics</code></td><td>Retrieve aggregated DORA metrics summary</td></tr></tbody></table>

**Example: Get DORA Summary**

```bash
curl -X GET "{OOBEYA_BASE_URL}/apis/v1/analysis/dora-summary-metrics?widgets=DORA_METRICS_SUMMARY&teamId=team-123" \
  -H "Oobeya-API-Key: <your_api_key>"
```

**Sample Response**

```json
{
  "leadTimeForChanges": { "formattedValue": "2.3 days" },
  "deploymentFrequency": { "formattedValue": "3 per week" },
  "changeFailureRate": { "formattedValue": "5%" },
  "timeToRestore": { "formattedValue": "4h 30m" }
}
```

***

#### 4.5. Deployments

<table><thead><tr><th width="152.432861328125">Method</th><th>Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>GET</code></td><td><code>/apis/v1/deployments</code></td><td>Retrieve deployments with pagination</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/deployments</code></td><td>Create new deployment record</td></tr><tr><td><code>DELETE</code></td><td><code>/apis/v1/deployments/{id}</code></td><td>Delete deployment</td></tr></tbody></table>

***

#### 4.6. Reports

<table><thead><tr><th width="107.50872802734375">Method</th><th width="381.5850830078125">Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>GET</code></td><td><code>/apis/v1/reports/team/{teamId}/commits</code></td><td>Get team-based commit metrics</td></tr><tr><td><code>GET</code></td><td><code>/apis/v1/reports/team/{teamId}/pull-requests</code></td><td>Get team-based PR metrics</td></tr><tr><td><code>GET</code></td><td><code>/apis/v1/reports/team/{teamId}/qualities</code></td><td>Get team-based quality metrics</td></tr><tr><td><code>GET</code></td><td><code>/apis/v1/reports/member/{memberId}/commits</code></td><td>Get member-based commit metrics</td></tr><tr><td><code>GET</code></td><td><code>/apis/v1/reports/member/{memberId}/pull-requests</code></td><td>Get member-based PR metrics</td></tr></tbody></table>

**Example: Get Team Pull Request Metrics**

```bash
curl -X GET "{OOBEYA_BASE_URL}/apis/v1/reports/team/team-123/pull-requests?startDate=2025-01-01&endDate=2025-01-31" \
  -H "Oobeya-API-Key: <your_api_key>"
```

***

#### 4.7. Qwiser (SonarQube Integration)

<table><thead><tr><th width="118.23583984375">Method</th><th width="388.5977783203125">Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>POST</code></td><td><code>/apis/v1/qwiser/analysis</code></td><td>Start a new Qwiser analysis</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/qwiser/analysis/list</code></td><td>List existing analyses</td></tr><tr><td><code>PUT</code></td><td><code>/apis/v1/qwiser/analysis/{analysisId}/teams</code></td><td>Update associated teams</td></tr></tbody></table>

***

#### 4.8. External Test Metrics

<table><thead><tr><th width="123.58233642578125">Method</th><th width="371.5352783203125">Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>POST</code></td><td><code>/apis/v1/test/external/execution</code></td><td>Create execution record</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/test/external/defect</code></td><td>Create defect record</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/test/external/coverage</code></td><td>Create coverage record</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/test/external/bug</code></td><td>Create bug record</td></tr></tbody></table>

**Example: Create Test Execution**

```bash
curl -X POST "{OOBEYA_BASE_URL}/apis/v1/test/external/execution" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{
    "executionId": "exec-12345",
    "status": "PASS",
    "executionTime": 120000,
    "executionStartDate": "2025-09-11T08:47:40.740Z",
    "executionEndDate": "2025-09-11T08:49:40.740Z",
    "applicationId": "app-98765",
    "scenarioId": "scn-4567",
    "scenarioName": "Login Test",
    "environment": "staging",
    "team": "QA-Team"
  }'
```

***

#### 4.9. Bulk Operations

<table><thead><tr><th width="128.30743408203125">Method</th><th width="332.44873046875">Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>POST</code></td><td><code>/apis/v1/bulk/analyses</code></td><td>Prepare bulk Git analyses</td></tr><tr><td><code>PUT</code></td><td><code>/apis/v1/bulk/analyses/sync</code></td><td>Synchronize analyses</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/bulk/analyses/analysis</code></td><td>Import new Git analysis file</td></tr></tbody></table>

***

#### 4.10. API Keys

<table><thead><tr><th width="136.7984619140625">Method</th><th>Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>GET</code></td><td><code>/apis/v1/api-keys</code></td><td>List all API keys</td></tr><tr><td><code>POST</code></td><td><code>/apis/v1/api-keys</code></td><td>Create a new API key</td></tr><tr><td><code>DELETE</code></td><td><code>/apis/v1/api-keys/{id}</code></td><td>Delete an API key</td></tr></tbody></table>

***

#### 4.11. System

<table><thead><tr><th width="133.6175537109375">Method</th><th>Endpoint</th><th>Description</th></tr></thead><tbody><tr><td><code>GET</code></td><td><code>/apis/v1/systems/logs</code></td><td>Retrieve system logs</td></tr><tr><td><code>DELETE</code></td><td><code>/apis/v1/systems/clear-git-analyses</code></td><td>Clear analyses older than 2 years</td></tr></tbody></table>

***

### 5. Best Practices

* Use **API keys** for automation, and **JWT tokens** for user-based integrations.
* Implement **retry logic** with exponential backoff for network errors.
* Cache frequent GET responses to optimize performance.
* Regularly **rotate API keys** for security.
* Use **bulk operations** when importing or syncing large datasets.

***

**Support Contact:** support@oobeya.io
