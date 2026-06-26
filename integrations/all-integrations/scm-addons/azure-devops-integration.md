---
description: Learn about Azure DevOps & Oobeya integration.
icon: windows
---

# Azure DevOps Integration

{% hint style="info" %}
Oobeya **Azure DevOps addon** is compatible with both Azure DevOps Services (cloud) and Azure DevOps Server (TFS2017, TFS2018, TFS2019).
{% endhint %}

## **1. Create Azure DevOps Personal Access Token**

1\. Navigate to **User Settings** and click **"Personal Access Tokens"**.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FhmDVE5PtAmUpx0mUOg2i%2Ffile.png?alt=media)

2\. Click the _**"New Token"**_ button and select _**read**_ permissions for the connection.&#x20;

The required permissions are:

* Build – _Read_
* Code – _Read_&#x20;
* Project and Team – _Read_&#x20;
* Pull Request Threads – _Read_
* Release – _Read_
* Test Management – _Read_&#x20;
* Work Items – _Read_&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FnK8bOYmMxQfrGHpgDJbL%2Ffile.png?alt=media)

3\. Copy and save the _access token_ to use it on the Oobeya data source connection.

## **2. Install Azure DevOps Addon on Oobeya** :jigsaw:&#x20;

1. Log in to [Oobeya](https://oobeya.io/) with an _Administrator_ account.
2. Navigate to **Integrations** and select the **Azure DevOps** addon and then click the **"Install"** button.&#x20;

![](<../../../.gitbook/assets/Screenshot 2024-12-13 at 16.33.15.png>)

## **3. Add A New Data Source** :electric\_plug:&#x20;

1.Navigate to **Data Sources**, select Azure DevOps to add a new data source.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FXV9PrLMKFQrLNfJNFUwl%2Ffile.png?alt=media)

2\. Click the **"New Data Source"** button and fill in the form using the Personal _Access Token_ which was created on Azure DevOps settings in the first step.&#x20;

**Data Source Name:** A custom name for your data source (e.g., "Oobeya Azure Data Source").&#x20;

**Server URL:** Your Azure DevOps organization’s URL (e.g., https://dev.azure.com/{your-organization})&#x20;

**Token:** The Personal Access Token you retrieved earlier.

<figure><img src="../../../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure>

3\. Click the **"Test Connection"** button to verify the connection.

## **Ready to Connect** :rocket:&#x20;

Now Oobeya is connected with your own Azure DevOps to get the real-time statistics of your code repositories to track each development activity.

## **Next Steps** :dart:&#x20;

* [Add a new Widget](../../../dashboards/adding-a-new-widget.md)
* [Create a new Gitwiser Analysis](../../../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
