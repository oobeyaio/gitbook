---
description: Learn about AppDynamics & Oobeya integration.
---

# AppDynamics Integration

### 1. Create A Local User for Oobeya

1. Access Appdynamics Controller and click the top right button on the screen.

![](https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F7lYAwBX8oHoZOLZbtukx%2Fimage.png?alt=media\&token=29893d41-ce8a-43d6-a427-33c23519e87e)

2\. Select the “**Administration**”

![](https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FSt3G8OXHtshKHd9wssfH%2Fimage.png?alt=media\&token=ec309d92-38b0-4557-975e-106ce1bacd75)

3\. In the "**Users**" tab, click “**Create**” and **fill** in the required fields.

4\. Add Roles by clicking the "**Add**” button below the Roles section.

![](https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F2w7FDhfFClkeG6eHRhTM%2Fimage.png?alt=media\&token=4f553974-f918-422a-94ad-1ac44bbb61a5)

5\. Select the listed role, then create the account by clicking “**Save**”.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fbp6awAQqxwxlppUssX3P%2Fimage.png?alt=media&#x26;token=56c77210-1cfc-4d42-a733-c5955558f2c7" alt="" width="375"><figcaption></figcaption></figure>

### 2. Connect AppDynamics in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Monitoring/APM** section, click the **AppDynamics** card. If AppDynamics already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **AppDynamics 4+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                           |
| -------------------- | ------------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _AppDynamics_.               |
| **Server URL**       | Your AppDynamics controller URL.                                                |
| **Account Name**     | Your AppDynamics account name. For on-premises controllers this is `customer1`. |
| **Password**         | The password of the local user from step 1.                                     |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FBpLTAaa9XQ78b5V7P9th%2Fform-appdynamics.png?alt=media&#x26;token=8eff9a71-77a1-410b-91f5-6702be5ed5c5" alt="AppDynamics data source form in Oobeya"><figcaption><p>The AppDynamics data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### Ready to Connect

Oobeya is now connected with your AppDynamics account to give you real-time performance monitoring and analytics for your applications. Stay ahead with insights into application health and performance.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
