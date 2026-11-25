---
description: >-
  Connect Testinium or Testinium Cloud to Oobeya to bring in automated test
  results.
---

# Testinium Integration

[Testinium](https://testinium.com) is a test automation platform for web and mobile tests. Oobeya reads Testinium test plans and their execution results. There are two cards in the **Test** category of the Integrations page:

* **Testinium**: a self-hosted (enterprise) Testinium installation, version 1.8 or later.
* **Testinium Cloud**: Testinium's cloud service, version 2.3 or later.

### 1. Prepare a Testinium user

Use a Testinium user that can see the projects and test plans you want to analyze. Oobeya signs in with its username and password.

### 2. Connect Testinium in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Test** section, click the **Testinium** or **Testinium Cloud** card. If it already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version (**Testinium 1.8+** or **TestiniumCloud 2.3+**) and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Testinium                                   | Testinium Cloud                                   |
| -------------------- | ------------------------------------------- | ------------------------------------------------- |
| **Data Source Name** | A name you choose, for example _Testinium_. | A name you choose, for example _Testinium Cloud_. |
| **Server URL**       | The URL of your Testinium installation.     | Not asked.                                        |
| **Username**         | The Testinium user.                         | The Testinium Cloud user.                         |
| **Password**         | The user's password.                        | The user's password.                              |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fxmjfd1lKj07X6yqUZRbk%2Fform-testinium.png?alt=media&#x26;token=63ad6660-31fc-49ce-8add-9391d01b9979" alt="Testinium data source form in Oobeya"><figcaption><p>The Testinium data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Next Steps**

* [Test Automation Metrics and API](https://docs.oobeya.io/test-analytics/test-otomasyon-metrikleri-ve-api-dokumani)
* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
