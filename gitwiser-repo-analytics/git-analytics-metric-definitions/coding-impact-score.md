# Coding Impact Score

### Overview

**Oobeya** measures the **Coding Impact Score** by evaluating the magnitude of code changes, which helps answer significant questions:

1. **Approximately** **how much cognitive load** did the developer experience **when implementing these changes**?
2. What is the **overall impact** of these changes **on the codebase**?

***

### Calculation

The Coding Impact Score is calculated based on the following factors:

1. **Files Touched:** How many files were affected by the changes? How many new files were added or deleted from the code base in this Git commit?
2. **Complexity/Scope of Changes:** How many insertion points (Git hunks) were changed in each file? How many different classes were modified, added, or deleted?
3. **Work Type of Code Changes:** What was the work type of each code line change? How many code lines were newly added, edited, or deleted? To learn more about work types, please click [here](./).

### Formula

**Coding Impact Score of A Commit =** (Files added x 10) + (Files modified x 6) +  (Files deleted x 6) + (Git hunks x 4) + (New code lines x 0.14) + (Edited code lines x 0.28) + (Deleted code lines x 0.28)

#### Find below the weighted coefficient of parameters in the Coding Impact Score formula:

<table><thead><tr><th width="182">Change Level</th><th width="399">Change Type</th><th align="center">Coefficient</th></tr></thead><tbody><tr><td>File</td><td>Adding a new file</td><td align="center">10</td></tr><tr><td>File</td><td>Editing an existing file</td><td align="center">6</td></tr><tr><td>File</td><td>Deleting an existing file</td><td align="center">6</td></tr><tr><td>Block</td><td>Working on a Git hunk (a separate code block)</td><td align="center">4</td></tr><tr><td>Line</td><td>Adding a new line </td><td align="center">0.14</td></tr><tr><td>Line</td><td>Editing an existing line</td><td align="center">0.28</td></tr><tr><td>Line</td><td>Deleting an existing line</td><td align="center">0.28</td></tr></tbody></table>

{% hint style="info" %}
In Oobeya, you can configure the appropriate coefficients in the administration settings.
{% endhint %}

***

### Why It Matters

Tracking the Coding Impact Score allows Oobeya to identify the approximate cognitive effort of developers during development cycles. This is crucial for recognizing:

* **Team Health and Individual Health Symptoms:** The risk of developers with high cognitive load burning out or becoming overloaded.
* **Working Practice / Collaboration Symptoms:** The knowledge silos that have formed within the team.

Explore the [Impact Ratio](impact-ratio-team-level.md) metric to get deeper insights into your team:

{% content-ref url="impact-ratio-team-level.md" %}
[impact-ratio-team-level.md](impact-ratio-team-level.md)
{% endcontent-ref %}

{% hint style="info" %}
[Oobeya](https://oobeya.io) uses the Coding Impact Score metric to identify the '[Recurring High Cognitive Load](../../team-insights-and-symptoms/symptoms-catalog/s2-recurring-high-cognitive-load.md)' symptom.
{% endhint %}

***

### How to Use It

While a higher Coding Impact Score isn't inherently positive or negative, it does shed light on the **cognitive load your team members are experiencing**. Here's how you can use it effectively:

1. **Balance Workload Within The Team:**
   * Monitor high Coding Impact Scores over time to identify developers who might be at risk of overload and burnout.
   * Redistribute tasks to balance the workload, ensuring sustainable productivity.
2. **Recognize Contributions:**
   * Use the Coding Impact Score to acknowledge and understand the complexity of the contributions made by each developer in a given period.
   * Highlight and reward significant efforts appropriately.
3. **Improve Processes:**
   * Analyze patterns in Impact Scores to identify areas where process improvements can fix the unbalanced workload among the team members.
   * Implement changes to streamline workflows, empower collaboration, and enhance efficiency.

***

### An Example To Better Understand The Coding Impact Score

To better understand the Coding Impact Score, consider the following example:

* **Commit #1:** An engineer added 100 new lines of code to **a single file**.&#x20;
* **Commit #2:** Another engineer **touched 6 files** at multiple modules, adding 40 lines, modifying 20 lines, and deleting 20 lines of code.&#x20;

This shows the total lines of code changed are the same (100 lines) for both commit activities.

Despite containing the same lines of code change, Commit #2 is likely more difficult to implement due to:

1. **Modifying previous work** (modifying 20 lines + deleting 20 lines at 6 different files)
2. **Edits in multiple different locations** (Git hunks/insertion points in code)
3. **Six different files were affected.** The engineer should understand all modules affected, and test them and their dependencies.

Impact Scores for the example are calculated as

* **Commit #1:** 24x
* **Commit #2:** 92.8x

{% hint style="success" %}
**The Result:**

They both had **one commit** and **100 lines of code changed**, but the second engineer exerted approximately four times (3.86x) more cognitive effort on her task compared to the first engineer.
{% endhint %}

***

### Conclusion

The Impact Score is a powerful tool in Oobeya's suite, providing valuable insights into the cognitive load on your engineering team. By using it to balance workloads, recognize contributions, improve processes, and enhance collaboration, you can support the well-being and productivity of your team, ensuring sustainable, efficient, and productive development cycles.
