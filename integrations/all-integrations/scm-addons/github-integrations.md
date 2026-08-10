---
description: Learn about GitHub & Oobeya integration.
icon: github
---

# GitHub Integration

There four options to integrate [Oobeya](https://oobeya.io) with [GitHub](https://github.com).&#x20;

1. **Option 1:** [Use a Personal Access Token](github-integrations.md#id-1.-generate-github-personal-access-token)
2. **Option 2:** [Use the official Oobeya GitHub App from the GitHub Marketplace. ](step-by-step-integration-instructions-for-the-oobeya-github-application.md#option-1-using-the-official-oobeya-github-app)
3. **Option 3:** [Register your own GitHub application.](step-by-step-integration-instructions-for-the-oobeya-github-application.md#option-2-registering-your-own-github-application)
4. **Option 4:** Use a GitHub App Installation Token

***

## 1. G**enerate GitHub Personal Access Token**

1. Navigate to GitHub **Settings** and click the **"Developer Settings"** tab.
2. Select the **"Personal access tokens"** tab, **"Tokens (classic)"**, **"Generate new token"** and **"Generate new token (classic)"** button. Select _**read**_ permissions for the connection.

<figure><img src="../../../.gitbook/assets/image (530).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (531).png" alt=""><figcaption></figcaption></figure>

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

* [Network Access Requirements ](../../network-access-requirements.md)
* [Create a new Gitwiser Analysis](../../../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
