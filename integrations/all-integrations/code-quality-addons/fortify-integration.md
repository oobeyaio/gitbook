---
description: Connect OpenText Fortify to Oobeya to track application security findings.
---

# Fortify Integration

Fortify is an application security testing suite best known for static code analysis (SAST). Oobeya reads the security findings stored on your Fortify server. You select a team's Fortify project versions in the Team Scorecard configuration, and the findings appear in the team's Fortify widget, next to the team's delivery and quality data. Fortify is in the **Code Quality & Security** category of the Integrations page.

### 1. Create a Fortify token

On your Fortify server (Software Security Center), create a token for a user that can read the application versions you want to analyze. Copy the token; you need it in the next step.

{% hint style="info" %}
Use a dedicated service account with read-only access, so the connection is not tied to a person.
{% endhint %}

### 2. Connect Fortify in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **Code Quality & Security** section, click the **Fortify** card. If Fortify already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Fortify v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                          |
| -------------------- | ------------------------------------------------------------------------------ |
| **Data Source Name** | A name you choose for this connection, for example _Fortify SSC_.              |
| **Server URL**       | The URL of your Fortify server, for example `https://fortify.example.com/ssc`. |
| **Token**            | The token from step 1.                                                         |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FHSyG73uqXwlISPxYxrcB%2Fform-fortify.png?alt=media&#x26;token=a031fee2-0bd7-4900-9ca0-90a0db1b6f26" alt="Fortify data source form in Oobeya"><figcaption><p>The Fortify data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Next Steps**

* [Network Access Requirements](https://docs.oobeya.io/integrations/network-access-requirements)
* [Team Scorecard](https://docs.oobeya.io/team-health/team-scorecards)
