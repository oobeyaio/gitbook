---
description: Learn about GitHub Enterprise & Oobeya integration...
icon: github
---

# GitHub Enterprise Integration

Use the **GitHub Enterprise** integration for a self-hosted **GitHub Enterprise Server**. For github.com, including GitHub Enterprise Cloud, use the [GitHub integration](https://docs.oobeya.io/integrations/all-integrations/scm-addons/github-integrations).

GitHub Enterprise feeds repositories, pull requests, issues, and Actions data into Git analytics, project analytics, and DORA metrics. It appears under **Project Management**, **Source Code Management**, and **CI/CD** on the Integrations page; it is the same integration in each.

### 1. Create a personal access token on GitHub Enterprise Server

1. On your GitHub Enterprise Server, open **Settings** > **Developer settings** > **Personal access tokens**.
2. Generate a new token with **read** permissions, as described for GitHub in [Generate GitHub Personal Access Token](https://docs.oobeya.io/integrations/all-integrations/scm-addons/github-integrations#id-1.-generate-github-personal-access-token).
3. Copy the token. You need it in the next step.

### 2. Connect GitHub Enterprise in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Source Code Management** section, click the **Github Enterprise** card. If GitHub Enterprise already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **GithubEnterprise Rest API V3+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                               |
| -------------------- | ----------------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _GitHub Enterprise_.             |
| **Server URL**       | The URL of your GitHub Enterprise Server, for example `https://github.example.com`. |
| **Token**            | The personal access token from step 1.                                              |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FAqZOLbj6awStGnZYkmMU%2Fform-github-enterprise.png?alt=media&#x26;token=67d47964-e37e-499a-b30c-1a0d66741297" alt="GitHub Enterprise data source form in Oobeya"><figcaption><p>The GitHub Enterprise data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
