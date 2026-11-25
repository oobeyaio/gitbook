---
description: >-
  Board, flow, sprint, backlog, and work-mix metrics from Jira, Azure Boards,
  and other project management tools.
---

# Project Analytics

Project Analytics analyzes work items from Jira, Azure Boards, and supported project management systems. Depending on the data-source configuration, metrics are calculated by work-item count, effort, story points, or time estimation.

See [Project Analytics - Metric Definitions](https://docs.oobeya.io/project-analytics/project-analytics-metric-definitions).

### Board-Level Metrics

| Metric                              | What it measures                                                    |
| ----------------------------------- | ------------------------------------------------------------------- |
| **Completed Sprints**               | Number of sprints started and completed during the selected period. |
| **Average Velocity by Effort**      | Average amount of estimated effort completed per sprint.            |
| **Average Lead Time**               | Average time from work-item creation to completion.                 |
| **Average Cycle Time**              | Average time from work start to completion.                         |
| **Completed Work Items**            | Total number of work items completed during the selected period.    |
| **Completed Work Items per Sprint** | Average number of work items completed in each sprint.              |
| **Average Throughput per Week**     | Average number of work items completed per working week.            |

### Flow and Reaction Time Metrics

| Metric                   | What it measures                                                                                              |
| ------------------------ | ------------------------------------------------------------------------------------------------------------- |
| **Pickup Time**          | Initial time between work-item creation and its recognition or placement into a ready backlog or queue.       |
| **Actual Reaction Time** | Time from the configured reference point or ready state until work starts.                                    |
| **Total Reaction Time**  | Pickup Time plus Actual Reaction Time.                                                                        |
| **Cycle Time**           | Time from when active work begins until the work item is completed.                                           |
| **Lead Time**            | Time from work-item creation until completion.                                                                |
| **Lead Time Breakdown**  | Distribution of total Lead Time across reaction, active development, waiting, and configured workflow phases. |
| **State Cycle Time**     | Time spent in each mapped workflow state.                                                                     |
| **Time in Status**       | Amount of time a work item remains in a specific status.                                                      |
| **Waiting Time**         | Time a work item remains idle between active workflow states.                                                 |

### Sprint Planning Metrics

| Metric                                | What it measures                                                                  |
| ------------------------------------- | --------------------------------------------------------------------------------- |
| **Planned**                           | Number of work items included before the sprint planning cut-off date.            |
| **Planned Effort**                    | Total estimated effort of work items included before the planning cut-off date.   |
| **Done Planned**                      | Number of planned work items completed by the end of the sprint.                  |
| **Done Planned Effort**               | Estimated effort of planned work items completed by the end of the sprint.        |
| **Pulled in Extra**                   | Number of work items added after the sprint planning cut-off date.                |
| **Effort Pulled in Extra**            | Estimated effort of work items added after the planning cut-off date.             |
| **Done Pulled in Extra**              | Number of pulled-in work items completed by the end of the sprint.                |
| **Done Pulled in Extra Effort**       | Estimated effort of pulled-in work completed by the end of the sprint.            |
| **Unfinished**                        | Number of work items incomplete at the end of the sprint.                         |
| **Unfinished Effort**                 | Estimated effort of work items incomplete at the end of the sprint.               |
| **Unfinished Planned**                | Number of planned work items incomplete at the end of the sprint.                 |
| **Unfinished Effort Planned**         | Estimated effort of planned work items incomplete at the end of the sprint.       |
| **Unfinished Pulled in Extra**        | Number of pulled-in work items incomplete at the end of the sprint.               |
| **Unfinished Effort Pulled in Extra** | Estimated effort of pulled-in work items incomplete at the end of the sprint.     |
| **Dropped**                           | Number of work items removed from an active sprint after the planning cut-off.    |
| **Effort Dropped**                    | Estimated effort of work items removed from the sprint.                           |
| **End of Sprint**                     | Total number of completed and incomplete work items at the end of the sprint.     |
| **Effort End of Sprint**              | Total estimated effort of completed and incomplete work at the end of the sprint. |
| **Done**                              | Total number of work items completed by the end of the sprint.                    |
| **Done Effort**                       | Total estimated effort of completed work items.                                   |

### Sprint Performance Metrics

| Metric                                     | What it measures                                                                                                                                   |
| ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint Velocity by Count**               | Number of work items completed during the sprint.                                                                                                  |
| **Sprint Velocity by Effort**              | Total estimated effort completed during the sprint.                                                                                                |
| **Predictability (%)**                     | Percentage of originally planned work completed: `Done Planned / Planned × 100`.                                                                   |
| **Productivity (%)**                       | Total completed planned and extra work relative to the original plan: `(Done Planned + Done Pulled in Extra) / Planned × 100`.                     |
| **Churn (%)**                              | Percentage of completed work that was pulled into the sprint after planning: `Done Pulled in Extra / (Done Planned + Done Pulled in Extra) × 100`. |
| **Sprint Delivery Rate by Count (%)**      | Completed work items divided by total work items at the end of the sprint.                                                                         |
| **Sprint Delivery Rate by Effort (%)**     | Completed effort divided by total effort at the end of the sprint.                                                                                 |
| **Sprint Planning Accuracy by Count (%)**  | Completed work items divided by planned work items.                                                                                                |
| **Sprint Planning Accuracy by Effort (%)** | Completed effort divided by planned effort.                                                                                                        |
| **Sprint Scope Change**                    | Amount of work added to or removed from a sprint after the planning cut-off.                                                                       |
| **Scope Change Rate (%)**                  | Relative change in sprint scope after planning.                                                                                                    |

### Backlog and Kanban Metrics

| Metric                           | What it measures                                                        |
| -------------------------------- | ----------------------------------------------------------------------- |
| **Backlog Size**                 | Number of uncompleted work items in the backlog, excluding active work. |
| **Backlog Age**                  | Age of the oldest or longest-waiting item in the backlog.               |
| **Average Backlog Age**          | Average age of work items currently in the backlog.                     |
| **Open Bugs in Backlog**         | Number of bug-type work items currently waiting in the backlog.         |
| **Current Backlog Items**        | Number of items waiting in a Kanban backlog.                            |
| **Work in Progress**             | Number of work items currently in active workflow states.               |
| **Work in Progress Over 5 Days** | Work items that have remained in progress for more than five days.      |
| **Throughput**                   | Number of work items completed during the selected period.              |
| **Average Throughput per Week**  | Average number of work items completed per week.                        |
| **Reopened Work Items**          | Number of work items reopened after completion.                         |
| **Work Item Reopen Count**       | Total number of reopen events during the selected period.               |

### Work Mix and Distribution Metrics

| Metric                              | What it measures                                                                                   |
| ----------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Innovation Rate by Count (%)**    | Percentage of completed or planned work items classified as innovation or new product work.        |
| **Innovation Rate by Effort (%)**   | Percentage of total effort allocated to innovation or new product work.                            |
| **Work Item Type Distribution**     | Distribution of work by configured work-item type.                                                 |
| **Work Item Priority Distribution** | Distribution of work by priority.                                                                  |
| **Work Item Status Distribution**   | Distribution of work items across workflow statuses.                                               |
| **Work Item Category Distribution** | Distribution of work across configured categories such as new work, maintenance, bugs, or support. |
| **Work Type by Member**             | Distribution of project work among team members and work categories.                               |
| **Project Contribution**            | Distribution of completed work or effort among contributors and teams.                             |

{% hint style="info" %}
Planning metrics depend on correct sprint dates, planning cut-off configuration, workflow mapping, effort fields, and excluded work-item types.
{% endhint %}
