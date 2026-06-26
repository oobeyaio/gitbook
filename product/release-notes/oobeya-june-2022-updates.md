---
description: Check out the new features and improvements we've released for you.
cover: ../../.gitbook/assets/Banner_Half _Page_Oobeya_blue.png
coverY: 0
---

# 🎁 Oobeya June 2022 Updates

## Summary

&#x20;:tada: We are super excited to introduce you to our new features and improvements!

* [x] DORA Stability Metrics -1: [Change Failure Rate](oobeya-june-2022-updates.md#dora-stability-metrics-1-change-failure-rate)
* [x] DORA Stability Metrics -2: [Time to Restore Service](oobeya-june-2022-updates.md#dora-stability-metrics-2-time-to-restore-service)
* [x] [Executive View & Organization-Wide Metrics](oobeya-june-2022-updates.md#executive-view-and-organization-wide-metrics)
* [x] [Improvements](oobeya-june-2022-updates.md#improvements) on AgileSpace, Gitwiser, Sonarqube, and UI/UX
* [x] Private Beta: [Symptoms ](oobeya-june-2022-updates.md#private-beta-cooking-something-special)(cooking something special...)

## ​🎁 NEW FEATURES

### DORA Stability Metrics -1: Change Failure Rate

We have added Change Failure Rate to Oobeya Deployment Analytics \[BETA]!&#x20;

{% hint style="info" %}
**Change Failure Rate:** The percentage of deployments causing a failure in production.

:bulb: Read more on Oobeya Blog: [How to Measure DORA Metrics Accurately?](https://oobeya.io/blog/how-to-measure-dora-metrics-accurately/)
{% endhint %}

You can set your deployment status as a failure manually now.&#x20;

![Setting deployment health status and fix deployment manually](<../../.gitbook/assets/image (333).png>)

In the next release, deployment failures will be detected automatically by **Git tags** and **branch names**.

![DORA Metrics - Change Failure Rate](<../../.gitbook/assets/image (385).png>)

<details>

<summary>Best tool to track DORA metrics: <strong>Why Oobeya Deployment Analytics?</strong></summary>

* Proven Metrics ([DevOps Research & Assessment](https://www.devops-research.com/))
* Quick Start (Measuring DORA metrics [has never been easier](https://www.youtube.com/watch?v=EYE4e1gTs80))
* Cross-Platform Analysis (SCM x CI/CD x APM)
* Accurate Results :white\_check\_mark:

**Discover DORA Metrics** with Oobeya: [https://oobeya.io/dora-metrics](https://oobeya.io/dora-metrics/)

Read more on Oobeya Blog: [How to Measure DORA Metrics Accurately?](https://oobeya.io/blog/how-to-measure-dora-metrics-accurately/)

</details>

{% hint style="info" %}
_**Oobeya Deployment Analytics**_ works with [GitLab CI](../../integrations/all-integrations/scm-addons/gitlab-addon.md), [AzureDevOps](../../integrations/all-integrations/scm-addons/azure-devops-integration.md), [Jenkins](../../integrations/all-integrations/scm-addons/jenkins-integration.md), and [GitHub Actions](../../integrations/all-integrations/scm-addons/github-integrations.md) for now.&#x20;

Coming soon: _Spinnaker, BB Pipelines, Octopus, PagerDuty, OpsGenie, ServiceNow,_ and more...
{% endhint %}



### DORA Stability Metrics -2: **Time to Restore Service**

We have added the Time to Restore Service / Mean Time To Recovery (MTTR) metric to Oobeya Deployment Analytics \[BETA]!&#x20;

{% hint style="info" %}
**Time to Restore Service:** How long it takes an organization to recover from a failure in production.

:bulb: Read more on Oobeya Blog: [How to Measure DORA Metrics Accurately?](https://oobeya.io/blog/how-to-measure-dora-metrics-accurately/)
{% endhint %}

![DORA Metrics - Mean Time To Recovery (MTTR)](<../../.gitbook/assets/image (357).png>)

### Executive View & Organization-Wide Metrics

You can set your own Organization Schema to create a hierarchical view in Oobeya.

![You can set your own Organization Schema to create a hierarchical view.](<../../.gitbook/assets/image (353).png>)

After you create your organization chart, you can view your organization-wide metrics with breakdowns. All the metrics shown will be customizable in this view.

![Organization-wide metrics along with breakdowns](<../../.gitbook/assets/image (336).png>)



## :muscle: IMPROVEMENTS

* \[AgileSpace] Added Total Story Points & Total Issue Count value to Sprint Reports
* \[AgileSpace] Added a new tab to Sprint Velocity Metrics widget: "Team Members”
* \[AgileSpace] Added task dropdown to Scope Changes widget
* \[AgileSpace] Added a new configuration option for Azure DevOps Story Points / Effort fields
* \[Gitwiser] Added automated-reanalyze feature for Pull Request Analysis
* \[Sonarqube] Started hiding Sonarqube issues which are set as "won't fix" on Sonarqube
* Performance improvements
* UI/UX improvements

## :lock: **PRIVATE BETA - Cooking something special**

We are currently working on a new module called "**Symptoms**".&#x20;

Oobeya _**Symptoms**_ module identifies automatically symptoms of software development and delivery processes.

20+ symptoms are ready-to-use and auto-detect unhealthy practices of dev teams in private beta.

| Symptoms of software development and delivery processes | Tags                                             |
| ------------------------------------------------------- | ------------------------------------------------ |
| Recurring high rework rate                              | low\_efficiency, slow\_delivery, dissatisfaction |
| Recurring high cognitive load                           | burnout\_risk, high\_workload, bad\_planning     |
| High weekend activity                                   | burnout\_risk, bad\_planning                     |
| High active coding days (%80+)                          | burnout\_risk                                    |
| Work on X+ repos in a selected period                   | interruption, burnout\_risk                      |
| High technical debt on Sonarqube                        | quality\_risk, dissatisfaction                   |
| High vulnerabilities on Sonarqube                       | quality\_risk, security\_risk                    |
| High code quality bugs on Sonarqube                     | quality\_risk                                    |
| Unreviewed Pull Requests                                | quality\_risk, unreviewed\_pr                    |
| Lightning Pull Requests                                 | quality\_risk, unreviewed\_pr                    |
| Oversized Pull Requests                                 | quality\_risk, bottleneck, large\_deploy\_risk   |
| High Pull Request review time                           | slow\_delivery                                   |
| Reviewer bottleneck %                                   | slow\_delivery, bottleneck, high\_workload       |
| High cycle time (tasks)                                 | slow\_delivery, dissatisfaction, bottleneck      |
| High lead time (tasks)                                  | slow\_delivery                                   |
| Low sprint planning accuracy                            | slow\_delivery, dissatisfaction                  |
| Low sprint delivery rate                                | low\_efficiency, slow\_delivery, dissatisfaction |
| Tasks in progress                                       | burnout\_risk, high\_workload, bad\_planning     |
| Recurring high scope changes                            | low\_efficiency, dissatisfaction, interruption   |
| High Lead Time For Changes                              | slow\_delivery                                   |
| High Deploy Duration                                    | slow\_delivery                                   |
| Low Deploy Frequency                                    | slow\_delivery, large\_deploy\_risk              |



## :person\_running: SEE OOBEYA IN ACTION!

{% hint style="info" %}
Do you want to see all the new features in action and talk about the product roadmap?

Click and [**book a demo**](https://oobeya.io/schedule-a-new-demo/?utm_source=releasenotes\&utm_medium=june2022) now.
{% endhint %}

