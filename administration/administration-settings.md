---
description: >-
  Platform, organization, analytics, and reporting settings of your Oobeya
  installation, in one place.
---

# Administration Settings

Administrators open **Administration** from the **Administration** section of the left menu. The settings are grouped into four sections.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FQjdhF0GSCZ7V0H3tMzUS%2Fadmin-authentication.png?alt=media&#x26;token=510ba551-2f00-4677-accc-9e65e1353658" alt="Administration page with the settings menu on the left"><figcaption><p>The Administration page: settings menu on the left, the selected page on the right.</p></figcaption></figure>

{% hint style="info" %}
Integrations and their data sources are on a separate page: **Integrations**, directly above Administration in the left menu. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### Platform

| Page                   | What you configure                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Authentication**     | Sign-in providers: [Microsoft Entra ID](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/azure-ad-integration), [LDAP](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/configuring-ldap-active-directory), [Okta](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/okta-integration), and [Keycloak](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/keycloak-integration). |
| **System Settings**    | Server settings of the installation: the **Base URL** used to create links in e-mails (for example `https://oobeya.mydomain.com`), and **System Logs** downloads.                                                                                                                                                                                                                                                                                                                                                     |
| **License Management** | Your license key, server ID, license type, expiry date, and licensed features. See [License Management](https://docs.oobeya.io/administration/license-management).                                                                                                                                                                                                                                                                                                                                                    |
| **Feature Management** | Turn Oobeya modules and features on or off for the whole organization, for example Individual Scorecard, Trend Reports, user access restrictions, and the **Modules** shown in the menu (Dashboards, Organization, Developer Heatmap, Resource Allocation, Test Analytics, Problem Analytics, AI Usage, DevEx Surveys, Document Analytics).                                                                                                                                                                           |
| **API Keys**           | Tokens for the Oobeya API and the Oobeya Collector. See [API Keys](https://docs.oobeya.io/administration/api-keys).                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Notifications**      | The mail server (SMTP host, port, StartTLS, authentication, sender address and name) used for invitations, reports, and alerts, with a **Send Test Email** check.                                                                                                                                                                                                                                                                                                                                                     |

### Organization

| Page                     | What you configure                                                                                                                                                                                                                                                     |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **User Management**      | People who can sign in, their roles, and their groups (**Users**, **Groups**, **Company Roles** tabs). See [User Management](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings).                                                      |
| **Roles & Tags**         | Company roles, the default company role for new users, which roles are excluded from the Team Scorecard, which roles show a contribution calendar, display names of company roles, and **Developer Tags** used to group developers (for example in developer leagues). |
| **Organizational Chart** | The levels of your organization and the lead role of each level.                                                                                                                                                                                                       |
| **Time Settings**        | System and local time zones, working days, and working hours. Working days are used, for example, by the working-days filters of AI Impact and Activity Heatmap.                                                                                                       |

### Analytics

| Page                          | What you configure                                                                                                                                                                                                                                                                          |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Projects & Boards**         | How boards and sprints are analyzed: automated reanalysis, calculation type (mean or weighted average across boards), and tool-specific settings on the **Jira**, **Azure Boards**, **GitHub**, and **ServiceNow** tabs.                                                                    |
| **Coding, Review & Delivery** | How Git, pull request, and deployment data are analyzed: **Git Analytics** (including automated reanalysis and [exclusions](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/git-analytics-exclusions)), **Pull Request Analytics**, and **Deployment Analytics**. |
| **Quality & Security**        | How the [Total Code Quality Index](https://docs.oobeya.io/quality-analytics/total-code-quality-index-tcqi) is calculated and reported (coefficients and the monthly reporting day).                                                                                                         |
| **Add-ons**                   | Tool-specific settings, for example SonarQube Server branch support and the API filter for instances with more than 10,000 projects.                                                                                                                                                        |

### Insights & AI

| Page                | What you configure                                                                                                                                                                                       |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **AI Impact**       | How Oobeya reads your AI coding assistants: automated reanalysis and its period. See [AI Impact Overview](https://docs.oobeya.io/ai-impact/ai-impact-overview).                                          |
| **Symptoms**        | Which team health symptoms are detected, their severity (Critical, Warning, Info), and their thresholds. See the [Symptoms Catalog](https://docs.oobeya.io/team-insights-and-symptoms/symptoms-catalog). |
| **Survey Settings** | Defaults for new DevEx surveys: confidentiality, who sees results, reminders, and notifications. See [DevEx Surveys](https://docs.oobeya.io/devex-surveys/devex-surveys).                                |
