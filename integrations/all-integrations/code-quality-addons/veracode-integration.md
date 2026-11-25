---
description: Learn about Veracode & Oobeya integration.
---

# Veracode Integration

{% hint style="info" %}
[Veracode](https://www.veracode.com/) is an application security platform that enables organizations to assess and manage the security of their software applications at scale. With Veracode, businesses can identify and remediate security flaws in their code and applications, ensuring their software is secure and compliant with industry standards.

[Oobeya](https://oobeya.io) and Veracode provide organizations with visibility into the security of their applications and code repositories. With detailed reports, development teams can track their progress over time and gain insights into potential vulnerabilities and areas for improvement.
{% endhint %}

### 1. **Generate Veracode API Credential**

1\. Navigate to **API Credentials** and generate a new API Credential in Veracode to connect [Oobeya](https://oobeya.io/).

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FWV87NB3Qnnx5p93isc4J%2Fimage.png?alt=media&#x26;token=490ab21a-bc32-4d91-b9a5-89d56e4c377d" alt=""><figcaption><p>Veracode API Credentials</p></figcaption></figure>

### 2. Connect Veracode in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Code Quality & Security** section, click the **Veracode** card. If Veracode already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Veracode v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                          |
| -------------------- | -------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Veracode_. |
| **Server URL**       | `https://api.veracode.com`                                     |
| **Access Key**       | The API ID from step 1.                                        |
| **Secret Key**       | The API secret key from step 1.                                |
| **Set as default**   | Optional. Makes this the default Veracode data source.         |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FSRkiZYHtxEG5iLiLCCF9%2Fform-veracode.png?alt=media&#x26;token=3d1cd612-7793-45ac-9b41-b6b8b3818bf9" alt="Veracode data source form in Oobeya"><figcaption><p>The Veracode data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Oobeya is now connected with your Veracode account to provide real-time security analysis for your code. Gain deeper insights into your application security and vulnerabilities.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
