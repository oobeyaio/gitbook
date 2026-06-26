---
description: Check out the new features and improvements we've released for you.
---

# 🎁 Oobeya 2023 Q4 - Release Notes

&#x20;:tada: We're thrilled to unveil the latest features and enhancements in [Oobeya](https://oobeya.io)'s Quarter 4 release! Dive into the exciting new integrations, powerful enhancements, and innovative features designed to elevate your software development and delivery experience.

## ​🎁 NEW FEATURES

1.  **Gitea Integration**

    * Introducing a new Version Control System tool integration: [Gitea](https://about.gitea.com/). Seamlessly analyze your source code repositories (repos, commits, pull requests) with this latest addition to our integration suite.&#x20;

    <figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption><p>Welcome Gitea! <a href="https://about.gitea.com/">https://about.gitea.com/</a></p></figcaption></figure>
2.  **Octopus Deploy Integration for DORA Metrics Tracking**

    * Elevate your CI/CD processes with the new [Octopus Deploy](https://octopus.com/) integration. Effortlessly measure and track DORA Metrics for Octopus Deploy pipelines integrated with any Git-based Version Control System tool.

    <figure><img src="../../.gitbook/assets/image (58).png" alt="" width="479"><figcaption><p>Gitwiser Analysis Modal</p></figcaption></figure>
3.  **AgileSpace Planning Cut-off Days**

    * Empower users to set planning cut-off days for each Scrum board analysis in AgileSpace. Enhance planning accuracy and streamline your Scrum board analysis process.

    <figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption><p>AgileSpace Planning Cut-off Days</p></figcaption></figure>
4.  **Time In State Widget Tabs in AgileSpace**

    * Gain deeper insights with new tabs for the Time In State Widget in AgileSpace. Visualize Lead Time Highest 50 and Lead Time Lowest 50 Tasks/Work Items for more comprehensive analytics.

    <figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption><p>AgileSpace Board Overview</p></figcaption></figure>
5. **DORA Metrics Calculation Enhancements for Bitbucket Server, Cloud, and Jenkins**
   * Extend DORA Metrics support for Bitbucket Server & Cloud users practicing trunk-based development.&#x20;
   * Track SCM Changes information from Jenkins for more accurate DORA metrics calculation.
6.  **New DORA Metrics Breakdown Widget for Parent Team Scorecards**

    * Enhance team performance visibility with a new widget in Parent Team Scorecards, displaying DORA Metrics by Team.

    <figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption><p>DORA Metrics by Team</p></figcaption></figure>
7.  **New Symptoms for DORA Metrics**

    * Introducing new symptoms related to DORA Metrics, including High Lead Time For Changes, Low Deployment Frequency, and High Change Failure Rate. Identify and address delivery-related issues proactively.

    <figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption><p>Oobeya Symptoms for delivery</p></figcaption></figure>



    <figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption><p>Symptom Thresholds</p></figcaption></figure>
8. **Azure DevOps Kanban Boards Analysis in AgileSpace**
   * Support for analyzing Azure DevOps Kanban Boards.
9.  **GitHub Pull Request Description Parsing for Value Stream Mapping (BETA)**

    * In the BETA version of Value Stream Mapping, Oobeya parses GitHub Pull Request descriptions and identifies related Work Items to track the journey from commit and work item (or issue/task) to Pull Requests to Production Deployments.

    <figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption><p>Oobeya <strong>Value Stream Mapping (BETA)</strong></p></figcaption></figure>
10. **Select AgileSpace Analysis in Gitwiser Analysis Settings (BETA)**
    * In the BETA version of Value Stream Mapping, users can select the related AgileSpace analysis in Gitwiser analysis settings (only for GitHub right now).
11. **Lead Time Metric Calculation in Value Stream Mapping (BETA)**
    * Calculate a lead time metric in the BETA version of Value Stream Mapping using the formula: Lead Time = Deployment Done - Work Item Created.
12. **Granularity Metric-1 in Team Scorecards (BETA)**

    * In the BETA version of Cognitive Load - Granularity Metrics, calculate a new metric for teams: Granularity Metric -1, with the formula Number of Team Repositories / Number of Team Developers.&#x20;

    <figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption><p><strong>Granularity Metric-1</strong></p></figcaption></figure>
13. **New Sprint Velocity Metrics in AgileSpace**

    * These enhancements in AgileSpace include calculating and displaying new metrics in the Sprint Velocity Widget's Last 8 Sprints table, such as Done Planned, Unfinished Planned, Unfinished Effort Pulled in Extra, Predictability, Productivity, Churn, etc.

    <figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption><p>Oobeya AgileSpace Board Analytics</p></figcaption></figure>

***

## :muscle: IMPROVEMENTS

* **Performance Improvements in Gitwiser**
  * A new analysis flow for PR & DORA analytics to improve overall performance in Gitwiser.
* **Enhancements in DORA Metrics Calculation**
  * Improvements were made in DORA metrics calculation for more accurate and insightful performance metrics.
* **Slider for DORA Timeline Widgets**
  * Improve data visualization with the addition of a slider to the x-axis of the DORA timeline widgets in Gitwiser.
* **Team Lead Authorization for Gitwiser Repository Analysis**
  * Team Leads are now empowered to update their teams' Gitwiser repository analysis, providing greater autonomy and efficiency.
* **GitHub Workflow ID in Gitwiser**
  * Enhance traceability with the addition of GitHub workflow ID to the Deployment Title in Gitwiser Deployment Analytics (DORA).
* **Merged Pull Request Widget Improvements**
  * Enhance visibility into pull request metrics with improvements to the Merged Pull Request widget, including average coding time and review time.
* **Main Page Improvements in AgileSpace**
  * Experience a more refined AgileSpace main page with improved search, sort, and filter functionalities.
* **Team Lead Authorization for AgileSpace Analysis**
  * Team Leads can now update their teams' AgileSpace analysis, streamlining analysis management.
* **Parallel AgileSpace Board Analysis**
  * Run AgileSpace board analysis in parallel for a more efficient and streamlined analysis process.
* **Display Removal Date for Work Items in AgileSpace**
  * AgileSpace now displays the date when a work item/issue was removed from the sprint, enhancing transparency in sprint reports.
* **Symptoms Threshold and Period Settings**
  * New threshold and period settings for Symptoms, providing greater customization and flexibility.
* **UI/UX Enhancements**
  * Enhance your user experience with various UI improvements, including displaying the license expiration date on the license warning bar and keeping selections in local storage for the hierarchical view of teams.
* **Inactive User Display**
  * Display inactive users and profiles with a distinct style for improved user management and visibility.
* **Value Percentage Display**
  * Show values as 500+% in comparison with the previous period if the value exceeds 500%, offering a more informative visual representation.

We're committed to delivering tools that empower your teams and improve your overall Oobeya experience. If you have any questions or feedback, our support team is ready to assist you. Here's to continued success in your software development journey with Oobeya!

***

## :person\_running: SEE OOBEYA IN ACTION!

{% hint style="info" %}
Do you want to see all the new features in action and talk about the product roadmap?

Click and [**book a demo**](https://oobeya.io/schedule-a-new-demo/?utm_source=releasenotes\&utm_medium=june2022) now.
{% endhint %}

