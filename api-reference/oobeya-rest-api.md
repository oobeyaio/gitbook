---
description: >-
  Enable secure, programmatic access to your Software Engineering Intelligence
  Platform. Automate analyses, synchronize integrations, and retrieve metrics.
---

# Oobeya REST API

The Oobeya REST API gives scripts and other tools the same data and actions you use in the Oobeya UI. Use it to manage users, members, and teams, start analyses, send deployments, production failures, test results, problems, and custom metrics from any tool, and read team and member reports.

{% hint style="info" %}
Every endpoint, with its parameters and request and response schemas, is listed in the **API reference** pages under this page. Each Oobeya instance also serves its own interactive Swagger UI at `https://<your-oobeya-host>/apis/docs/swagger-ui/index.html`.
{% endhint %}

### Base URL

All endpoints live under `/apis/v1` on your Oobeya host:

```
https://<your-oobeya-host>/apis/v1
```

For example `https://mycompany.oobeya.io/apis/v1` (SaaS) or `https://oobeya.mycompany.com/apis/v1` (on-premise). Requests and responses use JSON over HTTPS.

### Authentication

Send an API key in the `Oobeya-API-Key` header of every request.

```bash
curl "https://<your-oobeya-host>/apis/v1/teams/all" \
  -H "Oobeya-API-Key: <your_api_key>"
```

