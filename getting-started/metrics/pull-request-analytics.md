---
description: Pull request volume, review responsiveness, flow time, size, and review risks.
---

# Pull Request Analytics

Pull Request Analytics shows review responsiveness, collaboration, flow efficiency, pull request size, and review risks. Several metrics compare pull requests against configured goals and thresholds.

### Pull Request Volume

| Metric                           | What it measures                                                                   |
| -------------------------------- | ---------------------------------------------------------------------------------- |
| **Total Pull Requests**          | Total number of pull requests included in the selected period.                     |
| **Open PRs**                     | Number of pull requests currently open and awaiting review, approval, or merge.    |
| **Merged PRs**                   | Number of pull requests successfully merged.                                       |
| **Closed PRs**                   | Number of pull requests closed without being merged.                               |
| **PRs Created**                  | Number of pull requests created during the selected period.                        |
| **PRs per Contributor**          | Average number of pull requests created per active contributor.                    |
| **Reviewed PRs**                 | Number of pull requests reviewed by the selected reviewer, developer, or team.     |
| **Reviewed PRs / Total PRs (%)** | Percentage of pull requests reviewed by the selected reviewer, developer, or team. |

### Pull Request Time Metrics

| Metric                                   | What it measures                                                                |
| ---------------------------------------- | ------------------------------------------------------------------------------- |
| **Coding Time**                          | Time between the first commit and the opening of the pull request.              |
| **Code Review Cycle Time**               | Time between the pull request opening and merge.                                |
| **Time to Merge**                        | Time between the first commit and merge.                                        |
| **Average Review Time**                  | Average time taken by reviewers to complete a pull request review.              |
| **Coding Time Over Goal (%)**            | Percentage of pull requests whose Coding Time exceeds the configured goal.      |
| **Code Review Cycle Time Over Goal (%)** | Percentage of pull requests whose review cycle exceeds the configured goal.     |
| **Time to Merge Over Goal (%)**          | Percentage of pull requests whose Time to Merge exceeds the configured goal.    |
| **PRs Merged Within Goal (%)**           | Percentage of merged pull requests completed within the configured target time. |

### Pull Request Size and Review Metrics

| Metric                              | What it measures                                                      |
| ----------------------------------- | --------------------------------------------------------------------- |
| **Pull Request Size**               | Total number of lines added, removed, and changed in a pull request.  |
| **Average Pull Request Size**       | Average size of pull requests during the selected period.             |
| **Pull Request Size Over Goal (%)** | Percentage of pull requests exceeding the configured size goal.       |
| **Number of PR Reviewers**          | Number of reviewers assigned to or participating in pull requests.    |
| **Review Comment Count**            | Number of review comments added to pull requests.                     |
| **PR Approvals**                    | Number of pull request approvals.                                     |
| **PR Needs Work**                   | Number of pull requests returned for changes.                         |
| **PR Revert Rate (%)**              | Percentage of merged pull requests whose changes were later reverted. |

### Pull Request Risk Indicators

| Metric                   | What it measures                                                                      |
| ------------------------ | ------------------------------------------------------------------------------------- |
| **Oversized PRs**        | Number of pull requests exceeding the configured size threshold.                      |
| **Overdue PRs**          | Number of pull requests exceeding the configured completion or review-time threshold. |
| **Stale PRs**            | Number of open pull requests without meaningful activity for the configured period.   |
| **Pull Request Risks**   | Combined count of Oversized, Overdue, or Stale pull requests.                         |
| **PR Risk Distribution** | Distribution of pull requests by identified risk type.                                |
