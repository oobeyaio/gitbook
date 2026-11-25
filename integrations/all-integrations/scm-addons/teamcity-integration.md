---
description: Learn about TeamCity & Oobeya integration...
icon: plug
---

# TeamCity Integration

### 1. **Generate** TeamCity **API Token**

1. Open TeamCity and click on the "Profile" button.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F6QYekXJVV9sNsqKNMz9R%2Fimage.png?alt=media&#x26;token=17ecca32-daca-4d42-b5d3-64b059f8d4b0" alt=""><figcaption></figcaption></figure>

2\. Click on the "Access Tokens" button on the left and then the "Create access token" button.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fa9aeKD7BLso14l4irqlc%2Fimage.png?alt=media&#x26;token=a6c80abe-cebb-423e-8738-6080ceceddb5" alt=""><figcaption></figcaption></figure>

3\. Give a name to your token and then store it securely.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FUZ29fPxlatSpMSh4Svxh%2Fimage.png?alt=media&#x26;token=b5712b0f-946b-4f37-846c-ac423fd8152b" alt=""><figcaption></figcaption></figure>

### 2. Connect TeamCity in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **CI/CD** section, click the **TeamCity** card. If TeamCity already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **TeamCity 2018.1+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                          |
| -------------------- | -------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _TeamCity_. |
| **Server URL**       | Your TeamCity URL, for example `https://teamcity.example.com`. |
| **Token**            | The access token from step 1.                                  |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FXUfDs7GlKvB9FkZSrNQ2%2Fform-teamcity.png?alt=media&#x26;token=64ecbb16-f654-44a3-855b-c81b9d53d3f9" alt="TeamCity data source form in Oobeya"><figcaption><p>The TeamCity data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Now Oobeya is connected with your own TeamCity server to monitor the health status of your pipelines and track key metrics such as _time-to-fix, average deployment duration_...

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
