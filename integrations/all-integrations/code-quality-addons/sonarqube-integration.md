---
description: >-
  The Oobeya–Sonar Integration connects SonarQube Server and SonarQube Cloud
  with Oobeya’s Engineering Intelligence Platform, turning code quality and
  security data into actionable insights.
---

# SonarQube Server Integration

Delivering **high-quality software** requires continuous attention to **code reliability, security, and maintainability**. By integrating [**SonarQube Server**](https://www.sonarsource.com/) with [**Oobeya**](https://oobeya.io), your teams gain end-to-end visibility into code quality, technical debt, and maintainability trends — all in one place.

***

#### 1. Generate a SonarQube Server User Token

A **User Token** allows Oobeya to connect to your SonarQube Server instance and retrieve project data securely.

{% hint style="info" %}
The token creation process has been updated.\
For the official reference, see: [Generating and Using Tokens](https://docs.sonarsource.com/sonarqube-server/user-guide/managing-tokens)
{% endhint %}

**Steps:**

1. Log in to your **SonarQube Server** instance.
2. Click your **user avatar** (top-right corner) → select **My Account** → open the **Security** tab.
3. Under **Generate Tokens**, enter a **token name** (e.g., `oobeya-integration`).
4. Select **"User Token"** as token type.
5. Click **Generate**.
6. Copy and **store the token securely** — it’s shown only once.

{% hint style="info" %}
The token should belong to a user with at least **Browse** access to all relevant projects. For organization-wide visibility, use a user account with **Admin** permissions.
{% endhint %}

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FSRZyeeJAQqMSDZGkNaHa%2Fimage.png?alt=media&#x26;token=c1c9bb67-857e-48b6-80c5-21765cf94405" alt=""><figcaption><p>Generating a new user token</p></figcaption></figure>

***

### 2. Connect SonarQube Server in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Code Quality & Security** section, click the **SonarQube Server** card. If SonarQube Server already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Sonar 6+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                   |
| -------------------- | ----------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _SonarQube Server_.  |
| **Server URL**       | Your SonarQube Server URL, for example `https://sonarqube.example.com`. |
| **Token**            | The user token from step 1.                                             |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FCGIWq3MJVotDXBgQzVIy%2Fform-sonarqube-server.png?alt=media&#x26;token=a6a3cf69-ac28-49ab-8340-c440d914244f" alt="SonarQube Server data source form in Oobeya"><figcaption><p>The SonarQube Server data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

#### 3. Explore Your Code Quality Insights

After integration, Oobeya continuously imports your **SonarQube metrics**, including:

* **Code Quality Issues**
* **Quality Gate Status**
* **Technical Debt**
* **Maintainability, Reliability, and Security Ratings**

You can explore this data in:

* **Dashboards** — for overall visibility

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FJlKQQ2eDGm8eSzqPZ3fX%2Fimage.png?alt=media&#x26;token=c7ba2797-1fe6-4aad-bac1-f3ad27476e58" alt=""><figcaption><p>Improved visibility and ownership for better code quality and security</p></figcaption></figure>

* **Organizational, Team, and Individual Scorecards** — to track trends and KPIs

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FsD91TH29lh6Pf6t9y4Ax%2Fimage.png?alt=media&#x26;token=2db5cde2-3786-44da-8b68-45d2d6d3a2a7" alt=""><figcaption><p>Sonarqube metrics in Team Scorecards</p></figcaption></figure>

* **Engineering Insights / Symptoms** — to proactively detect unhealthy code practices **-** [_learn more here_](https://docs.oobeya.io/use-cases/proactive-issue-detection)_._<br>

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FfHlXLua9Qx96i9VSBnrI%2Fimage.png?alt=media&#x26;token=4650bf21-1cf6-4f5a-b075-2449e01444e5" alt=""><figcaption><p>Code Quality Insights: Auto-detected Symptoms</p></figcaption></figure>

* **Gamification -** [_learn more here_](https://docs.oobeya.io/use-cases/gamification-for-engineering-kpis)_._

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FjQ8S7p1dE3ISmWzvZimB%2Fimage.png?alt=media&#x26;token=e51efeaf-d291-4c48-be9e-c420ceec6e8f" alt=""><figcaption><p>Leveraging gamification to improve code quality</p></figcaption></figure>

***

#### 4. Troubleshooting

If your connection test fails or data is missing, review the following checks:

<table><thead><tr><th width="183.75469970703125">Issue</th><th width="195.8480224609375">Possible Cause</th><th>Solution</th></tr></thead><tbody><tr><td><strong>401 Unauthorized</strong></td><td>Invalid or expired token</td><td>Regenerate a valid User Token and update the Data Source.</td></tr><tr><td><strong>Connection Timeout</strong></td><td>Firewall or proxy blocking requests</td><td>Ensure outbound access to your SonarQube server from Oobeya’s network.</td></tr><tr><td><strong>No Projects Found</strong></td><td>Token lacks permissions</td><td>Verify the token user has project “Browse” or “Admin” permissions.</td></tr><tr><td><strong>SSL Error</strong></td><td>Invalid SSL certificate</td><td>Use a valid SSL certificate or enable trusted certificate configuration.</td></tr><tr><td><strong>Data Outdated</strong></td><td>Sync delay or rate limit</td><td>Trigger a manual re-sync or check your SonarQube server performance.</td></tr></tbody></table>

**💬 Still need help?**\
Contact Oobeya Support or reach out to your Customer Success Manager.

***

#### Summary: Connect in 5 Steps

<table><thead><tr><th width="83.13421630859375">Step</th><th width="329.26531982421875">Action</th><th>Result</th></tr></thead><tbody><tr><td>1</td><td>Generate a User Token in SonarQube</td><td>Secure authentication</td></tr><tr><td>2</td><td>Install the SonarQube Server Add-on in Oobeya</td><td>Enable integration</td></tr><tr><td>3</td><td>Add a Data Source</td><td>Connect Oobeya to your SonarQube server</td></tr><tr><td>4</td><td>View Dashboards and Scorecards</td><td>Monitor real-time code quality</td></tr></tbody></table>

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
