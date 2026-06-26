---
description: Let's learn about the Team Scorecard
---

# Team Scorecard

## OVERVIEW

Teams are created on [Oobeya](https://oobeya.io/) by grouping profiles. In this way, it is possible to see the work that the teams are working on and to follow up on team metrics. For example, a team like the one below can be created to track the metrics of the Core Banking team.

These fields in Oobeya, which allow the teams to see the work they are working on and to monitor the team metrics (software development contribution, open code quality findings, open records, etc.), are called 'Scorecards'. Data can be filtered according to the selected time intervals. As seen in the example above, the information of the software developers in this project and their work has been gathered under a single platform by establishing a Team.

![](<../.gitbook/assets/image (279).png>)

Different projects and therefore teams may exist in growing and developing companies. The 'Hierarchy of Teams' feature has been developed in Oobeya in order to facilitate the process of tracking metrics in general for a company consisting of many teams. In this way, units in a company will be able to connect in a meaningful way and a hierarchy will be established. For example, let's say the unit that the Platform Services team is affiliated with Core Banking. At the same time, the unit with which 'Core Banking' is associated should be 'C-Level', which is the highest unit. In this case, Oobeya will present you with a hierarchy like this:

![](<../.gitbook/assets/image (213).png>)



It should not be overlooked that there may be other projects/teams in a company. For example, let's have 'Digital Banking' and 'Retail Banking' projects besides Core Banking. The same process done in Oobeya is as follows.

![](<../.gitbook/assets/image (292).png>)

## INITIALIZE A TEAM SCORECARD

1. Click on the team that you have created before. This window will be displayed on your screen.

![](<../.gitbook/assets/image (210).png>)

2\. After clicking on the "Start" button, the user can continue with the selection of Gitwiser analysis. The user can add multiple analyses.&#x20;

**Note:**   The "Analyses" field is mandatory. There must be at least one Gitwiser analysis to proceed with initializing the team scorecard.

![](<../.gitbook/assets/image (247).png>)

3\. After the user selects a Gitwiser analysis, the user can continue with the selection of the Sonarqube project. The field "Code Quality" is optional.

{% hint style="info" %}
To increase customer satisfaction and engagement, all product teams aim to deliver high-quality products to end users. Therefore, engineering teams strive to develop more reliable, secure, high-performance software and systems.

[Oobeya](https://oobeya.io) and [Sonarqube](https://sonarqube.org) enable teams to build a comprehensive platform for continuous code quality inspection. Learn more about [Oobeya & Sonarqube integration here](https://oobeya.io/oobeya-sonarqube-code-quality-metrics/?utm_source=sonardocs).
{% endhint %}

![](<../.gitbook/assets/image (130).png>)

**Note:** The "Sonarqube" addon must be installed and connected to your project by providing credentials in Data Source (make sure that you have selected "Set as Default"). Otherwise, you can see this warning:

![](<../.gitbook/assets/image (126).png>)

4\. Click to "Next" button to continue with the selection of Jira Project. The field "Jira Issues" is optional.

![](<../.gitbook/assets/image (122).png>)

**Note:** The "Jira" addon must be installed and connected to your project by providing credentials in Data Source (make sure that you have selected "Set as Default"). Otherwise, you cannot see the "Jira Issues" tab, or you can see this warning:

![](<../.gitbook/assets/image (271).png>)

5\. Click to "Next" button to continue with the selection of Azure Boards. This field "Azure Boards" is optional.

![](<../.gitbook/assets/image (321).png>)

**Note:** The "Azure DevOps" addon must be installed and connected to your project by providing credentials in Data Source (make sure that you have selected "Set as Default"). Otherwise, you are unable to see the "Azure Boards" tab, or you can see this warning:

![](<../.gitbook/assets/image (104).png>)

6\. After adding Azure Boards, the user can click the "Next" button and select the Date range. According to the period the user can monitor the team scorecard. In the last step, click on the "Create" button to add the team scorecard.

![](<../.gitbook/assets/image (145).png>)

7\. The user is now able to see the team scorecard.

![](<../.gitbook/assets/image (117).png>)

