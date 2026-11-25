---
description: >-
  Create and revoke tokens that let other tools call the Oobeya API or send data
  to the Oobeya Collector.
icon: gear-api
---

# API Keys

**Administration** > **API Keys** (**Platform** section) holds the tokens that let other tools call the Oobeya public API or send data to the Oobeya Collector.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FzQGxTqJbhs4OwXYV1gq2%2Fadmin-api-keys.png?alt=media&#x26;token=353add6f-aa75-447f-ae68-e0a0e3eee007" alt="Administration > API Keys page with the two token scopes and the token list"><figcaption><p>Administration > API Keys.</p></figcaption></figure>

### Token scopes

Every token has one scope:

| Scope                  | Accepted by                                                                                                                     | Typical use                                                                                                                                     |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Full API**           | Every endpoint of the [Oobeya public API](https://docs.oobeya.io/api-reference/oobeya-rest-api). Not accepted by the collector. | Scripts and integrations that read or send data through the API, for example deployments or custom metrics.                                     |
| **Ingest (Collector)** | Only the Oobeya Collector (for example, OpenTelemetry data). Not accepted by the public API.                                    | The [Claude Code integration](https://docs.oobeya.io/ai-impact/claude-code-ai-impact): each Claude Code data source needs its own ingest token. |

### Generating a token

1. Under **Generate Tokens**, click **Generate** next to the scope you need.
2. Enter a **Token name** that you will recognize later. Names must be unique.
3. Generate the token and copy it.

{% hint style="warning" %}
The token is shown only once, right after it is created. Copy it immediately and store it securely; it must not be shared.
{% endhint %}

{% hint style="info" %}
For Claude Code, you can also create the ingest token directly in the data source form: the **Generate** button next to the **Ingest token** field creates a token named after the data source.
{% endhint %}

### Revoking a token

The **Existing Tokens** list shows each token's **Name**, **Scope**, **Created User**, and **Created Date**. Click **Revoke** to disable a token. Tools that use it stop working until they get a new token.

### Related

* [Oobeya REST API](https://docs.oobeya.io/api-reference/oobeya-rest-api)
* [Claude Code - AI Impact](https://docs.oobeya.io/ai-impact/claude-code-ai-impact)
* [Administration Settings](https://docs.oobeya.io/administration/administration-settings)
