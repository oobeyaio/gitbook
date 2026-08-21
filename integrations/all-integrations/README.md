---
description: See all documented integrations here.
icon: plug
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Integration Catalog

Connect Oobeya to the tools your engineering organization already uses across the software development lifecycle.

Oobeya supports **40+ integrations across 7 categories**, bringing development, delivery, planning, quality, testing, production, documentation, identity, and AI-assisted development data into a unified engineering intelligence platform.

### Integration Categories

<table data-header-hidden data-search="false"><thead><tr><th width="276.88946533203125">Category</th><th>What Oobeya Collects</th></tr></thead><tbody><tr><td><strong>Project Management &#x26; Documentation</strong></td><td>Work items, sprints, backlogs, boards, workflow activity, and documentation metadata</td></tr><tr><td><strong>SCM &#x26; CI/CD</strong></td><td>Commits, branches, pull requests, reviews, pipelines, builds, releases, and deployments</td></tr><tr><td><strong>AI Coding Assistants &#x26; Attribution</strong></td><td>AI-assisted coding adoption, attribution, acceptance rates, and productivity impact</td></tr><tr><td><strong>Quality &#x26; Security</strong></td><td>Bugs, vulnerabilities, code smells, technical debt, coverage, and security findings</td></tr><tr><td><strong>Test Management</strong></td><td>Test executions, test results, automation, UAT, and defect-related signals</td></tr><tr><td><strong>Monitoring / APM</strong></td><td>Incidents, errors, application performance, and production reliability signals</td></tr><tr><td><strong>SSO &#x26; Identity</strong></td><td>Authentication, user provisioning, directory synchronization, and identity management</td></tr></tbody></table>

### Integration List

