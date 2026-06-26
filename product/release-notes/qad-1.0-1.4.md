# QAD-1.0 - 1.4

## QAD-1.4.0 - _Executive Dashboard, Organizational Chart, Pull Request Analytics improvements..._

_See all the changes live in Oobeya Playground..._  :point\_right: [_Go to Playground_](https://playground.oobeya.io/)

### :new: New Features

* **Executive Dashboard:** Executive Dashboard enables senior leadership to monitor and understand the metrics of organizational units. This executive report provides actionable insights into software development quality and efficiency.

![Oobeya Executive Dashboard - Organization-wide metrics](<../../.gitbook/assets/image (300).png>)

![Executive Report of development units](<../../.gitbook/assets/image (87).png>)

You can set **goals** for the metrics you report:

![](<../../.gitbook/assets/image (257).png>)

* **Organizational Chart:** You can define your company's organizational chart on Oobeya. Executive Dashboard will be created according to this organizational chart configuration.

![Organizational Chart configuration](<../../.gitbook/assets/image (141).png>)

![Teams](<../../.gitbook/assets/image (134).png>)

* **Bitbucket Cloud Pull Request Analytics:** PRA is now ready-to-use for Bitbucket Cloud repositories.

![](<../../.gitbook/assets/image (196).png>)

* **PRA Default Goal Settings:** You can set default goals for the pull request analytics metrics.

![PRA default goals](<../../.gitbook/assets/image (283).png>)

### :muscle: Improvements

* **Jira Sprint Progress widget:** Support Kanban Boards for Jira Agile Progress widget.&#x20;

![](<../../.gitbook/assets/image (110).png>)

* **Jira Sprint Progress widget:** Removed project field. Added "Current Sprint" option.&#x20;

![](<../../.gitbook/assets/image (169).png>)

* Updates for the new product name.

![](../../.gitbook/assets/oobeya_logo.png)

### :lady\_beetle: Fixes

* Fixed - Jenkins Multibranch pipeline listing problem.&#x20;
* Fixed - GitHub Pull Request Analytics tooltip problem.
* Fixed - Set Gitwiser analysis status as "Failed" if the cloning process was failed.&#x20;

## QAD-1.3.2 - _Custom Addon, GitHub Pull Request Analytics, GitLab Clone with SSH..._

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.oobeya.io/)

### :new: New Features

* :jigsaw: **Custom Addon:** We have launched _Custom Addon_ integration for the QA Dashboard Market Place. Users can develop a connector application and integrate their own tools to QA Dashboard.&#x20;

![Adding custom addon to Market Place](<../../.gitbook/assets/image (78).png>)

