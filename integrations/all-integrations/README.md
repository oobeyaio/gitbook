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
  anchors:
    visible: true
---

# Integration Catalog

Connect Oobeya to the tools your engineering organization already uses across the software development lifecycle.

In Oobeya, every integration is on the **Integrations** page (**Administration** section of the left menu), grouped into seven categories. Sign-in providers (SSO and directory) are configured separately under **Administration** > **Authentication**.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FHse7i91bO4p05dwNDfRr%2Fintegrations-page.png?alt=media&#x26;token=7c6d68c4-3f16-4465-8558-24bd70761735" alt="Oobeya Integrations page"><figcaption><p>The Integrations page in Oobeya 2.1.</p></figcaption></figure>

#### Integration Categories

| Category                            | What Oobeya collects                                                                                  |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **Project Management**              | Work items, sprints, boards, workflow activity, incidents and change requests, documentation metadata |
| **Source Code Management**          | Commits, branches, pull requests, and code reviews                                                    |
| **AI Coding Assistants**            | AI-assisted coding adoption, usage, acceptance, and cost                                              |
| **CI/CD**                           | Pipelines, builds, releases, and deployments                                                          |
| **Code Quality & Security**         | Bugs, vulnerabilities, code smells, technical debt, coverage, and security findings                   |
| **Test**                            | Test executions, test results, test automation, and linked defects                                    |
| **Monitoring/APM**                  | Errors, application performance, and production reliability signals                                   |
| **Authentication** (Administration) | Single sign-on and user directory                                                                     |

#### Integration List

