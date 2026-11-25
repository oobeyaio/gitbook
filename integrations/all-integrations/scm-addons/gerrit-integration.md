---
description: Learn about Gerrit & Oobeya integration.
icon: calculator-simple
---

# Gerrit Integration

This guide provides a step-by-step walkthrough to integrate your **Gerrit** code review system with **Oobeya** to track engineering metrics and DORA analytics.

***

#### 1. Create Gerrit HTTP Credentials 🔑

To allow Oobeya to access your Gerrit repositories, you need to generate an HTTP access token.

1. **Access Settings:** Click the user icon in the top-right corner of your Gerrit UI, navigate to **Settings**.
2. **Generate Token:** Open the **"HTTP Credentials"** tab on the left sidebar and click the **"Generate New Password"** button.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fz2IpvfG94IG6miv3zkOW%2Fimage.png?alt=media&#x26;token=17296043-053b-44f7-8707-d5f955ce912b" alt=""><figcaption></figcaption></figure>

3. **Secure Your Password:** Copy and save the generated password immediately. You will need this for the Oobeya data source configuration.

***

### 2. Connect Gerrit in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Source Code Management** section, click the **Gerrit** card. If Gerrit already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Gerrit V1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                        |
| -------------------- | ------------------------------------------------------------ |
| **Data Source Name** | A name you choose for this connection, for example _Gerrit_. |
| **Server URL**       | Your Gerrit URL, for example `https://gerrit.example.com`.   |
| **Username**         | Your Gerrit username.                                        |
| **Token**            | The HTTP password from step 1.                               |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FlOnDBEFMubRfRY3UJ9K6%2Fform-gerrit.png?alt=media&#x26;token=9b816aff-d51d-4ce9-9e44-10a510c79ec7" alt="Gerrit data source form in Oobeya"><figcaption><p>The Gerrit data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

#### Ready to Connect 🚀

**Congratulations!** Oobeya is now connected to your Gerrit server. It will begin pulling real-time statistics from your repositories to track development velocity, code review cycles, and team performance.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
