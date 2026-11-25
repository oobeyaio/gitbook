---
description: Connect Jira Xray test management tool to the Oobeya Test Analytics module.
---

# Xray Integration

#### Overview

Xray integration allows Oobeya to:

* Analyze **manual test results** from Xray projects.
* Track **UAT success and escaped defects** across projects.
* Measure **team-level testing efficiency** and defect resolution performance.
* Display metrics and trends in **Team Health > Scorecards** and organization dashboards.

***

#### Prerequisites

Before starting the integration:

* You must have an active Jira instance with the **Xray plugin** installed.
* Your user account must have permission to access Xray APIs.
* An **API Token** or **Basic Auth** credentials are required.

***

#### Authentication Methods

Oobeya supports both authentication types depending on your Jira environment:

<table><thead><tr><th width="236.4971923828125">Environment</th><th width="336.054443359375">Authentication Type</th></tr></thead><tbody><tr><td><strong>Xray Server / DC</strong></td><td>API Token or Basic Auth</td></tr></tbody></table>

***

#### Setting up the Integration

**Add the Xray data source**

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Test** section, click the **Xray** card. If Xray already has data sources, click **+ New Data Source** in the window that opens.
3. Fill in the connection details:

<table><thead><tr><th width="158.52154541015625">Field</th><th width="293.4365234375">Description</th><th width="315.4296875">Example</th></tr></thead><tbody><tr><td><strong>Data Source Name</strong></td><td>A custom name for your connection.</td><td>Company Xray Server</td></tr><tr><td><strong>Server URL</strong></td><td>Base URL of your Jira Xray instance.</td><td>Server: <code>https://JIRA_SERVER_URL</code></td></tr><tr><td><strong>Access Type</strong></td><td>Choose <strong>Basic</strong> (username and password or API token) or <strong>Bearer</strong> (personal access token; the username field is hidden).</td><td>-</td></tr><tr><td><strong>Username / Email</strong></td><td>Your Jira username or email address.</td><td>test@company.com</td></tr><tr><td><strong>Password / Token</strong></td><td>Jira password or API token.</td><td>●●●●●●●</td></tr></tbody></table>

4. Click **Test Connection** to validate credentials.
5. Once the connection succeeds, click **Add** to save.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FzyJQa8vJxcPeK6mcTk3e%2Fform-xray.png?alt=media&#x26;token=a1733347-3f40-4913-bba7-772bf47f5871" alt="Xray data source form in Oobeya"><figcaption><p>The Xray data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

***

#### How It Works

Once connected, Oobeya can retrieve and process data from Xray:

* **Test Executions** – total test runs, status (pass/fail), duration, and owner.
* **Test Cases** – manual test details and associated UAT mappings.
* **Defects** – linked or related bugs for each test execution.

This data is normalized and displayed within the **Test Analytics** module.

***

#### Troubleshooting

| Issue                  | Possible Cause               | Resolution                                  |
| ---------------------- | ---------------------------- | ------------------------------------------- |
| Connection test fails  | Wrong URL or expired token   | Recheck credentials and API token validity. |
| No test data retrieved | Insufficient API permissions | Ensure your Jira user has Xray API access.  |

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
