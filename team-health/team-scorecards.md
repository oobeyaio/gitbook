---
description: Let's learn about the Team Scorecard
---

# Team Scorecard

The **Team Scorecard** shows how one team works across its whole delivery pipeline: planning, coding, code review, code quality, and delivery, together with the team's active symptoms. It reads the analyses selected in the team's scorecard configuration, for the period you choose.

To open it, select **Team Health** in the left menu and click a team name on the **Teams** tab. Use the team selector at the top of the scorecard to switch to another team.

<figure><img src="https://images.gitbook.com/__img/dpr=2,width=760,onerror=redirect,format=auto,signature=1165585774/https%3A%2F%2Ffiles.gitbook.com%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F04urjvL9rnhjsRAw1BmY%2Fteam-scorecard.png%3Falt%3Dmedia%26token%3D95e7c399-6fad-4203-9b94-aacf4702a6ca" alt="Team Scorecard with team card, most critical active signal, and Key Metrics Overview"><figcaption><p>Team Health > team > Team Scorecard.</p></figcaption></figure>

### Toolbar

| Control           | What it does                                                                                                                                                                                               |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Team selector** | Opens another team's scorecard.                                                                                                                                                                            |
| **Date range**    | Sets the period for every widget (for example **Last 90 Days**).                                                                                                                                           |
| **Excel export**  | Exports **Team Coding Efficiency**, **Developer Coding Efficiency** (when the Individual Scorecard is licensed), **Development Excellence**, and, when Fortify is configured, the **Fortify Issue Board**. |
| **Update**        | Opens the scorecard configuration. Shown to users who can update the team's scorecard.                                                                                                                     |

### Team card and most critical signal

The team card shows the **Team Lead**, the **Team Level** in your organizational chart, the **Members**, and the **Tools** the team's analyses come from.

Below it, **Most critical active signal** shows the team's most severe active [symptom](https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog) with its description and possible causes. **View symptoms** opens the full list.

### Key Metrics Overview

| Metric                          | What it shows                                                                                                                                                     |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Coding Efficiency**           | Percentage of analyzed code changes that are productive work rather than short-term rework (code churn), as a trend for the period and compared with the average. |
| **Coding Impact per Developer** | Coding Impact Score per developer in the period (scope of the code changes), compared with the average.                                                           |
| **% of PRs Merged Within Goal** | Percentage of merged pull requests completed within the configured target time.                                                                                   |
| **Avg Time To Merge**           | Average time between the first commit of a pull request and its merge.                                                                                            |
| **Lead Time for Changes**       | DORA lead time with its performance level (Elite, High, Medium, Low).                                                                                             |
| **Change Failure Rate**         | DORA change failure rate with its performance level.                                                                                                              |
| **Sprint Predictability**       | Percentage of originally planned sprint work that is completed.                                                                                                   |
| **Critical Symptoms**           | Number of active critical symptoms.                                                                                                                               |

