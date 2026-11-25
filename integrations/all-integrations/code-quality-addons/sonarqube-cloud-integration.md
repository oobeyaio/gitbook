---
description: >-
  The Oobeya–Sonar Integration connects SonarQube Server and SonarQube Cloud
  with Oobeya’s Engineering Intelligence Platform, turning code quality and
  security data into actionable insights.
---

# SonarQube Cloud Integration

Delivering **high-quality software** requires continuous attention to **code reliability, security, and maintainability**. By integrating **SonarQube Cloud** with [**Oobeya**](https://oobeya.io), your teams gain end-to-end visibility into code quality, technical debt, and maintainability trends — all in one place.

***

#### 1. Generate a **SonarQube Cloud** Token

A **Personal Access Token (PAT)** allows Oobeya to connect to your **SonarQube Cloud** organization securely.

{% hint style="info" %}
The token creation & lifecycle rules are managed in your **SonarQube Cloud** **My Account → Security** page. See **Managing Personal Access Tokens** in the official docs. [docs.sonarsource.com](https://docs.sonarsource.com/sonarqube-cloud/managing-your-account/managing-tokens?utm_source=chatgpt.com)
{% endhint %}

**Steps**

1. Log in to **SonarQube Cloud**.
2. Click your **user avatar** (top-right) → **My Account** → **Security**.
3. In **Tokens**, enter a name (e.g., `oobeya-integration`) and select **Generate**.
4. Copy and **store the token securely** — it’s shown only once.

{% hint style="info" %}
**Good to know:** SonarQube Cloud may automatically remove **inactive tokens** after a period (e.g., 60 days of inactivity). Rotate/renew tokens as needed. [docs.sonarsource.com](https://docs.sonarsource.com/sonarqube-cloud/managing-your-account/managing-tokens?utm_source=chatgpt.com)
{% endhint %}

***

#### 2. Find Your Organization Key

Oobeya uses the **Organization Key** (not just the display name) to fetch projects from **SonarQube Cloud**.

**Ways to get it**

* From the SonarQube Cloud UI: open your org; the **key** appears in the org page/URL\
  (e.g., `https://sonarcloud.io/organizations/<organization_key>/projects`).
* Or go to the org settings page and see/edit the **Organization key**.

***

### 3. Connect SonarQube Cloud in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Code Quality & Security** section, click the **SonarQube Cloud** card. If SonarQube Cloud already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **SonarCloud 1.0** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                 |
| -------------------- | --------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _SonarQube Cloud_. |
| **Token**            | The token from step 1.                                                |
| **Organization**     | The organization key from step 2.                                     |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FXf8UZbfNi154RF0a1PpK%2Fform-sonarqube-cloud.png?alt=media&#x26;token=d8c5aa25-8098-4cc0-ab9c-879e863493c3" alt="SonarQube Cloud data source form in Oobeya"><figcaption><p>The SonarQube Cloud data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

#### 4. Explore Your Code Quality Insights

After integration, Oobeya continuously imports your **SonarQube Cloud metrics**, including:

* **Issues:** Bugs, Vulnerabilities, Code Smells
* **Quality Gate Status**
* **Technical Debt**
* **Maintainability, Reliability, Security ratings**

View them in:

* **Dashboards** — for portfolio/org visibility

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FJlKQQ2eDGm8eSzqPZ3fX%2Fimage.png?alt=media&#x26;token=c7ba2797-1fe6-4aad-bac1-f3ad27476e58" alt=""><figcaption><p>Improved visibility and ownership</p></figcaption></figure>

* **Organizational, Team, and Individual Scorecards** — to track trends & KPIs

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FsD91TH29lh6Pf6t9y4Ax%2Fimage.png?alt=media&#x26;token=2db5cde2-3786-44da-8b68-45d2d6d3a2a7" alt=""><figcaption><p>Team Scorecards</p></figcaption></figure>

* **Engineering Insights / Symptoms** — to proactively detect unhealthy practices

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FfHlXLua9Qx96i9VSBnrI%2Fimage.png?alt=media&#x26;token=4650bf21-1cf6-4f5a-b075-2449e01444e5" alt=""><figcaption><p>Code Quality Insights: Auto-detected Symptoms</p></figcaption></figure>

* **Gamification** — to drive positive behaviors

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FjQ8S7p1dE3ISmWzvZimB%2Fimage.png?alt=media&#x26;token=e51efeaf-d291-4c48-be9e-c420ceec6e8f" alt=""><figcaption><p>Code Quality and Security metrics in gamification</p></figcaption></figure>

***

#### 5. Troubleshooting

<table><thead><tr><th width="186.00115966796875">Issue</th><th width="209.07318115234375">Possible Cause</th><th>Fix</th></tr></thead><tbody><tr><td><strong>401 Unauthorized</strong></td><td>Invalid/expired token</td><td>Re-generate a valid token in <strong>My Account → Security</strong> and update the data source. <a href="https://docs.sonarsource.com/sonarqube-cloud/managing-your-account/managing-tokens?utm_source=chatgpt.com">docs.sonarsource.com</a></td></tr><tr><td><strong>Organization not found</strong></td><td>Wrong <strong>Organization Key</strong> (display name vs key)</td><td>Use the <strong>org key</strong> from the org URL or settings page. <a href="https://docs.sonarsource.com/sonarqube-cloud/getting-started/viewing-organizations?utm_source=chatgpt.com">docs.sonarsource.com</a></td></tr><tr><td><strong>No projects discovered</strong></td><td>Token user lacks access / projects private via ALM binding</td><td>Ensure the token’s user actually has access to the organization and projects in SonarQube Cloud. Re-check ALM bindings/visibility in SonarQube Cloud.</td></tr><tr><td><strong>Connection timeout</strong></td><td>Corporate firewall/proxy blocks egress</td><td>Allow outbound access from Oobeya to <code>https://sonarcloud.io</code> and required endpoints.</td></tr><tr><td><strong>SSL / TLS error</strong></td><td>Middlebox/proxy inspection or cert issue</td><td>Ensure standard TLS outbound is allowed; avoid interception that breaks TLS handshakes.</td></tr></tbody></table>

**Need help?** Contact **Oobeya Support** or your **Customer Success Manager**.

***

**Summary: Connect in 4 Steps**

<table><thead><tr><th width="88.56866455078125">Step</th><th>Action</th><th>Result</th></tr></thead><tbody><tr><td>1</td><td>Generate a <strong>SonarQube Cloud</strong> token</td><td>Secure API access</td></tr><tr><td>2</td><td>Get your <strong>Organization Key</strong></td><td>Correct org scoping</td></tr><tr><td>3</td><td><strong>Install</strong> the <strong>SonarQube Cloud</strong> add-on</td><td>Enable integration</td></tr><tr><td>4</td><td><strong>Add Data Source</strong> &#x26; test</td><td>Start syncing insights</td></tr></tbody></table>

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
