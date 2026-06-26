---
description: Oobeya 2.0 released with Git Analytics feature.
---

# OOBEYA-2.0.0

## OOBEYA-2.0.0 :rocket: - _Git Analytics: Commit Work Type, Commit Impact, Scorecards Enhancements, and more..._

:tada: We are excited to introduce major features under _**"Git Analytics"**_ that strive to make your teams more productive. We have improved _Gitwiser_ (our analyzer for Git repositories) to _**analyze coding activities deeper**_ and to _**pinpoint bottlenecks**_ in the software development process.

**Oobeya 2.0** now provides you more metrics and insights to open the black-boxes of your engineering processes.

![](<../../.gitbook/assets/Oobeya 2.0.0 released (1).png>)

## :new: NEW FEATURES

### **Gitwiser Git Analytics** - _**A deeper understanding of development activities**_**.**

We've added new features to **Gitwiser** -_Oobeya's git repository analyzer_. Gitwiser started to analyze all the commits data of repositories. Therefore, we are ready now to provide you more metrics and insights in Oobeya. We have enhanced both **Individual** and **Team Scorecards** with Git Analytics metrics.

{% hint style="info" %}
After upgrading Oobeya, Git commits analysis will be performed in the first reanalyze process for your existing analyses.
{% endhint %}



### **Commit Work Type Analysis** :traffic\_light:&#x20;

Gitwiser analyzes all commits in the code repositories and identifies the work type of each coding activity. _Work type analysis_ provides you more insight into the health of your development lifecycle.&#x20;

See below the Git commit work types:

* :new:**New Work:** Newly written code lines.
* :tools:**Refactor:** Edits and updates made on the existing code (_written more than 3 weeks old_).
* :woman\_technologist:**Help Others (Pairings):** Edits and updates made on another developer's recent work (_written less than 3 weeks old_).
* :repeat:**Churn (Rework):** Code that rewritten or deleted in a short time by the same developer after being written (_less than 3 weeks_).

![Git commit work types & company average line](<../../.gitbook/assets/image (323).png>)



### **Git Analytics Metrics: Impact & Efficiency** :dart:&#x20;

Git Analytics offers you also two new metrics to pinpoint bottlenecks, risks, and workloads of your development lifecycle.

*   **Impact Score:** A way of measuring the extent of code changes that occur. Impact Score allows us to find answers to these questions:

    * Approximately how much cognitive load did the engineer perform when implementing these changes?
    * What is the overall impact of these changes on the codebase?


* **Efficiency:** The percentage of productive work (which is not rework or code churn).

We believe organizations and teams need more than a single dimension or metric to get a deeper understanding of how they are working. Therefore, we calculate and provide commit impact and efficiency metrics at different levels:

* [x] Commit-Level&#x20;
* [ ] Repository-Level (_upcoming_)
* [x] Individual-Level
* [x] Team-Level
* [ ] Organization-Level (_upcoming_)



### **Scorecards - New Design And Enhancements** :sparkles:&#x20;

We've received your feedback and made some major UI/UX enhancements on Individual and Team Scorecards. Now Scorecards have a more explicit view than before and it is easier to see trends on metrics.

![Individual Scorecard with new metrics and design](<../../.gitbook/assets/image (68).png>)

![Team Scorecard with new metrics and design](<../../.gitbook/assets/image (164).png>)



### **Gitwiser Analysis Exclusions** :scissors:&#x20;

We've added a new exclusion field for Gitwiser analysis. We give you several options for configuring exactly what will be analyzed in Gitwiser. You can completely exclude some files or directories from Gitwiser analysis.

| Example              | Scope                                                              |
| -------------------- | ------------------------------------------------------------------ |
| \*\*/\*.xml          | Excludes all _xml_ files from Gitwiser analysis.                   |
| \*\*/data.json       | Excludes all _data.json_ files from Gitwiser analysis.             |
| \*\*/\*sample\*/\*\* | Excludes directories that include "_sample_" in their folder name. |

![You can set your exclusion patterns while starting a new analysis.](<../../.gitbook/assets/image (228).png>)

![You can also update exclusion list later.](<../../.gitbook/assets/image (128).png>)



### **Gitwiser Analysis & Team Relation** :gear:&#x20;

We've added a new field for selecting Team relation for Gitwiser analysis. This repo & branch selection will be added to your Team Scorecard configuration.

![You can set team relation while starting a new analysis.](<../../.gitbook/assets/image (315).png>)

![You can also update Team relation later.](<../../.gitbook/assets/image (307).png>)



### **Show Team Info On Gitwiser Main List** :information\_source:&#x20;

We've just started to show related Team info on the Gitwiser main list.

![Team info on Gitwiser main list](<../../.gitbook/assets/image (273).png>)



### **Merge Git Accounts Easily** :star\_struck: **With Developer Profiles**&#x20;

You can now easily merge related git accounts (emails, usernames...) with Profiles defined on Oobeya.&#x20;

![Merge related accounts with Oobeya users.](<../../.gitbook/assets/image (75).png>)

Before this feature, you should go to the Profile detail and open the "Update Profile" popup to add a new related git account.

![The old & hard way of adding related account to a profile.](<../../.gitbook/assets/image (212).png>)
