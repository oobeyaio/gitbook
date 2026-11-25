---
description: Learn about Jira Cloud & Oobeya integration.
icon: jira
---

# Jira Cloud Integration

### 1. **Generate Jira Cloud API Token**

1. Click on the **profile** picture at the top right of the screen, then select **Account Settings**.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FbJT79Dk5G6ERsBMk17Ej%2Ffile.png?alt=media)

2\. Open the "Security" tab.

![Select Security tab.](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FdnJTMy2uk35njnI22hpk%2Ffile.png?alt=media)

3\. Click the link "**Create and manage API tokens**" under the API Token section.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F0mpsKeUqc89JaOJOoVZv%2Ffile.png?alt=media)

4\. Click the "**Create API token**" button at the top of the page.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FknosWWLqYDAZWUeyJEce%2Fimage.png?alt=media&#x26;token=6a34b4f5-aeb2-47c9-99ae-c751cea3438f" alt=""><figcaption></figcaption></figure>

5. Make sure you copy your new API token for further use.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FnWGTWW2c9BAliG4HqEwx%2Fimage.png?alt=media&#x26;token=148bc2d8-ecab-46b5-99cc-7fd8e148b4b9" alt=""><figcaption></figcaption></figure>

### 2. Connect Jira Cloud in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Project Management** section, click the **Jira** card. If Jira Cloud already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Jira V2** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                 | Value                                                                   |
| --------------------- | ----------------------------------------------------------------------- |
| **Data Source Name**  | A name you choose for this connection, for example _Jira Cloud_.        |
| **Server URL**        | Your Jira Cloud site, for example `https://your-company.atlassian.net`. |
| **Access Type**       | **Basic**.                                                              |
| **Username / E-mail** | The e-mail address of the Atlassian account that owns the API token.    |
| **Password / Token**  | The API token from step 1.                                              |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FCgBcQzIBi0ckrGvKIwbZ%2Fform-jira.png?alt=media&#x26;token=167e231b-d7d0-4ba6-98f1-5dc71d68c176" alt="Jira Cloud data source form in Oobeya"><figcaption><p>The Jira Cloud data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Now Oobeya is connected with your own Jira Cloud account to get the real-time project management data of your organization.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
