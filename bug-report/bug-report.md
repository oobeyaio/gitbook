---
description: >-
  Helps you monitor bug reports occurring during your teams' software
  development processes.
icon: bug
---

# Bug Report

The Oobeya Bug Report module helps you track bug records occurring during your teams' software development processes by collecting data from project management tools such as Jira and Azure Boards. It provides organization and team-level visibility into open and closed bugs. This empowers you to make data-driven decisions that improve software quality and detect bottlenecks at an early stage.

### Key Features

* Centralized reporting view across the entire organization
* Team-level filtering and analysis
* Multiple time interval views (_daily, weekly, monthly, quarterly_)
* Visualizations of open bug trends
* Severity distribution analysis
* Bug distribution by team
* Detailed bug list: Team Bugs, Unassigned Bugs, Other Teams' Bugs (_Work item, Assignee, Project, Status_, etc.)

***

### Prerequisites (Admin Settings)

To ensure the Bug Report module functions correctly, certain configurations must be completed in the **Admin Panel**.

#### **1. Category Mapping Settings**

Under `Administration > AgileSpace`, define the relevant issue types (_e.g., Bug, Defect, Problem, Incident, Error_) mapped to the **Bug Fixing** category.

{% hint style="warning" %}
If this mapping is not configured, related work items will not be classified as bugs and won't be reflected in the report.
{% endhint %}

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FZzIW76y26Xvzw4FABiyk%2Fimage.png?alt=media&#x26;token=2b7f5491-6ad0-43f4-b59d-e88d2daeaf26" alt=""><figcaption><p>Category Mapping</p></figcaption></figure>

#### **2. Severity Mapping**

To classify bugs by severity level, map the severity fields from Jira or Azure Boards to Oobeya’s predefined severity categories.

* **For Jira**: Map values from the `Priority` field such as `Highest`, `High`, `Medium`, `Low`, etc.
* **For Azure**: Use numeric values sorted by criticality (e.g., 1 - Critical, 2 - High, etc.)

Changes in these settings will trigger a reanalysis of historical data.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F3pUR1S1dTlmpkx86oNJd%2Fimage.png?alt=media&#x26;token=fab07836-8733-4612-a0d0-992363f4ecf9" alt=""><figcaption><p>Severity Mapping</p></figcaption></figure>

***

### Dashboard Components

#### **1. Open Bugs Over Time**

Displays the trend of open bugs over time, broken down by severity levels (_Blocker, Critical, High, Medium, Low_).

* **Interactive chart**: Hover to view detailed counts of bugs per severity for each time interval.
* **Time filter options**: Choose from _Last 7 Days, Last 30 Days, Monthly, Quarterly_, or custom date ranges.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FnSMZ4IAhpceyUmRxJFf3%2Fimage.png?alt=media&#x26;token=c892aed8-e48f-43b7-a743-8fc40fe3aed3" alt=""><figcaption><p>Open Bugs Over Time</p></figcaption></figure>

***

#### **2. Bug Severity Summary**

Displays the distribution of bugs by severity level.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F9jNhZKoRlgkAiiE2B2dV%2Fimage.png?alt=media&#x26;token=9bde15fb-874b-416e-801e-afd3e4512b3a" alt="" width="375"><figcaption><p>Bug Severity</p></figcaption></figure>

***

#### **3. Bug Distribution by Team**

Displays the number of bugs per team and helps identify which teams are reporting the most bugs.

* Pie chart visualization
* Quick identification of high-volume bug teams

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F6hyei25xd3zuvUnZtTzv%2Fimage.png?alt=media&#x26;token=9a2a403e-ea7e-4b14-a244-0e2b86e58612" alt=""><figcaption><p>Bug Distribution By Team</p></figcaption></figure>

***

#### **4. Bug Details**

Displays a full list of bugs, including:

* Work item ID
* Summary
* Assignee
* Project and Team
* Type, Severity, Status, and Date fields

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FdX5qTPJ2vRPbI7sWQFhz%2FScreenshot%202025-09-05%20at%2017.33.18.png?alt=media&#x26;token=a158d8d9-a73e-4aaa-bcf3-968b39621ff2" alt=""><figcaption><p>Bug Details Table</p></figcaption></figure>

***

### FAQ (Frequently Asked Questions)

<details>

<summary><strong>Is this module available to all users?</strong></summary>

Yes. The Bug Report Dashboard is available organization-wide. Users can filter results based on the teams to which they belong.

</details>

<details>

<summary><strong>Why are severity levels not showing correctly?</strong></summary>

Please verify your severity mapping settings in the Admin Panel. The fields in Jira or Azure Boards might not be correctly matched to Oobeya's categories.

</details>

<details>

<summary><strong>Why is the bug count different from what's shown in Jira or Azure?</strong></summary>

This might be due to incorrect category mapping or excluded work item types in your configuration.

</details>

***

### Conclusion

The Bug Report module is a powerful tool for teams aiming to streamline issue tracking and improve software quality. When properly configured, it enables clear visibility into bug volume, resolution trends, and risk zones.
