---
description: Check out the new features and improvements we've released for you.
cover: ../../.gitbook/assets/Banner_Half _Page_Oobeya_blue.png
coverY: 0
---

# 🎁 Oobeya August 2022 Updates

## SUMMARY

&#x20;:tada: We are super excited to share our new features and improvements with you!

* [x] TeamCity integration is ready! Calculate and track TeamCity DORA metrics!
* [x] Oobeya Dashboard DORA Metrics Widget now displays all DORA Metrics!
* [x] Exclude deployments to calculate DORA Metrics more accurately!
* [x] Select Gitwiser analysis period to optimize analysis performance
* [x] New Pull Request metrics are ready to use! Improve your teams' code review cycles.
* [x] Manage Team Members easily!

## ​🎁 NEW FEATURES

### Oobeya TeamCity integration is ready!

If you're using TeamCity for your CI/CD needs, we have some great news for you - the Oobeya TeamCity integration is now available!

You can now calculate and track your TeamCity DORA metrics seamlessly; we think it's a great way to improve your CI/CD process.&#x20;

<figure><img src="../../.gitbook/assets/image (391).png" alt=""><figcaption><p>TeamCity Addon</p></figcaption></figure>



To get started, simply head over to our [Marketplace](../../integrations/adding-new-integration/installing-an-addon.md) page and activate the TeamCity addon. Then, [add your TeamCity data source](../../integrations/adding-new-integration/adding-a-new-data-source.md). Once you have it set up and started [Oobeya Deployment Analytics](https://app.gitbook.com/s/-MGIlBSTjQtZxUoFwUx4/deployment-analytics), you'll be able to see your DORA metrics in Oobeya.

{% hint style="info" %}
:bulb: Read more on Oobeya Blog: [TeamCity Integration Is Ready!](https://oobeya.io/blog/github-enterprise-server-integration-is-ready/)
{% endhint %}

{% hint style="info" %}
_**Oobeya Deployment Analytics**_ works with [GitLab CI](../../integrations/all-integrations/scm-addons/gitlab-addon.md), [AzureDevOps](../../integrations/all-integrations/scm-addons/azure-devops-integration.md), [Jenkins](../../integrations/all-integrations/scm-addons/jenkins-integration.md), [GitHub Actions](../../integrations/all-integrations/scm-addons/github-integrations.md), and TeamCity for now.&#x20;

Coming soon: _Spinnaker, BB Pipelines, Octopus, PagerDuty, OpsGenie, ServiceNow,_ and more...
{% endhint %}

<figure><img src="../../.gitbook/assets/image (348).png" alt=""><figcaption><p>Oobeya calculates DORA Metrics for TeamCity Pipelines</p></figcaption></figure>

### Oobeya Team Scorecards now display all DORA Metrics!

We are excited to announce that the Oobeya Dashboard "**DORA Metrics Widget**" now displays all [four DORA Metrics](https://oobeya.io/dora-metrics-four-key/)! This improvement makes it easy to track your progress against the four key indicators of the DevOps Performance Framework: Lead Time For Changes, Deployment Frequency, Change Failure Rate, and Mean Time to Restore Service.

<figure><img src="../../.gitbook/assets/image (337).png" alt=""><figcaption><p>Oobeya DORA Metrics Widget</p></figcaption></figure>

To access the DORA Metrics Widget, simply go to your [Dashboard](https://app.gitbook.com/s/-MGIlBSTjQtZxUoFwUx4/dashboards) and [click on the "Widgets"](../../dashboards/adding-a-new-widget.md) button in the top right corner. From Gitwiser > Deployment Analytics, you can add the DORA Metrics Widget to your Dashboard.

We hope you find this new feature helpful in tracking your DORA Metrics!

### Exclude deployments to calculate DORA Metrics more accurately!

We're excited to announce a new feature for Oobeya Deployment Analytics - the ability to exclude deployments from your [DORA Metrics](https://oobeya.io/dora-metrics-four-key/) calculations!

Previously, when calculating your Lead Time For Changes, any deployments that were considered anomalies would be included in the calculation. This could lead to inaccurate results and made it difficult to get an accurate picture of your development and delivery process.

Now, with the new deployment exclusion feature, Oobeya automatically excludes any deployments that are considered anomalies. Oobeya users are also able to exclude any deployment manually.

This will give you a more accurate picture of your delivery process and help you identify and fix any issues more effectively.

We hope you find this new feature helpful! As always, if you have any questions or feedback, please don't hesitate to reach out to us.

<figure><img src="../../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>

### Select Gitwiser analysis period to optimize analysis performance

We are excited to announce a new feature for [Oobeya](https://oobeya.io/) - the ability to select the analysis period to optimize performance.

Gitwiser is a powerful git analytics tool that lets development teams see the impact and cognitive load of commits on the team average. It's been a valuable tool for development teams and leaders looking to improve their workflow and optimize their working practices.

With this new feature, you can select the period of time you want to analyze to get the most accurate results. This is especially **helpful for large projects with a lot of history**.

<figure><img src="../../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure>

See the other features below to optimize Gitwiser analysis performance:

* Commit Exclusions
* Source Code File and Folder Exclusions (exclusion patterns)

### New Key Pull Request metrics are ready to use! Improve your teams' code review cycles!

We've just released a new set of metrics for the Oobeya Pull Request Analytics module:&#x20;

* **Avg Time To Merge:** The time elapsed between the first commit and merge time.
* **% PRs Merged Within Goal:** The percentage of merged pull requests within the specified team goal.

These key metrics will help you improve your team's code review cycles and performance.

<figure><img src="../../.gitbook/assets/image (395).png" alt=""><figcaption><p>Key pull request metrics</p></figcaption></figure>

### Manage Team Members easily!

Oobeya is excited to announce this new feature to help team leads manage their team members easily! With this new feature, team leads can add and remove members with ease, as well as receive smart suggestions on who to add or remove to their team.&#x20;

This new feature is designed to make managing teams easier and more efficient for Oobeya users.

## :muscle: IMPROVEMENTS

* \[Gitwiser] GitHub API Rate Limit improvements
* \[Gitwiser] Bitbucket API Rate Limit improvements
* Performance improvements
* UI/UX improvements (on time in state widget, team search, date filter, and more...)

## :person\_running: SEE OOBEYA IN ACTION!

{% hint style="info" %}
Do you want to see all the new features in action and talk about the product roadmap?

Click and [**book a demo**](https://oobeya.io/schedule-a-new-demo/?utm_source=releasenotes\&utm_medium=june2022) now.
{% endhint %}

