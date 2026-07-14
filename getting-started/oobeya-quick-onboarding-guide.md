---
description: >-
  Welcome to Oobeya! We're excited to have you on board. This step-by-step guide
  will help you quickly get started.
icon: list-check
---

# Oobeya Quick Onboarding Guide

## Quick Onboarding Guide

Use this guide to connect your engineering tools, configure your organization, and create your first actionable engineering view in Oobeya.

This guide is primarily intended for Oobeya **Workspace Administrators** responsible for the initial configuration of Oobeya.

***

### Before You Begin

Make sure that:

* Your Oobeya workspace is available.
* You have administrator access to Oobeya.
* You have the required credentials or tokens for the tools you plan to connect.
* The service account used to generate tokens has access to the required repositories, projects, pipelines, and boards.
* Your organization has identified the first teams and repositories to onboard.

> Start with a small, representative scope. Configure one or two teams first, validate the results, and then expand the setup across the organization.

***

### Onboarding Overview

The recommended onboarding sequence is:

1. Define the initial scope
2. Connect your source code management platform
3. Initialize Development Analytics
4. Connect additional engineering tools
5. Add users and map identities
6. Create teams
7. Configure Team Scorecards
8. Initialize Project Analytics
9. Validate data and automate updates
10. Expand your Oobeya setup

***

### Step 1: Define Your Initial Scope

Before connecting tools, define what you want to onboard first.

For the initial setup, identify:

* One or two engineering teams
* The repositories owned by those teams
* The primary development branches
* The related project management boards
* The CI/CD pipelines used for production deployments
* The users who will access Oobeya
* The contributors who will be analyzed by Oobeya

Also decide which outcomes you want to review first:

* Development activity and productivity metrics
* Pull request and code review performance
* DORA metrics
* Project delivery and flow
* Code quality
* Team health and engineering risks
* AI coding assistant adoption and impact

A clearly defined scope makes it easier to validate data, repository ownership, team mapping, and metric accuracy.

***

### Step 2: Connect Your Source Code Management Platform

Oobeya uses source code management data as the foundation for Development Analytics.

Commonly supported SCM platforms include:

* GitHub, GitLab, Azure DevOps, Bitbucket, Gitea, Gerrit.

#### 2.1 Install the Add-on

1. Open **Integrations** in Oobeya.
2. Find your SCM platform.
3. Select the add-on.
4. Click **Install**.

