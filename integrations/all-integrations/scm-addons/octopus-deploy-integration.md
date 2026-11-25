---
description: >-
  Learn about Octopus Deploy & Oobeya Integration. This guide will walk you
  through the steps required to integrate Octopus Deploy with Oobeya.
icon: octopus-deploy
---

# Octopus Deploy Integration

#### 1. Getting the Integration URL

* Retrieve the base URL for your Octopus Deploy server directly from your browser. This URL is the address shown in the browser's address bar (e.g. `https://<your-octopus-server>`).

***

#### 2. Getting the Integration API Key

1. Log in to **Octopus Deploy**.
2. Click on your **profile icon** at the bottom left of the sidebar.
3. Select **My profile** from the menu.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FMOIxVXYEnVdEBjBNGrd8%2Fimage.png?alt=media&#x26;token=4c019514-28fe-4286-b8bb-f6344a14b40a" alt="" width="188"><figcaption></figcaption></figure>

4. On the **My Profile** page, go to the **My API Keys** tab.
5. Click **New API Key** to generate a new API key.
6. Copy the generated key — you will need it to configure the data source in Oobeya.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Ft0nUDsxxhvYxdATr2yHq%2Fimage.png?alt=media&#x26;token=57c812f8-8279-49f3-87d5-184ba972082b" alt=""><figcaption></figcaption></figure>

> **Note:** API keys allow automated tools like Oobeya to connect to Octopus without recording your personal password. Store the key securely, as it will only be shown once.

***

### 3. Connect Octopus Deploy in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **CI/CD** section, click the **Octopus Deploy** card. If Octopus Deploy already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Octopus v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                |
| -------------------- | -------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Octopus Deploy_. |
| **Server URL**       | The URL from step 1.                                                 |
| **Token**            | The API key from step 2.                                             |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FZV5Y9kBNJrSKQsOjq6pO%2Fform-octopus-deploy.png?alt=media&#x26;token=ca0c76b5-ba4b-4c4a-83fb-820d27167208" alt="Octopus Deploy data source form in Oobeya"><figcaption><p>The Octopus Deploy data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

#### Ready to Connect 🐙

Your Oobeya instance is now connected to your Octopus Deploy account. You can begin tracking and analyzing your deployment processes with Oobeya's analysis tools.

#### **Ready to Connect**

Now Oobeya is connected to your own Octopus Deploy account/server to enable you to track accurate DORA metrics calculated by Oobeya Deployment Analytics.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
