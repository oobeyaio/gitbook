---
description: >-
  Connect Cursor to Oobeya to see Cursor adoption and usage per team in AI
  Impact.
---

# Cursor Integration

[Cursor](https://cursor.com) is an AI code editor. Oobeya imports Cursor usage data and shows it per team in **AI Impact**, together with GitHub Copilot, Claude Code, and Codex, next to review time, rework, and quality for the same teams. Cursor is in the **AI Coding Assistants** category of the Integrations page.

### 1. Create a Cursor API key

In the Cursor dashboard of your team, an administrator creates an **Admin API key**. Copy the key; you need it in the next step.

### 2. Connect Cursor in Oobeya

1. Sign in to Oobeya with an **Administrator** account and select **Integrations** in the **Administration** section of the left menu.
2. In the **AI Coding Assistants** section, click the **Cursor** card. If Cursor already has data sources, click **+ New Data Source** in the window that opens.
3. Select the version **Cursor v1** and fill in the form (see the fields below).
4. Click **Test Connection** to verify the connection, then click **Add**.

| Field                | Value                                                                  |
| -------------------- | ---------------------------------------------------------------------- |
| **Data Source Name** | A unique name for this connection, for example _Cursor - Engineering_. |
| **Token**            | The Cursor API key from step 1.                                        |

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FpySZns09JCcF5Zwfne6z%2Fform-cursor.png?alt=media&#x26;token=ee9ae970-d0be-4cd4-b372-43e712cbc257" alt="Cursor data source form in Oobeya"><figcaption><p>The Cursor data source form on the Integrations page.</p></figcaption></figure>

{% hint style="info" %}
Since Oobeya 2.1 there is no separate install step: the integration is enabled when you save its first data source. See [Adding New Integration](https://docs.oobeya.io/integrations/adding-new-integration).
{% endhint %}

### **Next Steps**

* [Measuring the Impact of AI Coding Assistants](https://docs.oobeya.io/use-cases/measuring-the-impact-of-ai-coding-assistants)
