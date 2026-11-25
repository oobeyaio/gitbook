---
description: >-
  Engineering activity, contribution patterns, code changes, and work types from
  source code management data.
---

# Development Analytics

Development Analytics uses source code management data to analyze engineering activity, contribution patterns, code changes, work types, and development behavior. Supported data sources are GitHub, GitLab, Azure DevOps, Bitbucket, and Gitea.

For configuration and calculation details, see [Git Analytics - Metric Definitions](https://docs.oobeya.io/gitwiser-repo-analytics/git-analytics-metric-definitions).

### Engineering Efficiency and Impact

| Metric                          | What it measures                                                                                                                                                                              |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Coding Efficiency (%)**       | The percentage of analyzed code changes classified as productive work rather than short-term rework or Code Churn.                                                                            |
| **Coding Impact Score**         | A configurable score representing the scope and approximate cognitive impact of code changes. It considers files added, modified, or deleted; Git hunks; and lines added, edited, or deleted. |
| **Impact Ratio**                | Shows how Coding Impact is distributed among contributors within a team. It helps identify concentrated ownership, knowledge silos, and workload imbalance.                                   |
| **Coding Impact per Developer** | The Coding Impact Score attributed to each developer during the selected period.                                                                                                              |
| **Rework Rate (%)**             | The percentage of analyzed development activity classified as Code Churn or short-term rework.                                                                                                |
| **Coding Impact Trend**         | The change in Coding Impact Score over the selected period.                                                                                                                                   |
| **Coding Efficiency Trend**     | The change in Coding Efficiency over time.                                                                                                                                                    |

Learn more about [Coding Impact Score](https://docs.oobeya.io/gitwiser-repo-analytics/git-analytics-metric-definitions/coding-impact-score) and [Impact Ratio](https://docs.oobeya.io/gitwiser-repo-analytics/git-analytics-metric-definitions/impact-ratio-team-level).

### Work Type Metrics

| Metric                     | What it measures                                                                                                        |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **New Work**               | Newly written code lines.                                                                                               |
| **Refactor**               | Changes made to existing code after the configured aging period. The default aging period is 21 days.                   |
| **Help Others**            | Changes made by a developer to another developer's recent work.                                                         |
| **Code Churn / Rework**    | Code rewritten or deleted by the same developer shortly after it was originally written. The default period is 21 days. |
| **New Work Rate (%)**      | Percentage of analyzed code changes classified as New Work.                                                             |
| **Refactor Rate (%)**      | Percentage of analyzed code changes classified as Refactor.                                                             |
| **Help Others Rate (%)**   | Percentage of analyzed code changes classified as Help Others.                                                          |
| **Code Churn Rate (%)**    | Percentage of analyzed code changes classified as Code Churn.                                                           |
| **Work Type Distribution** | Distribution of New Work, Refactor, Help Others, and Code Churn within the selected period.                             |

### Development Activity Metrics

| Metric                                   | What it measures                                                                        |
| ---------------------------------------- | --------------------------------------------------------------------------------------- |
| **Total Commits**                        | Total number of commits during the selected period.                                     |
| **Active Coding Days**                   | Number of days with at least one commit or coding activity.                             |
| **Coding Days per Week**                 | Average number of active coding days per week.                                          |
| **Active Contributors**                  | Number of contributors with development activity during the configured activity period. |
| **Commits per Contributor**              | Average number of commits per active contributor.                                       |
| **Development Activities**               | Total development activities included in the selected scope and period.                 |
| **Contributor Activity Distribution**    | Distribution of development activity among contributors.                                |
| **Repository Contribution Distribution** | Distribution of development contributions across repositories.                          |
| **Contribution by Repository**           | Contribution attributed to each repository.                                             |
| **Contribution by Team**                 | Contribution attributed to each mapped team.                                            |
| **Contribution by Developer**            | Contribution attributed to each developer profile.                                      |

### Code Change Metrics

| Metric                       | What it measures                                               |
| ---------------------------- | -------------------------------------------------------------- |
| **Lines Added**              | Number of code lines added.                                    |
| **Lines Deleted**            | Number of code lines deleted.                                  |
| **Lines Edited**             | Number of existing code lines modified.                        |
| **Total Code Changes**       | Total number of added, deleted, and edited code lines.         |
| **Files Added**              | Number of new files added to the repository.                   |
| **Files Modified**           | Number of existing files modified.                             |
| **Files Deleted**            | Number of files deleted.                                       |
| **Files Touched**            | Total number of unique files affected by development activity. |
| **Git Hunks**                | Number of separate change blocks within the modified files.    |
| **Average Change Size**      | Average size of the analyzed commits or development changes.   |
| **Change Size Distribution** | Distribution of development activities by change size.         |
| **File Statistics**          | Summary of files added, modified, deleted, or touched.         |
| **Language Distribution**    | Distribution of code changes by programming language.          |

{% hint style="info" %}
Commit count and lines of code should not be treated as direct productivity measures. Use Coding Impact, Coding Efficiency, work type, quality, and delivery metrics together.
{% endhint %}
