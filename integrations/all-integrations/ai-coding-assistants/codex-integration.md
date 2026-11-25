---
description: >-
  Connect OpenAI Codex (ChatGPT Enterprise) to Oobeya for AI Impact and AI cost
  tracking.
---

# Codex Integration

Oobeya connects to your organization's **ChatGPT Enterprise** workspace and reads **OpenAI Codex** activity. Codex usage appears per team and over time in **AI Impact**, and Codex spending appears on the **Cost & Credits** tab, together with your other AI coding assistants. Codex is in the **AI Coding Assistants** category of the Integrations page.

{% hint style="info" %}
Codex does not report suggestions, acceptances, suggested lines, or a language breakdown. When Codex is selected together with other assistants, those metrics come from the other assistants.
{% endhint %}

### 1. Create an admin key in ChatGPT

A workspace administrator of the ChatGPT Enterprise workspace:

1. Opens the **ChatGPT Admin Console** > **Credentials** > **Admin keys** and creates an admin key.
2. Copies the key and the **workspace ID** (a UUID).

### 2. Connect Codex in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **AI Coding Assistants** section, click the **Codex** card. If Codex already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Codex v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                     |
| -------------------- | ------------------------------------------------------------------------- |
| **Data Source Name** | A name you choose for this connection, for example _Codex - Engineering_. |
| **Admin key**        | The admin key from step 1.                                                |
| **Workspace ID**     | The ChatGPT workspace ID. Oobeya checks that it is a valid UUID.          |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FSP7uDF3lY4JvRxX7FPXQ%2Fform-codex.png?alt=media&#x26;token=7a7a25ce-e1b9-4a2b-811d-42f789997ebd" alt="Codex data source form in Oobeya"><figcaption><p>The Codex data source form on the Integrations page.</p></figcaption></figure>

Usage and cost are refreshed on a schedule after the data source is added.

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Next Steps**

* [AI Cost & Credits](https://docs.oobeya.io/ai-impact/ai-cost-and-credits)
* [Measuring the Impact of AI Coding Assistants](https://docs.oobeya.io/use-cases/measuring-the-impact-of-ai-coding-assistants)
