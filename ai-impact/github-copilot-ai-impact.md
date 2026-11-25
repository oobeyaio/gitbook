---
description: >-
  Configuration guide for the AI Coding Assistant Impact module: GitHub Copilot
  data source setup, token scopes, and team scorecard mapping.
icon: github-alt
---

# GitHub Copilot - AI Impact

The **AI Coding Assistant Impact** module in Oobeya enables organizations to measure the adoption, engagement, and real-world impact of AI coding assistants, such as **GitHub Copilot**. By integrating with your GitHub environment, Oobeya provides visibility from **organization-level usage** down to **team-level insights**.

***

#### 1. Prerequisites

Before configuring the AI Impact module:

* Ensure [**GitHub Copilot**](https://github.com/features/copilot) is enabled in your GitHub organization.
* Verify that you have admin rights to generate a **Personal Access Token (PAT)** with the required scopes.
*   Network Access Requirements

    Before configuring the GitHub Copilot data source, make sure the Oobeya environment has outbound network access to the following addresses:

    * `copilot-reports.github.com`
    * `*.b01.azurefd.net`
    * `api.github.com`
    * `usagereports*.blob.core.windows.net`

    These endpoints are required for Oobeya to retrieve GitHub Copilot usage and reporting data. If access is restricted by a firewall, proxy, or allowlist policy, please allow outbound HTTPS traffic to these addresses.

***

#### 2. Add the GitHub Copilot Data Source

1. Select **Integrations** in the **Administration** section of the left menu.
2. In the **AI Coding Assistants** section, click the **GitHub Copilot** card. If GitHub Copilot already has data sources, click **+ New Data Source** in the window that opens.
3. Fill in the form as described below, click **Test Connection**, then **Add**.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FIyvdh91B3nNWJ2UCibyd%2Fform-github-copilot.png?alt=media&#x26;token=ab3d6f11-32f1-4ff1-806d-e884bb3af82c" alt="GitHub Copilot data source form in Oobeya"><figcaption><p>The GitHub Copilot data source form.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source.
{% endhint %}

When adding GitHub Copilot as a data source:

* **Data Source Name:** Assign a descriptive name (e.g., _GitHub Copilot Org_).
* **Enterprise** _(optional)_: the slug of your GitHub enterprise account, if your Copilot licenses are managed at enterprise level.
* **Token:** Provide a GitHub PAT with the following scopes:

**Required Token Scopes**

* `repo`
* `repo:status`
* `repo_deployment`
* `public_repo`
* `repo:invite`
* `security_event`
* `admin:org`
* `read:org`
* `manage_billing:copilot`
* `manage_billing:enterprise`_(required only for GH enterprise usage)_
* `read:enterprise` _(required only for GH enterprise usage)_

Once the token is entered, click **Test Connection** → **Update** to finalize.

***

#### 4. Map GitHub Copilot to Oobeya Teams

To ensure GitHub Copilot usage data flows correctly into Oobeya’s team dashboards, you need to map GitHub organizations and teams to Oobeya teams.

1. Go to **Insights → Teams**.
2. Open a **Level-2 team** that you want to configure.
3. Navigate to the **Scorecard** tab and click the **Update** button in the top-right corner.
4. Progress through the steps until you reach the **GitHub Copilot** step.
5. Select:
   * **Data Source**: Choose your GitHub Copilot data source.
   * **Organizations**: Pick the GitHub organization(s) linked with Copilot.
   * **Teams**: Map GitHub Copilot teams to the corresponding Oobeya team.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FOb22Ss23EJ3aCiIMJrRc%2Fimage.png?alt=media&#x26;token=11a1bd86-be3c-4231-925b-e147dc40f5d1" alt="Mapping GitHub Copilot Teams in Oobeya"><figcaption><p>Mapping GitHub Copilot Teams in Oobeya</p></figcaption></figure>

{% hint style="info" %}
This mapping ensures that adoption, engagement, and acceptance metrics from GitHub Copilot are correctly associated with your Oobeya team structure.
{% endhint %}

***

#### 5. Viewing Results

Once configured, the AI Impact module provides analytics from the **Org level → Team level → User level**:

* **Organization-Level Metrics**
  * Overall adoption rate
  * Active vs engaged users
  * Copilot license utilization
* **Team-Level Metrics**
  * Adoption and engagement breakdown per team
  * Most active teams
  * Teams with low or no activity
  * Comparison between the actual contributions and AI contributions
* **User-Level Metrics**
  * Individual adoption and engagement
  * Suggestions accepted vs rejected
  * Inactive users in the last 7/30 days

***

#### 6. Dashboard Components

* **Copilot Adoption Over Time** – Track licensed, active, and engaged users.
* **Engagement & Acceptance Trends** – Measure quality of usage (accepted vs suggested completions).
* **Usage by Language & IDE** – Identify where Copilot delivers the most value.
* **Feature Usage Insights** – Breakdown of completions, chat, and PR integrations.
* **Team & User Metrics** – Detect top users, low activity users, and training needs.
* **Comparison Between Actual Contributions and AI Contributions**

**Learn more about the module:**

* [Measuring the Impact of AI Coding Assistants](https://docs.oobeya.io/use-cases/measuring-the-impact-of-ai-coding-assistants)

***

#### 7. Troubleshooting

* **Connection Fails?**
  * Ensure token scopes are correct.
  * Verify the token is valid and not expired.
  * Ensure the required network addresses are allowlisted.
  * Verify that outbound HTTPS access is available from the Oobeya environment.
* **Data Missing for Some Teams?**
  * Confirm GitHub teams are properly mapped to Oobeya teams.
* **Low Engagement Metrics?**
  * Ensure developers have Copilot enabled in their IDEs.
  * Provide enablement sessions to improve adoption.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