{% hint style="info" %}
Check out the custom addon template with the documentation on GitHub: [https://github.com/dashboardqa/custom-addon-template](https://github.com/dashboardqa/custom-addon-template)

<img src="../../.gitbook/assets/image (91).png" alt="" data-size="original">
{% endhint %}

* **GitHub Pull Request Analytics:** We have added the Pull Request Analytics (PRA) module of Gitwiser for GitHub repositories. You can analyze the pull requests of existing repositories in Gitwiser by clicking the start button on the PRA tab.<br>
* **GitLab - Clone with SSH:** We started to support cloning GitLab repositories with SSH.

![](<../../.gitbook/assets/image (289).png>)

## QAD-1.2.0 - _Slack & Microsoft Teams Notifiers for individuals and teams..._

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* :bell: **Slack Notifier:** We have added a _**Slack**_ notifier for **individuals** and **teams**. \
  QA Dashboard has an integration with Slack to send notifications and reports into your own chat channels. See the steps [here ](../../alerts-and-notifications/adding-notifications-for-slack.md)to add notifiers for Slack.

![Individuals can set notifiers to get insights into their activities and metrics.](<../../.gitbook/assets/image (197).png>)

_See the sample message for an individual:_

![](<../../.gitbook/assets/image (94).png>)

_See the sample message for a team:_

![](<../../.gitbook/assets/image (284).png>)

* :bell: **MS Teams Notifier:** We have added _**MS Teams**_ notifier for **individuals** and **teams**.\
  [**QA Dashboard**](https://dashboard.qa) has an integration with **Microsoft Teams** to send notification messages and reports into your own channels. See the steps [here ](../../alerts-and-notifications/adding-notifications-for-ms-teams.md)to add _channels, connectors, incoming webhooks_ for MS Teams.

![Individuals can set notifiers to get insights into their activities and metrics.](<../../.gitbook/assets/image (298).png>)

_See the sample message for an individual:_

![](<../../.gitbook/assets/image (288).png>)

_See the sample message for a team:_

![](<../../.gitbook/assets/image (176).png>)



## QAD-1.1.0 - _Gitwiser Pull Request Analytics_

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* **Gitwiser Pull Request Analytics:** We have launched the Pull Request Analytics (PRA) module of Gitwiser for **GitLab** and **Azure DevOps**. _Bitbucket Server_ and _Bitbucket Cloud_ are on the way...  \
  With this release, Gitwiser has two modules: _Repository Analytics & Pull Request Analytics_.

![](<../../.gitbook/assets/image (90).png>)

* You can analyze the pull requests of existing repositories in Gitwiser by clicking the start button on the PRA tab:

![](<../../.gitbook/assets/image (161).png>)

* You can select the "**Analyze Pull Requests**" option to perform PRA for the new Gitwiser analysis.

![](<../../.gitbook/assets/image (125).png>)

* **PRA Widgets:** PRA has five widgets now: _Code Review Cycle Time, Coding Time, Time To Merge, Pull Request Size, and Work in Progress._
* **Code Review Cycle Time (time-to-review):** You can see the **stale** pull requests in red below. If code review time took longer than the goal, the pull request is identified as stale. Long review time is a blocker for development teams.

![Code Review Cycle Time widget](<../../.gitbook/assets/image (285).png>)

* **Coding Time (time-to-open):** The time elapsed between the first commit and open time for pull requests. Long coding time may block developers to see the problems earlier. Long coding time is a major risk for the high cycle time. Developers should break large features into small pieces and keep the coding time short for each pull request.
* **Time To Merge:** The time elapsed between the first commit and merge time.
* **Pull Request Size:** Total size (lines added, removed, and changed) of pull requests.

![Pull Request Size widget](<../../.gitbook/assets/image (71).png>)

* **Work in Progress:** Shows the open pull requests and bottlenecks of the development process. You can see the risky pull requests and take action to resolve them earlier. Alerts and reminders for open pull requests can help you improve your cycle time.

![Work in Progress PRs](<../../.gitbook/assets/image (237).png>)

* **PRA Goals:** You can set goals for each pull request metric. :dart:&#x20;

![](<../../.gitbook/assets/image (146).png>)



* **Jira Metrics with JQL Widget:** We have added a new predefined widget for Jira Addon. By using this widget, you can add your own metrics using Jira Query Language (JQL) syntax.

![If you define the second JQL, a ratio will be calculated to display in the widget.](<../../.gitbook/assets/image (302).png>)

![Metrics with JQL widget](<../../.gitbook/assets/image (142).png>)

* **Duplicate Widget:** We have added a duplication option for the widgets.&#x20;

![](<../../.gitbook/assets/image (281).png>)



## QAD-1.0.40 - _Azure Active Directory, Azure Container Registry, Azure DevOps Board Metrics..._

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* **Azure Active Directory Integration:** We have launched Azure AD integration as a new authentication type.

![](<../../.gitbook/assets/image (182).png>)

* Admin Settings for Azure AD:

![](<../../.gitbook/assets/image (272).png>)

* **Azure DevOps Widgets:** We have added new scopes (**Boards & Sprints**) and predefined widgets (**Board Metrics, Work Distribution, Sprint Size**) for Azure DevOps Addon.&#x20;

![Azure DevOps Widget Scopes](<../../.gitbook/assets/image (188).png>)

You can create your own metrics by using work item queries (WIQL).

![](<../../.gitbook/assets/image (291).png>)

![](<../../.gitbook/assets/image (317).png>)

* **Note:** If you define the second metric WIQL, a ratio will be calculated to display in the widget.

`Ratio formula = (metric1 / metric2) * 100`

* **Azure Container Registry:** We have built automation for **Azure Container Registry** to keep our customers using AKS up-to-date.

&#x20;

## QAD-1.0.38 - _Team Scorecard multiple branch support,_ _Performance & UI/UX Improvements..._

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* **SonarQube Branch Support for Team Scorecards:** We have added a project-branch mapping field to the Team Scorecard settings in order to enable _**custom branch selection for Team Scorecards.**_&#x20;
* We have added unit test and coverage results to the Azure DevOps Build Details widget.

![](<../../.gitbook/assets/image (274).png>)

### :muscle: Improvements

* Increased performance :rocket: of [Gitwiser](/broken/pages/-MGIrMC8EqiUIlw9lI0P) analysis main page.
* We have added a cancel option for the running Gitwiser analysis.

![](<../../.gitbook/assets/image (282).png>)

* We have added a progress bar on Gitwiser analysis.

![](<../../.gitbook/assets/image (137).png>)

### :lady\_beetle: Fixes

* Fixed- branch group problem on Azure DevOps Gitwiser analysis.
* Fixed- Timezone problem on Gitwiser.

## QAD-1.0.37 - _SonarQube multiple branch support, Cosmos DB,_ _Performance & UI/UX Improvements..._

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* **SonarQube Branch Support for Dashboards:** We have added branch selection option for SonarQube widgets on Dashboards. If you analyze multiple branches on SonarQube projects, you are now able to select the branch that you want to track on QA Dashboard widgets.&#x20;

![](<../../.gitbook/assets/image (198).png>)

* **SonarQube Branch Support for Developer Scorecards:** We have added a project-branch mapping field to the administrator settings in order to enable _**custom branch selection for Developer Scorecards.**_ You can prefer using default branch of analysis, or you can define your own default branch name for all projects, or you can define custom project & branch mapping to track branches specific to any project.&#x20;

![](<../../.gitbook/assets/image (322).png>)

* We have just launched a new support for Azure **Cosmos DB**. :tada:&#x20;

### :muscle: Improvements

* Increased performance :rocket: of [Gitwiser](/broken/pages/-MGIrMC8EqiUIlw9lI0P) analysis result page.
* UX - We have formatted the file name of the downloaded scorecards. _(ProfileName-Scorecard-2020-09-22.jpeg)_
* UX - We have added links for _documentation_ and _contact_ to the footer.

### :lady\_beetle: Fixes

* Fixed- contribution ratio problem on scorecards.
* Fixed- timeline graph problem on widgets.
* Fixed- sending biweekly email report problem.
* Fixed- missing GitLab merged\_at parameter problem on GitLab Merge Requests widget.

## QAD-1.0.36 - _Contributions Graph, Company Avg, Performance Improvements..._&#x20;

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* **Contributions Graph** - We have added a new widget to [_Developer Scorecards_](../../scorecards/individual-scorecards.md) in order to show you a "contributions graph" by using [Gitwiser ](/broken/pages/-MGIrMC8EqiUIlw9lI0P)repository analysis data. Now you can see your active contribution days on a calendar heatmap. :calendar\_spiral:&#x20;

![A calendar heat-map for the contributions.](<../../.gitbook/assets/image (119).png>)

* **Company Average For Metrics** - You can now see the "_company average_" value for the metrics on Developer Scorecard in order to know where you stand in your organization. :chart\_with\_upwards\_trend:&#x20;

![](<../../.gitbook/assets/image (150).png>)

* **Download Scorecards** - You can now download the scorecards as images.&#x20;

### :muscle: Improvements

* Increased performance for [Gitwiser](/broken/pages/-MGIrMC8EqiUIlw9lI0P) XL repository analysis. :rocket:&#x20;
* Increased performance for [Gitwiser widgets](../../scorecards/individual-scorecards.md#contribution-statistics) on Scorecards. :rocket:&#x20;
* We have added a linking option for the "Widget Header Note". :pencil2:&#x20;

![](<../../.gitbook/assets/image (229).png>)

### :lady\_beetle: Fixes

* [Gitwiser account mapping](../../scorecards/individual-scorecards.md#related-accounts-of-developer) is now case-insensitive. :abc:&#x20;
* Added new statuses (reopened, confirmed) for building of [SonarQube ](../../integrations/all-integrations/code-quality-addons/sonarqube-integration.md)Open Issues web link.&#x20;



## QAD-1.0.35 - _Dashboard Info drawer, UI/UX Improvements..._

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* **Dashboard Info** - We have added a drawer to show information about the Dashboard. We will also add audit information in future releases.

![](<../../.gitbook/assets/image (314).png>)

### :muscle: Improvements

* **UX** - All drop-down lists are sorted from A to Z.
* **UX** - We have added "_Read the docs_" links to [addon information](../../integrations/adding-new-integration/installing-an-addon.md) pop-up in order to navigate the user to the manual.

### :lady\_beetle: Fixes

* We no longer support "_Contributor Widget"_ for TFVC scope in Azure DevOps widgets. You can use [Gitwiser](/broken/pages/-MGIr_Ok2Wq0_M0SIia0) widget scope to visualize TFVC contribution metrics.



## QAD-1.0.34 - _Limited Docker Edition, Download Widgets, UI/UX Improvements..._

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* **Limited Docker Edition** - We have launched a **free-to-use** version of [**QA Dashboard**](https://dashboard.qa) with [**limited features**](https://dashboard.qa/#pricing). :tada:You can run your own instance using Docker 🐳  to **see QA Dashboard with your own data**. For detailed information, see the documentation [here](/broken/pages/-MGJBd_XLkkttJB500Ff). 📋&#x20;
* **Download Widgets** - You can now download the widgets as images.

<div align="center"><img src="../../.gitbook/assets/image (265).png" alt=""></div>

### :muscle: Improvements

* **Data Sources** - We have added "_Test Connection_" for [Bitbucket Cloud integration](../../integrations/all-integrations/scm-addons/bitbucket-cloud-integration.md).

![](<../../.gitbook/assets/image (364).png>)

* **Data Sources** - We have set [_SonarQube API Token_](../../integrations/all-integrations/code-quality-addons/sonarqube-integration.md#3-add-a-new-data-source) field as an optional field. You can now connect to Sonarqube instances which don't require authorization.
* **UX** - If there is only one [predefined widget](../../dashboards/adding-a-new-widget.md#adding-a-new-widget) in the drop-down list, select it automatically in widget create modal.

### :lady\_beetle: Fixes

* Fixed long text problem on the _Azure DevOps Build Details_ widget.
* Removed deprecated parameter from the date filter list.



## QAD-1.0.33 - _GitHub Addon, GitLab Merge Request Widget, UI/UX Improvements..._

_See all the changes live in QA Dashboard Playground..._  :point\_right: [_Go to Playground_](https://playground.dashboard.qa)

### :new: New Features

* **GitHub Addon -** We have launched our new integration with GitHub :tada: . \
  You can now connect to your GitHub repositories just like GitLab, Bitbucket, Azure DevOps and SVN... Learn more about GitHub & QA Dashboard integration [here](../../integrations/all-integrations/scm-addons/github-integrations.md)...\
  You can analyze your **GitHub repositories** on _**Gitwiser**_ to get insights about your development activities.&#x20;

![](https://img.announcekit.app/540307919ff28a6362fcfdd2e5f0e56b?s=3aebf81a6e8ae46a133996ab43ffa8ff)

*   **GitLab Merge Requests Widgets -** We have launched a new [GitLab ](../../integrations/all-integrations/scm-addons/gitlab-addon.md)widget to get visibility into the key _merge request_ metric "**Time to Merge**" to identify the _development bottlenecks_.&#x20;

    Tracking time-to-merge (_TTM_) will reduce your **cycle time** to deliver value and increase team efficiency.

![](https://img.announcekit.app/35ba1093171c1206e915875eba4adef8?s=56838a7f29318ffa9fa7205733ca041f)

### :muscle: Improvements

* **UI/UX -** Improvements on Market Place & Data Sources pages.
* **UX -** We have added a welcome modal including a basic product tour for the new users.
* **Leagues -** Increased pagination limit from 15 to 50 on Team Scoreboard.
* **Leagues -** We have added the count of selected Objectives/KPIs. You can now see the total count of selected Objectives/KPIs on the League cards.&#x20;

![](<../../.gitbook/assets/image (230).png>)

### :lady\_beetle: Fixes

* Fixed global date filter problem for "Last 2 weeks".
