---
description: >-
  Track trends and the historical progression of selected metrics across teams
  and sprints, and compare teams side by side.
---

# Trend Reports

**Trend Reports** shows how selected metrics move over time across your teams and sprints. Use it to compare teams side by side and to trace a value back to the sprint that produced it.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FjIC7kgAdW16wTkjWvm6t%2Ftrend-reports.png?alt=media&#x26;token=bfc4d16e-b0b0-43fc-b719-a851c0f5043a" alt="Trend Reports overview table comparing teams across delivery, code quality, development, project, and test metrics"><figcaption><p>Trend Reports: the Overview compares teams on the selected KPIs.</p></figcaption></figure>

{% hint style="info" %}
Trend Reports must be turned on in **Administration** > **Feature Management**. Until metrics are selected in **Administration** > **Trend Reports**, the page shows _"Trend Reports is Not Configured"_.
{% endhint %}

### Filters

* **Team**: all teams or a selection.
* **KPI**: the KPIs shown on the page (for example _5 KPIs Selected_).
* Date range, for example **Last 90 Days**.

### Overview

Since Oobeya 2.1, the **Overview** is a date-based table that lists teams as a tree, with metrics as columns grouped by area: **Delivery**, **Code Quality**, **Development Analytics**, **Project Analytics**, and **Test Analytics**. Examples of columns are Lead Time for Changes, Change Failure Rate, Technical Debt, Technical Debt Ratio, Reliability Rating, Code Churn / Rework, Refactor, Coding Efficiency, Active Contributors, Backlog Size, Open Bugs in the Backlog, Work in Progress, and Unit Test Coverage.

Values carry a status label such as **Elite**, **Needs Focus**, or **At Risk**. Expand a team to see its sub-teams. The table can be exported to Excel, and each metric links to its detail widget.

### Metric widgets

Below the overview, each selected metric has its own widget, for example **Cycle Time**, **Lead Time**, **Throughput**, and **Avg Pull Request Size** from Project Analytics:

* Choose the range, for example **Last 10 Sprints**.
* Switch between the **chart** and **table** views, or export to Excel.
* The tables show the boards and sprints behind each value. Selecting a sprint opens it in Projects & Boards.

### Configuring the metrics (administrators)

In **Administration** > **Trend Reports** (**Analytics** section), move metrics from **Available Metrics** to **Selected Metrics** and click **Save**. The selected metrics appear on the Trend Reports page.
