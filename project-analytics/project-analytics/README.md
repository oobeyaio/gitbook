# Project Analytics

**Project Analytics** analyzes how an agile team plans and delivers work on its Scrum or Kanban board. It shows where work waits, how predictable sprints are, and how scope changes, so that the team and its Product Owner can use the data in sprint planning and sprint reviews.

Open it with **Analytics** > **Projects & Boards** in the left menu. Each board analysis has a **Board Overview** and a **Sprint Reports** tab. Board metrics also appear in the **Project Management** stage of each [Team Scorecard](https://docs.oobeya.io/team-health/team-scorecards).

### Before you start

Connect your project management tool on the [Integrations](https://docs.oobeya.io/integrations/adding-new-integration) page: [Jira Cloud](https://docs.oobeya.io/integrations/all-integrations/project-management-addons/jira-cloud-integration), [Jira Server / Data Center](https://docs.oobeya.io/integrations/all-integrations/project-management-addons/jira-server-integration), [Azure DevOps](https://docs.oobeya.io/integrations/all-integrations/scm-addons/azure-devops-integration) (Azure Boards), or [ServiceNow](https://docs.oobeya.io/integrations/all-integrations/project-management-addons/servicenow-integration). Then [start a board analysis](https://docs.oobeya.io/project-analytics/project-analytics/starting-an-agile-board-analysis).

### Board Overview

| Widget                          | What it shows                                                         |
| ------------------------------- | --------------------------------------------------------------------- |
| **Summary**                     | Basic information about the board, such as its name and type.         |
| **Time in State**               | Average time a work item stays in each state before it is completed.  |
| **Sprint Velocity Metrics**     | How much work the team completes in a single sprint.                  |
| **Assignee List**               | All assignees and their activity on the board.                        |
| **Work In Progress (> 5 days)** | Open work items that have been in progress for more than 5 days.      |
| **Scope Change**                | Changes during the sprint, as work item count and estimated effort.   |
| **Estimated/Actual Effort**     | Estimated effort compared with the time the team spent on work items. |

### Sprint Reports

**Sprint Reports** shows the metrics of one sprint at a time, so you can follow the history of the team's sprints.

| Widget                          | What it shows                                                                                          |
| ------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Sprint Velocity Metrics**     | Number of work items and estimated effort per sprint.                                                  |
| **Sprint Assignee List**        | Team members with work items assigned in the sprint.                                                   |
| **Completed Issues in Sprint**  | Work items completed by the end of the sprint.                                                         |
| **Incomplete Issues in Sprint** | Work items still open at the end of the sprint.                                                        |
| **Removed Issues in Sprint**    | Work items dropped from the running sprint, including pulled-in items dropped before the sprint ended. |
| **Issue Distribution**          | Distribution of work item types and priorities, by count and by story points.                          |
| **Scope Change**                | Changes during the sprint, as story count and estimated effort.                                        |

### Update or delete a board analysis

Open the board analysis and select **Update Analysis** in its actions menu. Every setting except the **Data Source** and the **Board** can be changed; go through the steps and update the board analysis at the last step. **Delete Analysis** in the same menu removes the analysis. **Reanalyze** runs the analysis again.

### Metric definitions

Every Project Analytics metric is defined in [Project Analytics - Metric Definitions](https://docs.oobeya.io/project-analytics/project-analytics-metric-definitions) and in the [Metrics List](https://docs.oobeya.io/getting-started/metrics/project-analytics).

### Related

* [Starting an Agile Board Analysis](https://docs.oobeya.io/project-analytics/project-analytics/starting-an-agile-board-analysis)
* [Best practices for integrating Oobeya with Azure DevOps Scrum Boards](https://docs.oobeya.io/project-analytics/best-practices-for-integrating-oobeya-with-azure-devops-scrum-boards)
