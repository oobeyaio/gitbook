---
description: Learn about Azure Application Insights & Oobeya integration.
---

# Azure Application Insights Integration

***

### 1. Generate Auth Token

1. **Select your application in Azure Application Insights**:
   * Go to your Azure Application Insights account and select the desired application.
2. **Navigate to API key configuration**:
   * Under the "**Configure**" section, click on the **API Access**.
   *   Save the **Application ID** for later use in the integration with Oobeya.\
       <br>

       <figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F3lwbaz10dP7VwHtpKqm6%2Fimage.png?alt=media&#x26;token=d435b536-169e-4ff8-8202-84a90252e6da" alt=""><figcaption><p>Create API key - Application Insights</p></figcaption></figure>
3. **Create a new API key**:
   * In the top-left corner, click on **Create API Key**.
4. **Set token permissions**:
   * Assign the required permissions for Oobeya:
     * **Read Telemetry**
     * **Authenticate SDK Control Channel**
   * Once the key is created, make sure to copy it for use in the next steps.

***

### 2. Connect Azure Application Insights in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Monitoring/APM** section, click the **Azure Application Insights** card. If Azure Application Insights already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **AzureApplicationInsights v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                      |
| -------------------- | -------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Application Insights_. |
| **Application ID**   | The Application ID from step 1.                                            |
| **API Key**          | The API key from step 1.                                                   |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F4HQJb5C2q6oKsRYvmL6d%2Fform-azure-app-insights.png?alt=media&#x26;token=cb0761ab-d43b-47d2-a008-12254a4ac695" alt="Azure Application Insights data source form in Oobeya"><figcaption><p>The Azure Application Insights data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### Ready to Connect

Your Oobeya instance is now successfully connected to your Azure Application Insights account. You can now begin to diagnose, fix, and optimize the performance of your code using Oobeya's insights and analytics tools.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
