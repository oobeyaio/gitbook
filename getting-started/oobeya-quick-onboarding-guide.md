---
description: >-
  Welcome to Oobeya! We're excited to have you on board. This step-by-step guide
  will help you quickly get started.
icon: list-check
---

# Oobeya Quick Onboarding Guide

### Step 1: Activate Your Add-ons

The add-ons on the Oobeya Integrations page allow you to connect your SDLC/ALM tools with Oobeya, providing complete, real-time visibility into your development and delivery pipeline.

* [Install your addons](../integrations/adding-new-integration/installing-an-addon.md) from the Integrations page.

### Step 2: Connect Your Git Provider

After activating an add-on from the Integrations page, you can connect your tools and accounts with Oobeya by adding a new data source.

* [Add a new data source](../integrations/adding-new-integration/adding-a-new-data-source.md) for your Git provider. For detailed integration instructions, check the documentation links below:

| SCM Addons       | Integration Documentation                                                                                                |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------ |
| GitHub           | [github-integrations.md](../integrations/all-integrations/scm-addons/github-integrations.md "mention")                   |
| GitLab           | [gitlab-addon.md](../integrations/all-integrations/scm-addons/gitlab-addon.md "mention")                                 |
| Azure DevOps     | [azure-devops-integration.md](../integrations/all-integrations/scm-addons/azure-devops-integration.md "mention")         |
| Bitbucket Server | [bitbucket-server-integration.md](../integrations/all-integrations/scm-addons/bitbucket-server-integration.md "mention") |
| Bitbucket Cloud  | [bitbucket-cloud-integration.md](../integrations/all-integrations/scm-addons/bitbucket-cloud-integration.md "mention")   |

### Step 3: Initialize Development Analytics for Your Team

You can now analyze all of your Git repositories with Oobeya's Development Analytics module.

* [Start the Development Analytics](../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md) for your team's Git repositories.

### Step 4: While Development Analyses are in Progress, Connect Other SDLC Tools

Oobeya will now analyze your commits, pull requests, and deployments. While this process continues, we recommend connecting your other SDLC tools, such as Jira, SonarQube Server and Cloud, Fortify, Jenkins, New Relic, Dynatrace, XRay, etc. See all integrations [here](../integrations/all-integrations/).

* Install additional SDLC add-ons and define their data sources.

### Step 5: Add Your Teammates

With your tools integrated and repositories analyzed, it’s time to add your teammates.

* **Option 1:** You can integrate your organization's [LDAP](../administration/user-management-single-sign-on-auth-settings/configuring-ldap-active-directory.md) / [Active Directory](../administration/user-management-single-sign-on-auth-settings/configuring-ldap-active-directory.md) / [Azure AD](../administration/user-management-single-sign-on-auth-settings/azure-ad-integration.md) for a better onboarding process.
* **Option 2:** [Manually create new users](../administration/user-management-single-sign-on-auth-settings/adding-a-new-user.md).
* **Option 3:** Import new users from [LDAP / AD / Azure AD](../administration/user-management-single-sign-on-auth-settings/importing-a-new-user-from-ldap-ad.md).

### Step 6: Create Your Team and Team Scorecard

Now that your teammates are added, you can create your teams on Oobeya.

* Create your first team (See detailed documentation [here](../team-health/adding-a-team.md)).
* Once you created your first team, you can [configure the scorecard](../team-health/team-scorecards.md) of your team to see the real-time health status of your team.&#x20;

### Step 7: Initialize Project Analytics for Your Agile Team

Gain greater visibility into your software engineering flow by connecting project management tools like Jira or Azure Boards.

* [Start the analysis](../project-analytics/project-analytics/starting-an-agile-board-analysis.md) of your agile boards.

### Step 8: Advanced configurations:

Enhance your Oobeya experience with these configurations:

* Merge duplicate contributor accounts.
* Exclude outlier commits.
* [Set automated reanalyze period](../gitwiser-repo-analytics/settings-for-git-analytics/setting-automated-reanalyze-for-gitwiser.md) for Development Analytics and Project Analytics.

## We are here for you

The Oobeya team is dedicated to ensuring a smooth onboarding experience. If you have any questions or feedback, reach out to us on our [website](https://oobeya.io/contact/).
