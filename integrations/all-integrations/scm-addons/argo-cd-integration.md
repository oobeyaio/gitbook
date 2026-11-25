---
description: Connect Argo CD to Oobeya to bring deployment data into DORA metrics.
---

# Argo CD Integration

[Argo CD](https://argo-cd.readthedocs.io/) is a GitOps continuous delivery tool for Kubernetes. Oobeya reads Argo CD deployment data and uses it for DORA metrics such as deployment frequency and lead time for changes. On the Integrations page, Argo CD appears as **Argo CD Deploy** in the **CI/CD** category.

### 1. Create an Argo CD API token

Oobeya connects to the Argo CD API with a token of an Argo CD account.

1. Use a local Argo CD account that has the `apiKey` capability, ideally a dedicated account with a read-only role.
2.  Generate a token for that account, either in the Argo CD UI under **Settings** > **Accounts**, or with the CLI:

    ```bash
    argocd account generate-token --account <account-name>
    ```
3. Copy the token. You need it in the next step.

### 2. Connect Argo CD in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **CI/CD** section, click the **Argo CD Deploy** card. If Argo CD already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **ArgoCD v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                      |
| -------------------- | -------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Argo CD - Production_. |
| **Server URL**       | The URL of your Argo CD server, for example `https://argocd.example.com`.  |
| **Token**            | The API token from step 1.                                                 |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F1ds2dpwgGQBtbYcEKMvi%2Fform-argo-cd.png?alt=media&#x26;token=68faba56-2c9d-416a-afe5-e335d05b58eb" alt="Argo CD data source form in Oobeya"><figcaption><p>The Argo CD data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Deployment Analytics (DORA Metrics)](https://docs.oobeya.io/gitwiser-repo-analytics/deployment-analytics-dora-metrics)
