# OOBEYA-2.0.4 - Release Notes

## OOBEYA-2.0.4 :rocket: - _New Jira Widgets, Metric Thresholds, Improvements, UI/UX Enhancements, and more..._

:tada: We are excited to introduce our new features and improvements. We have added new widgets for Jira Server & Cloud and implemented a new infrastructure for setting metric thresholds on dashboard widgets.

## :new: NEW FEATURES

### Metrics With JQL Widget **- New Metric: Resolution Time (avg)** :clock5:&#x20;

We've added a new _metric type_ for "Metrics With JQL Widget": _**Resolution Time (avg)**_. This metric shows the average resolution time of the issues for the given JQL.

{% hint style="info" %}
The "Resolution Time" is the difference between an issue's Resolution Date and Created date. See the Jira docs [here](https://confluence.atlassian.com/jirakb/how-resolution-time-is-calculated-278072482.html).
{% endhint %}

![Average Resolution Time in 2021](<../../.gitbook/assets/image (206).png>)

![project = DAS AND Resolution = Done AND resolved >= startOfYear()](<../../.gitbook/assets/image (240).png>)



### **Jira Issue Search Widget - New Column: Resolution Time** :clock5:&#x20;

We've added a new _column_ for "Jira Issue Search Widget": _**Resolution Time**_. This column shows the resolution time of each issue in the table.

![Resolution Time column for Jira Issues Table Widget.](<../../.gitbook/assets/image (127).png>)

![Resolved Issues in 2021 with resolution time.](<../../.gitbook/assets/image (192).png>)



### **New Widget: Jira Issue Aging Chart** :chart\_with\_upwards\_trend:&#x20;

We've launched a new _widget_ for Jira [Cloud ](../../integrations/all-integrations/project-management-addons/jira-cloud-integration.md)& [Server ](../../integrations/all-integrations/project-management-addons/jira-server-integration.md)Addon: _**Jira Issue Aging Chart**_. This widget visualizes the age of open issues for the given JQL.

![Visualizes the age of unresolved issues.](<../../.gitbook/assets/image (262).png>)

![Issue Aging Chart](<../../.gitbook/assets/image (327).png>)



### **Metric Threshold For JQL Widget** :vertical\_traffic\_light:&#x20;

We've built an infrastructure for Metric Thresholds and released the first widget implementation.

You can now set thresholds for the metrics in the "Metrics With JQL" Widget.

![Setting metric thresholds.](<../../.gitbook/assets/image (319).png>)

![Metrics With JQL Widget](<../../.gitbook/assets/image (85).png>)



### **Gitwiser PR Analysis: GitHub Pull Request Review Stats**

We've added a new widget "Review Stats" for Gitwiser's Pull Request Analytics (PRA) module. Now, this feature is only available for GitHub Addon.

![Shows the Pull Request review stats to pinpoint bottlenecks of the code review process.](<../../.gitbook/assets/image (140).png>)



## :muscle: IMPROVEMENTS

### Show Company Roles In The User Table:new:&#x20;

We've added a new _column_ to the user table:

![Administration > Users & Groups](<../../.gitbook/assets/image (121).png>)

### New Company Role: Tech Lead:new:&#x20;

We've added a new _company role_ to the role list: Tech Lead. You can add it to your company role list.

![](<../../.gitbook/assets/image (180).png>)

### Suggest Repositories While Initializing Team Scorecard :man\_technologist::woman\_technologist:&#x20;

We've started to suggest Git repositories related to team members while initializing Team Scorecard.

![Team Scorecard Initialize](<../../.gitbook/assets/image (111).png>)

### Select Automatically If There Is Only One Branch&#x20;

We've started to select the branch automatically if there is only one branch available.&#x20;

![Team Scorecard Initialize](<../../.gitbook/assets/image (252).png>)

### Gitwiser - Commits Per File List

We've increased the number of files listed in the "Commits Per File" widget:

![Commits Per File - Top 50](<../../.gitbook/assets/image (175).png>)



## :lady\_beetle: FIXES

* Fixed - Navigate to the analysis pending page after updating the Gitwiser Analysis exclusion list.
* Fixed - Upper-Level team list problem while adding a new team.

