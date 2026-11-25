---
description: Learn about Bitbucket Cloud & Oobeya integration.
icon: bitbucket
---

# Bitbucket Cloud Integration

### 1. **Create an Atlassian API token**

1. Navigate to [Atlassian Account – Security → API tokens](https://id.atlassian.com/manage-profile/security/api-tokens).
2. Click **Create API token with scopes**.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fh524BlARiZzZyGDnDJl7%2Fimage.png?alt=media&#x26;token=a82214e4-6212-4fe9-a397-4740cd218de3" alt=""><figcaption></figcaption></figure>

3. Name your token and choose an expiration date.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FBpqZbCdKsrmw3d7BGVpY%2Fimage.png?alt=media&#x26;token=6778f45a-b488-458b-b133-dfec6697c9de" alt=""><figcaption></figcaption></figure>

4. Select Bitbucket from the app list.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FseoUs61pNEUTvc8L2g4T%2Fimage.png?alt=media&#x26;token=4498ea9b-1563-484c-a32f-645fd3d15025" alt=""><figcaption></figcaption></figure>

5. Select the scopes as shown below:<br>

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FZw5lo2mvHEu6kpIvBf1z%2Fimage.png?alt=media&#x26;token=bf6dbe96-78b6-448c-81ec-c755d97d81ec" alt=""><figcaption></figcaption></figure>

6. Review the token and complete the token creation process.

### 2. Connect Bitbucket Cloud in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Source Code Management** section, click the **Bitbucket Cloud** card. If Bitbucket Cloud already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **BitbucketCloud 2.0** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                  |
| -------------------- | ---------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Bitbucket Cloud_.  |
| **Username**         | The e-mail address of your Atlassian account.                          |
| **App Password**     | The API token from step 1. The field is still labelled _App Password_. |
| **Workspace**        | Your Bitbucket Cloud workspace ID.                                     |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FtU2T0pxZDtKI0hWrl8Q1%2Fform-bitbucket-cloud.png?alt=media&#x26;token=903c1d0b-6f4c-414a-829f-e1f8e0876db0" alt="Bitbucket Cloud data source form in Oobeya"><figcaption><p>The Bitbucket Cloud data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Ready to Connect**

Now Oobeya is connected with your own Bitbucket Cloud account to get the real-time statistics of your code repositories to track each development activity.

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Create a new Gitwiser Analysis](https://docs.oobeya.io/gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics)
