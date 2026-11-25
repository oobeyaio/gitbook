---
description: Learn about TestRail & Oobeya integration...
hidden: true
---

# TestRail Integration

### 1. Enable API Setting on TestRail

1. Click "**Administration**" on the right as follows:

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FaSlXej5ix51TzSYch3N3%2Ffile.png?alt=media)

2\. Click "**Site Settings**":

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fz4TmtxPdcEDDJQaCnxUa%2Ffile.png?alt=media)

3\. Click to the "**API**" tab, select the "**Enable API**" option, and click the "**Save Settings**" button:

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F3OSiFPQeZXve94UaOkC6%2Ffile.png?alt=media)

### 2. Connect TestRail in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Test** section, click the **Test Rail** card. If TestRail already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **TestRail V2** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                              |
| -------------------- | ------------------------------------------------------------------ |
| **Data Source Name** | A name you choose for this connection, for example _TestRail_.     |
| **Server URL**       | Your TestRail URL, for example `https://your-company.testrail.io`. |
| **Username**         | The e-mail address of a TestRail user.                             |
| **Password**         | The password the user signs in to TestRail with.                   |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fi0bcYwB1okUgzPK97JKl%2Fform-testrail.png?alt=media&#x26;token=db025eb3-11bd-4454-bd5b-5858cf839800" alt="TestRail data source form in Oobeya"><figcaption><p>The TestRail data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### Ready to Connect

Now Oobeya is connected with your own TestRail Cloud to track & visualize the status of tests with dashboards and reports.

### **Next Steps**

* [Add a new Widget](https://docs.oobeya.io/dashboards/adding-a-new-widget)
