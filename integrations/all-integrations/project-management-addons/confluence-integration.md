---
description: >-
  Connect Confluence Cloud or Confluence Server / Data Center to Oobeya for
  Document Analytics.
---

# Confluence Integration

Oobeya reads space and page metadata from Confluence (creation and update dates, versions, and contributors) and reports documentation health in [Document Analytics](https://docs.oobeya.io/document-analytics/document-analytics-confluence). Both **Confluence Cloud** (since Oobeya 2.1) and **Confluence Server / Data Center** are supported. Confluence is in the **Project Management** category of the Integrations page.

### 1. Prepare the credentials

* **Confluence Cloud:** use the e-mail address of an Atlassian account and an [Atlassian API token](https://id.atlassian.com/manage-profile/security/api-tokens) of that account.
* **Confluence Server / Data Center:** use a Confluence user's username and password, or a personal access token.

The account needs read access to the spaces you want to analyze.

### 2. Connect Confluence in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Project Management** section, click the **Confluence** card. If Confluence already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Confluence v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                                                                               |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Confluence Cloud_.                                                              |
| **Server URL**       | The address of your Confluence Cloud site or of your Confluence Server / Data Center, for example `https://confluence.example.com`. |
| **Username**         | The Atlassian account e-mail (Cloud) or the Confluence username (Server / Data Center).                                             |
| **Password / Token** | The API token (Cloud), or the password or personal access token (Server / Data Center).                                             |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fuorzz6K9GTJoVrWMx1qf%2Fform-confluence.png?alt=media&#x26;token=f65c2d01-e89b-4e4e-aca8-fdde3d12565f" alt="Confluence data source form in Oobeya"><figcaption><p>The Confluence data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Next Steps**

* [Document Analytics (Confluence)](https://docs.oobeya.io/document-analytics/document-analytics-confluence)
* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
