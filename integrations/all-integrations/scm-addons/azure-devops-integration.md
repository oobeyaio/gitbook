---
description: Learn about Azure DevOps & Oobeya integration.
icon: windows
---

# Azure DevOps Integration

{% hint style="info" %}
Oobeya **Azure DevOps addon** is compatible with both Azure DevOps Services (cloud) and Azure DevOps Server (TFS2017, TFS2018, TFS2019).
{% endhint %}

### **1. Create Azure DevOps Personal Access Token**

1\. Navigate to **User Settings** and click **"Personal Access Tokens"**.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FhmDVE5PtAmUpx0mUOg2i%2Ffile.png?alt=media)

2\. Click the _**"New Token"**_ button and select _**read**_ permissions for the connection.

The required permissions are:

* Build – _Read_
* Code – _Read_
* Project and Team – _Read_
* Pull Request Threads – _Read_
* Release – _Read_
* Test Management – _Read_
* Work Items – _Read_

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FnK8bOYmMxQfrGHpgDJbL%2Ffile.png?alt=media)

3\. Copy and save the _access token_ to use it on the Oobeya data source connection.

### 2. Connect Azure DevOps in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Source Code Management** section, click the **Azure DevOps** card. If Azure DevOps already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **AzureDevops 5+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                                                                       |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Azure DevOps - Production_.                                             |
| **Server URL**       | Your organization URL, for example `https://dev.azure.com/{your-organization}`, or your Azure DevOps Server collection URL. |
| **Token**            | The Personal Access Token from step 1.                                                                                      |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FixiZyEb5uhEpBjtANf6D%2Fform-azure-devops.png?alt=media&#x26;token=db091888-2e74-4c72-ad60-07a53968f12e" alt="Azure DevOps data source form in Oobeya"><figcaption><p>The Azure DevOps data source form on the Integrations page.</p></figcaption></figure>

Azure DevOps appears under **Project Management**, **Source Code Management**, and **CI/CD**; it is the same integration in each. For older Azure DevOps Server versions, select **AzureDevops 4.1**.

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Now Oobeya is connected with your own Azure DevOps to get the real-time statistics of your code repositories to track each development activity.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
