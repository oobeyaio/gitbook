---
description: >-
  Configuration guide for the AI Coding Assistant Impact module: GitHub Copilot
  data source setup, token scopes, and team scorecard mapping.
icon: github-alt
---

# GitHub Copilot - AI Impact

The **AI Coding Assistant Impact** module in Oobeya enables organizations to measure the adoption, engagement, and real-world impact of AI coding assistants, such as **GitHub Copilot**. By integrating with your GitHub environment, Oobeya provides visibility from **organization-level usage** down to **team-level insights**.

***

### 1. Prerequisites

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

### 2. Enable GitHub Copilot Integration

1. Navigate to **Integrations → Coding Assistant** in Oobeya.
2. Select **GitHub Copilot** and **click "Install".**

<figure><img src="../.gitbook/assets/image (485).png" alt=""><figcaption><p>GitHub Copilot Integration</p></figcaption></figure>

***

### 3. Configure Data Source

Go to Data Sources and add a **Data Source for GitHub Copilot.**

<figure><img src="../.gitbook/assets/image (487).png" alt=""><figcaption><p>Adding A Data Source</p></figcaption></figure>

When adding GitHub Copilot as a data source:

* **Data Source Name:** Assign a descriptive name (e.g., _GitHub Copilot Org_).
* **API Token:** Provide a GitHub PAT with the following scopes:

#### Required Token Scopes

* `repo`
* `repo:status`
* `repo_deployment`
* `public_repo`
* `repo:invite`
* `security_event`
* `admin:org`
* `read:org`
* `manage_billing:copilot`
* `read:enterprise` _(required only for GH enterprise usage)_

Once the token is entered, click **Test Connection** → **Update** to finalize.

***

### 4. Map GitHub Copilot to Oobeya Teams

To ensure GitHub Copilot usage data flows correctly into Oobeya’s team dashboards, you need to map GitHub organizations and teams to Oobeya teams.

1. Go to **Insights → Teams**.
2. Open a **Level-2 team** that you want to configure.
3. Navigate to the **Scorecard** tab and click the **Update** button in the top-right corner.
4. Progress through the steps until you reach the **GitHub Copilot** step.
5. Select:
   * **Data Source**: Choose your GitHub Copilot data source.
   * **Organizations**: Pick the GitHub organization(s) linked with Copilot.
   * **Teams**: Map GitHub Copilot teams to the corresponding Oobeya team.

<figure><img src="../.gitbook/assets/image (484).png" alt="Mapping GitHub Copilot Teams in Oobeya"><figcaption><p>Mapping GitHub Copilot Teams in Oobeya</p></figcaption></figure>

{% hint style="info" %}
This mapping ensures that adoption, engagement, and acceptance metrics from GitHub Copilot are correctly associated with your Oobeya team structure.
{% endhint %}

***

### 5. Viewing Results

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

### 6. Dashboard Components

* **Copilot Adoption Over Time** – Track licensed, active, and engaged users.
* **Engagement & Acceptance Trends** – Measure quality of usage (accepted vs suggested completions).
* **Usage by Language & IDE** – Identify where Copilot delivers the most value.
* **Feature Usage Insights** – Breakdown of completions, chat, and PR integrations.
* **Team & User Metrics** – Detect top users, low activity users, and training needs.
* **Comparison Between Actual Contributions and AI Contributions**

#### Learn more about the module:

{% content-ref url="../use-cases/measuring-the-impact-of-ai-coding-assistants.md" %}
[measuring-the-impact-of-ai-coding-assistants.md](../use-cases/measuring-the-impact-of-ai-coding-assistants.md)
{% endcontent-ref %}

***

### 7. Troubleshooting

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

## **Next Steps** :dart:&#x20;

* [Network Access Requirements ](../integrations/network-access-requirements.md)
* [Create a new Gitwiser Analysis](../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
