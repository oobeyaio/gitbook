---
description: >-
  The Oobeya–Sonar Integration connects SonarQube Server and SonarQube Cloud
  with Oobeya’s Engineering Intelligence Platform, turning code quality and
  security data into actionable insights.
---

# SonarQube Server Integration

Delivering **high-quality software** requires continuous attention to **code reliability, security, and maintainability**. By integrating [**SonarQube Server**](https://www.sonarsource.com/) with [**Oobeya**](https://oobeya.io), your teams gain end-to-end visibility into code quality, technical debt, and maintainability trends — all in one place.

***

### 1. Generate a SonarQube Server User Token&#x20;

A **User Token** allows Oobeya to connect to your SonarQube Server instance and retrieve project data securely.

{% hint style="info" %}
The token creation process has been updated.\
For the official reference, see: [Generating and Using Tokens](https://docs.sonarsource.com/sonarqube-server/user-guide/managing-tokens)
{% endhint %}

#### Steps:

1. Log in to your **SonarQube Server** instance.
2. Click your **user avatar** (top-right corner) → select **My Account** → open the **Security** tab.
3. Under **Generate Tokens**, enter a **token name** (e.g., `oobeya-integration`).
4. Select **"User Token"** as token type.
5. Click **Generate**.
6. Copy and **store the token securely** — it’s shown only once.

{% hint style="info" %}
The token should belong to a user with at least **Browse** access to all relevant projects. For organization-wide visibility, use a user account with **Admin** permissions.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (503).png" alt=""><figcaption><p>Generating a new user token</p></figcaption></figure>

***

### 2. Install the SonarQube Add-on in Oobeya

1. Log in to Oobeya with an **Administrator** account.
2. Navigate to **Integrations.**
3. Locate **SonarQube Server** and click **Install**.

<figure><img src="../../../.gitbook/assets/image (518).png" alt="SonarQube Integration"><figcaption><p>SonarQube Server Integration</p></figcaption></figure>

Once installed, the SonarQube Server connector becomes available in your **Data Sources** list.

***

### 3. Add a SonarQube Data Source

1. Go to **Data Sources → SonarQube Server**.
2. Click **New Data Source**.
3. Fill out the form:
   * **Name:** (e.g., `SonarQube – Production`)
   * **Base URL:** Your SonarQube server address (e.g., `https://sonar.company.com`)
   * **User Token:** Paste the token you generated earlier
4. Click **Test Connection** to verify access.

<figure><img src="../../../.gitbook/assets/image (519).png" alt="" width="375"><figcaption><p>Adding a new SonarQube data source</p></figcaption></figure>

***

### 4. Explore Your Code Quality Insights

After integration, Oobeya continuously imports your **SonarQube metrics**, including:

* **Code Quality Issues**
* **Quality Gate Status**
* **Technical Debt**
* **Maintainability, Reliability, and Security Ratings**

You can explore this data in:

* **Dashboards** — for overall visibility

<figure><img src="../../../.gitbook/assets/image (510).png" alt=""><figcaption><p>Improved visibility and ownership for better code quality and security</p></figcaption></figure>



* **Organizational, Team, and Individual Scorecards** — to track trends and KPIs

<figure><img src="../../../.gitbook/assets/image (509).png" alt=""><figcaption><p>Sonarqube metrics in Team Scorecards</p></figcaption></figure>



* **Engineering Insights / Symptoms** — to proactively detect unhealthy code practices **-** [_learn more here_](../../../use-cases/proactive-issue-detection.md)_._<br>

<figure><img src="../../../.gitbook/assets/image (508).png" alt=""><figcaption><p>Code Quality Insights: Auto-detected Symptoms</p></figcaption></figure>

* **Gamification -** [_learn more here_](../../../use-cases/gamification-for-engineering-kpis.md)_._

<figure><img src="../../../.gitbook/assets/image (511).png" alt=""><figcaption><p>Leveraging gamification to improve code quality</p></figcaption></figure>

***

### 5. Troubleshooting

If your connection test fails or data is missing, review the following checks:

<table><thead><tr><th width="183.75469970703125">Issue</th><th width="195.8480224609375">Possible Cause</th><th>Solution</th></tr></thead><tbody><tr><td><strong>401 Unauthorized</strong></td><td>Invalid or expired token</td><td>Regenerate a valid User Token and update the Data Source.</td></tr><tr><td><strong>Connection Timeout</strong></td><td>Firewall or proxy blocking requests</td><td>Ensure outbound access to your SonarQube server from Oobeya’s network.</td></tr><tr><td><strong>No Projects Found</strong></td><td>Token lacks permissions</td><td>Verify the token user has project “Browse” or “Admin” permissions.</td></tr><tr><td><strong>SSL Error</strong></td><td>Invalid SSL certificate</td><td>Use a valid SSL certificate or enable trusted certificate configuration.</td></tr><tr><td><strong>Data Outdated</strong></td><td>Sync delay or rate limit</td><td>Trigger a manual re-sync or check your SonarQube server performance.</td></tr></tbody></table>

**💬 Still need help?**\
Contact Oobeya Support or reach out to your Customer Success Manager.

***

### Summary: Connect in 5 Steps

<table><thead><tr><th width="83.13421630859375">Step</th><th width="329.26531982421875">Action</th><th>Result</th></tr></thead><tbody><tr><td>1</td><td>Generate a User Token in SonarQube</td><td>Secure authentication</td></tr><tr><td>2</td><td>Install the SonarQube Server Add-on in Oobeya</td><td>Enable integration</td></tr><tr><td>3</td><td>Add a Data Source</td><td>Connect Oobeya to your SonarQube server</td></tr><tr><td>4</td><td>View Dashboards and Scorecards</td><td>Monitor real-time code quality</td></tr></tbody></table>
