---
description: Learn about Jira Server & Oobeya integration.
icon: jira
---

# Jira Server Integration

### 1. Connect Jira Server in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Project Management** section, click the **Jira** card. If Jira Server already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Jira V2** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                 | Value                                                                                                  |
| --------------------- | ------------------------------------------------------------------------------------------------------ |
| **Data Source Name**  | A name you choose for this connection, for example _Jira Server_.                                      |
| **Server URL**        | The URL of your Jira Server or Data Center, for example `https://jira.example.com`.                    |
| **Access Type**       | **Basic** (username and password) or **Bearer** (personal access token; the username field is hidden). |
| **Username / E-mail** | A Jira user with read access to the projects (Basic only).                                             |
| **Password / Token**  | The user's password, or the personal access token for Bearer.                                          |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FCgBcQzIBi0ckrGvKIwbZ%2Fform-jira.png?alt=media&#x26;token=167e231b-d7d0-4ba6-98f1-5dc71d68c176" alt="Jira Server data source form in Oobeya"><figcaption><p>The Jira Server data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Now Oobeya is connected with your own Jira Server account to get the real-time project management data of your organization.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
