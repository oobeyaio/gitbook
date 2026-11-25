---
description: Learn about Elastic APM & Oobeya Integration.
---

# Elastic APM Integration

This guide will walk you through the steps required to integrate Elastic APM with Oobeya.

***

### 1. Getting the Integration URL

**If You Are Connecting via HTTPS:**

* If you’re connecting via HTTPS, retrieve the base URL for Kibana directly from your browser. This URL is the address shown in the browser's address bar.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FAY3Sm0wURFdAQXGru8oI%2Fimage.png?alt=media&#x26;token=dc6197bc-b3d3-4bd2-9e54-f2181182ea45" alt=""><figcaption></figcaption></figure>

**If You Are Connecting via HTTP:**

* If you’re not using HTTPS, the URL structure would be:\
  `http://<Your_IP_or_Domain>:5601`\
  where `<Your_IP_or_Domain>` refers to the IP address or the Domain of the server running Kibana.

***

### 2. Getting the Integration Username and Password

* Use the same username and password that were entered on the screen to log into Oobeya.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F6RZi4KT3jaR41Nay6aTT%2Fimage.png?alt=media&#x26;token=9050cb5e-0f1b-432f-aa19-ca56c7650c97" alt=""><figcaption></figcaption></figure>

***

### 3. Connect Elastic APM in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Monitoring/APM** section, click the **Elastic APM** card. If Elastic APM already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **ElasticApm 7.12 or ElasticApm 8+** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                             |
| -------------------- | ----------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Elastic APM_. |
| **Server URL**       | The URL from step 1.                                              |
| **Username**         | The username from step 2.                                         |
| **Password**         | The password from step 2.                                         |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fxw6sA8oLB6LzHz8Ng0xN%2Fform-elastic-apm.png?alt=media&#x26;token=f2a1afaf-c5b2-4bf4-83b6-b2bd8ecaf8ee" alt="Elastic APM data source form in Oobeya"><figcaption><p>The Elastic APM data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### Ready to Connect

Your Oobeya instance is now connected to your Elastic APM account. You can begin diagnosing, fixing, and optimizing the performance of your code with Oobeya's analysis tools.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
