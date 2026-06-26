---
description: >-
  Connect Octopus Deploy and track accurate DORA metrics calculated by Oobeya
  Deployment Analytics.
icon: octopus-deploy
---

# Octopus Deploy Integration

Enhance the software delivery process by seamlessly integrating [Octopus Deploy ](https://octopus.com/)with [Oobeya](https://oobeya.io). With this powerful integration, you can effortlessly track and monitor [DORA metrics,](https://oobeya.io/dora-metrics-four-key/) including Lead Time For Changes, Deployment Frequency, Change Failure Rate, and Time To Restore Service, to ensure accurate and insightful analysis of your CI/CD pipeline. Octopus Deploy serves as a continuous deployment tool, while the Oobeya integration brings effective data collection, analysis, and visualization capabilities, enabling you to gain valuable insights into the software delivery process.

## **1. Generate** Octopus Deploy **API Token**

1. Log into the Octopus Web Portal, click your profile image, and select Profile. \
   Then, click "My API Keys".&#x20;
2. Click the "New API Key" button, state the purpose of the API key, and click Generate. \
   Finally, copy the new API key to your clipboard.

<figure><img src="../../../.gitbook/assets/image (48).png" alt=""><figcaption><p>Octopus Deploy API Keys</p></figcaption></figure>

## **2. Install Octopus Deploy Addon on Oobeya**

1. Log in to Oobeya with an _Administrator_ account.
2. Navigate to **Integrations,** select the **Octopus Deploy** addon, and click the **"Install"** button.&#x20;

<figure><img src="../../../.gitbook/assets/Screenshot 2024-12-17 at 11.32.37.png" alt=""><figcaption></figcaption></figure>

## **3. Add A New Data Source**

1. Navigate to **Data Sources**, and select **Octopus Deploy** to add a new data source.&#x20;
2. Click the **"New Data Source"** button and fill in the form using the _API Token (API Key)_ created on Octopus Deploy settings in the first step.&#x20;

<div data-full-width="false"><figure><img src="../../../.gitbook/assets/Screenshot 2024-12-17 at 11.42.19.png" alt="" width="375"><figcaption></figcaption></figure></div>

3. Click the **"Test Connection"** button to verify the connection.

***

### **Ready to Connect** :rocket:&#x20;

Now Oobeya is connected to your own Octopus Deploy account/server to enable you to track accurate DORA metrics calculated by Oobeya Deployment Analytics.

