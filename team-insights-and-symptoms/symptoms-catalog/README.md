---
description: >-
  Oobeya helps software engineering organizations identify recurring patterns,
  risks, and improvement opportunities across their development and delivery
  processes.
icon: wave-pulse
---

# Symptoms Catalog

Symptoms turn signals collected from connected engineering tools into actionable guidance for teams and engineering leaders.

The Oobeya Symptoms module analyzes software engineering data to detect patterns that may indicate inefficiencies, delivery bottlenecks, quality risks, and gaps in data coverage.

It provides:

* **Automated symptom detection:** Identify recurring anti-patterns, bottlenecks, and operational signals from connected tools.
* **Explanations and recommendations:** Understand possible causes, potential complications, and improvement areas for each symptom.
* **Team-level visibility:** See which symptoms affect a team and use them to guide investigation and improvement.
* **Configurable severity:** Classify each symptom by its default importance and adapt its severity to your organization's needs.

![Oobeya Team Health and Symptoms](https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FTE7FOZBwlA2icSzESxrP%2Fimage.png?alt=media\&token=21bf687a-bc10-4a4d-9f62-bc16979341f1)

### Benefits

* **Improve delivery and productivity:** Surface conditions that may cause delays, unnecessary rework, or inefficient workflows.
* **Protect engineering quality:** Identify code review, code quality, and delivery risks before they become persistent problems.
* **Understand team health:** Detect activity patterns that may require investigation or support.
* **Increase data reliability:** Highlight unreachable or unused data sources that can compromise the completeness of engineering insights.

### Symptom Severity

Every symptom has a **default severity**, which determines its relative importance when it is detected. Administrators can configure the severity of each symptom in **Administration → Symptoms Settings**.

<table><thead><tr><th width="140.427978515625">Severity</th><th>Description</th></tr></thead><tbody><tr><td><strong>Critical</strong></td><td>A high-priority signal that may indicate a significant risk to delivery, engineering quality, team health, or the reliability of engineering insights. Requires prompt investigation.</td></tr><tr><td><strong>Warning</strong></td><td>A signal that deserves attention and may require corrective action or continuous improvement.</td></tr><tr><td><strong>Info</strong></td><td>An informational signal that provides useful context or identifies a lower-urgency improvement opportunity.</td></tr></tbody></table>

Severity and detection are different concepts: **severity** represents the importance configured for a symptom, while **detection** indicates whether that symptom was observed for a team during the evaluated period.&#x20;

### Available Symptoms

The Oobeya Symptoms catalog currently contains **15 symptoms**. The values below are the recommended **default severity settings** and can be changed by administrators.

<table><thead><tr><th width="68.5068359375">ID</th><th width="280.45330810546875">Symptom</th><th width="307.2645263671875">Symptom Source</th><th>Default Severity</th></tr></thead><tbody><tr><td>S1</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s1-recurring-high-rework-rate">Recurring high rework rate</a></td><td>Git Analytics (VCS tools)</td><td><strong>Critical</strong></td></tr><tr><td>S2</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s2-recurring-high-cognitive-load">Recurring high cognitive load</a></td><td>Git Analytics (VCS tools)</td><td><strong>Critical</strong></td></tr><tr><td>S3</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s3-high-weekend-activity">High weekend activity</a></td><td>Git Analytics (VCS tools)</td><td><strong>Warning</strong></td></tr><tr><td>S4</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s4-high-code-review-time">High Code Review Time</a></td><td>PR Analytics (VCS tools)</td><td><strong>Warning</strong></td></tr><tr><td>S6</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s6-high-technical-debt-on-sonar">High technical debt on Sonar</a></td><td>SonarQube</td><td><strong>Warning</strong></td></tr><tr><td>S7</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s7-high-vulnerabilities-on-sonar">High vulnerabilities on Sonar</a></td><td>SonarQube</td><td><strong>Critical</strong></td></tr><tr><td>S8</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s8-high-code-quality-bugs-on-sonar">High code quality bugs on Sonar</a></td><td>SonarQube</td><td><strong>Warning</strong></td></tr><tr><td>S9</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s9-unreviewed-pull-requests">Unreviewed Pull Requests</a></td><td>PR Analytics (VCS tools)</td><td><strong>Critical</strong></td></tr><tr><td>S10</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s10-lightning-pull-requests">Lightning Pull Requests</a></td><td>PR Analytics (VCS tools)</td><td><strong>Critical</strong></td></tr><tr><td>S11</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s11-oversize-pull-requests">Oversize Pull Requests</a></td><td>PR Analytics (VCS tools)</td><td><strong>Warning</strong></td></tr><tr><td>S12</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s12-high-lead-time-for-changes-dora">High Lead Time For Changes (DORA)</a></td><td>DORA Metrics (VCS + CI/CD + APM/IM tools)</td><td><strong>Warning</strong></td></tr><tr><td>S13</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s13-low-deployment-frequency-dora">Low Deployment Frequency (DORA)</a></td><td>DORA Metrics (VCS + CI/CD + APM/IM tools)</td><td><strong>Warning</strong></td></tr><tr><td>S14</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s14-high-change-failure-rate-dora">High Change Failure Rate (DORA)</a></td><td>DORA Metrics (VCS + CI/CD + APM/IM tools)</td><td><strong>Critical</strong></td></tr><tr><td>S15</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s15-unreachable-data-sources">Unreachable Data Sources</a></td><td>Data Health (connected data sources)</td><td><strong>Warning</strong></td></tr><tr><td>S16</td><td><a href="https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog/s16-unused-data-sources">Unused Data Sources</a></td><td>Data Health (team analysis configuration)</td><td><strong>Info</strong></td></tr></tbody></table>

### Understanding a Symptom

Each symptom has a dedicated detail page with:

* **Why is this a symptom?** – What the signal means and why it may matter.
* **Level** – Whether the symptom applies at team or individual level.
* **Potential Complications** – Associated impacts or risks.
* **Possible Causes** – Likely conditions contributing to the symptom.
* **Improvement Areas** – Suggested actions to investigate or improve the situation.
* **Detection Method** – The condition or formula used by Oobeya to identify the symptom.

Symptoms should guide investigation rather than be treated as definitive diagnoses. Interpret them alongside team context, data coverage, and trends over time.
