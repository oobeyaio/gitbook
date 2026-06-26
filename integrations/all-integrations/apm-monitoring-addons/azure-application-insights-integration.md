---
description: Learn about Azure Application Insights & Oobeya integration.
---

# Azure Application Insights Integration

***

## 1. Generate Auth Token

1. **Select your application in Azure Application Insights**:
   * Go to your Azure Application Insights account and select the desired application.
2. **Navigate to API key configuration**:
   * Under the "**Configure**" section, click on the **API Access**.
   *   Save the **Application ID** for later use in the integration with Oobeya.\
       <br>

       <figure><img src="../../../.gitbook/assets/image (421).png" alt=""><figcaption><p>Create API key - Application Insights</p></figcaption></figure>
3. **Create a new API key**:
   * In the top-left corner, click on **Create API Key**.
4. **Set token permissions**:
   * Assign the required permissions for Oobeya:
     * **Read Telemetry**
     * **Authenticate SDK Control Channel**
   * Once the key is created, make sure to copy it for use in the next steps.

***

## 2. Install Azure Application Insights Addon on Oobeya

1. **Log in to Oobeya** with an Administrator account.
2. Go to the **Integrations** page, find the **Azure Application Insights** addon, and click the **Install** button.

<figure><img src="../../../.gitbook/assets/image (423).png" alt=""><figcaption><p>Oobeya Integrations</p></figcaption></figure>

***

## 3. Add a New Data Source

1. Go to the **Data Sources** section in Oobeya and select **Azure Application Insights**.
2. **Create a new data source**:
   * Click on the **New Data Source** button.
   * Choose a custom name for your data source in the **Data Source Name** field.
   * Enter the **API Key** you created earlier in Azure Application Insights.
   * Input the **Application ID** you saved.

<div data-full-width="false"><figure><img src="../../../.gitbook/assets/image (424).png" alt=""><figcaption><p>Data source connection</p></figcaption></figure></div>

***

## Ready to Connect :rocket:&#x20;

Your Oobeya instance is now successfully connected to your Azure Application Insights account. You can now begin to diagnose, fix, and optimize the performance of your code using Oobeya's insights and analytics tools.

## **Next Steps** :dart:&#x20;

* [Add a new Widget](../../../dashboards/adding-a-new-widget.md)
