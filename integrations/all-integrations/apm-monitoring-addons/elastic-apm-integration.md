---
description: Learn about Elastic APM & Oobeya Integration.
---

# Elastic APM Integration

This guide will walk you through the steps required to integrate Elastic APM with Oobeya.

***

## 1. Getting the Integration URL

**If You Are Connecting via HTTPS:**

* If you’re connecting via HTTPS, retrieve the base URL for Kibana directly from your browser. This URL is the address shown in the browser's address bar.

<figure><img src="../../../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>

**If You Are Connecting via HTTP:**

* If you’re not using HTTPS, the URL structure would be:\
  `http://<Your_IP_or_Domain>:5601`\
  where `<Your_IP_or_Domain>` refers to the IP address or the Domain of the server running Kibana.

***

## 2. Getting the Integration Username and Password

* Use the same username and password that were entered on the screen to log into Oobeya.

<figure><img src="../../../.gitbook/assets/image (426).png" alt=""><figcaption></figcaption></figure>

***

## 3. Install Elastic APM on Oobeya

1. **Log in to Oobeya** with an Administrator account.
2. Go to the **Integrations** section, select **Elastic APM**, and click the **Install** button.

<figure><img src="../../../.gitbook/assets/image (428).png" alt=""><figcaption><p>Oobeya Integrations</p></figcaption></figure>

***

## 4. Create Data Source and Test Connection

1. Go to the **Data Sources** section in Oobeya, and select **Elastic APM**.
2. **Create a new data source**:
   * Click on the **New Data Source** button.
   * Fill out the form using the URL, username, and password obtained in Step 1.
   * You can assign any name for the **Data Source Name** field.
3. **Test the connection**:
   * Click the **Test Connection** button to verify the connection with Elastic APM.

<figure><img src="../../../.gitbook/assets/image (429).png" alt=""><figcaption><p>Data source connection</p></figcaption></figure>

***

## Ready to Connect :rocket:&#x20;

Your Oobeya instance is now connected to your Elastic APM account. You can begin diagnosing, fixing, and optimizing the performance of your code with Oobeya's analysis tools.

## **Next Steps** :dart:&#x20;

* [Network Access Requirements ](../../network-access-requirements.md)
* [Create a new Gitwiser Analysis](../../../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
