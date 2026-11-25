---
description: >-
  Daily developer activity scores used to spot workload imbalance, concentrated
  contribution, and low participation.
---

# Activity Heatmap

Activity Heatmap visualizes daily developer activities and helps identify workload imbalance, concentrated contribution, unusually high activity, and low participation. It turns commit and pull request activity into weighted, normalized scores.

See [Activity Heatmap](https://docs.oobeya.io/activity-heatmap/activity-heatmap).

### Activity Inputs

| Metric            | What it measures                              |
| ----------------- | --------------------------------------------- |
| **Commits**       | Number of commits made by a developer.        |
| **Lines Added**   | Number of code lines added.                   |
| **Lines Deleted** | Number of code lines deleted.                 |
| **Lines Edited**  | Number of code lines modified.                |
| **PRs Created**   | Number of pull requests created.              |
| **PR Reviews**    | Number of code reviews performed.             |
| **PR Approvals**  | Number of pull requests approved.             |
| **PR Needs Work** | Number of pull requests returned for changes. |
| **PR Comments**   | Number of comments added to pull requests.    |

Each activity type can have a configurable coefficient that determines its contribution to the score.

### Calculated Scores

| Metric                          | What it measures                                                                                   |
| ------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Commit Activity Score**       | Weighted score generated from commits and code-change activity.                                    |
| **Pull Request Activity Score** | Weighted score generated from PR creation, review, approval, change-request, and comment activity. |
| **Total Activity Score**        | Combined weighted score across commit and pull request activity.                                   |
| **Daily Rank Ratio**            | A developer's daily score relative to the highest-scoring developer for that day.                  |
| **Daily Normalized Score**      | Daily activity score normalized for team comparison.                                               |
| **Activity Z-Score**            | Standardized activity score calculated from the team's daily distribution.                         |
| **Heatmap Score**               | Normalized 0-100 score used to determine heatmap intensity.                                        |
| **Developer Total Score**       | Total activity score attributed to a developer during the selected period.                         |
| **Team Activity Distribution**  | Distribution of normalized activity scores across team members.                                    |

{% hint style="info" %}
Activity Heatmap scores represent activity intensity, not work quality, value, or individual performance.
{% endhint %}