1. Sign in with an **Administrator** account and select **Administration** > **API Keys**.
2. Generate a token with the **Full API** scope. **Ingest (Collector)** tokens are not accepted by the REST API.
3. Copy the token right away; it is shown only once. See [API Keys](https://docs.oobeya.io/administration/api-keys).

The **API Keys** endpoints themselves (`/apis/v1/api-keys`) are the exception: they need the bearer token of a signed-in user in the `Authorization: Bearer <token>` header.

{% hint style="warning" %}
Treat an API key like a password: store it in a secret manager, never in source code, and revoke it in **Administration** > **API Keys** when it is no longer needed.
{% endhint %}

### Pagination and sorting

List endpoints take `page` (0-based), `size`, and, where supported, `sort` in the form `field:ASC` or `field:DESC`:

```bash
curl "https://<your-oobeya-host>/apis/v1/teams?page=0&size=50&sort=unitName:ASC" \
  -H "Oobeya-API-Key: <your_api_key>"
```

Paged responses return the items with `page`, `size`, `totalElements`, `totalPages`, and `isLast`. Some endpoints keep `size` between 1 and 100. Dates and times use ISO 8601, for example `2026-06-15T10:00:00.000Z`.

### What you can do

| Area                           | Endpoints                                                                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| **Organization**               | Organization levels, users, members (developer profiles), teams and their hierarchy, company roles, team scorecards        |
| **Analyses**                   | Git analyses, DORA analyses, code quality (SonarQube) analyses, board analyses, bulk imports, onboarding                   |
| **Send data from other tools** | Deployments, production failures (defect detection), test executions, coverage, defects and bugs, problems, custom metrics |
| **Reports**                    | Team and member commits, pull requests, quality, DORA, and onboarding metrics                                              |
| **Administration**             | API keys, system logs, clean-up of old Git analysis data                                                                   |

### Common tasks

#### Send a deployment from any CI/CD tool

Deployments sent through the API count in the DORA metrics of the analysis they belong to.

```bash
curl -X POST "https://<your-oobeya-host>/apis/v1/deployments" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{
    "analysisId": "<git-analysis-id>",
    "cloneUrl": "https://git.example.com/payments/payment-api.git",
    "name": "payment-api",
    "title": "Release 2.4.0",
    "targetBranch": "main",
    "lastCommitSha": "9f2c1e7",
    "deploymentType": "RELEASE",
    "analysisType": "PULL_REQUEST",
    "pipelineStartAt": "2026-06-15T09:40:00.000Z",
    "deployedAt": "2026-06-15T10:00:00.000Z"
  }'
```

`deploymentType` is `RELEASE` or `HOTFIX`; `analysisType` is `PULL_REQUEST` or `TRUNK_BASED`. List Git analyses with `GET /apis/v1/analysis` to find the `analysisId`.

#### Report a production failure and its fix

Defect detections feed Change Failure Rate and Time to Restore Service. Send the record when the failure is detected and again with `fixedDate` when it is fixed; records are matched by `id` or by your own `externalKey`.

```bash
curl -X POST "https://<your-oobeya-host>/apis/v1/defect-detections" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{
    "externalKey": "INC-4711",
    "repoName": "payment-api",
    "environment": "production",
    "description": "Payments fail after release 2.4.0",
    "detectedDate": "2026-06-15T10:30:00.000Z",
    "detectedDeploymentTitle": "Release 2.4.0"
  }'
```

#### Read a team's DORA metrics

```bash
curl "https://<your-oobeya-host>/apis/v1/reports/team/<team-id>/dora?startDate=2026-06-01&endDate=2026-06-30" \
  -H "Oobeya-API-Key: <your_api_key>"
```

The response holds `leadTimeForChanges`, `deploymentFrequency`, `changeFailureRate`, and `timeToRestore`, each with a `value` and a `formattedValue`. Add `includeRepositoryDetail=true` for a per-repository breakdown. The same pattern works for `/commits`, `/pull-requests`, and `/qualities`, and for a single member under `/reports/team/<team-id>/member/<member-id>/qualities` or `/reports/member/<member-id>/...`.

#### Trigger the analyses of a team

```bash
curl -X POST "https://<your-oobeya-host>/apis/v1/teams/trigger-analysis" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{ "teamIds": ["<team-id>"], "trigger": { "git": true, "pullRequest": true, "deployment": true } }'
```

#### Send a custom metric

Custom metrics appear on custom dashboards and team views as cards, charts, or tables.

```bash
curl -X POST "https://<your-oobeya-host>/apis/v1/custom-metrics/card" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{
    "team": "Payments Team",
    "metricCategory": "Portfolio Management",
    "metricKey": "initial_planned_delivery",
    "metricDisplayName": "Initial Planned Delivery",
    "metricStartDate": "2026-06-01",
    "metricEndDate": "2026-06-30",
    "metricValue": 42,
    "unit": "COUNT",
    "aggregationType": "SUM",
    "decreaseIsGood": false
  }'
```

`unit` is `COUNT`, `AVERAGE`, `PERCENT`, `STRING`, or `TEXT`; `aggregationType` is `SUM`, `AVERAGE`, or `LAST`. Use `/custom-metrics/chart` for a time series and `/custom-metrics/table` for rows of columns.

#### Send a test execution

```bash
curl -X POST "https://<your-oobeya-host>/apis/v1/test/external/execution" \
  -H "Oobeya-API-Key: <your_api_key>" \
  -H "Content-Type: application/json" \
  -d '{
    "executionId": "exec-12345",
    "status": "PASS",
    "executionTime": 120000,
    "executionStartDate": "2026-06-15T08:47:40.740Z",
    "executionEndDate": "2026-06-15T08:49:40.740Z",
    "actionDate": "2026-06-15T08:49:40.740Z",
    "applicationId": "app-98765",
    "scenarioId": "scn-4567",
    "scenarioName": "Login Test",
    "environment": "staging",
    "team": "QA Team"
  }'
```

`status` is `TODO`, `EXECUTING`, `FAIL`, `PASS`, or `ABORTED`. See [Test Otomasyon Metrikleri ve API Dokümanı](https://docs.oobeya.io/test-analytics/test-otomasyon-metrikleri-ve-api-dokumani) for test metrics.

#### Send a problem

Problems sent with `POST /apis/v1/problem` appear in [Problem Analytics](https://docs.oobeya.io/problem-analytics/problem-analytics). The required fields are `externalId`, `applicationId`, `applicationName`, `status`, and `updatedAt`; send the same `externalId` again to update a problem.

### Good practice

* Use one API key per integration so that you can revoke it without breaking the others.
* Retry network errors with exponential backoff, and keep bulk imports for large data sets.
* Read only the period you need; report endpoints take a date range.
* Rotate API keys regularly.

### Related

* [API Keys](https://docs.oobeya.io/administration/api-keys)
* [Oobeya MCP](https://docs.oobeya.io/mcp/oobeya-mcp): ask about the same data from your AI tool.
