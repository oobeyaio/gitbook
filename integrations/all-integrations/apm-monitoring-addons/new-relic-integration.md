---
description: Learn about New Relic & Oobeya Integration.
---

# New Relic Integration

### 1. **Create An API Key on New Relic**

1. Click the **"Profile"** button as in the figure.

![](https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FdUP3V0ghiIrJTbNR4lwH%2FPicture1.png?alt=media\&token=30db3217-4b8d-4652-8268-53ba5a02e6b8)

2\. Click the **"API Keys"** button.

![](https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FWkGVNsLmtis5Xo4PPTrJ%2FPicture2.png?alt=media\&token=bd3a5e55-a0aa-497c-8059-8cc306074cc5)

3. Click the "Create a key" button.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FLNhZLuGBiwl4Q4oPViUS%2Fimage.png?alt=media&#x26;token=0900538d-ef9b-495c-8509-47ae9bcacf25" alt=""><figcaption></figcaption></figure>

4. Select the account and click the "Create a key" button to create the API key.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FBeguRC0IZmSGzjUKAeB3%2Fimage.png?alt=media&#x26;token=781b4d3a-8fd7-4414-bc36-1400337b3a8a" alt="" width="375"><figcaption></figcaption></figure>

### 2. Creating A Query Key on New Relic Insights

1. Click the **"Profile"** button as in the figure.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FzkJlbh4nQ7FpKwUgD0S4%2FPicture5.png?alt=media&#x26;token=cfadaa9a-1a64-4ab7-8640-3681aba8a5dc" alt=""><figcaption></figcaption></figure>

2\. Click the "**API Keys**" button.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FiPQgFGkwL5eW9IsTkv26%2FPicture6.png?alt=media&#x26;token=fec91475-976e-4af8-9b10-c5a6ffaf5dd7" alt=""><figcaption></figcaption></figure>

3\. Click on the **"Insights Query Keys”** button.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FkUNIjDCakexwELVH18yo%2FInsight%20Query%20Keys%20pic.png?alt=media&#x26;token=fbeea54c-620a-4a7b-9919-686daea05064" alt=""><figcaption></figcaption></figure>

4. Click the add icon next to the **"Query Keys"** to add a query key.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FLqgM7vB2c6dadK5ScIwq%2Fimage.png?alt=media&#x26;token=e829b837-188c-41aa-a999-a809e74d7d2a" alt=""><figcaption></figcaption></figure>

5. You can use the created query key as shown below to add a data source in Oobeya.

### 3. Connect New Relic in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Monitoring/APM** section, click the **New Relic** card. If New Relic already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **NewRelic V2 (or NewRelic EU V2 for EU accounts)** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                           |
| -------------------- | --------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _New Relic_. |
| **Token**            | The API key from step 1.                                        |
| **Query Key**        | The query key from step 2.                                      |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FoUgSUFPCrzziYFrxzlIv%2Fform-new-relic.png?alt=media&#x26;token=45057268-3e57-4a55-b003-1025a7363304" alt="New Relic data source form in Oobeya"><figcaption><p>The New Relic data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### Ready to Connect

Now Oobeya is connected with your own New Relic account to track the real-time and average performance metrics.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
