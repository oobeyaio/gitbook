---
description: Connect Jira Xray test management tool to the Oobeya Test Analytics module.
---

# Xray Integration

### Overview

Xray integration allows Oobeya to:

* Analyze **manual test results** from Xray projects.
* Track **UAT success and escaped defects** across projects.
* Measure **team-level testing efficiency** and defect resolution performance.
* Display metrics and trends in **Team Health > Scorecards** and organization dashboards.

***

### Prerequisites

Before starting the integration:

* You must have an active Jira instance with the **Xray plugin** installed.
* Your user account must have permission to access Xray APIs.
* An **API Token** or **Basic Auth** credentials are required.

***

### Authentication Methods

Oobeya supports both authentication types depending on your Jira environment:

<table><thead><tr><th width="236.4971923828125">Environment</th><th width="336.054443359375">Authentication Type</th></tr></thead><tbody><tr><td><strong>Xray Cloud</strong></td><td>API Token or Basic Auth</td></tr><tr><td><strong>Xray Server / DC</strong></td><td>API Token or Basic Auth</td></tr></tbody></table>

{% hint style="info" %}
&#x20;For Xray Cloud users, you can generate your API token from Atlassian Account → Security → API Tokens.
{% endhint %}

***

### Setting up the Integration

#### Step 1 — Enable Xray Plugin

Go to `Integrations → Test → Xray` and make sure the Xray addon is **installed**.

#### Step 2 — Add Data Source

1. Navigate to `Data Sources`.
2. Click **Xray** addon and click **New Data Source**.
3. Fill in the connection details:

<table><thead><tr><th width="158.52154541015625">Field</th><th width="293.4365234375">Description</th><th width="315.4296875">Example</th></tr></thead><tbody><tr><td><strong>Data Source Name</strong></td><td>A custom name for your connection.</td><td>Company Xray Server</td></tr><tr><td><strong>Server URL</strong></td><td>Base URL of your Jira Xray instance.</td><td><p>Server: <code>https://JIRA_SERVER_URL</code> </p><p>Cloud: <code>https://yourcompany.atlassian.net</code></p></td></tr><tr><td><strong>Access Type</strong></td><td>Choose <strong>Basic</strong> or <strong>Token</strong>.</td><td>-</td></tr><tr><td><strong>Username / Email</strong></td><td>Your Jira username or email address.</td><td>test@company.com</td></tr><tr><td><strong>Password / Token</strong></td><td>Jira password or API token.</td><td>●●●●●●●</td></tr></tbody></table>

4. Click **Test Connection** to validate credentials.
5. Once the connection succeeds, click **Add** to save.

<figure><img src="https://docs.oobeya.io/assets/xray-datasource-setup.png" alt=""><figcaption><p>Xray Data Source Configuration</p></figcaption></figure>

***

### How It Works

Once connected, Oobeya can retrieve and process data from Xray:

* **Test Executions** – total test runs, status (pass/fail), duration, and owner.
* **Test Cases** – manual test details and associated UAT mappings.
* **Defects** – linked or related bugs for each test execution.

This data is normalized and displayed within the **Test Analytics** module.

***

### Troubleshooting

| Issue                  | Possible Cause               | Resolution                                  |
| ---------------------- | ---------------------------- | ------------------------------------------- |
| Connection test fails  | Wrong URL or expired token   | Recheck credentials and API token validity. |
| No test data retrieved | Insufficient API permissions | Ensure your Jira user has Xray API access.  |
