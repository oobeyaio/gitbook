---
description: Learn about Jenkins & Oobeya integration.
icon: jenkins
---

# Jenkins & Cloudbees Integration

### 1. **Generate Jenkins API Token**

1\. On Jenkins, open the user dropdown at the top right and click the **"Security"** option.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FOODRGLpChJIq34IeVwWv%2Fimage.png?alt=media&#x26;token=2b84d16c-6252-4369-8482-d7845c8bca4b" alt=""><figcaption></figcaption></figure>

2\. Generate a new API Token by clicking "Add new token".

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F5Xti0ppB67xUgS82dYIl%2Fimage.png?alt=media&#x26;token=de45d22c-b89d-43ce-bcd4-0e484bf02d5c" alt=""><figcaption></figcaption></figure>

3\. Copy and save the _API Token_ to use on the Oobeya data source connection.

### 2. Connect Jenkins in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **CI/CD** section, click the **Jenkins** card. If Jenkins already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Jenkins 2+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                     |
| -------------------- | ------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Jenkins_.             |
| **Server URL**       | Your Jenkins or CloudBees URL, for example `https://jenkins.example.com`. |
| **Username**         | The Jenkins user that owns the API token.                                 |
| **Token**            | The API token from step 1.                                                |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FrwKopnOFGJX2ktIZZxdj%2Fform-jenkins.png?alt=media&#x26;token=008b6417-c4a1-48a0-a56f-c85314106083" alt="Jenkins data source form in Oobeya"><figcaption><p>The Jenkins data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Now Oobeya is connected with your own Jenkins server to monitor the health status of your pipelines and track key metrics such as _time-to-fix, average deployment duration..._

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