See [Installing an Add-on](https://docs.oobeya.io/integrations/adding-new-integration/installing-an-addon).

#### 2.2 Add a Data Source

After installing the add-on:

1. Navigate to **Data Sources**.
2. Select the installed SCM platform.
3. Click **New Data Source**.
4. Enter the required URL, credentials, token, or connection details.
5. Save the data source.
6. Validate that Oobeya can access the expected organizations, projects, and repositories.

See [Adding a New Data Source](https://docs.oobeya.io/integrations/adding-new-integration/adding-a-new-data-source).

For provider-specific requirements and permission details, review the [Integration Catalog](https://docs.oobeya.io/integrations/all-integrations).

> The connected service account must be able to access every repository and project that you want to analyze.

***

### Step 3: Initialize Development Analytics

After connecting your SCM platform, create your first Development Analytics analysis.

Development Analytics can analyze:

* Commits
* Contributors
* Branches
* Pull requests
* Code review activity
* Development patterns
* Deployment activity
* DORA metrics

To start an analysis:

1. Open **Development Analytics**.
2. Click **New Analysis**.
3. Select your SCM platform and data source.
4. Select the project, repository, and branch.
5. Choose the CI/CD strategy used by the repository.
6. Configure deployment and incident detection options when applicable.
7. Select the related team and historical analysis period.
8. Review the configuration and click **Finish**.

See [Setting Up Development Analytics and DORA Metrics](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics).

#### Configuration Notes

* Select the correct primary or development branch.
* Choose the CI/CD strategy that reflects the actual delivery workflow.
* Configure the production deployment pipeline when you want to calculate deployment metrics.
* Select the correct development model, such as pull request-based or trunk-based development.
* Configure an incident source to calculate Change Failure Rate and Time to Restore Service accurately.
* Avoid starting with every repository before validating the configuration on a smaller scope.

The initial historical analysis may take some time depending on the selected date range, repository size, and number of activities.

***

### Step 4: Connect Additional Engineering Tools

While the initial repository analysis is running, connect the other tools used across your software delivery lifecycle.

Depending on your reporting goals, you can connect:

<table><thead><tr><th width="186.2650146484375">Data Source</th><th width="246.2806396484375">Examples</th><th>What It Adds</th></tr></thead><tbody><tr><td>Project management</td><td>Jira, Azure Boards, ServiceNow</td><td>Work items, flow, predictability, lead time, cycle time</td></tr><tr><td>CI/CD</td><td>ArgoCD, Jenkins, GitHub Actions, GitLab CI, Azure Pipelines</td><td>Build, pipeline, and deployment activity</td></tr><tr><td>Code quality and security</td><td>SonarQube, SonarCloud, Fortify</td><td>Quality, security, maintainability, and technical debt signals</td></tr><tr><td>Monitoring and APM</td><td>New Relic, Dynatrace, Datadog, Elastic</td><td>Production incidents and operational signals</td></tr><tr><td>Test management</td><td>Xray, Testinium and supported testing tools</td><td>Test execution, automation, and efficiency signals</td></tr><tr><td>AI coding assistants</td><td>GitHub Copilot and supported AI tools</td><td>Adoption, usage, cost, and engineering impact signals</td></tr><tr><td>Identity providers</td><td>Microsoft Entra ID, LDAP, Active Directory</td><td>Authentication, provisioning, and user onboarding</td></tr></tbody></table>

Browse all available tools in the [Integration Catalog](https://docs.oobeya.io/integrations/all-integrations).

> Connect only the tools required for your initial use case. Additional integrations can be introduced after the first teams and metrics are validated.

***

### Step 5: Add Users and Map Identities

Users must be configured correctly so that Oobeya can associate engineering activity with the correct profiles and teams.

You can add users through:

#### Microsoft Entra ID

Configure authentication and user access through Microsoft Entra ID.

See [Microsoft Entra ID Integration](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/azure-ad-integration).

#### LDAP or Active Directory

Connect your corporate directory to authenticate and import users.

See [LDAP / Active Directory Integration](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/configuring-ldap-active-directory).

#### Manual User Creation

Create individual users directly in Oobeya.

See [Adding a New User](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/adding-a-new-user).

#### Verify Contributor Accounts

A single developer may appear under different usernames or email addresses across Git, project management, code quality, and identity systems.

Review contributor identities and merge duplicate accounts where necessary. Correct identity mapping is especially important for:

* Developer Profiles
* Team Scorecards
* Resource Allocation
* AI Impact
* Individual-level metrics
* Cross-platform reporting

***

### Step 6: Create Your Teams

Teams connect people, repositories, projects, and engineering metrics within Oobeya.

To create a team:

1. Open the team management area.
2. Click **Add Team**.
3. Enter the team name and description.
4. Add team members.
5. Assign the relevant team roles.
6. Save the team.

See [Adding a Team](https://docs.oobeya.io/team-health/adding-a-team).

#### Team Configuration Checklist

Before continuing, verify that:

* All current team members are included.
* Former team members are removed or marked correctly.
* Contributor identities are mapped to the correct users.
* The correct repositories are associated with the team.
* The correct project boards are associated with the team.
* Team ownership reflects the selected reporting period.

> Team configuration affects scorecards, Symptoms, resource allocation, benchmarks, and team-level reporting. Review team membership regularly.

***

### Step 7: Configure the Team Scorecard

Team Scorecards provide a unified view of engineering health by combining metrics from multiple data sources.

To configure the first scorecard:

1. Open the team.
2. Navigate to **Team Scorecard**.
3. Add the relevant scorecard widgets.
4. Select the required repositories, projects, and data sources.
5. Configure targets and benchmarks where applicable.
6. Save the scorecard.
7. Validate the results with the team or engineering manager.

See [Team Scorecard](https://docs.oobeya.io/team-health/team-scorecards).

A first scorecard can include signals from:

* Development Analytics
* Pull Request Analytics
* DORA metrics
* Project Analytics
* Code Quality
* Test Analytics
* Bug Analytics
* AI Impact
* Engineering Symptoms

Start with a small number of meaningful metrics rather than displaying every available metric.

***

### Step 8: Initialize Project Analytics

Connect a project management platform when you want to analyze delivery flow, work item progress, planning effectiveness, and predictability.

Project Analytics can provide visibility into:

* Lead Time
* Cycle Time
* Velocity
* Throughput
* Predictability
* Productivity
* Work in Progress
* Backlog Health
* Innovation Rate
* Project Contribution

To start an analysis:

1. Connect Jira, Azure Boards, or another supported project management platform.
2. Open **Project Analytics**.
3. Click **New Analysis**.
4. Select the data source, project, and board.
5. Configure work item types, workflow statuses, and analysis settings.
6. Associate the analysis with the relevant team.
7. Select the historical analysis period.
8. Review the configuration and start the analysis.

See [Starting a Project Analytics Analysis](https://docs.oobeya.io/project-analytics/project-analytics/starting-an-agile-board-analysis).

> Review status mappings and excluded work item types carefully. Incorrect workflow configuration can affect flow and delivery metrics.

***

### Step 9: Validate Your Data

Before expanding Oobeya across the organization, validate the first results with the relevant engineering teams.

#### Development Analytics

Confirm that:

* [ ] The expected repositories are visible.
* [ ] The correct branches are analyzed.
* [ ] Commit authors are mapped correctly.
* [ ] Pull requests and reviews are visible.
* [ ] Bot accounts and service users are handled appropriately.
* [ ] Outlier or irrelevant commits are excluded when necessary.

#### DORA Metrics

Confirm that:

* [ ] The correct production pipeline is selected.
* [ ] Deployments are detected correctly.
* [ ] The development model matches the team workflow.
* [ ] Production failures are detected from the correct source.
* [ ] Deployment environments are mapped correctly.

#### Project Analytics

Confirm that:

* [ ] The correct project and board are selected.
* [ ] Workflow statuses are mapped correctly.
* [ ] Completed, active, and backlog states are classified correctly.
* [ ] Unnecessary work item types are excluded.
* [ ] Team and project relationships are accurate.

#### Teams and Users

Confirm that:

* [ ] Team membership is current.
* [ ] Duplicate contributor profiles are merged.
* [ ] Repositories and boards are assigned to the correct teams.
* [ ] Access permissions match user responsibilities.

Data validation should involve both the Oobeya administrator and the engineering teams that understand the actual workflows.

***

### Step 10: Configure Automatic Updates

After validating the first analyses, configure automatic reanalysis so that Oobeya keeps engineering data up to date.

See [Setting Automated Reanalyze for Development Analytics](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/setting-automated-reanalyze-for-gitwiser).

When selecting an update frequency, consider:

* The size of the organization
* The number of repositories and boards
* The frequency of engineering activity
* Available infrastructure resources
* Reporting and operating review schedules

For on-premise environments, monitor resource consumption as the number of integrations and analyses increases.

***

### Step 11: Expand Your Oobeya Setup

After the initial teams and data sources are validated, you can gradually enable additional Oobeya capabilities.

#### Engineering Insights and Symptoms

Automatically identify recurring bottlenecks, risks, and engineering anti-patterns.

* [Symptoms Catalog](https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog)
* [Engineering Benchmarks](https://docs.oobeya.io/team-insights-and-symptoms/engineering-benchmarks)

#### AI Coding Assistant Impact

Understand AI coding assistant adoption and its relationship with engineering outcomes.

* [Measuring the Impact of AI Coding Assistants](https://docs.oobeya.io/use-cases/measuring-the-impact-of-ai-coding-assistants)
* [GitHub Copilot – AI Impact](https://docs.oobeya.io/ai-impact/github-copilot-ai-impact)
* [AI Cost and Credits](../ai-impact/ai-cost-and-credits.md)

#### Resource Allocation

Understand how engineering capacity is distributed across projects and work categories.

* [Resource Allocation](https://docs.oobeya.io/allocations/resource-allocation)

***

### Recommended Rollout Approach

For enterprise onboarding, use an incremental rollout:

#### Phase 1: Pilot

* [ ] Select one or two representative teams.
* [ ] Connect the minimum required tools.
* [ ] Validate identities, repositories, boards, and pipelines.
* [ ] Create the first Team Scorecards.
* [ ] Review results with engineering managers.

#### Phase 2: Standardize

* [ ] Define common repository and project configuration standards.
* [ ] Establish consistent team ownership and identity mapping.
* [ ] Agree on the core metrics and scorecard structure.
* [ ] Document exceptions for different engineering workflows.

#### Phase 3: Scale

* [ ] Onboard additional teams and business units.
* [ ] Introduce additional integrations and modules.
* [ ] Create organization-level dashboards.
* [ ] Configure role-based access.
* [ ] Establish recurring engineering reviews.

#### Phase 4: Improve

* [ ] Review engineering Symptoms and trends.
* [ ] Compare teams using relevant benchmarks and context.
* [ ] Track improvement goals over time.
* [ ] Evaluate the impact of process, tooling, and AI-assisted development changes.

***

### Onboarding Completion Checklist

Use this checklist before completing the initial onboarding:

* [ ] Oobeya is installed or the SaaS workspace is accessible.
* [ ] The primary SCM platform is connected.
* [ ] At least two repository analysis is completed.
* [ ] Repository, branch, and contributor data is validated.
* [ ] Required CI/CD, project management, quality, and monitoring tools are connected.
* [ ] Users are added or imported.
* [ ] Duplicate contributor identities are reviewed.
* [ ] At least two teams are created.
* [ ] Team members, repositories, and boards are mapped correctly.
* [ ] The first Team Scorecard is configured.
* [ ] Project Analytics is initialized where applicable.
* [ ] DORA configuration is validated where applicable.
* [ ] Automatic reanalysis is enabled.
* [ ] Access permissions are reviewed.
* [ ] Engineering managers have validated the initial results.

***

### Next Steps

After completing the onboarding process:

* Review the [Metrics List](https://docs.oobeya.io/getting-started/metrics).
* Review the [Symptoms Catalog](https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog).
* Establish a recurring review process for team health, delivery, quality, and AI impact.

***

### Need Help?

The Oobeya team is dedicated to ensuring a smooth onboarding experience. If you have any questions or feedback, reach out to us on our [website](https://oobeya.io/contact/) or via your dedicated support channels.
