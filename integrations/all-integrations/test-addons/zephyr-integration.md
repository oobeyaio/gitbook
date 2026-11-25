---
description: Connect Zephyr (Zephyr Scale) to Oobeya for Test Analytics.
---

# Zephyr Integration

Zephyr is a test management tool for Jira. Oobeya reads Zephyr test projects and execution results for [Test Analytics](https://docs.oobeya.io/test-analytics/yeni-test-analizi-olusturma). Both Zephyr on Jira Server / Data Center and **Zephyr Scale Cloud** are supported. Zephyr is in the **Test** category of the Integrations page.

### 1. Prepare the credentials

* **Zephyr on Jira Server / Data Center:** a Jira user with read access to the test projects, with its password or a personal access token.
* **Zephyr Scale Cloud:** three values:
  * the e-mail address of an Atlassian account,
  * a Jira API token of that account,
  * a Zephyr API token, created in Jira from the Zephyr Scale settings of your profile.

### 2. Connect Zephyr in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Test** section, click the **Zephyr** card. If Zephyr already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version: **Zephyr v1** for Jira Server / Data Center, or **Zephyr Cloud** for Zephyr Scale Cloud. Fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

**Zephyr v1 (Server / Data Center)**

| Field                 | Value                                                                    |
| --------------------- | ------------------------------------------------------------------------ |
| **Data Source Name**  | A name you choose for this connection, for example _Zephyr_.             |
| **Server URL**        | Your Jira URL, for example `https://jira.example.com`.                   |
| **Access Type**       | **Basic** (username and password) or **Bearer** (personal access token). |
| **Username / E-mail** | The Jira user (Basic only).                                              |
| **Password / Token**  | The password, or the personal access token for Bearer.                   |

**Zephyr Cloud**

| Field                | Value                                                                    |
| -------------------- | ------------------------------------------------------------------------ |
| **Data Source Name** | A name you choose for this connection, for example _Zephyr Scale Cloud_. |
| **Server URL**       | Your Jira Cloud site, for example `https://your-company.atlassian.net`.  |
| **Jira E-mail**      | The Atlassian account e-mail.                                            |
| **Jira API Token**   | The Jira API token of that account.                                      |
| **Zephyr API Token** | The Zephyr API token.                                                    |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FWuB5mtcoO8UyJaWgEXvA%2Fform-zephyr.png?alt=media&#x26;token=060a0d9e-6bfa-4d85-b653-000c05cc95b4" alt="Zephyr data source form in Oobeya"><figcaption><p>The Zephyr data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Next Steps**

* [Test Analytics: creating a new test analysis](https://docs.oobeya.io/test-analytics/yeni-test-analizi-olusturma)
* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
