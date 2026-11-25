---
description: Learn about Bitbucket Server & Oobeya integration.
icon: bitbucket
---

# Bitbucket Server Integration

### 1. Connect Bitbucket Server in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Source Code Management** section, click the **Bitbucket** card. If Bitbucket Server already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Bitbucket 5+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                                         |
| -------------------- | --------------------------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Bitbucket Server_.                        |
| **Server URL**       | The URL of your Bitbucket Server or Data Center, for example `https://bitbucket.example.com`. |
| **Username**         | A Bitbucket user with read access to the repositories.                                        |
| **Password**         | The password of that user.                                                                    |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FXPWaF7AtcOYltf6IHSZm%2Fform-bitbucket-server.png?alt=media&#x26;token=cba0cb6a-4f63-43cb-a14e-2b6d5abc2a3d" alt="Bitbucket Server data source form in Oobeya"><figcaption><p>The Bitbucket Server data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Now Oobeya is connected with your own Bitbucket Server to get the real-time statistics of your code repositories to track each development activity.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
