---
description: >-
  View a comprehensive list of the metrics in Oobeya, which is organised into
  different categories for your convenience.
icon: list-ol
---

# Metrics List

## Oobeya Metrics List

This page provides a module-by-module reference for the metrics, scores, distributions, and analytical indicators avaier permissions

* Team, repository, project, and data-source mappings
* Selected date range
* Organization-specific configuration

> Oobeya metrics should be interpreted together and within the context of each team. A single metric should not be used as an individual performance target.

***

### Metrics by Module

* [Development Analytics](metrics.md#development-analytics)
* [Pull Request Analytics](metrics.md#pull-request-analytics)
* [Delivery Analytics and DORA Metrics](metrics.md#delivery-analytics-and-dora-metrics)
* [Project Analytics](metrics.md#project-analytics)
* [Code Quality Analytics](metrics.md#code-quality-analytics)
* [Application Performance Metrics](metrics.md#application-performance-metrics)
* [Test Analytics](metrics.md#test-analytics)
* [AI Coding Assistant Impact](metrics.md#ai-coding-assistant-impact)
* [AI Cost and Credits](metrics.md#ai-cost-and-credits)
* [Document Analytics for Confluence](metrics.md#document-analytics-for-confluence)
* [Resource Allocation](metrics.md#resource-allocation)
* [Bug Report](metrics.md#bug-report)
* [Activity Heatmap](metrics.md#activity-heatmap)
* [Gamification](metrics.md#gamification)
* [Team Scorecards, Developer Profiles, and Dashboards](metrics.md#team-scorecards-developer-profiles-and-dashboards)
* [Engineering Insights and Symptoms](metrics.md#engineering-insights-and-symptoms)

***

## Development Analytics

Development Analytics uses source code management data to analyze engineering activity, contribution patterns, code changes, work types, and development behavior.

Supported data sources include GitHub, GitLab, Azure DevOps, Bitbucket, and Gitea.

For detailed configuration and calculation information, see [Git Analytics – Metric Definitions](https://docs.oobeya.io/gitwiser-repo-analytics/git-analytics-metric-definitions).

### Engineering Efficiency and Impact

<table><thead><tr><th width="261.29095458984375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Coding Efficiency (%)</strong></td><td>The percentage of analyzed code changes classified as productive work rather than short-term rework or Code Churn.</td></tr><tr><td><strong>Coding Impact Score</strong></td><td>A configurable score representing the scope and approximate cognitive impact of code changes. It considers files added, modified, or deleted; Git hunks; and lines added, edited, or deleted.</td></tr><tr><td><strong>Impact Ratio</strong></td><td>Shows how Coding Impact is distributed among contributors within a team. It helps identify concentrated ownership, knowledge silos, and workload imbalance.</td></tr><tr><td><strong>Coding Impact per Developer</strong></td><td>The Coding Impact Score attributed to each developer during the selected period.</td></tr><tr><td><strong>Rework Rate (%)</strong></td><td>The percentage of analyzed development activity classified as Code Churn or short-term rework.</td></tr><tr><td><strong>Coding Impact Trend</strong></td><td>The change in Coding Impact Score over the selected period.</td></tr><tr><td><strong>Coding Efficiency Trend</strong></td><td>The change in Coding Efficiency over time.</td></tr></tbody></table>

Learn more about [Coding Impact Score](https://docs.oobeya.io/gitwiser-repo-analytics/git-analytics-metric-definitions/coding-impact-score) and [Impact Ratio](https://docs.oobeya.io/gitwiser-repo-analytics/git-analytics-metric-definitions/impact-ratio-team-level).

### Work Type Metrics

<table><thead><tr><th width="254.81317138671875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>New Work</strong></td><td>Newly written code lines.</td></tr><tr><td><strong>Refactor</strong></td><td>Changes made to existing code after the configured aging period. The default aging period is 21 days.</td></tr><tr><td><strong>Help Others</strong></td><td>Changes made by a developer to another developer’s recent work.</td></tr><tr><td><strong>Code Churn / Rework</strong></td><td>Code rewritten or deleted by the same developer shortly after it was originally written. The default period is 21 days.</td></tr><tr><td><strong>New Work Rate (%)</strong></td><td>Percentage of analyzed code changes classified as New Work.</td></tr><tr><td><strong>Refactor Rate (%)</strong></td><td>Percentage of analyzed code changes classified as Refactor.</td></tr><tr><td><strong>Help Others Rate (%)</strong></td><td>Percentage of analyzed code changes classified as Help Others.</td></tr><tr><td><strong>Code Churn Rate (%)</strong></td><td>Percentage of analyzed code changes classified as Code Churn.</td></tr><tr><td><strong>Work Type Distribution</strong></td><td>Distribution of New Work, Refactor, Help Others, and Code Churn within the selected period.</td></tr></tbody></table>

### Development Activity Metrics

<table><thead><tr><th width="285.24676513671875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Total Commits</strong></td><td>Total number of commits during the selected period.</td></tr><tr><td><strong>Active Coding Days</strong></td><td>Number of days with at least one commit or coding activity.</td></tr><tr><td><strong>Coding Days per Week</strong></td><td>Average number of active coding days per week.</td></tr><tr><td><strong>Active Contributors</strong></td><td>Number of contributors with development activity during the configured activity period.</td></tr><tr><td><strong>Commits per Contributor</strong></td><td>Average number of commits per active contributor.</td></tr><tr><td><strong>Development Activities</strong></td><td>Total development activities included in the selected scope and period.</td></tr><tr><td><strong>Contributor Activity Distribution</strong></td><td>Distribution of development activity among contributors.</td></tr><tr><td><strong>Repository Contribution Distribution</strong></td><td>Distribution of development contributions across repositories.</td></tr><tr><td><strong>Contribution by Repository</strong></td><td>Contribution attributed to each repository.</td></tr><tr><td><strong>Contribution by Team</strong></td><td>Contribution attributed to each mapped team.</td></tr><tr><td><strong>Contribution by Developer</strong></td><td>Contribution attributed to each developer profile.</td></tr></tbody></table>

### Code Change Metrics

<table><thead><tr><th width="243.466552734375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Lines Added</strong></td><td>Number of code lines added.</td></tr><tr><td><strong>Lines Deleted</strong></td><td>Number of code lines deleted.</td></tr><tr><td><strong>Lines Edited</strong></td><td>Number of existing code lines modified.</td></tr><tr><td><strong>Total Code Changes</strong></td><td>Total number of added, deleted, and edited code lines.</td></tr><tr><td><strong>Files Added</strong></td><td>Number of new files added to the repository.</td></tr><tr><td><strong>Files Modified</strong></td><td>Number of existing files modified.</td></tr><tr><td><strong>Files Deleted</strong></td><td>Number of files deleted.</td></tr><tr><td><strong>Files Touched</strong></td><td>Total number of unique files affected by development activity.</td></tr><tr><td><strong>Git Hunks</strong></td><td>Number of separate change blocks within the modified files.</td></tr><tr><td><strong>Average Change Size</strong></td><td>Average size of the analyzed commits or development changes.</td></tr><tr><td><strong>Change Size Distribution</strong></td><td>Distribution of development activities by change size.</td></tr><tr><td><strong>File Statistics</strong></td><td>Summary of files added, modified, deleted, or touched.</td></tr><tr><td><strong>Language Distribution</strong></td><td>Distribution of code changes by programming language.</td></tr></tbody></table>

> Commit count and lines of code should not be treated as direct productivity measures. Use Coding Impact, Coding Efficiency, work type, quality, and delivery metrics together.

***

## Pull Request Analytics

Pull Request Analytics helps teams understand review responsiveness, collaboration, flow efficiency, pull request size, and review risks.

### Pull Request Volume

<table><thead><tr><th width="278.0870361328125">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Total Pull Requests</strong></td><td>Total number of pull requests included in the selected period.</td></tr><tr><td><strong>Open PRs</strong></td><td>Number of pull requests currently open and awaiting review, approval, or merge.</td></tr><tr><td><strong>Merged PRs</strong></td><td>Number of pull requests successfully merged.</td></tr><tr><td><strong>Closed PRs</strong></td><td>Number of pull requests closed without being merged.</td></tr><tr><td><strong>PRs Created</strong></td><td>Number of pull requests created during the selected period.</td></tr><tr><td><strong>PRs per Contributor</strong></td><td>Average number of pull requests created per active contributor.</td></tr><tr><td><strong>Reviewed PRs</strong></td><td>Number of pull requests reviewed by the selected reviewer, developer, or team.</td></tr><tr><td><strong>Reviewed PRs / Total PRs (%)</strong></td><td>Percentage of pull requests reviewed by the selected reviewer, developer, or team.</td></tr></tbody></table>

### Pull Request Time Metrics

<table><thead><tr><th width="295.94287109375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Coding Time</strong></td><td>Time between the first commit and the opening of the pull request.</td></tr><tr><td><strong>Code Review Cycle Time</strong></td><td>Time between the pull request opening and merge.</td></tr><tr><td><strong>Time to Merge</strong></td><td>Time between the first commit and merge.</td></tr><tr><td><strong>Average Review Time</strong></td><td>Average time taken by reviewers to complete a pull request review.</td></tr><tr><td><strong>Coding Time Over Goal (%)</strong></td><td>Percentage of pull requests whose Coding Time exceeds the configured goal.</td></tr><tr><td><strong>Code Review Cycle Time Over Goal (%)</strong></td><td>Percentage of pull requests whose review cycle exceeds the configured goal.</td></tr><tr><td><strong>Time to Merge Over Goal (%)</strong></td><td>Percentage of pull requests whose Time to Merge exceeds the configured goal.</td></tr><tr><td><strong>PRs Merged Within Goal (%)</strong></td><td>Percentage of merged pull requests completed within the configured target time.</td></tr></tbody></table>

### Pull Request Size and Review Metrics

<table><thead><tr><th width="277.56207275390625">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Pull Request Size</strong></td><td>Total number of lines added, removed, and changed in a pull request.</td></tr><tr><td><strong>Average Pull Request Size</strong></td><td>Average size of pull requests during the selected period.</td></tr><tr><td><strong>Pull Request Size Over Goal (%)</strong></td><td>Percentage of pull requests exceeding the configured size goal.</td></tr><tr><td><strong>Number of PR Reviewers</strong></td><td>Number of reviewers assigned to or participating in pull requests.</td></tr><tr><td><strong>Review Comment Count</strong></td><td>Number of review comments added to pull requests.</td></tr><tr><td><strong>PR Approvals</strong></td><td>Number of pull request approvals.</td></tr><tr><td><strong>PR Needs Work</strong></td><td>Number of pull requests returned for changes.</td></tr><tr><td><strong>PR Revert Rate (%)</strong></td><td>Percentage of merged pull requests whose changes were later reverted.</td></tr></tbody></table>

### Pull Request Risk Indicators

<table><thead><tr><th width="232.456298828125">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Oversized PRs</strong></td><td>Number of pull requests exceeding the configured size threshold.</td></tr><tr><td><strong>Overdue PRs</strong></td><td>Number of pull requests exceeding the configured completion or review-time threshold.</td></tr><tr><td><strong>Stale PRs</strong></td><td>Number of open pull requests without meaningful activity for the configured period.</td></tr><tr><td><strong>Pull Request Risks</strong></td><td>Combined count of Oversized, Overdue, or Stale pull requests.</td></tr><tr><td><strong>PR Risk Distribution</strong></td><td>Distribution of pull requests by identified risk type.</td></tr></tbody></table>

***

## Delivery Analytics and DORA Metrics

Delivery Analytics connects source code management, CI/CD, deployment, and incident data to measure software delivery performance.

See [DORA Metrics Introduction](https://docs.oobeya.io/deployment-analytics/dora-metrics-introduction) and [Deployment Analytics](https://docs.oobeya.io/gitwiser-repo-analytics/deployment-analytics-dora-metrics).

### Four Key DORA Metrics

<table><thead><tr><th width="289.87567138671875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Lead Time for Changes</strong></td><td>Time from a code commit or development change until that change is successfully deployed to production.</td></tr><tr><td><strong>Deployment Frequency</strong></td><td>How often the team successfully deploys changes to production.</td></tr><tr><td><strong>Change Failure Rate (%)</strong></td><td>Percentage of production deployments that result in a failure or incident.</td></tr><tr><td><strong>Time to Restore Service / MTTR</strong></td><td>Time required to restore service after a production failure.</td></tr></tbody></table>

### Delivery Flow Metrics

<table><thead><tr><th width="266.318603515625">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Development Time</strong></td><td>Time between the first commit and merge of the related pull request or change.</td></tr><tr><td><strong>Waiting for Deploy</strong></td><td>Time between the pull request merge and the start of the deployment pipeline.</td></tr><tr><td><strong>Deployment Duration</strong></td><td>Time between the deployment pipeline start and successful completion.</td></tr><tr><td><strong>Lead Time Breakdown</strong></td><td>Breakdown of Lead Time for Changes into development, waiting, and deployment phases.</td></tr><tr><td><strong>Deploy Size</strong></td><td>Number of commits and pull requests included in a deployment package.</td></tr><tr><td><strong>Average Deploy Size</strong></td><td>Average number of commits and pull requests delivered per deployment.</td></tr></tbody></table>

### Deployment and Incident Volume

<table><thead><tr><th width="302.5740966796875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Number of Deployments</strong></td><td>Total number of detected successful production deployments.</td></tr><tr><td><strong>Number of Contributors</strong></td><td>Number of contributors whose changes were included in deployments.</td></tr><tr><td><strong>Deployments Leading to an Incident</strong></td><td>Number of deployments associated with a production incident or failure.</td></tr><tr><td><strong>Production Incidents</strong></td><td>Number of incidents included in Change Failure Rate and restoration calculations.</td></tr><tr><td><strong>Successful Deployments</strong></td><td>Number of production deployments completed without a detected failure.</td></tr><tr><td><strong>Failed Changes</strong></td><td>Number of production changes associated with an incident or rollback condition.</td></tr><tr><td><strong>Deployment Frequency Trend</strong></td><td>Change in successful deployment frequency over time.</td></tr><tr><td><strong>Change Failure Rate Trend</strong></td><td>Change in the percentage of failed production changes over time.</td></tr><tr><td><strong>Lead Time Trend</strong></td><td>Change in Lead Time for Changes over time.</td></tr><tr><td><strong>Time to Restore Service Trend</strong></td><td>Change in restoration time over time.</td></tr></tbody></table>

> Change Failure Rate and Time to Restore Service require a correctly configured failure-detection source and production deployment mapping.

***

## Project Analytics

Project Analytics analyzes work items from Jira, Azure Boards, and supported project management systems.

Metrics can be calculated by work-item count, effort, story points, or time estimation depending on the data-source configuration.

See [Project Analytics – Metric Definitions](https://docs.oobeya.io/project-analytics/project-analytics-metric-definitions).

### Board-Level Metrics

<table><thead><tr><th width="281.23956298828125">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Completed Sprints</strong></td><td>Number of sprints started and completed during the selected period.</td></tr><tr><td><strong>Average Velocity by Effort</strong></td><td>Average amount of estimated effort completed per sprint.</td></tr><tr><td><strong>Average Lead Time</strong></td><td>Average time from work-item creation to completion.</td></tr><tr><td><strong>Average Cycle Time</strong></td><td>Average time from work start to completion.</td></tr><tr><td><strong>Completed Work Items</strong></td><td>Total number of work items completed during the selected period.</td></tr><tr><td><strong>Completed Work Items per Sprint</strong></td><td>Average number of work items completed in each sprint.</td></tr><tr><td><strong>Average Throughput per Week</strong></td><td>Average number of work items completed per working week.</td></tr></tbody></table>

### Flow and Reaction Time Metrics

<table><thead><tr><th width="245.96649169921875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Pickup Time</strong></td><td>Initial time between work-item creation and its recognition or placement into a ready backlog or queue.</td></tr><tr><td><strong>Actual Reaction Time</strong></td><td>Time from the configured reference point or ready state until work starts.</td></tr><tr><td><strong>Total Reaction Time</strong></td><td>Pickup Time plus Actual Reaction Time.</td></tr><tr><td><strong>Cycle Time</strong></td><td>Time from when active work begins until the work item is completed.</td></tr><tr><td><strong>Lead Time</strong></td><td>Time from work-item creation until completion.</td></tr><tr><td><strong>Lead Time Breakdown</strong></td><td>Distribution of total Lead Time across reaction, active development, waiting, and configured workflow phases.</td></tr><tr><td><strong>State Cycle Time</strong></td><td>Time spent in each mapped workflow state.</td></tr><tr><td><strong>Time in Status</strong></td><td>Amount of time a work item remains in a specific status.</td></tr><tr><td><strong>Waiting Time</strong></td><td>Time a work item remains idle between active workflow states.</td></tr></tbody></table>

### Sprint Planning Metrics

<table><thead><tr><th width="283.47698974609375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Planned</strong></td><td>Number of work items included before the sprint planning cut-off date.</td></tr><tr><td><strong>Planned Effort</strong></td><td>Total estimated effort of work items included before the planning cut-off date.</td></tr><tr><td><strong>Done Planned</strong></td><td>Number of planned work items completed by the end of the sprint.</td></tr><tr><td><strong>Done Planned Effort</strong></td><td>Estimated effort of planned work items completed by the end of the sprint.</td></tr><tr><td><strong>Pulled in Extra</strong></td><td>Number of work items added after the sprint planning cut-off date.</td></tr><tr><td><strong>Effort Pulled in Extra</strong></td><td>Estimated effort of work items added after the planning cut-off date.</td></tr><tr><td><strong>Done Pulled in Extra</strong></td><td>Number of pulled-in work items completed by the end of the sprint.</td></tr><tr><td><strong>Done Pulled in Extra Effort</strong></td><td>Estimated effort of pulled-in work completed by the end of the sprint.</td></tr><tr><td><strong>Unfinished</strong></td><td>Number of work items incomplete at the end of the sprint.</td></tr><tr><td><strong>Unfinished Effort</strong></td><td>Estimated effort of work items incomplete at the end of the sprint.</td></tr><tr><td><strong>Unfinished Planned</strong></td><td>Number of planned work items incomplete at the end of the sprint.</td></tr><tr><td><strong>Unfinished Effort Planned</strong></td><td>Estimated effort of planned work items incomplete at the end of the sprint.</td></tr><tr><td><strong>Unfinished Pulled in Extra</strong></td><td>Number of pulled-in work items incomplete at the end of the sprint.</td></tr><tr><td><strong>Unfinished Effort Pulled in Extra</strong></td><td>Estimated effort of pulled-in work items incomplete at the end of the sprint.</td></tr><tr><td><strong>Dropped</strong></td><td>Number of work items removed from an active sprint after the planning cut-off.</td></tr><tr><td><strong>Effort Dropped</strong></td><td>Estimated effort of work items removed from the sprint.</td></tr><tr><td><strong>End of Sprint</strong></td><td>Total number of completed and incomplete work items at the end of the sprint.</td></tr><tr><td><strong>Effort End of Sprint</strong></td><td>Total estimated effort of completed and incomplete work at the end of the sprint.</td></tr><tr><td><strong>Done</strong></td><td>Total number of work items completed by the end of the sprint.</td></tr><tr><td><strong>Done Effort</strong></td><td>Total estimated effort of completed work items.</td></tr></tbody></table>

### Sprint Performance Metrics

<table><thead><tr><th width="293.3480224609375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Sprint Velocity by Count</strong></td><td>Number of work items completed during the sprint.</td></tr><tr><td><strong>Sprint Velocity by Effort</strong></td><td>Total estimated effort completed during the sprint.</td></tr><tr><td><strong>Predictability (%)</strong></td><td>Percentage of originally planned work completed: <code>Done Planned / Planned × 100</code>.</td></tr><tr><td><strong>Productivity (%)</strong></td><td>Total completed planned and extra work relative to the original plan: <code>(Done Planned + Done Pulled in Extra) / Planned × 100</code>.</td></tr><tr><td><strong>Churn (%)</strong></td><td>Percentage of completed work that was pulled into the sprint after planning: <code>Done Pulled in Extra / (Done Planned + Done Pulled in Extra) × 100</code>.</td></tr><tr><td><strong>Sprint Delivery Rate by Count (%)</strong></td><td>Completed work items divided by total work items at the end of the sprint.</td></tr><tr><td><strong>Sprint Delivery Rate by Effort (%)</strong></td><td>Completed effort divided by total effort at the end of the sprint.</td></tr><tr><td><strong>Sprint Planning Accuracy by Count (%)</strong></td><td>Completed work items divided by planned work items.</td></tr><tr><td><strong>Sprint Planning Accuracy by Effort (%)</strong></td><td>Completed effort divided by planned effort.</td></tr><tr><td><strong>Sprint Scope Change</strong></td><td>Amount of work added to or removed from a sprint after the planning cut-off.</td></tr><tr><td><strong>Scope Change Rate (%)</strong></td><td>Relative change in sprint scope after planning.</td></tr></tbody></table>

### Backlog and Kanban Metrics

<table><thead><tr><th width="292.5478515625">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Backlog Size</strong></td><td>Number of uncompleted work items in the backlog, excluding active work.</td></tr><tr><td><strong>Backlog Age</strong></td><td>Age of the oldest or longest-waiting item in the backlog.</td></tr><tr><td><strong>Average Backlog Age</strong></td><td>Average age of work items currently in the backlog.</td></tr><tr><td><strong>Open Bugs in Backlog</strong></td><td>Number of bug-type work items currently waiting in the backlog.</td></tr><tr><td><strong>Current Backlog Items</strong></td><td>Number of items waiting in a Kanban backlog.</td></tr><tr><td><strong>Work in Progress</strong></td><td>Number of work items currently in active workflow states.</td></tr><tr><td><strong>Work in Progress Over 5 Days</strong></td><td>Work items that have remained in progress for more than five days.</td></tr><tr><td><strong>Throughput</strong></td><td>Number of work items completed during the selected period.</td></tr><tr><td><strong>Average Throughput per Week</strong></td><td>Average number of work items completed per week.</td></tr><tr><td><strong>Reopened Work Items</strong></td><td>Number of work items reopened after completion.</td></tr><tr><td><strong>Work Item Reopen Count</strong></td><td>Total number of reopen events during the selected period.</td></tr></tbody></table>

### Work Mix and Distribution Metrics

<table><thead><tr><th width="299.15478515625">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Innovation Rate by Count (%)</strong></td><td>Percentage of completed or planned work items classified as innovation or new product work.</td></tr><tr><td><strong>Innovation Rate by Effort (%)</strong></td><td>Percentage of total effort allocated to innovation or new product work.</td></tr><tr><td><strong>Work Item Type Distribution</strong></td><td>Distribution of work by configured work-item type.</td></tr><tr><td><strong>Work Item Priority Distribution</strong></td><td>Distribution of work by priority.</td></tr><tr><td><strong>Work Item Status Distribution</strong></td><td>Distribution of work items across workflow statuses.</td></tr><tr><td><strong>Work Item Category Distribution</strong></td><td>Distribution of work across configured categories such as new work, maintenance, bugs, or support.</td></tr><tr><td><strong>Work Type by Member</strong></td><td>Distribution of project work among team members and work categories.</td></tr><tr><td><strong>Project Contribution</strong></td><td>Distribution of completed work or effort among contributors and teams.</td></tr></tbody></table>

> Planning metrics depend on correct sprint dates, planning cut-off configuration, workflow mapping, effort fields, and excluded work-item types.

***

## Code Quality Analytics

Code Quality Analytics uses SonarQube or SonarCloud data to provide visibility into technical debt, security, reliability, maintainability, and codebase health.

See [Total Code Quality Index](https://docs.oobeya.io/quality-analytics/total-code-quality-index-tcqi).

### Core Quality Metrics

<table><thead><tr><th width="267.99993896484375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Technical Debt – Overall</strong></td><td>Estimated remediation time required to fix all maintainability issues in the analyzed codebase.</td></tr><tr><td><strong>Technical Debt – New Period</strong></td><td>Technical debt introduced during the selected period or on new code.</td></tr><tr><td><strong>Technical Debt per Developer</strong></td><td>Technical debt attributed to each developer based on source-control author information.</td></tr><tr><td><strong>Added Technical Debt</strong></td><td>Technical debt introduced during the selected period.</td></tr><tr><td><strong>Code Quality Issues</strong></td><td>Total number of quality issues detected by the connected code-quality platform.</td></tr><tr><td><strong>Bugs</strong></td><td>Number of reliability issues.</td></tr><tr><td><strong>Vulnerabilities</strong></td><td>Number of security issues.</td></tr><tr><td><strong>Code Smells</strong></td><td>Number of maintainability issues.</td></tr><tr><td><strong>Duplicated Lines (%)</strong></td><td>Percentage of code identified as duplicated.</td></tr><tr><td><strong>Test Coverage (%)</strong></td><td>Percentage of analyzed code covered by tests.</td></tr><tr><td><strong>Lines of Code</strong></td><td>Total analyzed codebase size used as an input for normalization and quality analysis.</td></tr></tbody></table>

### Severity and Risk Metrics

<table><thead><tr><th width="291.96014404296875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Blocker Issues</strong></td><td>Number of issues classified at the highest configured severity.</td></tr><tr><td><strong>High-Severity Issues</strong></td><td>Number of issues classified as high severity.</td></tr><tr><td><strong>Medium-Severity Issues</strong></td><td>Number of issues classified as medium severity.</td></tr><tr><td><strong>Low-Severity Issues</strong></td><td>Number of issues classified as low severity.</td></tr><tr><td><strong>Security Severity – Blocker, Overall</strong></td><td>Total blocker-level security issues in the analyzed codebase.</td></tr><tr><td><strong>Security Severity – High, Overall</strong></td><td>Total high-severity security issues in the analyzed codebase.</td></tr><tr><td><strong>Security Severity – Blocker, New Period</strong></td><td>New blocker-level security issues introduced during the selected period.</td></tr><tr><td><strong>Security Severity – High, New Period</strong></td><td>New high-severity security issues introduced during the selected period.</td></tr><tr><td><strong>Issue Risk Score</strong></td><td>Risk score calculated using issue severity, quality category, and remediation effort.</td></tr><tr><td><strong>Project Security Risk Score</strong></td><td>Aggregated security risk for the analyzed project.</td></tr><tr><td><strong>Project Reliability Risk Score</strong></td><td>Aggregated reliability risk for the analyzed project.</td></tr><tr><td><strong>Project Maintainability Risk Score</strong></td><td>Aggregated maintainability risk for the analyzed project.</td></tr></tbody></table>

The Issue Risk calculation follows this structure:

```
Issue Risk =
Severity Coefficient
× Quality Category Coefficient
× Remediation Coefficient
```

### Total Code Quality Index Metrics

<table><thead><tr><th width="298.04608154296875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Total Code Quality Index – TCQI</strong></td><td>Composite quality score based on issue severity, security, reliability, maintainability, remediation effort, and codebase size.</td></tr><tr><td><strong>Security Index</strong></td><td>Normalized score representing the security health of the codebase.</td></tr><tr><td><strong>Reliability Index</strong></td><td>Normalized score representing reliability health.</td></tr><tr><td><strong>Maintainability Index</strong></td><td>Normalized score representing maintainability health.</td></tr><tr><td><strong>Security Score / Rating</strong></td><td>Overall security rating provided by the connected quality platform.</td></tr><tr><td><strong>Reliability Score / Rating</strong></td><td>Overall reliability rating provided by the connected quality platform.</td></tr><tr><td><strong>Maintainability Score / Rating</strong></td><td>Overall maintainability rating provided by the connected quality platform.</td></tr><tr><td><strong>TCQI Trend</strong></td><td>Change in Total Code Quality Index over time.</td></tr><tr><td><strong>Security Index Trend</strong></td><td>Change in the Security Index over time.</td></tr><tr><td><strong>Reliability Index Trend</strong></td><td>Change in the Reliability Index over time.</td></tr><tr><td><strong>Maintainability Index Trend</strong></td><td>Change in the Maintainability Index over time.</td></tr></tbody></table>

> TCQI coefficients can be configured under the Code Quality administration settings.

***

## Application Performance Metrics

Application Performance metrics are available when Oobeya is connected to a supported APM or monitoring platform.

<table><thead><tr><th width="254.8720703125">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>APDEX Score</strong></td><td>Application Performance Index representing user satisfaction based on response-time thresholds.</td></tr><tr><td><strong>Error Rate (%)</strong></td><td>Percentage of application requests that result in an error.</td></tr><tr><td><strong>Average Response Time</strong></td><td>Average time required for the application or service to respond to requests.</td></tr><tr><td><strong>Transaction Volume</strong></td><td>Number of monitored application transactions during the selected period.</td></tr><tr><td><strong>Incident Count</strong></td><td>Number of detected operational incidents associated with the selected service or application.</td></tr><tr><td><strong>Application Performance Trend</strong></td><td>Change in application performance over time.</td></tr><tr><td><strong>Error Rate Trend</strong></td><td>Change in application errors over time.</td></tr><tr><td><strong>Response Time Trend</strong></td><td>Change in average response time over time.</td></tr></tbody></table>

Availability depends on the connected APM tool and the data exposed by that integration.

***

## Test Analytics

Test Analytics combines manual and automated test data from supported test management and automation systems.

See [Measuring and Improving Test Efficiency](https://docs.oobeya.io/use-cases/measuring-test-efficiency).

<table><thead><tr><th width="281.11083984375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Test Efficiency (%)</strong></td><td>Percentage of successful tests across all analyzed test runs.</td></tr><tr><td><strong>Escaped Defects (%)</strong></td><td>Ratio of defects discovered after UAT or the configured testing stage.</td></tr><tr><td><strong>Automation Coverage (%)</strong></td><td>Share of the tested scope or code covered by automated tests.</td></tr><tr><td><strong>UAT Success Rate (%)</strong></td><td>Percentage of successful User Acceptance Testing executions.</td></tr><tr><td><strong>Defect Resolution Rate (%)</strong></td><td>Percentage of detected defects resolved during the test cycle.</td></tr><tr><td><strong>Execution Time (ms)</strong></td><td>Average time required to execute a test.</td></tr><tr><td><strong>Total Test Executions</strong></td><td>Number of test executions during the selected period.</td></tr><tr><td><strong>Successful Test Executions</strong></td><td>Number of test executions completed successfully.</td></tr><tr><td><strong>Failed Test Executions</strong></td><td>Number of failed test executions.</td></tr><tr><td><strong>Manual Test Executions</strong></td><td>Number of manually executed tests.</td></tr><tr><td><strong>Automated Test Executions</strong></td><td>Number of tests executed through automation.</td></tr><tr><td><strong>Test Success Trend</strong></td><td>Change in successful test execution rate over time.</td></tr><tr><td><strong>Escaped Defect Trend</strong></td><td>Change in post-testing defect leakage over time.</td></tr><tr><td><strong>Automation Trend</strong></td><td>Change in automation coverage or automated execution share over time.</td></tr></tbody></table>

***

## AI Coding Assistant Impact

The AI Coding Assistant Impact module measures adoption, engagement, usage effectiveness, and the relationship between AI usage and software engineering outcomes.

See [GitHub Copilot – AI Impact](https://docs.oobeya.io/ai-impact/github-copilot-ai-impact) and [Measuring the Impact of AI Coding Assistants](https://docs.oobeya.io/use-cases/measuring-the-impact-of-ai-coding-assistants).

### User and License Metrics

<table><thead><tr><th width="276.793212890625">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Licensed Users</strong></td><td>Number of users assigned an AI coding assistant license.</td></tr><tr><td><strong>Active Users</strong></td><td>Number of licensed users who were active during the selected period.</td></tr><tr><td><strong>Engaged Users</strong></td><td>Number of active users who meaningfully interacted with AI coding assistant features.</td></tr><tr><td><strong>Inactive Users</strong></td><td>Licensed users without qualifying activity during the selected period.</td></tr><tr><td><strong>Inactive Users – Last 7 Days</strong></td><td>Users without qualifying AI activity during the last seven days.</td></tr><tr><td><strong>Inactive Users – Last 30 Days</strong></td><td>Users without qualifying AI activity during the last 30 days.</td></tr><tr><td><strong>Adoption Rate (%)</strong></td><td>Percentage of active users who are engaged: <code>Engaged Users / Active Users × 100</code>.</td></tr><tr><td><strong>License Utilization (%)</strong></td><td>Percentage of licensed users who actively use the AI coding assistant.</td></tr><tr><td><strong>User Activation Rate (%)</strong></td><td>Percentage of licensed users who became active during the selected period.</td></tr><tr><td><strong>Total Users</strong></td><td>Total number of users included in AI Impact reporting.</td></tr></tbody></table>

### Suggestion and Acceptance Metrics

<table><thead><tr><th width="285.92742919921875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Total Suggestions</strong></td><td>Number of code suggestions generated by the AI coding assistant.</td></tr><tr><td><strong>Accepted Suggestions</strong></td><td>Number of AI-generated suggestions accepted by users.</td></tr><tr><td><strong>Rejected Suggestions</strong></td><td>Number of suggestions not accepted by users.</td></tr><tr><td><strong>Suggestion Acceptance Rate (%)</strong></td><td>Percentage of suggestions accepted: <code>Accepted Suggestions / Total Suggestions × 100</code>.</td></tr><tr><td><strong>Suggested Lines</strong></td><td>Number of code lines suggested by the AI coding assistant.</td></tr><tr><td><strong>Accepted Lines</strong></td><td>Number of suggested code lines accepted by users.</td></tr><tr><td><strong>Line Acceptance Rate (%)</strong></td><td>Percentage of suggested lines accepted: <code>Accepted Lines / Suggested Lines × 100</code>.</td></tr><tr><td><strong>Accepted vs. Rejected Suggestions</strong></td><td>Distribution of accepted and rejected AI suggestions.</td></tr><tr><td><strong>Engagement and Acceptance Trend</strong></td><td>Change in assistant engagement and acceptance over time.</td></tr></tbody></table>

### Feature and Tool Usage Metrics

<table><thead><tr><th width="285.01873779296875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>IDE Code Completion Usage</strong></td><td>Usage generated through inline IDE code completions.</td></tr><tr><td><strong>Chat Usage</strong></td><td>Usage generated through AI chat interactions.</td></tr><tr><td><strong>Pull Request Integration Usage</strong></td><td>Usage generated through AI features integrated with pull request workflows.</td></tr><tr><td><strong>Feature Usage Distribution</strong></td><td>Distribution of AI usage across completion, chat, PR, and supported feature types.</td></tr><tr><td><strong>Usage by IDE / Editor</strong></td><td>Distribution of AI coding assistant activity by IDE or editor.</td></tr><tr><td><strong>Usage by Programming Language</strong></td><td>Distribution of AI activity by programming language.</td></tr><tr><td><strong>Usage by Model</strong></td><td>Distribution of usage across available AI models.</td></tr><tr><td><strong>Usage by Product</strong></td><td>Distribution across AI coding assistant products or SKUs.</td></tr><tr><td><strong>Usage Trend</strong></td><td>Change in AI coding assistant activity over time.</td></tr></tbody></table>

### Team and User-Level Indicators

<table><thead><tr><th width="305.95703125">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Team Adoption Rate (%)</strong></td><td>Adoption Rate calculated for a mapped Oobeya team.</td></tr><tr><td><strong>Team Engagement Rate (%)</strong></td><td>Percentage of team members meaningfully interacting with AI features.</td></tr><tr><td><strong>Team Acceptance Rate (%)</strong></td><td>Suggestion or line acceptance rate for a team.</td></tr><tr><td><strong>Most Active Team</strong></td><td>Team with the highest qualifying AI usage during the selected period.</td></tr><tr><td><strong>Most Efficient Usage Team</strong></td><td>Team with the strongest usage-effectiveness result based on configured acceptance and engagement indicators.</td></tr><tr><td><strong>Teams with Low Activity</strong></td><td>Teams whose AI usage remains below the configured activity level.</td></tr><tr><td><strong>Users with Low Activity</strong></td><td>Users whose AI usage remains below the configured activity level.</td></tr><tr><td><strong>Top Active Users</strong></td><td>Users with the highest qualifying AI activity.</td></tr><tr><td><strong>User Adoption and Engagement</strong></td><td>Adoption and engagement indicators shown at user level.</td></tr><tr><td><strong>Actual Contribution vs. AI Contribution</strong></td><td>Comparison between overall development contribution and AI-assisted contribution signals.</td></tr><tr><td><strong>AI Contribution Rate (%)</strong></td><td>Share of tracked development contribution associated with AI-assisted activity, where supported.</td></tr></tbody></table>

***

## AI Cost and Credits

The AI Cost and Credits module provides financial visibility into AI coding assistant consumption at organization, team, user, model, product, repository, and cost-center levels.

See [AI Cost and Credits](https://docs.oobeya.io/ai-impact/ai-cost-and-credits).

### Summary Metrics

<table><thead><tr><th width="260.155029296875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Total Users</strong></td><td>Number of users represented in the selected AI cost and credit data.</td></tr><tr><td><strong>AI Credit Pool Value</strong></td><td>Monetary value of the organization’s available AI credit pool.</td></tr><tr><td><strong>Total AI Credits Used</strong></td><td>Total number of AI credits consumed during the selected period.</td></tr><tr><td><strong>Remaining AI Credits</strong></td><td>Unused credits remaining in the configured credit pool.</td></tr><tr><td><strong>Total Gross Cost</strong></td><td>Total cost before discounts or adjustments.</td></tr><tr><td><strong>Discount Amount</strong></td><td>Total discount applied to AI usage charges.</td></tr><tr><td><strong>Net Cost</strong></td><td>Cost after discounts and adjustments.</td></tr><tr><td><strong>Applied Cost per Credit</strong></td><td>Monetary rate applied to each AI credit.</td></tr><tr><td><strong>Remaining Credit Pool Value</strong></td><td>Monetary value of credits remaining in the configured pool.</td></tr><tr><td><strong>Credit Utilization Rate (%)</strong></td><td>Percentage of the total credit pool consumed.</td></tr><tr><td><strong>Cost per User</strong></td><td>Average or individual AI cost attributed to a user.</td></tr><tr><td><strong>Credits per User</strong></td><td>Average or individual AI credits consumed by a user.</td></tr></tbody></table>

Where the standard AI credit rate is configured as USD 0.01:

```
AI Cost (USD) = AI Credits × 0.01
```

The actual rate may differ based on product configuration, provider pricing, contract terms, discounts, and imported billing data.

### Cost and Credit Breakdown Metrics

<table><thead><tr><th width="265.58935546875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Cost by User</strong></td><td>AI cost attributed to each user.</td></tr><tr><td><strong>Credits by User</strong></td><td>AI credits consumed by each user.</td></tr><tr><td><strong>Cost by Team</strong></td><td>AI cost aggregated by mapped Oobeya team.</td></tr><tr><td><strong>Credits by Team</strong></td><td>AI credits aggregated by team.</td></tr><tr><td><strong>Cost by Organization</strong></td><td>AI cost aggregated by source organization.</td></tr><tr><td><strong>Credits by Organization</strong></td><td>AI credits aggregated by source organization.</td></tr><tr><td><strong>Cost by Product</strong></td><td>AI cost grouped by AI coding assistant product.</td></tr><tr><td><strong>Credits by Product</strong></td><td>AI credits grouped by product.</td></tr><tr><td><strong>Cost by SKU</strong></td><td>Cost grouped by provider SKU.</td></tr><tr><td><strong>Credits by SKU</strong></td><td>Credit usage grouped by provider SKU.</td></tr><tr><td><strong>Cost by Model</strong></td><td>AI cost grouped by language model.</td></tr><tr><td><strong>Credits by Model</strong></td><td>Credit consumption grouped by language model.</td></tr><tr><td><strong>Model Usage Share (%)</strong></td><td>Percentage of total AI consumption attributed to each model.</td></tr><tr><td><strong>Cost by Repository</strong></td><td>AI cost associated with each repository, where repository data is available.</td></tr><tr><td><strong>Credits by Repository</strong></td><td>AI credit usage associated with each repository.</td></tr><tr><td><strong>Cost by Cost Center</strong></td><td>AI cost aggregated by mapped cost center.</td></tr><tr><td><strong>Credits by Cost Center</strong></td><td>AI credit usage aggregated by cost center.</td></tr></tbody></table>

### Cost Trend Metrics

<table><thead><tr><th width="303.2926025390625">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Daily Credit Consumption</strong></td><td>AI credits consumed per day.</td></tr><tr><td><strong>Monthly Credit Consumption</strong></td><td>AI credits consumed per month.</td></tr><tr><td><strong>Credit Consumption Trend</strong></td><td>Change in credit usage over time.</td></tr><tr><td><strong>Daily AI Cost</strong></td><td>AI cost generated per day.</td></tr><tr><td><strong>Monthly AI Cost</strong></td><td>AI cost generated per month.</td></tr><tr><td><strong>AI Cost Trend</strong></td><td>Change in AI cost over time.</td></tr><tr><td><strong>Average Daily Cost</strong></td><td>Average AI cost generated per day.</td></tr><tr><td><strong>Average Monthly Cost</strong></td><td>Average AI cost generated per month.</td></tr><tr><td><strong>Projected Period Cost</strong></td><td>Estimated cost for the full reporting period based on current consumption.</td></tr><tr><td><strong>Budget or Pool Consumption Trend</strong></td><td>Progress of cost or credit consumption against the configured pool.</td></tr></tbody></table>

### Estimated Token Metrics

Detailed input, output, and cached-token telemetry may not be provided directly by every AI coding assistant.

When estimated token reporting is enabled, Oobeya may display:

<table><thead><tr><th width="283.34942626953125">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Estimated Total Token Usage</strong></td><td>Estimated number of tokens represented by the observed AI cost and model-pricing assumptions.</td></tr><tr><td><strong>Estimated Input Tokens</strong></td><td>Estimated input-token volume.</td></tr><tr><td><strong>Estimated Output Tokens</strong></td><td>Estimated output-token volume.</td></tr><tr><td><strong>Estimated Cached Tokens</strong></td><td>Estimated token volume served from provider cache.</td></tr><tr><td><strong>Estimated Token Range</strong></td><td>Low, expected, and high token-usage estimates based on pricing and usage assumptions.</td></tr><tr><td><strong>Estimation Confidence</strong></td><td>Confidence indicator associated with the available model, feature, and pricing information.</td></tr></tbody></table>

> Estimated token metrics are estimates, not provider-reported exact telemetry. They must always be labeled as **Estimated**.

### Cost and Engineering Impact Analysis

The module can compare AI cost and credit consumption with engineering outcome metrics.

<table><thead><tr><th width="306.9544677734375">Analysis</th><th>Description</th></tr></thead><tbody><tr><td><strong>AI Cost vs. Adoption Rate</strong></td><td>Compares financial consumption with AI adoption.</td></tr><tr><td><strong>AI Cost vs. Acceptance Rate</strong></td><td>Compares cost with suggestion or line acceptance.</td></tr><tr><td><strong>AI Cost vs. Coding Efficiency</strong></td><td>Examines whether cost changes coincide with changes in Coding Efficiency.</td></tr><tr><td><strong>AI Cost vs. Coding Impact</strong></td><td>Compares AI spend with the scope and impact of development activity.</td></tr><tr><td><strong>AI Cost vs. Code Churn</strong></td><td>Examines whether increased AI consumption coincides with more or less short-term rework.</td></tr><tr><td><strong>AI Cost vs. Pull Request Cycle Time</strong></td><td>Compares AI spend with pull request review and merge speed.</td></tr><tr><td><strong>AI Cost vs. Lead Time for Changes</strong></td><td>Compares cost with end-to-end delivery time.</td></tr><tr><td><strong>AI Cost vs. Deployment Frequency</strong></td><td>Compares AI spend with production delivery frequency.</td></tr><tr><td><strong>AI Cost vs. Change Failure Rate</strong></td><td>Examines the relationship between AI spend and delivery stability.</td></tr><tr><td><strong>AI Cost vs. Time to Restore Service</strong></td><td>Compares AI spend with production restoration performance.</td></tr><tr><td><strong>AI Cost vs. Technical Debt</strong></td><td>Examines whether AI consumption coincides with changes in technical debt.</td></tr><tr><td><strong>AI Cost vs. Code Quality</strong></td><td>Compares AI spend with quality, security, reliability, and maintainability indicators.</td></tr></tbody></table>

> Correlation does not prove causation. These analyses are intended to identify patterns that should be investigated together with team context, workflow changes, and sample size.

***

## Document Analytics for Confluence

Document Analytics provides visibility into documentation activity, content freshness, contribution patterns, and Confluence Space health.

Metrics may be available at organization, Space, team, and contributor levels.

See [Document Analytics – Confluence](https://docs.oobeya.io/document-analytics/document-analytics-confluence).

### Organization and Space Overview

<table><thead><tr><th width="267.8265380859375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Total Spaces</strong></td><td>Total number of Confluence Spaces included in the analysis.</td></tr><tr><td><strong>Active Spaces</strong></td><td>Number of Spaces with qualifying documentation activity during the selected period.</td></tr><tr><td><strong>Inactive Spaces</strong></td><td>Number of Spaces without qualifying activity during the selected period.</td></tr><tr><td><strong>Total Pages</strong></td><td>Total number of analyzed Confluence pages.</td></tr><tr><td><strong>Total Contributors</strong></td><td>Number of contributors associated with analyzed content.</td></tr><tr><td><strong>Active Contributors</strong></td><td>Number of contributors who created or updated content during the selected period.</td></tr><tr><td><strong>Pages per Space</strong></td><td>Average or total number of pages within each Space.</td></tr><tr><td><strong>Contributors per Space</strong></td><td>Number of active contributors associated with each Space.</td></tr><tr><td><strong>Space Activity Score</strong></td><td>Relative indicator representing documentation activity within a Space.</td></tr><tr><td><strong>Space Ranking</strong></td><td>Ranking of Spaces based on selected activity, freshness, or health indicators.</td></tr></tbody></table>

### Documentation Activity Metrics

<table><thead><tr><th width="297.08935546875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Pages Created</strong></td><td>Number of pages created during the selected period.</td></tr><tr><td><strong>Pages Updated</strong></td><td>Number of unique pages updated during the selected period.</td></tr><tr><td><strong>Page Update Count</strong></td><td>Total number of page-update activities.</td></tr><tr><td><strong>Content Activity</strong></td><td>Combined view of page creation and update activity.</td></tr><tr><td><strong>Page Creation Trend</strong></td><td>Change in newly created pages over time.</td></tr><tr><td><strong>Page Update Trend</strong></td><td>Change in page-update activity over time.</td></tr><tr><td><strong>Space Activity Trend</strong></td><td>Change in documentation activity for a Space over time.</td></tr><tr><td><strong>Contributor Activity</strong></td><td>Number of page creation and update activities attributed to each contributor.</td></tr><tr><td><strong>Contribution Distribution</strong></td><td>Distribution of documentation activity across contributors.</td></tr><tr><td><strong>Pages Created per Contributor</strong></td><td>Average or individual number of pages created by contributors.</td></tr><tr><td><strong>Pages Updated per Contributor</strong></td><td>Average or individual number of pages updated by contributors.</td></tr></tbody></table>

### Freshness and Documentation Health

<table><thead><tr><th width="283.18157958984375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Documentation Health Score</strong></td><td>Composite indicator summarizing freshness, maintenance activity, contributor participation, and other configured documentation signals.</td></tr><tr><td><strong>Fresh Pages</strong></td><td>Number of pages updated within the configured freshness period.</td></tr><tr><td><strong>Fresh Content Rate (%)</strong></td><td>Percentage of analyzed pages classified as fresh.</td></tr><tr><td><strong>Stale Pages</strong></td><td>Number of pages not updated within the configured stale-content threshold.</td></tr><tr><td><strong>Stale Content Rate (%)</strong></td><td>Percentage of analyzed pages classified as stale.</td></tr><tr><td><strong>Average Page Age</strong></td><td>Average age of analyzed pages since creation.</td></tr><tr><td><strong>Average Time Since Last Update</strong></td><td>Average elapsed time since pages were last updated.</td></tr><tr><td><strong>Oldest Page Update Age</strong></td><td>Longest elapsed time since a page was updated.</td></tr><tr><td><strong>Pages Needing Attention</strong></td><td>Number of pages identified as stale, inactive, or requiring review.</td></tr><tr><td><strong>Spaces Needing Attention</strong></td><td>Number of Spaces with low activity, stale content, or other documentation-health risks.</td></tr></tbody></table>

### Team and Ownership Indicators

<table><thead><tr><th width="302.822265625">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Mapped Teams</strong></td><td>Number of Oobeya teams associated with analyzed Confluence Spaces.</td></tr><tr><td><strong>Spaces with Team Mapping</strong></td><td>Number of Spaces connected to at least one Oobeya team.</td></tr><tr><td><strong>Spaces without Team Mapping</strong></td><td>Number of Spaces without an assigned team relationship.</td></tr><tr><td><strong>Pages by Team</strong></td><td>Documentation pages attributed to each mapped team.</td></tr><tr><td><strong>Activity by Team</strong></td><td>Documentation creation and update activity attributed to each team.</td></tr><tr><td><strong>Contributors by Team</strong></td><td>Active documentation contributors grouped by team.</td></tr><tr><td><strong>Team-to-Space Relationships</strong></td><td>Distribution of mapped team relationships across Spaces.</td></tr><tr><td><strong>Documentation Coverage by Team</strong></td><td>Visibility into whether mapped teams maintain active and current documentation.</td></tr></tbody></table>

> Freshness and health results depend on the configured stale-content period and the availability of Confluence history and contributor data.

***

## Resource Allocation

Resource Allocation shows how planned workload and engineering capacity are distributed across projects and contributors.

See [Resource Allocation](https://docs.oobeya.io/allocations/resource-allocation).

### Overview Metrics

<table><thead><tr><th width="295.1171875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Total Projects</strong></td><td>Number of projects included in Resource Allocation analysis.</td></tr><tr><td><strong>Total Resources</strong></td><td>Number of contributors included in the analysis.</td></tr><tr><td><strong>Utilization by Effort (%)</strong></td><td>Resource utilization calculated using estimated effort.</td></tr><tr><td><strong>Utilization by Count (%)</strong></td><td>Resource utilization calculated using work-item count.</td></tr><tr><td><strong>Resource Status Distribution</strong></td><td>Distribution of resources classified as Underutilized, Optimally Utilized, Slightly Overloaded, or Overloaded.</td></tr><tr><td><strong>Planned Work Items</strong></td><td>Number of work items assigned to a resource or team.</td></tr><tr><td><strong>Delivered Work Items</strong></td><td>Number of work items completed by a resource or team.</td></tr><tr><td><strong>Planned Effort</strong></td><td>Estimated effort assigned to a resource or team.</td></tr><tr><td><strong>Delivered Effort</strong></td><td>Estimated effort completed by a resource or team.</td></tr><tr><td><strong>Team Average Capacity</strong></td><td>Delivered work divided by the number of contributors in the team.</td></tr></tbody></table>

### Resource Utilization Metrics

<table><thead><tr><th width="322.19873046875">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Resource Utilization (%)</strong></td><td>Planned work assigned to a resource relative to the team’s average delivery capacity.</td></tr><tr><td><strong>Team Utilization (%)</strong></td><td>Aggregated utilization level of a team.</td></tr><tr><td><strong>Underutilized Resources</strong></td><td>Resources whose utilization is below the configured lower threshold.</td></tr><tr><td><strong>Optimally Utilized Resources</strong></td><td>Resources operating within the configured optimal range.</td></tr><tr><td><strong>Slightly Overloaded Resources</strong></td><td>Resources above the optimal range but below the highest overload threshold.</td></tr><tr><td><strong>Overloaded Resources</strong></td><td>Resources whose utilization exceeds the configured overload threshold.</td></tr></tbody></table>

Default calculation:

```
Team Average Capacity =
Delivered Work Items / Number of Contributors
```

```
Resource Utilization (%) =
Planned Work Items / Team Average Capacity × 100
```

Default classification:

<table><thead><tr><th width="284.8621826171875">Utilization</th><th>Status</th></tr></thead><tbody><tr><td><strong>≤ 85%</strong></td><td>Underutilized</td></tr><tr><td><strong>85%–110%</strong></td><td>Optimally Utilized</td></tr><tr><td><strong>110%–130%</strong></td><td>Slightly Overloaded</td></tr><tr><td><strong>> 130%</strong></td><td>Overloaded</td></tr></tbody></table>

Thresholds can be customized by administrators.

### Project Allocation Metrics

<table><thead><tr><th width="302.4014892578125">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Project Allocation (%)</strong></td><td>Percentage of a contributor’s planned work assigned to a particular project.</td></tr><tr><td><strong>Allocation by Work-Item Count (%)</strong></td><td>Project allocation calculated using planned work-item count.</td></tr><tr><td><strong>Allocation by Effort (%)</strong></td><td>Project allocation calculated using estimated effort.</td></tr><tr><td><strong>Projects per Contributor</strong></td><td>Number of projects to which a contributor is allocated.</td></tr><tr><td><strong>Contributors per Project</strong></td><td>Number of contributors allocated to a project.</td></tr><tr><td><strong>Allocation Distribution</strong></td><td>Distribution of contributor capacity across projects.</td></tr></tbody></table>

Calculation:

```
Project Allocation (%) =
Planned Items for the Contributor in the Project
/
Total Planned Items for the Contributor Across All Projects
× 100
```

***

## Bug Report

The Bug Report module provides organization- and team-level visibility into open defects, severity, ownership, and bug trends.

See [Bug Report Dashboard](https://docs.oobeya.io/bug-report/bug-report-dashboard).

<table><thead><tr><th width="262.41448974609375">Metric or Indicator</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Open Bugs</strong></td><td>Number of bug-type work items currently in an open status.</td></tr><tr><td><strong>Open Bugs Over Time</strong></td><td>Trend of open bugs across the selected period.</td></tr><tr><td><strong>Bugs by Severity</strong></td><td>Distribution of bugs across Blocker, Critical, High, Medium, and Low severity levels.</td></tr><tr><td><strong>Blocker Bugs</strong></td><td>Number of open bugs mapped to Blocker severity.</td></tr><tr><td><strong>Critical Bugs</strong></td><td>Number of open bugs mapped to Critical severity.</td></tr><tr><td><strong>High-Severity Bugs</strong></td><td>Number of open bugs mapped to High severity.</td></tr><tr><td><strong>Medium-Severity Bugs</strong></td><td>Number of open bugs mapped to Medium severity.</td></tr><tr><td><strong>Low-Severity Bugs</strong></td><td>Number of open bugs mapped to Low severity.</td></tr><tr><td><strong>Bug Distribution by Team</strong></td><td>Number or percentage of bugs associated with each mapped team.</td></tr><tr><td><strong>Team Bugs</strong></td><td>Bugs assigned to or associated with the selected team.</td></tr><tr><td><strong>Unassigned Bugs</strong></td><td>Bugs without an assigned owner.</td></tr><tr><td><strong>Other Teams’ Bugs</strong></td><td>Bugs visible in the current scope but associated with other teams.</td></tr><tr><td><strong>Bug Status Distribution</strong></td><td>Distribution of bugs across mapped workflow statuses.</td></tr><tr><td><strong>Bug Type Distribution</strong></td><td>Distribution across configured Bug, Defect, Problem, Incident, Error, or similar work-item types.</td></tr><tr><td><strong>Bug Trend by Severity</strong></td><td>Change in open bugs for each severity level over time.</td></tr></tbody></table>

Bug reporting depends on correct category and severity mapping in the administration settings.

***

## Activity Heatmap

Activity Heatmap visualizes daily developer activities and helps identify workload imbalance, concentrated contribution, unusually high activity, and low participation.

See [Activity Heatmap](https://docs.oobeya.io/activity-heatmap/activity-heatmap).

### Activity Inputs

<table><thead><tr><th width="238.089599609375">Metric</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Commits</strong></td><td>Number of commits made by a developer.</td></tr><tr><td><strong>Lines Added</strong></td><td>Number of code lines added.</td></tr><tr><td><strong>Lines Deleted</strong></td><td>Number of code lines deleted.</td></tr><tr><td><strong>Lines Edited</strong></td><td>Number of code lines modified.</td></tr><tr><td><strong>PRs Created</strong></td><td>Number of pull requests created.</td></tr><tr><td><strong>PR Reviews</strong></td><td>Number of code reviews performed.</td></tr><tr><td><strong>PR Approvals</strong></td><td>Number of pull requests approved.</td></tr><tr><td><strong>PR Needs Work</strong></td><td>Number of pull requests returned for changes.</td></tr><tr><td><strong>PR Comments</strong></td><td>Number of comments added to pull requests.</td></tr></tbody></table>

Each activity type can have a configurable coefficient that determines its contribution to the score.

### Calculated Scores

<table><thead><tr><th width="252.76470947265625">Metric or Score</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Commit Activity Score</strong></td><td>Weighted score generated from commits and code-change activity.</td></tr><tr><td><strong>Pull Request Activity Score</strong></td><td>Weighted score generated from PR creation, review, approval, change-request, and comment activity.</td></tr><tr><td><strong>Total Activity Score</strong></td><td>Combined weighted score across commit and pull request activity.</td></tr><tr><td><strong>Daily Rank Ratio</strong></td><td>A developer’s daily score relative to the highest-scoring developer for that day.</td></tr><tr><td><strong>Daily Normalized Score</strong></td><td>Daily activity score normalized for team comparison.</td></tr><tr><td><strong>Activity Z-Score</strong></td><td>Standardized activity score calculated from the team’s daily distribution.</td></tr><tr><td><strong>Heatmap Score</strong></td><td>Normalized 0–100 score used to determine heatmap intensity.</td></tr><tr><td><strong>Developer Total Score</strong></td><td>Total activity score attributed to a developer during the selected period.</td></tr><tr><td><strong>Team Activity Distribution</strong></td><td>Distribution of normalized activity scores across team members.</td></tr></tbody></table>

> Activity Heatmap scores represent activity intensity, not work quality, value, or individual performance.

***

## Gamification

Gamification converts selected Oobeya metrics and manually defined KPIs into configurable points, rounds, leagues, and rankings.

See [Gamification](https://docs.oobeya.io/gamification/gamification).

Gamification can use metrics from:

* Project Management
* Development Analytics
* Pull Request Analytics
* Code Quality
* Security
* Engineering Symptoms
* Manually defined KPIs

### Gamification Outputs

<table><thead><tr><th width="261.750244140625">Metric or Score</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Metric Result</strong></td><td>Actual value of the selected engineering metric for a scoring round.</td></tr><tr><td><strong>Metric Threshold</strong></td><td>Configured value range used to assign points.</td></tr><tr><td><strong>Metric Points</strong></td><td>Points earned from a metric based on its scoring thresholds.</td></tr><tr><td><strong>Manual KPI Points</strong></td><td>Points manually entered and approved by a league referee.</td></tr><tr><td><strong>Round Score</strong></td><td>Total points earned by a team during a scoring round.</td></tr><tr><td><strong>Approved Round Score</strong></td><td>Round Score after referee review and approval.</td></tr><tr><td><strong>Cumulative Score</strong></td><td>Total points accumulated across completed rounds.</td></tr><tr><td><strong>Team Rank</strong></td><td>Position of a team based on cumulative or selected-round score.</td></tr><tr><td><strong>League Ranking</strong></td><td>Ranking of all participating teams within a league.</td></tr><tr><td><strong>Maximum Available Points</strong></td><td>Maximum points a team can earn under the configured rules.</td></tr><tr><td><strong>Achievement Rate (%)</strong></td><td>Earned points relative to the maximum available points, where displayed.</td></tr></tbody></table>

> Gamification scores are derived outputs. The underlying engineering metrics retain their original definitions and units.

***

## Team Scorecards, Developer Profiles, and Dashboards

Team Scorecards, Developer Profiles, and Custom Dashboards do not create a separate set of underlying engineering metrics.

They present and aggregate metrics from the modules listed above at different organizational levels.

### Team Scorecards

Team Scorecards can include:

* Development Analytics
* Pull Request Analytics
* DORA Metrics
* Project Analytics
* Code Quality
* Test Analytics
* Bug Analytics
* AI Impact
* Resource Allocation
* Custom scorecard widgets

Metrics are filtered by the repositories, projects, integrations, and users mapped to the selected team.

### Developer Profiles

Developer Profiles can include:

* Coding Impact
* Coding Efficiency
* Work Type
* Code Churn
* Commit activity
* Repository contribution
* Pull requests
* Code reviews
* Code quality contribution
* Project activity
* AI usage and engagement, where available

Developer-level metrics depend on accurate identity matching across connected tools.

***

## Engineering Insights and Symptoms

Engineering Insights and Symptoms analyze multiple metrics together to identify significant patterns, risks, improvements, and recurring engineering anti-patterns.

They are analytical outputs rather than separate raw metrics.

Examples include:

* Recurring high rework
* Oversized pull requests
* Review bottlenecks
* High cognitive load
* Low Coding Efficiency
* Delivery slowdown
* Low Sprint Predictability
* High Change Failure Rate
* Unbalanced contribution
* Rising technical debt
* Workload imbalance

Each insight or Symptom may include:

<table><thead><tr><th width="283.422607421875">Indicator</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Current Value</strong></td><td>Metric value for the selected reporting period.</td></tr><tr><td><strong>Previous Period Value</strong></td><td>Metric value for the comparison period.</td></tr><tr><td><strong>Change (%)</strong></td><td>Percentage change between periods.</td></tr><tr><td><strong>Benchmark Value</strong></td><td>Relevant engineering benchmark or configured target.</td></tr><tr><td><strong>Primary Contributor</strong></td><td>Repository, team member, project, service, or pipeline most associated with the result.</td></tr></tbody></table>

See the [Symptoms Catalog](https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog) and [Engineering Benchmarks](https://docs.oobeya.io/team-insights-and-symptoms/engineering-benchmarks).

***

## Important Interpretation Guidelines

### Use Trends, Not Isolated Values

A single value rarely provides enough context. Review:

* Current value
* Previous-period value
* Long-term trend
* Team history
* Engineering benchmark
* Product and workflow context

### Do Not Rank Developers Using Activity Volume Alone

Metrics such as commits, code lines, pull requests, or Activity Heatmap scores should not be used alone to evaluate individual performance.

They do not directly measure:

* Business value
* Code quality
* Task difficulty
* Mentoring
* Architecture work
* Incident response
* Collaboration outside tracked tools
* Product discovery
* Customer impact

### Correlation Does Not Prove Causation

When two metrics move together, use language such as:

* Appears to be associated with
* Coincides with
* May be contributing to
* Is concentrated in
* Should be investigated together with

Avoid assuming that one metric directly caused another without supporting evidence.

### Validate Data Configuration

Unexpected metric results are often related to:

* Incorrect user or contributor mapping
* Missing repositories
* Incorrect branch selection
* Incorrect production pipeline mapping
* Missing incident sources
* Incorrect workflow status mapping
* Excluded work-item types
* Missing effort values
* Incorrect team membership
* Missing Confluence Space mappings
* Missing AI product, model, or cost-center mappings

***

## Related Documentation

* [Oobeya Quick Onboarding Guide](https://docs.oobeya.io/getting-started/oobeya-quick-onboarding-guide)
* [Git Analytics – Metric Definitions](https://docs.oobeya.io/gitwiser-repo-analytics/git-analytics-metric-definitions)
* [DORA Metrics Introduction](https://docs.oobeya.io/deployment-analytics/dora-metrics-introduction)
* [Project Analytics – Metric Definitions](https://docs.oobeya.io/project-analytics/project-analytics-metric-definitions)
* [Total Code Quality Index](https://docs.oobeya.io/quality-analytics/total-code-quality-index-tcqi)
* [Test Analytics](https://docs.oobeya.io/use-cases/measuring-test-efficiency)
* [GitHub Copilot – AI Impact](https://docs.oobeya.io/ai-impact/github-copilot-ai-impact)
* [AI Cost and Credits](https://docs.oobeya.io/ai-impact/ai-cost-and-credits)
* [Document Analytics – Confluence](https://docs.oobeya.io/document-analytics/document-analytics-confluence)
* [Resource Allocation](https://docs.oobeya.io/allocations/resource-allocation)
* [Bug Report Dashboard](https://docs.oobeya.io/bug-report/bug-report-dashboard)
* [Activity Heatmap](https://docs.oobeya.io/activity-heatmap/activity-heatmap)
* [Gamification](https://docs.oobeya.io/gamification/gamification)
* [Symptoms Catalog](https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog)
* [Engineering Benchmarks](https://docs.oobeya.io/team-insights-and-symptoms/engineering-benchmarks)
