---
description: >-
  Configuration guide for Claude Code in the AI Coding Assistant Impact module:
  Oobeya Collector, ingest token, data source setup, and rolling out the Claude
  Code settings to your developers.
---

# Claude Code - AI Impact

The **AI Coding Assistant Impact** module measures how your developers use [**Claude Code**](https://code.claude.com/docs), Anthropic's agentic coding tool, side by side with GitHub Copilot, Cursor and Codex. Claude Code reports its usage through **OpenTelemetry**: Claude Code on each developer's machine sends usage metrics and events to the **Oobeya Collector**, and Oobeya turns them into adoption, activity, model, tool and cost insights from the **organization level** down to the **user level**.

The integration works with every way of running Claude Code:

* **Claude Console** (API billing)
* **Claude Team** and **Claude Enterprise** plans
* **Amazon Bedrock, Google Vertex AI, Microsoft Foundry** or an LLM gateway (requires one extra setting, see [step 4](claude-code-ai-impact.md#claude-code-on-amazon-bedrock-google-vertex-ai-microsoft-foundry-or-an-llm-gateway))

***

### How It Works

```
Claude Code (developer machines) ──HTTPS / OpenTelemetry──▶ Oobeya Collector ──▶ Oobeya AI Impact
```

* Claude Code sends its usage totals every **5 minutes** and its events (prompts, model requests, tool runs) every **minute**.
* The **Oobeya Collector** checks the ingest token of every request and queues the data. It is the only Oobeya address your developers' machines need to reach.
* Oobeya stores the data as it arrives and calculates the AI Impact metrics on the [reanalysis schedule](claude-code-ai-impact.md#id-6.-set-the-analysis-schedule). Every analysis recalculates the last 7 days, so data that arrives late is still counted.
* Optionally, an **Anthropic API key** on the data source adds the list of licensed members and, on Claude Enterprise, the billed cost.

{% hint style="info" %}
Oobeya does not receive or store the content of prompts, responses, code or files. See [Collected Data and Privacy](claude-code-ai-impact.md#id-9.-collected-data-and-privacy).
{% endhint %}

***

### 1. Prerequisites

* **Oobeya Collector** is installed and reachable from your developers' machines over HTTPS.
  * On-premise installations: your DevOps team installs it with the [Oobeya Collector Installation (Docker)](/broken/pages/23785dc8b8dc6ef478c2619a247b1ab217db0078) guide and gives you the collector address (for example `https://oobeya-collector.mycompany.com`).
  * If the Oobeya team hosts your installation, ask them for your collector address.
* You have admin rights in Oobeya (Integrations, Data Sources and Api Key pages).
* For an organization-wide rollout, someone who can change the Claude Code **managed settings**: a Claude organization owner (Team and Enterprise plans) or your device management (MDM) team.
* Network access:

| From                                   | To                                                       | Port | Required                               |
| -------------------------------------- | -------------------------------------------------------- | ---- | -------------------------------------- |
| Developer machines running Claude Code | Collector address, e.g. `oobeya-collector.mycompany.com` | 443  | Yes                                    |
| Oobeya server                          | `api.anthropic.com`                                      | 443  | Only when you add an Anthropic API key |

***

### 2. Enable the Claude Code Integration

1. Navigate to **Integrations → Coding Assistant** in Oobeya.
2. Select **Claude Code** and click **Install**.

***

### 3. Configure the Data Source

Go to **Data Sources** and add a **Data Source for Claude Code**:

* **Data Source Name:** a descriptive name (e.g. _Claude Code - Engineering_).
* **Version:** _OpenTelemetry_.
* **Ingest token:** generate a new token in the form, or paste one you created on the Api Key page. See [Ingest Token](claude-code-ai-impact.md#ingest-token) below.
* **Anthropic API key** _(optional)_: adds information that OpenTelemetry does not carry. See [Anthropic API Key](claude-code-ai-impact.md#anthropic-api-key) below.

Click **Test Connection**, then save the data source.

#### Ingest Token

Claude Code authenticates to the Oobeya Collector with an **ingest token**. You can get one in two ways:

* **In the data source form (simplest):** generate the token while you add the data source. Oobeya creates it with the **Ingest (Collector)** scope, and it also appears on the **Admin → Api Key** page, where you can revoke it later.
* **On the Api Key page:**
  1. Go to **Admin → Api Key**.
  2. Under **Generate Tokens**, select the scope **Ingest (Collector)**.
  3. Enter a **Token name** that you will recognize later (e.g. _Claude Code - Engineering_) and click **Generate Ingest (Collector) token**.
  4. Copy the token. It is shown only once, right after it is created.
  5. Paste it into the **Ingest token** field of the data source.

{% hint style="info" %}
An **Ingest (Collector)** token only works for sending data to the Oobeya Collector and is not accepted by the Oobeya public API. A **Full API** token is not accepted by the collector. Each Claude Code data source needs its own ingest token, and a token can be added to only one data source.
{% endhint %}

{% hint style="warning" %}
The ingest token is distributed to every developer's machine as part of the Claude Code settings, so anyone who has it can send data to this data source. Treat it as a shared secret. If it leaks, revoke it on the **Api Key** page, create a new one, update the data source and distribute the new settings.
{% endhint %}

#### Anthropic API Key

The Anthropic API key is optional. Claude Code data flows without it; the key adds what OpenTelemetry does not carry.

| Your Claude organization         | Key to use                                                                     | Where to create it                                          | What Oobeya adds                                                     |
| -------------------------------- | ------------------------------------------------------------------------------ | ----------------------------------------------------------- | -------------------------------------------------------------------- |
| Claude Console                   | Admin key (`sk-ant-admin01-…`)                                                 | Claude Console → Settings → Admin keys (organization admin) | Member list, so licensed developers with no activity are visible     |
| Claude Enterprise                | API key (`sk-ant-api01-…`) with the `read:members` and `read:analytics` scopes | claude.ai → Organization settings → API (primary owner)     | Member list, seat counts, and the **billed** cost per user and model |
| Team plan, third-party platforms | —                                                                              | Not available                                               | —                                                                    |

{% hint style="info" %}
Scopes cannot be added to an existing Claude Enterprise key. If the test reports a missing scope, create a new key with both scopes.
{% endhint %}

***

### 4. Roll Out the Claude Code Settings

Claude Code starts sending data once it is configured with the collector address and the ingest token. Oobeya prepares this configuration for you:

1. Open the Claude Code data source and click **Data status and Claude Code settings**.
2. In the **Claude Code settings** section, click **Show token** and copy the JSON.

The JSON looks like this:

{% code title="Claude Code settings" %}
```json
{
  "env": {
    "CLAUDE_CODE_ENABLE_TELEMETRY": "1",
    "OTEL_METRICS_EXPORTER": "otlp",
    "OTEL_LOGS_EXPORTER": "otlp",
    "OTEL_EXPORTER_OTLP_PROTOCOL": "http/protobuf",
    "OTEL_EXPORTER_OTLP_COMPRESSION": "gzip",
    "OTEL_EXPORTER_OTLP_ENDPOINT": "https://oobeya-collector.mycompany.com/claude",
    "OTEL_EXPORTER_OTLP_HEADERS": "Oobeya-API-Key=<INGEST_TOKEN>",
    "OTEL_EXPORTER_OTLP_METRICS_TEMPORALITY_PREFERENCE": "cumulative",
    "OTEL_METRIC_EXPORT_INTERVAL": "300000",
    "OTEL_LOGS_EXPORT_INTERVAL": "60000"
  }
}
```
{% endcode %}

{% hint style="warning" %}
Use the JSON as Oobeya generates it. In particular, keep `cumulative` temporality: usage totals then recover by themselves after a network interruption, which `delta` cannot do.

If the endpoint shows `https://<collector-address>`, the collector address is not configured in your installation. Replace it with the address your DevOps team gives you.
{% endhint %}

Then distribute the settings with one of these options. Claude Code applies them the next time it starts, so ask your developers to **restart Claude Code**.

| Option                                          | Plans                      | How                                                                                                                                                                                                                                                                        |
| ----------------------------------------------- | -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Managed settings in Claude.ai** (recommended) | Team, Enterprise           | Paste the JSON into the [Claude Code managed settings](https://claude.ai/admin-settings/claude-code) of your Claude organization. It applies to everyone signed in to the organization.                                                                                    |
| **Managed settings via MDM**                    | All                        | Deploy the JSON as the `managed-settings.json` file with your device management tool, e.g. `/Library/Application Support/ClaudeCode/managed-settings.json` on macOS. See [Claude Code settings](https://code.claude.com/docs/en/settings) for the Linux and Windows paths. |
| **User settings**                               | All (pilots, single users) | Add the `env` entries to `~/.claude/settings.json` on macOS and Linux, or `%USERPROFILE%\.claude\settings.json` on Windows.                                                                                                                                                |

Managed settings take precedence over every other settings file, so developers cannot turn them off locally.

#### Claude Code on Amazon Bedrock, Google Vertex AI, Microsoft Foundry or an LLM gateway

Without a Claude account sign-in, Claude Code does not report the developer's e-mail. Add it for each developer, for example through a per-user MDM profile or the user settings:

```json
"OTEL_RESOURCE_ATTRIBUTES": "user.email=developer@mycompany.com"
```

***

### 5. Verify the Data Flow

Ask a developer to restart Claude Code and run a prompt. Events arrive within about a minute, usage totals within five minutes.

Open the data source and click **Data status and Claude Code settings**. The **Data status** section updates as soon as data arrives; click **Refresh** to reload it.

| Status                           | Meaning                                                                                      |
| -------------------------------- | -------------------------------------------------------------------------------------------- |
| **No data received yet**         | No developer has sent data with this data source's token. Check the rollout and the network. |
| **Receiving data**               | Data arrived in the last 24 hours.                                                           |
| **No data in the last 24 hours** | Data arrived before, but not in the last 24 hours.                                           |

The section also shows the **Last received** time, the number of **Developers sending data in the last 24 hours**, the **First data date**, the **Accepted requests** and the **Claude organization IDs** the data came from. If the collector or its queue has a problem, a message explains it (see [Troubleshooting](claude-code-ai-impact.md#id-11.-troubleshooting)).

{% hint style="info" %}
The Data status shows data the moment Oobeya receives it. The AI Impact dashboards show it after the next analysis.
{% endhint %}

***

### 6. Set the Analysis Schedule

Oobeya calculates the AI Impact metrics from the received data on a schedule.

1. Go to **Admin → AI Assistant → Automated Reanalysis**.
2. Choose a **Reanalyze Period**: _Daily at 6:00 AM_, _Every hour_, _Every 6 hours_ or _Every 12 hours_. The setting applies to all AI assistants and follows the server time zone.
3. Click **Save**.

For Claude Code we recommend **Every hour**, because its data arrives continuously. To calculate immediately, click **Reanalyze** in the AI Impact header.

Every analysis recalculates the last 7 days. Reanalysis never deletes the Claude Code data Oobeya has received; it only recalculates the metrics from it.

***

### 7. Match Claude Code Users to Developers

Claude Code reports the **e-mail of the Claude account** the developer is signed in with. Oobeya matches this e-mail to its developer accounts, and team-level metrics follow each developer's team membership.

If a developer's Claude e-mail differs from the e-mail Oobeya knows, merge the accounts:

* [Merging Contributor Accounts](../gitwiser-repo-analytics/settings-for-git-analytics/merging-contributor-accounts.md)
* [Adding A Related Account Information To Oobeya Profile](../scorecards/adding-a-related-account-information-to-oobeya-profile.md)

***

### 8. Viewing Results

Go to **AI Impact** and select your Claude Code data source. Claude Code data appears in the **AI Impact**, **Metrics** and **Cost & Credits** tabs, together with your other AI coding assistants.

**What Claude Code reports**

* **Adoption:** active users, sessions and active time per user
* **Activity:** prompts, model requests and errors, commits and pull requests created with Claude Code
* **Code:** lines of code added and removed, accepted and rejected code edits, languages and editors (terminal or IDE)
* **Models:** requests, errors and input, output and cache tokens per model
* **Tools:** tool runs (Bash, Edit, MCP tools, …), success rate, and the developers' accept and reject decisions
* **Cost:** usage cost per user and model

**Claude Code widgets**

* **Activity Summary** – Sessions, prompts, model requests, active time, commits, pull requests and cost.
* **Model Usage** – Requests, errors and tokens per model, sorted by total tokens.
* **Tool Usage** – Tools Claude Code ran, their success rate, and how often developers accepted or rejected them.

{% hint style="info" %}
Claude Code does not report suggested lines, chat usage, lines per language or AI credits. Oobeya shows these metrics as empty, not as zero, and the widgets explain which assistants a combined figure includes.
{% endhint %}

#### Cost

On the **Cost & Credits** tab, Claude Code cost is **estimated from Claude Code list prices**. When a Claude Enterprise API key is set on the data source, the net amount is the **billed** amount and the difference is shown as discount. See [AI Cost & Credits](ai-cost-and-credits.md).

***

### 9. Collected Data and Privacy

**Stored per developer, day and session**

* Usage totals: sessions, active time, lines of code, commits, pull requests, tokens, cost
* Event counts: prompts, model requests, model errors (with the HTTP status code), tool runs and tool permission decisions
* Their labels: model, tool name, decision, success, language, editor
* The developer's e-mail, the Claude organization ID and the editor type

**Not stored**

* Prompt text, model responses, code, file paths, tool inputs and outputs, error messages

Claude Code does not send prompt text unless `OTEL_LOG_USER_PROMPTS` is enabled; Oobeya does not need it, so leave it unset.

**Retention.** Claude Code cannot send past data again, so Oobeya keeps the received data until the data source is deleted. Deleting the data source deletes this data permanently. To stop the token as well, revoke it on the **Api Key** page.

***

### 10. Limitations

* **No historical backfill.** Data starts when developers restart Claude Code with the settings.
* **Inactive users.** OpenTelemetry carries only usage, so licensed developers who do not use Claude Code are visible only when an Anthropic API key is set on the data source.
* **Unreachable collector.** Claude Code does not keep data it could not send, for example while a developer is outside the VPN. Usage totals catch up with the next successful send as long as the Claude Code session stays open; prompt and tool events from that period are lost. Keep the collector reachable from every network your developers work from.
* **Personal accounts.** With managed settings in Claude.ai, data is sent only while the developer is signed in to your Claude organization. With MDM or user settings, the settings apply to the machine, so usage from a personal Claude login on the same machine is sent too. The **Claude organization IDs** in the Data status show where the data comes from.
* **One OpenTelemetry endpoint.** Claude Code sends its telemetry to a single endpoint. If you already send Claude Code telemetry to another tool, contact the Oobeya team.

***

### 11. Troubleshooting

**Test Connection fails**

| Message                                                                               | What to do                                                                                                            |
| ------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| The token was not found. Create a token with the Ingest scope on the API Tokens page. | Check that the whole token was copied, or generate a new one ([Ingest Token](claude-code-ai-impact.md#ingest-token)). |
| The token has been revoked. / The token has expired.                                  | Generate a new ingest token.                                                                                          |
| The token does not have the Ingest scope.                                             | Full API tokens do not work here. Use an Ingest (Collector) token.                                                    |
| This token is already used by another Claude data source.                             | Each data source needs its own ingest token.                                                                          |
| The token could not be verified because of a system configuration problem.            | Contact your system administrator; the Oobeya services cannot reach each other.                                       |
| Anthropic rejected the API key.                                                       | Use a Claude Console admin key (`sk-ant-admin01-…`) or a Claude Enterprise key (`sk-ant-api01-…`).                    |
| The Claude Enterprise key has neither the read:members nor the read:analytics scope.  | Create a new key with both scopes.                                                                                    |
| The Anthropic API (api.anthropic.com) is not reachable from the addons service.       | Allow outbound HTTPS from the Oobeya server to `api.anthropic.com`.                                                   |

**Data status shows "No data received yet"**

* Make sure developers restarted Claude Code after the settings were distributed.
* Check that the endpoint in the settings is your collector address and not `https://<collector-address>`.
* From a developer machine, check that the collector is reachable. A `401` response means the collector is reachable and only the token was missing from this test request:

```bash
curl -i -X POST https://oobeya-collector.mycompany.com/claude/v1/metrics -H "Content-Type: application/x-protobuf"
```

**Data status shows a collector message**

| Message                                                                         | Meaning                                                                                    |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| The collector is not set up in this installation.                               | The Oobeya Collector is not installed or not configured. Contact your DevOps team.         |
| The collector cannot be reached.                                                | Oobeya cannot reach the collector's management port.                                       |
| The collector cannot reach its queue (RabbitMQ). No data is accepted right now. | The collector rejects data until RabbitMQ is reachable again.                              |
| The disk or memory of the collector queue is full. No data is accepted.         | RabbitMQ has blocked publishing; free disk or memory on the RabbitMQ host.                 |
| The collector cannot update its token list.                                     | The collector cannot reach Oobeya; it keeps working with the last token list it received.  |
| The collector cannot update its token list and accepts no data until it does.   | The collector has never received a token list. Check its connection to the Oobeya gateway. |
| Oobeya is not reading the queue, so waiting data is not processed.              | Data waits safely in the queue; check the Oobeya addons service.                           |
| _n_ messages are waiting to be processed. No data is lost.                      | Data is queued and will be processed.                                                      |
| _n_ messages could not be processed and were set aside (kept for 7 days).       | Contact the Oobeya team; these messages can be processed again once the cause is fixed.    |

**Collector logs**

Go to **Admin → General Settings → System Logs**, and under **Download Service Logs** select **Oobeya Collector**. It is listed while the Claude Code integration is installed.

**Data status shows data, but the dashboards are empty**

* Wait for the next analysis, or click **Reanalyze** in the AI Impact header.
* Check that the developers' Claude e-mails match their Oobeya accounts ([step 7](claude-code-ai-impact.md#id-7.-match-claude-code-users-to-developers)).

***

### FAQ

<details>

<summary>Which Claude plans are supported?</summary>

All of them: Claude Console, Team, Enterprise, and Claude Code running on Amazon Bedrock, Google Vertex AI, Microsoft Foundry or an LLM gateway.

</details>

<details>

<summary>Can I connect more than one Claude organization?</summary>

Yes. One data source can receive data from several organizations; the Data status lists their organization IDs. If you want to view them separately, create one data source and one ingest token per organization and distribute each organization's own settings.

</details>

<details>

<summary>How long until the data is visible?</summary>

The Data status updates within a minute. The dashboards update after the next analysis; with the recommended hourly schedule, within an hour.

</details>

<details>

<summary>Does Oobeya see our prompts or code?</summary>

No. Oobeya stores counts and totals only. See [Collected Data and Privacy](claude-code-ai-impact.md#id-9.-collected-data-and-privacy).

</details>

<details>

<summary>What happens to the data while Oobeya is being upgraded?</summary>

On installations that follow the [Oobeya Collector Installation (Docker)](/broken/pages/23785dc8b8dc6ef478c2619a247b1ab217db0078) guide, the collector and its queue keep running during an Oobeya upgrade, and the data is processed once Oobeya is back.

</details>

#### Learn more about the module:

{% content-ref url="ai-cost-and-credits.md" %}
[ai-cost-and-credits.md](ai-cost-and-credits.md)
{% endcontent-ref %}

{% content-ref url="../use-cases/measuring-the-impact-of-ai-coding-assistants.md" %}
[measuring-the-impact-of-ai-coding-assistants.md](../use-cases/measuring-the-impact-of-ai-coding-assistants.md)
{% endcontent-ref %}

## **Next Steps** :dart:

* [Oobeya Collector Installation (Docker)](/broken/pages/23785dc8b8dc6ef478c2619a247b1ab217db0078)
* [Network Access Requirements](../integrations/network-access-requirements.md)