All metrics are defined in the [Metrics List](https://docs.oobeya.io/getting-started/metrics).

### Delivery Pipeline

The **Delivery Pipeline** splits the team's work into four stages. Each stage card shows a headline figure; select a stage to open its details below.

| Stage                  | Card                               | Details                                                                                                                                                                                                                                                                                                                                                        |
| ---------------------- | ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Project Management** | Sprints, cycle time, and lead time | Project Analytics for **Scrum Teams** (Summary, Delivery Report, Backlog Health, Allocations, Value Area Report, Work Item Report, Resolution Time Report) and **Kanban Teams** (Summary, Delivery Report). See [Project Analytics (Scrum Teams) Widget](https://docs.oobeya.io/team-health/project-analytics-scrum-teams-widget).                             |
| **Development**        | Commits and repositories           | Development Analytics: Work Type (by Members and by Teams), Code Changes (by Teams and by Members), Commit Distribution, and Pipeline Analytics. The member table lists revisions, coding efficiency, coding impact, impact ratio, new work, refactor, help others, and code churn.                                                                            |
| **Code Quality**       | Open issues                        | Code quality from SonarQube: Code Quality & Technical Debt Trends, [Total Code Quality Index](https://docs.oobeya.io/quality-analytics/total-code-quality-index-tcqi), and TCQI Breakdown.                                                                                                                                                                     |
| **Delivery**           | Deployment frequency               | [DORA metrics](https://docs.oobeya.io/deployment-analytics/dora-metrics-introduction) for production and development pipelines: Lead Time for Changes broken down into Development Time, Waiting For Deploy, and Deployment Time; Change Failure Rate; Deployment Frequency; Time to Restore Service; a deployment frequency chart; and DORA Metrics by Teams. |

Teams that have Fortify, Veracode, Dynatrace, Azure Application Insights, or Test Analytics configured also see their security, monitoring, and test widgets.

### Symptoms

The **Symptoms** panel lists the team's symptoms across all pipeline steps. Filter by **Active**, **Deactive**, or **All**; the levels are **Critical**, **Warning**, and **Info**. Select a symptom to see why it is a symptom, its possible causes, improvement areas, detection method, and the teams where it is detected. See the [Symptoms Catalog](https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog).

### Configure the Team Scorecard

The scorecard configuration decides which analyses feed the scorecard. Open it with **Update** on the scorecard. A team without a configuration shows **New Setup**.

<figure><img src="https://images.gitbook.com/__img/dpr=2,width=760,onerror=redirect,format=auto,signature=-744388013/https%3A%2F%2Ffiles.gitbook.com%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FnsPWY4OkvVPddT52WH5E%2Fteam-scorecard-config.png%3Falt%3Dmedia%26token%3D64a0ac56-681b-42aa-ae12-6b2a3e9c43b8" alt="Team Scorecard Configuration page with the Modules list and the Analyses selection"><figcaption><p>Team Scorecard Configuration &#x26; Addon Settings. Repository names are sample values.</p></figcaption></figure>

1. Select a module in the **Modules** list.
2. Move items from the **Source** list to the **Target** list to select them for the team, or back to remove them. Some lists are preselected from the team's recent activity.
3. Click **Save**. **Reset Tab** discards the changes of the current module. The footer shows **Unsaved changes** until you save and **All modules synced** after.
4. Click **View Team Scorecard** to go back to the scorecard.

| Module                                          | What you select                                                                                                                                                                 |
| ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Analyses**                                    | Git repositories (Development Analytics) of the team. Repositories the team's developers committed to in the last 6 months are preselected. Required for the Development stage. |
| **Deployments**                                 | Deployment analyses (pipelines and environments) of the team. Required for DORA metrics in the Delivery stage.                                                                  |
| **Agile Boards**                                | Board analyses of the team. Boards the team members worked on in the last 3 months are preselected.                                                                             |
| **Testing** > **Test Projects**                 | Test Analytics project analyses.                                                                                                                                                |
| **Testing** > **Automation Coverage**           | Automation coverage software modules.                                                                                                                                           |
| **Code Quality** > **Unit Test Coverage**       | SonarQube data sources, projects, and branches used for the team's unit test coverage.                                                                                          |
| **Code Quality** > **TCQI Projects**            | SonarQube data source, code quality projects, and unit test projects for the TCQI calculation.                                                                                  |
| **Monitoring** > **Dynatrace**                  | Dynatrace applications or services.                                                                                                                                             |
| **Monitoring** > **Azure Application Insights** | The Application Insights resource for Apdex Score, Error Rate, and Response Time.                                                                                               |
| **Security** > **Fortify**                      | Fortify applications and versions.                                                                                                                                              |
| **Working Branch**                              | Branches used for symptom detection and pull request size. If none is selected, all branches are analyzed.                                                                      |

The modules you see depend on the integrations connected on the [Integrations](https://docs.oobeya.io/integrations/adding-new-integration) page. Data from a module appears only after its analysis has run at least once.

{% hint style="info" %}
To show DORA metrics for a team, select the team's pipelines in the **Deployments** module and save. The deployment analyses must exist first: see [Setting Up Development Analytics And DORA Metrics](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics).
{% endhint %}

### Related

* [Team Health](https://docs.oobeya.io/team-health/team-health-overview)
* [Adding A Team](https://docs.oobeya.io/team-health/adding-a-team)
* [Developer Onboarding Metrics Widget](https://docs.oobeya.io/team-health/developer-onboarding-metrics-widget)