<table data-full-width="false"><thead><tr><th width="233">Tool</th><th width="208">Categories</th><th>Modules</th><th>Plan</th></tr></thead><tbody><tr><td>GitHub Copilot</td><td>AI Coding Assistant</td><td>All</td><td>All</td></tr><tr><td>Cursor</td><td>AI Coding Assistant</td><td>All</td><td>All</td></tr><tr><td>Claude Code</td><td>AI Coding Assistant</td><td>All</td><td>All</td></tr><tr><td><a href="https://blamely.ai/docs/welcome">Blamely AI</a> <em>(backed by Oobeya)</em></td><td>AI Code Attribution</td><td>All</td><td>All</td></tr><tr><td>Git AI</td><td>AI Code Attribution</td><td>All</td><td>All</td></tr><tr><td><a href="project-management-addons/jira-cloud-integration.md">Jira Cloud</a></td><td>Project Management</td><td>All</td><td>Cloud</td></tr><tr><td><a href="project-management-addons/jira-server-integration.md">Jira Server / Data Center</a></td><td>Project Management</td><td>All</td><td>Server, Data Center</td></tr><tr><td>Confluence</td><td>Documentation</td><td>All</td><td>Server, Data Center</td></tr><tr><td><a href="scm-addons/azure-devops-integration.md">Azure DevOps</a></td><td>SCM &#x26; CI/CD &#x26; Project Management</td><td>Repos, Azure Boards, Pipelines, Releases</td><td>Cloud, Server</td></tr><tr><td><a href="scm-addons/github-integrations.md">GitHub</a></td><td>SCM &#x26; CI/CD</td><td>Repos, GitHub Actions</td><td>Cloud, Enterprise Cloud, Enterprise On-premise</td></tr><tr><td><a href="scm-addons/gitlab-addon.md">GitLab</a></td><td>SCM &#x26; CI/CD</td><td>Repos, GitLab CI</td><td>Cloud, Self Managed, Enterprise</td></tr><tr><td><a href="scm-addons/bitbucket-cloud-integration.md">Bitbucket Cloud</a></td><td>SCM &#x26; CI/CD</td><td>Repos, Bitbucket Pipelines</td><td>Cloud</td></tr><tr><td><a href="scm-addons/bitbucket-server-integration.md">Bitbucket Server / Data Center</a></td><td>SCM</td><td>Repos</td><td>Server, Data Center</td></tr><tr><td><a href="scm-addons/gitea-integration.md">Gitea</a></td><td>SCM</td><td>Repos</td><td>Server</td></tr><tr><td><a href="scm-addons/gerrit-integration.md">Gerrit</a></td><td>SCM </td><td>All</td><td>Cloud, Server</td></tr><tr><td>ArgoCD</td><td>CI/CD</td><td>All</td><td>Server</td></tr><tr><td><a href="scm-addons/jenkins-integration.md">Jenkins</a></td><td>CI/CD</td><td>All</td><td>Server</td></tr><tr><td>Cloudbees</td><td>CI/CD</td><td>All</td><td>Server</td></tr><tr><td><a href="scm-addons/teamcity-integration.md">TeamCity</a></td><td>CI/CD</td><td>All</td><td>Cloud, Server</td></tr><tr><td><a href="scm-addons/octopus-deploy-integration.md">Octopus Deploy</a></td><td>CI/CD</td><td>All</td><td>Cloud, Server</td></tr><tr><td><a href="code-quality-addons/sonarqube-integration.md">SonarQube Server</a></td><td>Quality &#x26; Security</td><td>All</td><td>Server</td></tr><tr><td><a href="https://docs.oobeya.io/integrations/all-integrations/code-quality-addons/sonarqube-cloud-integration">SonarQube Cloud</a></td><td>Quality &#x26; Security</td><td>All</td><td>Cloud</td></tr><tr><td>Fortify</td><td>Quality &#x26; Security</td><td>All</td><td>Server</td></tr><tr><td><a href="code-quality-addons/veracode-integration.md">Veracode</a></td><td>Quality &#x26; Security</td><td>SAST</td><td>Cloud</td></tr><tr><td><a href="code-quality-addons/xray-integration.md">Xray</a> (for Jira)</td><td>Quality &#x26; Security</td><td>All</td><td>Cloud, Server / DC</td></tr><tr><td><a href="apm-monitoring-addons/azure-application-insights-integration.md">Azure Application Insights</a></td><td>Monitoring &#x26; APM</td><td>APM</td><td>Cloud</td></tr><tr><td><a href="apm-monitoring-addons/new-relic-integration.md">New Relic</a></td><td>Monitoring &#x26; APM</td><td>APM, Incident Management</td><td>Cloud</td></tr><tr><td>Datadog (Beta)</td><td>Monitoring &#x26; APM</td><td>APM, Incident Management</td><td>Cloud</td></tr><tr><td><a href="../../administration/user-management-single-sign-on-auth-settings/azure-ad-integration.md">Microsoft Entra (Azure AD)</a></td><td>Authentication</td><td>SSO</td><td>-</td></tr><tr><td>Okta (SAML)</td><td>Authentication</td><td>SSO</td><td>-</td></tr><tr><td><a href="../../administration/user-management-single-sign-on-auth-settings/configuring-ldap-active-directory.md">LDAP</a></td><td>Authentication</td><td>SSO</td><td>-</td></tr></tbody></table>

***

## How Oobeya Integrations Work

Most Oobeya integrations follow the same basic setup flow.

### 1. Install the Add-on

Navigate to **Integrations** and install the add-on for the tool you want to connect.

[Learn how to install an add-on](https://docs.oobeya.io/integrations/adding-new-integration/installing-an-addon).

### 2. Create a Data Source

Navigate to **Data Sources**, select the installed integration, and enter the required connection information.

Depending on the platform, this may include:

* Server URL
* Organization or workspace
* API token
* Personal Access Token
* Application credentials
* Client ID and secret

[Learn how to add a data source](https://docs.oobeya.io/integrations/adding-new-integration/adding-a-new-data-source).

### 3. Test the Connection

Use **Test Connection** to verify that Oobeya can access the connected platform.

***

## Need Another Integration?

Engineering toolchains differ across organizations.

If a tool you use is not currently listed, contact your Oobeya representative or Customer Success team with:

* Tool name
* Product edition and version
* Cloud or self-managed deployment
* Primary use case
* Required Oobeya analytics
* Available API documentation
* Network or security constraints

Integration requests can be evaluated based on the available APIs and the engineering use case.

***

### Visit Oobeya's blog post to learn more about integrations

{% embed url="https://oobeya.io/blog/achieving-seamless-integration-connecting-your-tools-with-oobeya/" %}

