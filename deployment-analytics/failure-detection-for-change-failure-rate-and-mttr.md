---
description: >-
  Oobeya sets the health status of each deployment by using four methods: manual
  health status setting, API call, hotfix pattern detection, and tracking
  incidents from APM/Incident Management tools.
icon: octagon-exclamation
---

# Failure Detection (For Change Failure Rate & MTTR)

[Oobeya](https://oobeya.io/) is a software engineering intelligence platform that allows software development organizations to gather and analyze data from various sources to make informed decisions and optimize their development and delivery processes.

[Oobeya](https://oobeya.io/) is also a [DORA Metrics Tracking tool](https://oobeya.io/dora-metrics-four-key/) that provides valuable insights into the effectiveness of software development and delivery.

Oobeya has a unique mechanism for calculating [DORA Metrics](https://oobeya.io/dora-metrics-four-key/) across platforms/tools (VCS, CICD, and APM-Incident Management tools) so that any organization can accurately and effortlessly track the journey of a commit from development to production deployment. Furthermore, no changes to workflows or pipelines are required; Oobeya seamlessly integrates with existing tools (GitHub, GitLab, Azure DevOps, Bitbucket, Jenkins, TeamCity, GitHub Actions, GitLab CI, Azure Pipelines, Releases, and more) to calculate DORA metrics.

Oobeya analyzes all deployments, detects production failures, and ties them back to production deployments.

Oobeya calculates all four key DORA Metrics. The **Change Failure Rate** (CFR) is the percentage of deployments causing a failure in production. This metric provides a clear and concise representation of the stability and reliability of software systems. Oobeya uses the health status of each deployment to calculate the CFR metric.

<figure><img src="https://i0.wp.com/cdn-images-1.medium.com/max/800/1*FIq4QEUhXQ6vtVllmaMIfQ.png?resize=800%2C340&#x26;ssl=1" alt="Oobeya DORA Metrics — Change Failure Rate CFR"><figcaption><p>Oobeya DORA Metrics — Change Failure Rate CFR</p></figcaption></figure>

In Oobeya, each analyzed production deployment has a health status, which is either **Success** or **Failure**. Oobeya sets the health status of each deployment by using four methods: manual health status setting, API call, hotfix pattern detection, and tracking incidents from APM/Incident Management tools.

\*\*\*

## OOBEYA FAILURE DETECTION

1. Setting the health status manually.
2. Detecting “hotfix” patterns (in Git branch, PR, Deployment name) automatically.&#x20;
3. Tracking incidents from Application Performance / Incident Management tools.
4. Oobeya Deployment API – Oobeya will provide an API that can be used to set the health status of each deployment.

\*\*\*

### 1. Setting Health Status Manually

In this method, a user sets the health status of the deployment manually.&#x20;

This method is useful when there is a need for verification, for example, when there is a complex deployment that involves multiple systems and applications or **where you don’t have any mechanism to detect** and **track failures automatically** by the tools.

<figure><img src="../.gitbook/assets/image (404).png" alt=""><figcaption><p>You can manually set the health status of your deployments as “Failure”.</p></figcaption></figure>

### 2. Detecting Hotfix Naming Patterns In The Branch Name, PR, And Deployment Title

Oobeya automatically sets the health status of each deployment by detecting hotfix patterns. To identify hotfix deployments, Oobeya looks for naming patterns in the branch name, Pull Request title, and deployment title. Because hotfix deployments are used to fix critical production issues, Oobeya sets the health status of previous deployments to Failure.

<figure><img src="../.gitbook/assets/image (399).png" alt=""><figcaption><p>Setting naming patterns</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (368).png" alt=""><figcaption><p>Automatically detected Failure</p></figcaption></figure>

### 3. Tracking Incidents From Application Performance / Incident Management Tools

Oobeya integrates with [Application Performance Management (APM) and Incident Management tools](https://oobeya.io/integrations/) (New Relic, Datadog, etc.) to track incidents in production. If these tools detect an incident in production, Oobeya sets the health status of the most recent deployment prior to the incident to Failure.

<figure><img src="../.gitbook/assets/image (382).png" alt=""><figcaption><p>Oobeya — DORA Metrics Incident Source</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (369).png" alt=""><figcaption><p>Automatically detected by tracking New Relic Incidents and Alerts</p></figcaption></figure>

See our blog post here:&#x20;

{% embed url="https://oobeya.io/blog/dora-metrics-tracking-how-to-effectively-detect-production-failures/" %}
