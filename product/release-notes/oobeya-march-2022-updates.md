---
description: Check out the new features and improvements we've released for you.
cover: ../../.gitbook/assets/Banner_Half _Page_Oobeya_blue.png
coverY: 0
---

# 🎁 Oobeya March 2022 Updates

## Summary

:tada: We are super excited to introduce our new features and improvements.

* [x] \[BETA] Deployment Analytics (DA) - [DORA Metrics](https://oobeya.io/dora-metrics/)
* [x] DA - Jenkins Integration
* [x] DA - Git Release Integration
* [x] DA - Team Goals
* [x] DA - Automated Reanalyze
* [x] DA - Time Period Comparison
* [x] DA - Deploy Size
* [x] DA - [DORA Metrics](https://oobeya.io/dora-metrics/) on Team Scorecards
* [x] Gitwiser Active Analytics Types
* [x] AgileSpace Reset Analysis
* [x] Download System Logs

## :beginner: \[BETA] Deployment Analytics (DORA Metrics)&#x20;

Calculating [DORA metrics](https://oobeya.io/dora-metrics/) is not easy. We're still working on the Deployment Analytics module so that teams can effortlessly track accurate [DORA metrics](https://oobeya.io/dora-metrics/) calculated by Oobeya.

<details>

<summary>Best tool to track DORA metrics: <strong>Why Oobeya Deployment Analytics?</strong></summary>

* Proven Metrics ([DevOps Research & Assessment](https://www.devops-research.com/))
* Quick Start (Measuring DORA metrics [has never been easier](https://www.youtube.com/watch?v=EYE4e1gTs80))
* Cross-Platform Analysis (SCM x CI/CD x APM)
* Accurate Results :white\_check\_mark:

**Discover DORA Metrics** with Oobeya: [https://oobeya.io/dora-metrics](https://oobeya.io/dora-metrics/)

</details>

{% hint style="info" %}
_**Oobeya Deployment Analytics**_ works with [GitLab CI](../../integrations/all-integrations/scm-addons/gitlab-addon.md), [AzureDevOps](../../integrations/all-integrations/scm-addons/azure-devops-integration.md), [Jenkins](../../integrations/all-integrations/scm-addons/jenkins-integration.md) for now.&#x20;

Coming soon: _GitHub Actions, Spinnaker, BB Pipelines, Octopus,_ and more...
{% endhint %}

## :electric\_plug: New Integrations

#### 1- Deployment Analytics (DORA metrics) - Jenkins Integration

Oobeya Deployment Analytics now works with [Jenkins](../../integrations/all-integrations/scm-addons/jenkins-integration.md). If you have a **\[Git Repo X Jenkins]** pipeline configured, you can calculate [DORA metrics](https://oobeya.io/dora-metrics/) by using Oobeya.

![GitLab-GitHub-Bitbucket-AzureDevOps X Jenkins](<../../.gitbook/assets/dora-jenkins (1).gif>)

#### 2- Deployment Analytics (DORA metrics) - Git Release

**Calculate DORA metrics without pipeline configuration (Git Release)**

Oobeya Deployment Analytics now works without any CI/CD pipeline integration. You can calculate DORA metrics just by selecting the git branch your team released.

![Select the git branch your team released](<../../.gitbook/assets/image (157).png>)

## :gift: New **Features**

#### **1-** Deployment Analytics - **Team Goals**

You can set your organizations' default goals for each stage of the "Lead Time For Changes" breakdown.

![Deployment Analytics default goals - Admin Panel](<../../.gitbook/assets/image (194).png>)

Oobeya checks these goals and displays warnings on the deployment flow to show you where you may improve.

![Lead Time For Changes breakdown - where you may improve.](<../../.gitbook/assets/image (129).png>)

#### **2-** Deployment Analytics - **Automated Reanalyze**

We've added new functionality for Deployment Analtyics (BETA): Automated Reanalyze is now ready to use!

#### **3-** Deployment Analytics - **Time Period Comparison**

To track the changes in [DORA metrics](https://oobeya.io/dora-metrics/), we've added a time period comparison: _"Last week" vs. "Previous week"._

!["Last 6 months" vs. "Previous 6 months" ](<../../.gitbook/assets/image (151).png>)

#### **4-** Deployment Analytics - **Deploy Size**

We've started to show the size of each deployment pipeline: _Small, Medium, Large, Gigantic._

![Deploy Size](<../../.gitbook/assets/image (293).png>)

#### **5-** DORA Metrics on Team Scorecards

Oobeya [Team Scorecards](../../team-health/team-scorecards.md) now display [DORA Metrics](https://oobeya.io/dora-metrics/), allowing you to track and improve metrics (Lead Time For Changes, Deployment Frequency) at the team level.

#### 6- Gitwiser - Active Analytics Types

On Gitwiser's home page, we've started to show active analytics types for repositories. You can now navigate to the analysis results with ease.

![Gitwiser Active Analytics Types](<../../.gitbook/assets/image (294).png>)

#### 7- AgileSpace - Reset Analysis Button

You can now reset your existing [AgileSpace Board Analytics](https://app.gitbook.com/s/-MGIlBSTjQtZxUoFwUx4/project-analytics) reports via the "Reset Analysis" button. After clicking the button, all history will be removed, but your settings and configuration will be preserved.

![Oobeya AgileSpace Reset Board Analysis](<../../.gitbook/assets/image (177).png>)

#### 8- Administration - Download System Logs

Now you can download system logs from the administration panel.

![System Logs](<../../.gitbook/assets/image (235).png>)

