---
description: Learn about Bitbucket Cloud & Oobeya integration.
icon: bitbucket
---

# Bitbucket Cloud Integration

## 1. **Create an Atlassian API token**

1. Navigate to [Atlassian Account – Security → API tokens](https://id.atlassian.com/manage-profile/security/api-tokens).&#x20;
2. Click **Create API token with scopes**.

<figure><img src="../../../.gitbook/assets/image (497).png" alt=""><figcaption></figcaption></figure>

3. Name your token and choose an expiration date.

<figure><img src="../../../.gitbook/assets/image (498).png" alt=""><figcaption></figcaption></figure>

4. Select Bitbucket from the app list.

<figure><img src="../../../.gitbook/assets/image (499).png" alt=""><figcaption></figcaption></figure>

5. Select the scopes as shown below:<br>

<figure><img src="../../../.gitbook/assets/image (496).png" alt=""><figcaption></figcaption></figure>

6. Review the token and complete the token creation process.



## **2. Install Bitbucket Cloud Addon on Oobeya** :jigsaw:&#x20;

1. Log in to Oobeya with an _Administrator_ account.
2. Navigate to **Integrations** and select the **Bitbucket Cloud** addon and then click the **"Install"** button.&#x20;

![](<../../../.gitbook/assets/Screenshot 2024-12-17 at 11.02.58.png>)

## **3. Add A New Data Source** :electric\_plug:&#x20;

1\. Navigate to **Data Sources**, and select Bitbucket Cloud to add a new data source.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FR6StYegMSpYq1AvucXED%2Ffile.png?alt=media)

2\. Click the **"New Data Source"** button and fill in the form by using the _API Token (instead of the App Password, which will be changed in the next release),_ which was generated on Bitbucket Cloud in the first step.&#x20;

**Data Source Name:** A custom name for your data source (e.g., "Bitbucket Cloud").&#x20;

**Username:** E-mail account used for Atlassian.

**App Password:** API Token created in the previous steps.

**Workspace:** Your workspace on Bitbucket Cloud.

<figure><img src="../../../.gitbook/assets/image (502).png" alt=""><figcaption></figcaption></figure>

3\. Click the **"Test Connection"** button to verify the connection.

## **Ready to Connect** :rocket:&#x20;

Now Oobeya is connected with your own Bitbucket Cloud account to get the real-time statistics of your code repositories to track each development activity.

## **Next Steps** :dart:&#x20;

* [Network Access Requirements ](../../network-access-requirements.md)
* [Create a new Gitwiser Analysis](../../../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
