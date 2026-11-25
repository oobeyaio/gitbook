---
description: Learn about GitLab & Oobeya integration.
icon: gitlab
---

# GitLab Integration

### 1. **Create GitLab Access Token**

1. Navigate to GitLab **Settings** and click the **"Access Tokens"** tab.
2. Select _**read**_ permissions for the connection and click the **"Create personal access token"** button.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FmbU5bPqLafKgvMjjxiqA%2Ffile.png?alt=media)

3\. Copy and save the _access token_ to use on the Oobeya data source connection.

### 2. Connect GitLab in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Source Code Management** section, click the **GitLab** card. If GitLab already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **GitLab 9+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                        |
| -------------------- | ------------------------------------------------------------ |
| **Data Source Name** | A name you choose for this connection, for example _GitLab_. |
| **Server URL**       | `https://gitlab.com` or the URL of your self-managed GitLab. |
| **Token**            | The access token from step 1.                                |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fnm61yoIyrBGylHAxNqqx%2Fform-gitlab.png?alt=media&#x26;token=e08b75bc-08cb-4a50-9d0f-f3e57feeff09" alt="GitLab data source form in Oobeya"><figcaption><p>The GitLab data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Now Oobeya is connected with your own GitLab server to get the real-time statistics of your code repositories to track each development activity.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
