---
description: Learn about GitHub & Oobeya integration.
icon: github
---

# GitHub Integration

There are three options to integrate [Oobeya](https://oobeya.io) with [GitHub](https://github.com). This integration guide only covers **Option 3**.

1. **Option 1:** Use the [official Oobeya GitHub App](https://github.com/marketplace/oobeya-dora-metrics) from the GitHub Marketplace. This option provides a straightforward integration process by installing the official Oobeya GitHub App and selecting it when creating a data source in Oobeya. See the [step-by-step integration guide here](step-by-step-integration-instructions-for-the-oobeya-github-application.md#option-1-use-the-official-oobeya-github-app-listed-on-the-github-marketplace).
2. **Option 2:** Register your own GitHub application. This option offers more flexibility and customization by allowing you to create your own GitHub App, and configure settings. See the [step-by-step integration guide here](step-by-step-integration-instructions-for-the-oobeya-github-application.md#option-2-register-your-own-github-application-to-integrate-with-oobeya).
3. **Option 3:** Use a Personal Access Token for the integration. See the step-by-step integration guide below.

***

## 1. G**enerate GitHub Personal Access Token**

1. Navigate to GitHub **Settings** and click the **"Developer Settings"** tab.
2. Select the _**"Personal access tokens"**_ tab and click the **"Generate new token"** button. Select _**read**_ permissions for the connection.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F1IpCmnLe5nKuBJNfDZy2%2Ffile.png?alt=media)

&#x20; 3\. Copy and save the _**access token**_ to use it on the Oobeya data source connection.

## **2. Install GitHub Addon on Oobeya** :jigsaw:&#x20;

1. Log in to Oobeya with an _Administrator_ account.
2. Navigate to **Integrations** and select the **GitHub** addon. Then click the **"Install"** button.

![](<../../../.gitbook/assets/Screenshot 2024-12-17 at 11.14.44.png>)

## **3. Add A New Data Source** :electric\_plug:&#x20;

1. Navigate to **Data Sources** and select GitHub to add a new data source.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FMdy8XkdBBN0iRNS6u2Fr%2Ffile.png?alt=media)

2\. Click the **"New Data Source"** button and fill in the form using the _Access Token_ created on GitHub settings in the first step.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fgq76eb9TWJSqFZegBdvJ%2Ffile.png?alt=media)

3\. Click the **"Test Connection"** button to verify the connection.

## **Ready to Connect** :rocket:&#x20;

Following these steps, you can integrate the Oobeya seamlessly with your GitHub account, enhancing your development workflow with insightful metrics and data such as [DORA metrics](https://oobeya.io/dora-metrics-four-key/) and [pull request metrics](https://oobeya.io/oobeya-metric-definitions/).

## **Next Steps** :dart:&#x20;

{% content-ref url="../../../gitwiser-repo-analytics/git-analytics-metric-definitions/" %}
[git-analytics-metric-definitions](../../../gitwiser-repo-analytics/git-analytics-metric-definitions/)
{% endcontent-ref %}

{% content-ref url="../../../deployment-analytics/how-to-calculate-dora-metrics-for-github.md" %}
[how-to-calculate-dora-metrics-for-github.md](../../../deployment-analytics/how-to-calculate-dora-metrics-for-github.md)
{% endcontent-ref %}
