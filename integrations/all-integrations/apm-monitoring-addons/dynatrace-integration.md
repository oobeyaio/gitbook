# Dynatrace Integration

### 1. Generate a Dynatrace Access Token

1.  Click on the search box and search for “Access Tokens”.<br>

    <figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FigfFB8DzrLTsxYCElNFO%2Fimage.png?alt=media&#x26;token=bc4aeda2-03f3-43d9-b1b3-a13bf3e1aeba" alt=""><figcaption><p>Dynatrace Access Tokens</p></figcaption></figure>
2.  Click on the "**Generate new token**" button:<br>

    <figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FuZXuhXRpl9UQGJdlL1SO%2Fimage.png?alt=media&#x26;token=fea4ab92-48f7-4e74-8123-9dbd51494c1f" alt=""><figcaption></figcaption></figure>
3.  Select the required permission scopes.\
    **Required Scopes:** Read API token, Read entities, Read metrics\
    \
    The required **URL address** (https://\*\*\*\*\*\*\*.live.dynatrace.com) for Oobeya's data source form is in the second box below. You can copy it.\
    \
    Then, click on the "Generate token" button.<br>

    <figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FWzY06hqyvZRZNi59F3CB%2Fimage.png?alt=media&#x26;token=d635c751-da57-4f04-a653-529ef36e908b" alt=""><figcaption></figcaption></figure>

### 2. Connect Dynatrace in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Monitoring/APM** section, click the **Dynatrace** card. If Dynatrace already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Dynatrace API V2** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                           |
| -------------------- | --------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Dynatrace_. |
| **Server URL**       | Your Dynatrace environment URL.                                 |
| **Token**            | The access token from step 1.                                   |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F3FVtl4H7oESi32bygkkZ%2Fform-dynatrace.png?alt=media&#x26;token=0f23e361-e211-4701-addb-5fea5472e54d" alt="Dynatrace data source form in Oobeya"><figcaption><p>The Dynatrace data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### Ready to Connect

Now Oobeya is connected to your **Dynatrace** account to diagnose, fix, and optimize the performance of the code.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
