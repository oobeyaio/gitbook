---
description: Learn about Jira Cloud & Oobeya integration.
icon: jira
---

# Jira Cloud Integration

## 1. **Generate Jira Cloud API Token**

1. Click on the **profile** picture at the top right of the screen, then select **Account Settings**.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FbJT79Dk5G6ERsBMk17Ej%2Ffile.png?alt=media)

2\. Open the "Security" tab.

![Select Security tab.](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FdnJTMy2uk35njnI22hpk%2Ffile.png?alt=media)

3\. Click the link "**Create and manage API tokens**" under the API Token section.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F0mpsKeUqc89JaOJOoVZv%2Ffile.png?alt=media)

4\. Click the "**Create API token**" button at the top of the page.&#x20;

<figure><img src="../../../.gitbook/assets/image (532).png" alt=""><figcaption></figcaption></figure>

5. Make sure you copy your new API token for further use.

<figure><img src="../../../.gitbook/assets/image (533).png" alt=""><figcaption></figcaption></figure>

## **2. Install Jira Addon on Oobeya** :jigsaw:&#x20;

1. Log in to [Oobeya](https://oobeya.io/) with an _Administrator_ account.
2. Navigate to **Integrations** and select the **Jira** addon and then click the **"Install"** button.

![](<../../../.gitbook/assets/Screenshot 2024-12-17 at 13.37.58.png>)

## **3. Add A New Data Source** :electric\_plug:&#x20;

1\. Navigate to **Data Sources**, select Jira to add a new data source.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F2RNvEaQB5JJsMdfJKp6G%2Ffile.png?alt=media)

2\. Click the **"New Data Source"** button and fill in the form.

* **Server URL:** Enter your Jira Cloud account URL (e.g. https://yourcompany.atlassian.net)
* **Username:** Enter the email address registered on Jira Cloud.
* **Password:** Enter the API Token which was created on Jira settings in the first step.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FGJWsJ31zrtTHKbIyxRDG%2Ffile.png?alt=media)

3. Click the **"Test Connection"** button to verify the connection.

&#x20;4\. Select the **"Set as default"** option to provide a default data source for the Scorecards.

## **Ready to Connect** :rocket:&#x20;

Now Oobeya is connected with your own Jira Cloud account to get the real-time project management data of your organization.

## **Next Steps** :dart:&#x20;

* [Network Access Requirements ](../../network-access-requirements.md)
* [Create a new Gitwiser Analysis](../../../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
