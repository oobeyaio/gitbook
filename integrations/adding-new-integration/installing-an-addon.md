---
description: Learn about how to work with addons on Oobeya Integrations...
icon: plug-circle-check
---

# Installing An Addon

{% hint style="success" %}
**No install step since Oobeya 2.1.** The former **Marketplace** (where add-ons were installed) and **Data Sources** pages are now one **Integrations** page. An integration is enabled automatically when you save its first data source.
{% endhint %}

### The Integrations page

Open **Integrations** from the **Administration** section of the left menu. Only users with the **Administrator** or **Super User** role can open the connection forms; other users can see which tools are connected.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FHse7i91bO4p05dwNDfRr%2Fintegrations-page.png?alt=media&#x26;token=7c6d68c4-3f16-4465-8558-24bd70761735" alt="Oobeya Integrations page"><figcaption><p>Categories on the left, a card per tool, and the connection status on each card.</p></figcaption></figure>

The page shows:

* **Categories** on the left, with the number of tools in each. A tool can appear in more than one category. For example, Azure DevOps and GitHub appear under Project Management, Source Code Management, and CI/CD.
* **Search for an app**, and the **All**, **Connected**, and **Not connected** filters.
* A card per tool with a short description and its status:
  * **N success** and **N failed**: results of the latest connection check of the tool's data sources.
  * **N data source(s)**: data sources whose connection is not checked automatically.
  * **Not connected**: the tool has no data source yet.
* A document icon on each card that opens the tool's integration guide.
* **Last checked** and **Check all now** at the top right. Oobeya checks the connection of every data source each night; **Check all now** starts a check immediately.

{% hint style="info" %}
When data sources fail the latest connection check, Oobeya shows a banner with the number of failed data sources and a **Go to Integrations** link.
{% endhint %}

#### Categories

| Category                | Tools                                                                                                             |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Project Management      | Azure DevOps, Jira, Confluence, ServiceNow, GitHub, GitHub Enterprise                                             |
| Source Code Management  | Azure DevOps, Bitbucket (Server / Data Center), Bitbucket Cloud, Gitea, GitHub, GitLab, Gerrit, GitHub Enterprise |
| AI Coding Assistants    | Claude Code, Codex, Cursor, GitHub Copilot                                                                        |
| CI/CD                   | Azure DevOps, Argo CD, Bitbucket Cloud, GitHub, GitLab, Jenkins, Octopus Deploy, TeamCity, GitHub Enterprise      |
| Code Quality & Security | SonarQube Server, SonarQube Cloud, Fortify, Veracode                                                              |
| Test                    | Xray, Zephyr, TestRail, Testinium, Testinium Cloud                                                                |
| Monitoring/APM          | AppDynamics, Azure Application Insights, Dynatrace, Elastic APM, New Relic, Sentry, Oobeya APM                    |

Which integrations you can use depends on your license. When an integration is not included in your license, Oobeya shows _"This integration isn't included in your license."_ when you select it.

### Next step

* [Adding A New Data Source](https://docs.oobeya.io/integrations/adding-new-integration/adding-a-new-data-source)
