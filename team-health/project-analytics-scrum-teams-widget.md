---
description: Let's learn about the Project Analytics (Scrum Teams) widget.
---

# Project Analytics (Scrum Teams) Widget

### Introduction

The Project Analytics (Scrum Teams) widget on the team scorecard provides agile teams with in-depth insights into their performance and progress. Integrated seamlessly with Oobeya's AgileSpace module, gathering data from Jira or Azure Boards, this widget empowers teams to track sprint metrics, assess backlog health, and manage resource allocation effectively. It is designed to help stakeholders make informed, data-driven decisions to optimize team performance.

***

### Requirements

To use the Project Analytics (Scrum Teams) widget effectively, the following requirements must be met:

* **Team Setup:** A team must be created within Oobeya to enable data aggregation and analysis.
* **Agile Space Analysis:** An Agile Space analysis must be set up and configured properly to retrieve relevant data from Jira or Azure Boards.
* **Analysis Association:** The Agile Space analysis must be linked to the corresponding team for accurate reporting and tracking.
* **Team Scorecard Creation:** A Team Scorecard must be created for the designated team to visualize and analyze the collected data effectively.

For detailed instructions on setting up teams and Agile Space analysis check out [Team Health](https://app.gitbook.com/s/-MGIlBSTjQtZxUoFwUx4/team-health "mention") and [Project Analytics](https://app.gitbook.com/s/-MGIlBSTjQtZxUoFwUx4/project-analytics "mention").

***

### Key Features

#### Summary

<figure><img src="../.gitbook/assets/image (445).png" alt=""><figcaption></figcaption></figure>

This section provides a comprehensive high-level overview of metrics that represent team performance. It serves as the starting point for quick evaluation of key areas, enabling users to:

* **Monitor Sprint Metrics:** Quickly view critical data such as completed sprints, velocity, cycle time, and predictability.
* **Assess Overall Productivity:** Metrics such as productivity and predictability help assess how effectively the team distributes their efforts across delivering planned work and handling operational tasks. These metrics provide a clear picture of team efficiency and capacity to meet objectives.
* **Navigate Agile Boards:** Board names are clickable links that redirect users to AgileSpace, offering deeper task-level details.

***

#### Delivery Report

<figure><img src="../.gitbook/assets/image (447).png" alt=""><figcaption></figcaption></figure>

The Delivery Report focuses on visualizing the team’s sprint performance over time. It helps users understand trends and evaluate areas for improvement:

* **Velocity Trends:** Displays the average work completed across sprints, helping assess delivery capacity and consistency.
* **Predictability Insights:** Shows the team's ability to plan and deliver accurately. The closer predictability is to 100%, the better the team is at meeting commitments.
* **Productivity Comparisons:** Provides a breakdown of total completed work, including unplanned or pulled-in tasks, highlighting responsiveness and team efficiency.

<figure><img src="../.gitbook/assets/image (449).png" alt=""><figcaption></figcaption></figure>

***

#### Backlog Health

<figure><img src="../.gitbook/assets/image (448).png" alt=""><figcaption></figcaption></figure>

Backlog Health provides insights into the readiness and relevance of tasks waiting to be worked on. It ensures that the backlog is actionable and aligned with team priorities:

* **Backlog Age:** Highlights the maximum time items have spent in the backlog, helping identify and address items at risk of becoming irrelevant.
* **Backlog Size:** Reflects the number of uncompleted tasks in the backlog, excluding work in progress. This helps gauge whether the backlog is sufficient for upcoming sprints.
* **Bug Tracking:** Helps teams keep track of unresolved bugs, ensuring they are addressed and managed efficiently.
* **Sprint Removals:** Monitors the number of items removed from sprints. This ensures accountability and helps teams analyze why tasks were removed, whether due to reprioritization, blockers, or other factors affecting sprint execution.

***

#### Allocations

<figure><img src="../.gitbook/assets/image (450).png" alt=""><figcaption></figcaption></figure>

The Allocations tab highlights how team resources are distributed across different task categories. This breakdown supports balanced prioritization and sustainable growth:

* **Innovation Rate:** Focuses on the percentage of resources dedicated to product growth through new features or enhancements, relative to operational tasks.
* **Effort Distribution:** Displays how much effort is dedicated to bug fixes, maintenance, innovation, and uncategorized tasks.
* **Trend Analysis:** Offers both bar and line chart visualizations to monitor how allocation trends evolve over time.

<figure><img src="../.gitbook/assets/image (451).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure>

***

### Widget Filters and Settings

#### Sprint Range

This widget offers flexibility in sprint analysis by allowing users to select specific sprint ranges, such as 'Last 5 Sprints,' 'Last 10 Sprints,' or 'Last 20 Sprints.' It does not rely on the global date filter, ensuring precise and tailored data insights.

#### Visualization Modes

* **Item Count vs Effort:** Users can toggle between metrics based on item count or the estimated/actual effort.
* **Bar and Line Charts:** The widget provides visual representations of metrics like innovation rate, predictability, and productivity across selected sprints, helping to identify trends and areas for improvement.
* **Downloadable Charts:** Users can download bar and line charts as images for reporting and analysis.
* **Exportable Tables:** All tables in the widget can be exported as Excel files for further data manipulation and record-keeping.

***

### Metric Definitions

* **Board Name:** Lists the names of the boards linked to the widget. Each board name is a clickable link to its corresponding AgileSpace board.
* **Completed Sprints:** Number of sprints successfully started and completed by the team during the selected period.
* **Velocity per Sprint:** Average work completed by the team in each sprint. Indicates the team’s delivery capacity.
* **Predictability:** Calculated as (Completed Items / Planned Items) × 100%. Reflects how accurately the team estimates and delivers on their commitments. High predictability indicates reliable sprint planning and execution.
* **Productivity:** Evaluates the team's total output relative to the initial plan, including both planned and extra work that was completed. It is calculated by adding the completed planned tasks and any additional tasks (pulled-in work) that were done, divided by the total planned tasks, and then multiplying by 100. This metric shows the team's overall capacity and responsiveness by including any additional work taken on beyond the original plan.
* **Avg Cycle Time:** Average duration from when work starts on a task to when it is completed. Lower values indicate faster throughput. Useful for identifying bottlenecks in the workflow.
* **Avg Lead Time:** Average duration from task creation to its completion. Reflects the total time taken to deliver work items. Helps in understanding the overall efficiency of the development process.
* **Backlog Age:** The maximum time items have been in the backlog. Aged items may lose relevance.
* **Backlog Size:** The number of uncompleted items in the backlog, excluding in-progress work items. Helps gauge workload readiness.
* **Innovation Rate:** The percentage of the time, story points, or work items allocated to innovation (e.g., building new features) relative to the total effort (innovation + maintenance + bug fixes). A higher rate indicates a focus on driving product growth and competitiveness.

***

### Conclusion

The Project Analytics (Scrum Teams) widget is a powerful tool that provides teams with actionable insights into their sprint performance, backlog health, and resource allocation. By leveraging key metrics, visual reports, and historical trends, teams can make informed decisions to optimize workflows, improve predictability, and enhance overall efficiency. The ability to export data and download charts further supports transparency and reporting needs. This widget is an essential component for agile teams striving to continuously improve and deliver value effectively.
