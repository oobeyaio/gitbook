---
description: >-
  This guide explains how to initialize Project Analytics → Agile Board Analysis
  using an existing Agile data source.
---

# Starting an Agile Board Analysis

**Step 0 – Create a New Analysis**

To start an Agile Board Analytics setup:

1. Open **Analytics** from the left-hand menu.
2. Select **Projects & Boards**.
3. Click **+ Analysis** in the top-right corner.

This opens the Agile Board Analysis initialization wizard.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fu5iJDssDb2rkQgHhCyYh%2Fimage.png?alt=media&#x26;token=b458a147-a0c6-4dc1-afcc-918193e1b989" alt=""><figcaption></figcaption></figure>

***

**Step 1 – General Settings**

In this step, you define the main context of the analysis.

**Required fields**

* **Data Source**: Select one of the previously configured Agile data sources\
  _(e.g. Jira Cloud, Jira Data Center, Azure DevOps)_
* **Board**: Select the Agile board to analyze
* **Board Type**: Scrum or Kanban

**Optional fields**

* **Area:** For Azure DevOps boards, select one or more Areas. If no Area is selected, all Areas will be included in the calculations.
* **Product Owner**: Select the responsible Product Owner
* **Scrum Master**: Select the Scrum Master
* **Team(s)**: Associate one or more teams with this analysis
* **Analysis Date Range**: Time period to analyze (default: Last 24 Months)

Click **Next** to continue.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FIWUZedm2NX3S7Q1bMjvp%2Fimage.png?alt=media&#x26;token=b29180d3-41a9-41a6-9be4-445b93e04ef7" alt=""><figcaption></figcaption></figure>

***

**Step 2 – State Mapping**

Map workflow states to Oobeya’s standard flow categories. By default, Oobeya automatically maps states using the selected board’s workflow configuration.

**Required mappings**

* **To Do**: States representing work that has not started\
  _(e.g. Backlog, To Do, Open, Analysis, Blocked)_
* **In Progress**: States representing active work\
  _(e.g. Development, Code Review)_
* **Done**: Final states\
  _(e.g. Done, Cancelled)_

**Additional settings**

* **Method for Actual Reaction Time**\
  Defines when the reaction time calculation starts (e.g. _From Work Item Creation Date_).
* **Flow Efficiency – Active States**\
  Select the In Progress states that should be considered in Cycle Time and Flow Efficiency calculations. If no state is selected, all In Progress states will be included by default.

Click **Next** to continue.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FLkNHrx0A77RcLLk4b4wS%2Fimage.png?alt=media&#x26;token=e4d5b719-e358-4b22-b0a5-e504aba7ccf6" alt=""><figcaption></figcaption></figure>

***

**Step 3 – Field Mapping**

Configure how effort and sprint planning behavior are interpreted.

**Required**

* **Effort Field**: Field used to calculate effort\
  _(commonly Story Points)_

**Optional**

* **Ignore sprint scope changes made on planning day**\
  Excludes scope changes occurring on the sprint planning day.
* **Planning Days**\
  Number of days considered as sprint planning (default: 1).

Click **Next** to proceed.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fb5Si5Y4n2S0h0lGrR3iI%2Fimage.png?alt=media&#x26;token=bce8cd97-4379-4d1a-9260-0a915da8f6af" alt=""><figcaption></figcaption></figure>

***

**Step 4 – Finish**

Review the configuration and complete the setup. Once finished, Oobeya starts analyzing historical data for the selected board and date range.
