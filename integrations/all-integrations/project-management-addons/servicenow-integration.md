---
description: >-
  Connect ServiceNow to Oobeya to analyze incidents, change requests, and other
  work items.
---

# ServiceNow Integration

ServiceNow is an IT service management platform where teams record incidents and change requests. Oobeya reads these records as work items for Project Analytics. ServiceNow is in the **Project Management** category of the Integrations page.

### 1. Prepare a ServiceNow user

Oobeya connects to the ServiceNow REST API with a username and password. Create (or choose) a ServiceNow user that can read the records you want to analyze, for example incidents and change requests. Use a dedicated integration user with read-only roles where possible.

### 2. Connect ServiceNow in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Project Management** section, click the **ServiceNow** card. If ServiceNow already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **ServiceNow v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                             |
| -------------------- | --------------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _ServiceNow_.                  |
| **Server URL**       | Your ServiceNow instance URL, for example `https://your-company.service-now.com`. |
| **Username**         | The ServiceNow user from step 1.                                                  |
| **Password**         | The password of that user.                                                        |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FCCPsLZWR0syfQdC6LRfi%2Fform-servicenow.png?alt=media&#x26;token=33f01c12-50c3-4ef0-8e0f-3062e3c145d3" alt="ServiceNow data source form in Oobeya"><figcaption><p>The ServiceNow data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### 3. Choose the work item types and state field

In **Administration** > **Projects & Boards** (**Analytics** section), the **ServiceNow** tab decides which ServiceNow records are analyzed:

* **Work Item Type**: only the selected ServiceNow work item types are retrieved through the API and included in metric calculations.
* **Work Item State (ServiceNow)**: the ServiceNow field whose values Oobeya reads as the state of each work item.

Changing one of these settings resets the analysis, so its results change.

### **Next Steps**

* [Project Analytics](https://docs.oobeya.io/project-analytics/project-analytics)
* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
