---
description: Automated Reanalysis – Supported Intervals & Configuration
icon: arrows-rotate
---

# Automated Reanalysis for Analytics

Oobeya supports automated reanalysis to keep engineering metrics and reports up to date with the latest information from connected data sources.

After the initial analysis, Oobeya periodically checks for new or updated data and refreshes the analysis results according to the configured reanalysis interval.

Supported intervals vary by analytics module.

### Supported Reanalysis Intervals

The following table summarizes the available automated reanalysis periods across Oobeya's analytics modules.

<table data-header-hidden><thead><tr><th width="214.92388916015625"></th><th width="308.945556640625"></th><th></th></tr></thead><tbody><tr><td><strong>Analytics Module</strong></td><td><strong>Available Reanalysis Intervals</strong></td><td><strong>Configuration</strong></td></tr><tr><td><strong>Development Analytics</strong></td><td>15 min, 30 min, 1 hour, 6 hours, 12 hours, 24 hours</td><td>Configurable</td></tr><tr><td><strong>Project Analytics</strong></td><td>1 hour, 6 hours, 12 hours, 24 hours</td><td>Configurable</td></tr><tr><td><strong>Quality Analytics (SonarQube)</strong></td><td>15 minutes (default)</td><td>Default schedule</td></tr><tr><td><strong>Test Analytics</strong></td><td>1 hour, 6 hours, 12 hours, 24 hours</td><td>Configurable</td></tr></tbody></table>

### Reanalysis Configuration by Module

#### 1. Development Analytics

Development Analytics supports configurable automated reanalysis intervals for keeping repository activity, commits, pull requests, and related engineering metrics up to date.

**Available intervals:** 15 minutes, 30 minutes, 1 hour, 6 hours, 12 hours, and 24 hours.

#### 2. Project Analytics&#x20;

Project Analytics periodically retrieves updates from connected project management tools, such as Jira and Azure DevOps Boards, to refresh work item, sprint, and delivery metrics.

**Available intervals:** 1 hour, 6 hours, 12 hours, and 24 hours.

#### 3. Quality Analytics

Quality Analytics uses an automated reanalysis schedule to retrieve updated code quality information from SonarQube, including issues, technical debt, and quality metrics.

**Default interval: 15 minutes.**

Unlike the other modules listed above, Quality Analytics has a default 15-minute reanalysis interval.&#x20;

#### 4. Test Analytics

Test Analytics supports configurable automated reanalysis to refresh testing metrics and results from connected testing tools.

**Available intervals:** 1 hour, 6 hours, 12 hours, and 24 hours.
