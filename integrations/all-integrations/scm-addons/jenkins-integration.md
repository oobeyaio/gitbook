---
description: Learn about Jenkins & Oobeya integration.
icon: jenkins
---

# Jenkins & Cloudbees Integration

## 1. **Generate Jenkins API Token**

1\. On Jenkins, open the user dropdown at the top right and click the **"Security"** option.&#x20;

<figure><img src="../../../.gitbook/assets/image (537).png" alt=""><figcaption></figcaption></figure>

2\. Generate a new API Token by clicking "Add new token".

<figure><img src="../../../.gitbook/assets/image (538).png" alt=""><figcaption></figcaption></figure>

3\. Copy and save the _API Token_ to use on the Oobeya data source connection.

## **2. Install Jenkins Addon on Oobeya** :jigsaw:&#x20;

1. Log in to [Oobeya](https://oobeya.io/) with an _Administrator_ account.
2. Navigate to **Integrations**, select the Jenkins addon, and click the **"Install"** button.&#x20;

<figure><img src="../../../.gitbook/assets/Screenshot 2024-12-17 at 11.29.17.png" alt=""><figcaption></figcaption></figure>

## **3. Add A New Data Source** :electric\_plug:&#x20;

1\. Navigate to **Data Sources**, and select Jenkins to add a new data source.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FlPEJ9ZdExRIcbNRLGeMm%2Ffile.png?alt=media)

2\. Click the **"New Data Source"** button and fill in the form by using the _API Token_ which was created on Jenkins settings in the first step.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fv3pOYb7pNqJpxTsUF88b%2Ffile.png?alt=media)

3\. Click the **"Test Connection"** button to verify the connection.

## **Ready to Connect** :rocket:&#x20;

Now Oobeya is connected with your own Jenkins server to monitor the health status of your pipelines and track key metrics such as _time-to-fix, average deployment duration..._

## **Next Steps** :dart:&#x20;

* [Add a new Widget](../../../dashboards/adding-a-new-widget.md)
