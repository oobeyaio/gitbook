---
description: Learn about Sentry & Oobeya Integration.
---

# Sentry Integration

### 1. Generate Sentry Auth Token

1. Click on your **account** name on Sentry and select the "**API keys**" as in the following:

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F02MyNKdx6EC4OSpB9seu%2Ffile.png?alt=media)

2\. Click to the "**Create New Token**" button:

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fg8cOw0U6XLkbBb8Z6vl6%2Ffile.png?alt=media)

3\. Configure the "**Scopes**" area by selecting permissions and then click the "**Create Token**" button.

![Inserting image...](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FbiL51gPGL9GYDblzgT2q%2Ffile.png?alt=media)

4\. Copy and save the auth token.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FaEoYHdQaKLCuzuhLyA4A%2Ffile.png?alt=media)

### 2. Connect Sentry in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Monitoring/APM** section, click the **Sentry** card. If Sentry already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Sentry v0** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                        |
| -------------------- | ------------------------------------------------------------ |
| **Data Source Name** | A name you choose for this connection, for example _Sentry_. |
| **Server URL**       | The URL of your Sentry instance.                             |
| **Token**            | The auth token from step 1.                                  |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fm2pGUBcXo6bUjxsovySl%2Fform-sentry.png?alt=media&#x26;token=26bd5a4c-d950-4289-a35d-fb17382da1d7" alt="Sentry data source form in Oobeya"><figcaption><p>The Sentry data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### Ready to Connect

Now Oobeya is connected with your own **Sentry** account to diagnose, fix, and optimize the performance of the code.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
