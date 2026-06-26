---
description: Let's learn about the Developer Scorecard
---

# Developer Scorecard

## OVERVIEW

Oobeya **Scorecard** module collects and brings all the **developer-related data** together to give insight into the **development productivity**.&#x20;

It is created from data sources of different addons and enables the monitoring of the work and metrics (software development contribution, open code quality findings, open records, etc.) on which user can work on. Data can be filtered according to different time slots. Profile has different company Roles:

·       Developer

·       QA Engineer

·       Director

·       Business Analyst and so on

{% hint style="info" %}
Scorecards give developers a chance to **know where they stand** in order to **improve** their **engineering skills**.
{% endhint %}

## HOW CAN I SEE DEVELOPER SCORECARDS?

Developer Scorecards do not require any special creation process. It is only necessary to choose for which roles the scorecard will be displayed.

By default, Developer Scorecards are displayed for _Developers, Team Leads_ and _QA Engineers._ Follow the steps below in order to set new roles.

1. Navigate to **Administration Panel > Company**.
2. Select the company roles to set up the Scorecard display rule. Then click **Save** button.

![](<../.gitbook/assets/image (253).png>)

## RELATED ACCOUNTS OF DEVELOPER :id:&#x20;

Scorecard **collects individual's data** automatically from different tools (SDLC/ALM/DevOps) and environments by using **related accounts** info of the profile. Therefore, you need to update _Related Accounts_ of the profile to cover all the accounts of a user in different tools.

![](<../.gitbook/assets/image (199).png>)

Click the **"..."** on the right corner of the Scorecard and select **"Update Profile"**.&#x20;

Use **"Add Account"** button to add new account info. Then, **Save** the changes.

![](<../.gitbook/assets/image (208).png>)

## SCORECARD DATE FILTER :calendar\_spiral:&#x20;

You can use _date filter bar_ to see the metrics for a selected period of time.

![](<../.gitbook/assets/image (143).png>)

### Developer Scorecard Default Date Range

You can set **default date range** for all Developer Scorecards. If your organization is only interested in data of the last year, you can set default date range as _Last Year_ to open Scorecards with this filter directly.

1. Navigate to **Administration Panel > General Settings > Date Filter**.
2. Select Default Date Range and **Save** the changes.

![](<../.gitbook/assets/image (236).png>)

## SCORECARD SUMMARY :bar\_chart:&#x20;



![](<../.gitbook/assets/image (301).png>)

## CONTRIBUTION STATISTICS :woman\_technologist:&#x20;

We track commit statistics in _Developer Scorecards_ because commits are one of the most important activities of the software development process.&#x20;

Find out which repositories the developer works on for the selected date range.

### Git Work Type

**Gitwiser** analyzes all commits in the code repository and identifies the work type of each development activity with Git Analytics metrics. Work type analysis provides software development teams with insights into the health of the development process.

Oobeya shows these Work Type analysis results in Developer Scorecards by matching the related account of the profiles with the corresponding tools.

![](<../.gitbook/assets/image (191).png>)

_<mark style="color:green;">New Work:</mark>_ New work (New Work) is a measure of how many new and fresh jobs have occurred in a given time period.&#x20;

For a job to be considered "New Work", pieces of code written should not replace others, on the contrary, they must be written from scratch and independently. Newly added lines that are covered by an existing change (git hunk) do not count as "New Work".

_<mark style="color:orange;">Refactor:</mark>_ For work done on Oobeya to be considered a “Refactor”, at least 3 weeks (industry standard) must have passed since the previous work was added or edited.

New feature development and maintenance often require reworking legacy code pieces. As their codebase ages, maintaining the code and keeping things up-to-date is one of the key goals of companies.

_<mark style="color:blue;">Help others:</mark>_ It is a measure of how much one software developer edits and updates another developer's final code.

The Help Others ratio gives an idea of the team's culture of working together (pair) and sharing information within the team.

_<mark style="color:purple;">Churn:</mark>_ Churn is the measurement of the level of code complexity, accumulating technical debt, or code that is rewritten/deleted shortly after it is written.

By following the Churn value in terms of iterations, it is ensured that the problems that arise during the development periods (lack of analysis, lack of know-how, high technical debt, work sharing, etc.) are made visible at an early stage.

In order for a job to be considered Churn/Rework in Oobeya, the change must be made by the same person and must be on a new code block for more than 3 weeks. (Over 3 weeks counts as a Refactor.)

### Commit Distribution

We track commit statistics in _Developer Scorecards_ because commits are one of the most important activities of the software development process.&#x20;

Find out which repositories the developer works on for the selected date range.

![](<../.gitbook/assets/image (147).png>)

See the developer's contribution rate for each repository.&#x20;

![](<../.gitbook/assets/image (114).png>)

### Contribution Graph

Your contributions, including commits, proposed pull requests, and opened issues, are displayed on your profile so people can easily see the work you've done.

![](<../.gitbook/assets/image (73).png>)

### Contributions During Selected Period

Shows the contributions that have been analyzed by Gitwiser during the selected period. The table shows up to 100 commits.

![](<../.gitbook/assets/image (193).png>)



## CODE QUALITY WIDGETS :chart\_with\_upwards\_trend: :chart\_with\_downwards\_trend:&#x20;

To increase customer satisfaction and engagement, all product teams aim to deliver high-quality products to end users. Therefore, engineering teams strive to develop more reliable, secure, high-performance software and systems.

[Oobeya](https://oobeya.io) and [Sonarqube](https://sonarqube.org) enable teams to build a comprehensive platform for continuous code quality inspection. Learn more about [Oobeya & Sonarqube integration here](https://oobeya.io/oobeya-sonarqube-code-quality-metrics/?utm_source=sonardocs).

Scorecards collect real-time data from your code analysis tools ([SonarQube](../integrations/all-integrations/code-quality-addons/sonarqube-integration.md), CAST, Fortify) to show the code quality metrics of the developers.&#x20;

**Scorecards** make your _organization's open issues_ **visible**, to give you a chance to improve.

See where your **code quality** stands, **identify** the problematic units, and **improve** it.

![Added Technical Debt](<../.gitbook/assets/image (215).png>)

![Code Quality Issues](<../.gitbook/assets/image (219).png>)

## JIRA OPEN ISSUES WIDGET

The issues that are still unsolved are listed in this widget. The information reflected from the Jira is matched with the related accounts of the profile.

![](<../.gitbook/assets/image (139).png>)

## AZURE OPEN ISSUES WIDGET

The issues that are still unsolved are listed in this widget. The information reflected from the Azure DevOps is matched with the related accounts of the profile.

![](<../.gitbook/assets/image (203).png>)
