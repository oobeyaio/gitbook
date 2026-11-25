---
description: Learn about GitHub & Oobeya integration.
icon: github
---

# GitHub Integration

There four options to integrate [Oobeya](https://oobeya.io) with [GitHub](https://github.com).

1. **Option 1:** [Use a Personal Access Token](https://docs.oobeya.io/integrations/all-integrations/scm-addons/github-integrations#id-1.-generate-github-personal-access-token)
2. **Option 2:** [Use the official Oobeya GitHub App from the GitHub Marketplace.](https://docs.oobeya.io/integrations/all-integrations/scm-addons/step-by-step-integration-instructions-for-the-oobeya-github-application#option-1-using-the-official-oobeya-github-app)
3. **Option 3:** [Register your own GitHub application.](https://docs.oobeya.io/integrations/all-integrations/scm-addons/step-by-step-integration-instructions-for-the-oobeya-github-application#option-2-registering-your-own-github-application)
4. **Option 4:** [Use a GitHub App Installation Token](https://docs.oobeya.io/integrations/all-integrations/scm-addons/step-by-step-integration-instructions-for-the-oobeya-github-application#option-3-using-a-github-app-installation-token)

***

### 1. G**enerate GitHub Personal Access Token**

1. Navigate to GitHub **Settings** and click the **"Developer Settings"** tab.
2. Select the **"Personal access tokens"** tab, **"Tokens (classic)"**, **"Generate new token"** and **"Generate new token (classic)"** button. Select _**read**_ permissions for the connection.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FvosP09HxDNgGsCaaPycR%2Fimage.png?alt=media&#x26;token=dd1e8a24-dad5-41eb-86da-6784fc84200a" alt=""><figcaption></figcaption></figure>

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fj1kzOV1BSuBZJcHtJS17%2Fimage.png?alt=media&#x26;token=9d49c588-fba0-4c81-9110-9ab6d64e81be" alt=""><figcaption></figcaption></figure>

3\. Copy and save the _**access token**_ to use it on the Oobeya data source connection.

### 2. Connect GitHub in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Source Code Management** section, click the **GitHub** card. If GitHub already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **GitHub Rest API V3+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                   |
| -------------------- | ----------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _GitHub - Platform_. |
| **Token**            | The personal access token from step 1.                                  |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F30zNyxVLn7RhEPTXUzL1%2Fform-github.png?alt=media&#x26;token=1c903515-444b-4df3-bca9-dc1587028c2c" alt="GitHub data source form in Oobeya"><figcaption><p>The GitHub data source form on the Integrations page.</p></figcaption></figure>

The version list also offers **Oobeya GitHub App**, **Own GitHub App**, and **Installation Token**; see [Step-by-Step Integration Instructions for the Oobeya GitHub Application](https://docs.oobeya.io/integrations/all-integrations/scm-addons/step-by-step-integration-instructions-for-the-oobeya-github-application). GitHub appears under **Project Management**, **Source Code Management**, and **CI/CD**; it is the same integration in each.

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Following these steps, you can integrate the Oobeya seamlessly with your GitHub account, enhancing your development workflow with insightful metrics and data such as [DORA metrics](https://oobeya.io/dora-metrics-four-key/) and [pull request metrics](https://oobeya.io/oobeya-metric-definitions/).

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
