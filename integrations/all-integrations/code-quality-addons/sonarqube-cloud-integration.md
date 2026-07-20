---
description: >-
  The Oobeya–Sonar Integration connects SonarQube Server and SonarQube Cloud
  with Oobeya’s Engineering Intelligence Platform, turning code quality and
  security data into actionable insights.
---

# SonarQube Cloud Integration

Delivering **high-quality software** requires continuous attention to **code reliability, security, and maintainability**. By integrating **SonarQube Cloud** with [**Oobeya**](https://oobeya.io), your teams gain end-to-end visibility into code quality, technical debt, and maintainability trends — all in one place.

***

### 1. Generate a **SonarQube Cloud** Token&#x20;

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

### 2. Find Your Organization Key&#x20;

Oobeya uses the **Organization Key** (not just the display name) to fetch projects from **SonarQube Cloud**.

**Ways to get it**

* From the SonarQube Cloud UI: open your org; the **key** appears in the org page/URL\
  (e.g., `https://sonarcloud.io/organizations/<organization_key>/projects`).&#x20;
* Or go to the org settings page and see/edit the **Organization key**.

***

### 3. Install the **SonarQube Cloud** Add-on in Oobeya&#x20;

1. Log in to **Oobeya** with an **Administrator** account.
2. Navigate to **Integrations**.
3. Find **SonarQube Cloud** and click **Install**.

***

### 4. Add a New **SonarQube Cloud** Data Source&#x20;

1. Go to **Data Sources → SonarQube Cloud**.
2. Click **New Data Source**.
3. Fill out the form:
   * **Name:** e.g., `SonarQube Cloud – Production`
   * **API Token:** (from Step 1)
   * **Organization Key:** (from Step 2)
4. Click **Test Connection** to verify access.

<figure><img src="../../../.gitbook/assets/image (8).png" alt="" width="375"><figcaption></figcaption></figure>

***

### 5. Explore Your Code Quality Insights&#x20;

After integration, Oobeya continuously imports your **SonarQube Cloud metrics**, including:

* **Issues:** Bugs, Vulnerabilities, Code Smells
* **Quality Gate Status**
* **Technical Debt**
* **Maintainability, Reliability, Security ratings**

View them in:

* **Dashboards** — for portfolio/org visibility

<figure><img src="../../../.gitbook/assets/image (510).png" alt=""><figcaption><p>Improved visibility and ownership</p></figcaption></figure>



* **Organizational, Team, and Individual Scorecards** — to track trends & KPIs

<figure><img src="../../../.gitbook/assets/image (509).png" alt=""><figcaption><p>Team Scorecards</p></figcaption></figure>



* **Engineering Insights / Symptoms** — to proactively detect unhealthy practices

<figure><img src="../../../.gitbook/assets/image (508).png" alt=""><figcaption><p>Code Quality Insights: Auto-detected Symptoms</p></figcaption></figure>



* **Gamification** — to drive positive behaviors

<figure><img src="../../../.gitbook/assets/image (511).png" alt=""><figcaption><p>Code Quality and Security metrics in gamification</p></figcaption></figure>

***

### 6. Troubleshooting&#x20;

<table><thead><tr><th width="186.00115966796875">Issue</th><th width="209.07318115234375">Possible Cause</th><th>Fix</th></tr></thead><tbody><tr><td><strong>401 Unauthorized</strong></td><td>Invalid/expired token</td><td>Re-generate a valid token in <strong>My Account → Security</strong> and update the data source. <a href="https://docs.sonarsource.com/sonarqube-cloud/managing-your-account/managing-tokens?utm_source=chatgpt.com">docs.sonarsource.com</a></td></tr><tr><td><strong>Organization not found</strong></td><td>Wrong <strong>Organization Key</strong> (display name vs key)</td><td>Use the <strong>org key</strong> from the org URL or settings page. <a href="https://docs.sonarsource.com/sonarqube-cloud/getting-started/viewing-organizations?utm_source=chatgpt.com">docs.sonarsource.com</a></td></tr><tr><td><strong>No projects discovered</strong></td><td>Token user lacks access / projects private via ALM binding</td><td>Ensure the token’s user actually has access to the organization and projects in SonarQube Cloud. Re-check ALM bindings/visibility in SonarQube Cloud.</td></tr><tr><td><strong>Connection timeout</strong></td><td>Corporate firewall/proxy blocks egress</td><td>Allow outbound access from Oobeya to <code>https://sonarcloud.io</code> and required endpoints.</td></tr><tr><td><strong>SSL / TLS error</strong></td><td>Middlebox/proxy inspection or cert issue</td><td>Ensure standard TLS outbound is allowed; avoid interception that breaks TLS handshakes.</td></tr></tbody></table>

**Need help?** Contact **Oobeya Support** or your **Customer Success Manager**.

***

#### Summary: Connect in 4 Steps

<table><thead><tr><th width="88.56866455078125">Step</th><th>Action</th><th>Result</th></tr></thead><tbody><tr><td>1</td><td>Generate a <strong>SonarQube Cloud</strong> token</td><td>Secure API access</td></tr><tr><td>2</td><td>Get your <strong>Organization Key</strong></td><td>Correct org scoping</td></tr><tr><td>3</td><td><strong>Install</strong> the <strong>SonarQube Cloud</strong> add-on</td><td>Enable integration</td></tr><tr><td>4</td><td><strong>Add Data Source</strong> &#x26; test</td><td>Start syncing insights</td></tr></tbody></table>

## **Next Steps** :dart:&#x20;

* [Network Access Requirements ](../../network-access-requirements.md)
* [Create a new Gitwiser Analysis](../../../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