| Tool                                                                                                                                                                                                                                        | Category on the Integrations page                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| [Azure DevOps](https://docs.oobeya.io/integrations/all-integrations/scm-addons/azure-devops-integration)                                                                                                                                    | Project Management, Source Code Management, CI/CD |
| [GitHub](https://docs.oobeya.io/integrations/all-integrations/scm-addons/github-integrations)                                                                                                                                               | Project Management, Source Code Management, CI/CD |
| [GitHub Enterprise](https://docs.oobeya.io/integrations/all-integrations/scm-addons/github-enterprise-integration)                                                                                                                          | Project Management, Source Code Management, CI/CD |
| [Jira Cloud](https://docs.oobeya.io/integrations/all-integrations/project-management-addons/jira-cloud-integration) / [Jira Server](https://docs.oobeya.io/integrations/all-integrations/project-management-addons/jira-server-integration) | Project Management                                |
| [Confluence](https://docs.oobeya.io/integrations/all-integrations/project-management-addons/confluence-integration)                                                                                                                         | Project Management                                |
| [ServiceNow](https://docs.oobeya.io/integrations/all-integrations/project-management-addons/servicenow-integration)                                                                                                                         | Project Management                                |
| [GitLab](https://docs.oobeya.io/integrations/all-integrations/scm-addons/gitlab-addon)                                                                                                                                                      | Source Code Management, CI/CD                     |
| [Bitbucket Cloud](https://docs.oobeya.io/integrations/all-integrations/scm-addons/bitbucket-cloud-integration)                                                                                                                              | Source Code Management, CI/CD                     |
| [Bitbucket Server / Data Center](https://docs.oobeya.io/integrations/all-integrations/scm-addons/bitbucket-server-integration)                                                                                                              | Source Code Management                            |
| [Gitea](https://docs.oobeya.io/integrations/all-integrations/scm-addons/gitea-integration)                                                                                                                                                  | Source Code Management                            |
| [Gerrit](https://docs.oobeya.io/integrations/all-integrations/scm-addons/gerrit-integration)                                                                                                                                                | Source Code Management                            |
| [Claude Code](https://docs.oobeya.io/ai-impact/claude-code-ai-impact)                                                                                                                                                                       | AI Coding Assistants                              |
| [Codex](https://docs.oobeya.io/integrations/all-integrations/ai-coding-assistants/codex-integration)                                                                                                                                        | AI Coding Assistants                              |
| [Cursor](https://docs.oobeya.io/integrations/all-integrations/ai-coding-assistants/cursor-integration)                                                                                                                                      | AI Coding Assistants                              |
| [GitHub Copilot](https://docs.oobeya.io/ai-impact/github-copilot-ai-impact)                                                                                                                                                                 | AI Coding Assistants                              |
| [Argo CD](https://docs.oobeya.io/integrations/all-integrations/scm-addons/argo-cd-integration)                                                                                                                                              | CI/CD                                             |
| [Jenkins / CloudBees](https://docs.oobeya.io/integrations/all-integrations/scm-addons/jenkins-integration)                                                                                                                                  | CI/CD                                             |
| [Octopus Deploy](https://docs.oobeya.io/integrations/all-integrations/scm-addons/octopus-deploy-integration)                                                                                                                                | CI/CD                                             |
| [TeamCity](https://docs.oobeya.io/integrations/all-integrations/scm-addons/teamcity-integration)                                                                                                                                            | CI/CD                                             |
| [SonarQube Server](https://docs.oobeya.io/integrations/all-integrations/code-quality-addons/sonarqube-integration)                                                                                                                          | Code Quality & Security                           |
| [SonarQube Cloud](https://docs.oobeya.io/integrations/all-integrations/code-quality-addons/sonarqube-cloud-integration)                                                                                                                     | Code Quality & Security                           |
| [Fortify](https://docs.oobeya.io/integrations/all-integrations/code-quality-addons/fortify-integration)                                                                                                                                     | Code Quality & Security                           |
| [Veracode](https://docs.oobeya.io/integrations/all-integrations/code-quality-addons/veracode-integration)                                                                                                                                   | Code Quality & Security                           |
| [Xray](https://docs.oobeya.io/integrations/all-integrations/code-quality-addons/xray-integration)                                                                                                                                           | Test                                              |
| [Zephyr](https://docs.oobeya.io/integrations/all-integrations/test-addons/zephyr-integration)                                                                                                                                               | Test                                              |
| [TestRail](https://docs.oobeya.io/integrations/all-integrations/code-quality-addons/testrail-integration)                                                                                                                                   | Test                                              |
| [Testinium / Testinium Cloud](https://docs.oobeya.io/integrations/all-integrations/test-addons/testinium-integration)                                                                                                                       | Test                                              |
| [AppDynamics](https://docs.oobeya.io/integrations/all-integrations/apm-monitoring-addons/appdynamics-integration)                                                                                                                           | Monitoring/APM                                    |
| [Azure Application Insights](https://docs.oobeya.io/integrations/all-integrations/apm-monitoring-addons/azure-application-insights-integration)                                                                                             | Monitoring/APM                                    |
| [Dynatrace](https://docs.oobeya.io/integrations/all-integrations/apm-monitoring-addons/dynatrace-integration)                                                                                                                               | Monitoring/APM                                    |
| [Elastic APM](https://docs.oobeya.io/integrations/all-integrations/apm-monitoring-addons/elastic-apm-integration)                                                                                                                           | Monitoring/APM                                    |
| [New Relic](https://docs.oobeya.io/integrations/all-integrations/apm-monitoring-addons/new-relic-integration)                                                                                                                               | Monitoring/APM                                    |
| [Sentry](https://docs.oobeya.io/integrations/all-integrations/apm-monitoring-addons/sentry-integration)                                                                                                                                     | Monitoring/APM                                    |
| [Microsoft Entra ID](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/azure-ad-integration)                                                                                                               | Authentication                                    |
| [Okta](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/okta-integration)                                                                                                                                 | Authentication                                    |
| [Keycloak](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/keycloak-integration)                                                                                                                         | Authentication                                    |
| [LDAP / Active Directory](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/configuring-ldap-active-directory)                                                                                             | Authentication                                    |

**AI code attribution.** Line-level attribution of AI-written code comes from [Blamely AI](https://blamely.ai/docs/welcome) (backed by Oobeya) and Git AI, which work on developers' machines and are not configured on the Integrations page.

***

### How Oobeya Integrations Work

Most integrations follow the same setup flow.

#### 1. Prepare credentials in the tool

Create a token or a read-only service account in the tool you want to connect. Each integration guide lists the permissions it needs.

#### 2. Add a data source

Open **Integrations**, select the tool's card, and fill in the form. Depending on the tool, the form asks for a server URL, an organization or workspace, a token, or a username and password. There is no separate install step. [Learn how to add a data source](https://docs.oobeya.io/integrations/adding-new-integration/adding-a-new-data-source).

#### 3. Test the connection

Click **Test Connection** to verify that Oobeya can reach the tool, then **Add**. Oobeya re-checks every data source each night and shows the result on the tool's card.

***

### Need Another Integration?

Engineering toolchains differ across organizations.

If a tool you use is not listed, contact your Oobeya representative or Customer Success team with:

* Tool name
* Product edition and version
* Cloud or self-managed deployment
* Primary use case
* Required Oobeya analytics
* Available API documentation
* Network or security constraints

Integration requests can be evaluated based on the available APIs and the engineering use case.

***

#### Visit Oobeya's blog post to learn more about integrations

{% embed url="https://oobeya.io/blog/achieving-seamless-integration-connecting-your-tools-with-oobeya/" %}
