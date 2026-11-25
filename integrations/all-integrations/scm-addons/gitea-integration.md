---
description: Learn about Gitea & Oobeya Integration
icon: mug-tea
---

# Gitea Integration

This guide provides a step-by-step walkthrough to integrate your **Gitea** code review system with **Oobeya** to track engineering metrics and DORA analytics.

***

#### 1. Create Gitea Access Tokens 🔑

To allow Oobeya to access your Gitea repositories, you need to generate an access token.

1. **Settings:** Click the user icon in the top-right corner of your Gitea UI, navigate to **Settings**.
2. **Generate Token:** Open the **"HTTP Credentials"** tab on the left sidebar and click the **"Generate New Password"** button.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FYBG1HWqH2jt6mABtoaJS%2Ffoto1.png?alt=media&#x26;token=27304a7d-78db-4195-bec8-db393b948238" alt=""><figcaption></figcaption></figure>

3. **Secure Your Password:** Copy and save the generated password immediately. You will need this for the Oobeya data source configuration.

***

### 2. Connect Gitea in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Source Code Management** section, click the **Gitea** card. If Gitea already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Gitea 1.19.4** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                       |
| -------------------- | ----------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Gitea_. |
| **Server URL**       | Your Gitea URL, for example `https://gitea.example.com`.    |
| **Token**            | The access token from step 1.                               |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F2hv7HHaJJ1L06ep6IyOU%2Fform-gitea.png?alt=media&#x26;token=1668be8f-5b85-46d6-baa7-03849ad3c125" alt="Gitea data source form in Oobeya"><figcaption><p>The Gitea data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

#### Ready to Connect 🚀

**Congratulations!** Oobeya is now connected to your Gitea server. It will begin pulling real-time statistics from your repositories to track development velocity, code review cycles, and team performance.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
