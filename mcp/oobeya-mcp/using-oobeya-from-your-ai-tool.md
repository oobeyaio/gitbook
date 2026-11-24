---
description: >-
  Connect your AI tool to Oobeya and ask about your engineering data in plain
  language: team reports, pull requests, DORA metrics, sprints and more.
---

# Using Oobeya from Your AI Tool

The Oobeya MCP server gives your AI tool direct access to Oobeya through the Model Context Protocol (MCP). You ask a question in your own words, the tool reads the answer from Oobeya, and every number comes from the same data you see in the Oobeya UI. The tool works with your Oobeya account and your permissions.

{% hint style="info" %}
Available from **Oobeya 2.1.0**. Your administrator sets it up once; see [Oobeya MCP Server: Setup for Administrators](setup-for-administrators.md).
{% endhint %}

## What You Can Do

* Read team reports: DORA metrics, pull requests, code and work types, code quality, bugs, sprints and boards.
* Look at one developer's work: reports, commits and pull requests.
* Follow a work item to its commits, pull requests and deployments.
* Compare several teams over the same period.
* Ask how a metric is calculated and why a number looks the way it does.
* If you are an administrator or a team lead: connect tools, start analyses, and create or maintain teams and developers.

## 1. Before You Start

* You have an Oobeya account.
* Your Oobeya administrator has enabled the MCP server. If it is enabled, your profile shows the **AI access (MCP)** tab.
* One of the supported AI tools is installed on your computer.
* Your computer can reach Oobeya, for example from the office network or over VPN.

Supported AI tools:

| AI tool          | How you add Oobeya                                                |
| ---------------- | ----------------------------------------------------------------- |
| Claude Code      | One-click open (terminal or Claude Desktop), or terminal commands |
| Codex            | One-click open (Codex app), or terminal commands                  |
| Cursor           | One-click install                                                 |
| VS Code          | One-click install                                                 |
| Devin (Windsurf) | One-click install, or terminal commands                           |
| GitHub Copilot   | Terminal commands                                                 |
| Gemini CLI       | Terminal commands                                                 |
| Grok Build       | Terminal commands                                                 |
| OpenCode         | Terminal commands                                                 |

## 2. Connect Your AI Tool

1. In Oobeya, open **Profile → AI access (MCP)**. You can also use the **Connect your AI tool (MCP)** card on the home page.
2. Under **Connect your AI tool**, select your tool. Oobeya shows the steps and the commands with your MCP address already filled in.
3. Follow the steps for your tool below.

Your MCP address is your Oobeya address followed by `/mcp`, for example `https://oobeya.mycompany.com/mcp`.

{% hint style="info" %}
After adding the server, close and reopen your AI tool or start a new session so that Oobeya becomes active.
{% endhint %}

### Claude Code

Click **Open in terminal** or **Open in Claude Desktop** on the Oobeya screen. Claude Code opens with the setup request typed in; press Enter and allow the command it runs. If nothing opens, run `claude` in a terminal once and send any message, or use the commands below.

1. Add the Oobeya server. It becomes available in all your folders:

```bash
claude mcp add --transport http -s user oobeya https://<your-oobeya-address>/mcp
```

2. Run the sign-in command. The Oobeya sign-in screen opens in your browser:

```bash
claude mcp login oobeya
```

3. Allow access on the Oobeya screen that opens.

{% hint style="info" %}
You can also sign in from inside Claude Code: run `/mcp`, select `oobeya` and choose to authenticate.
{% endhint %}

### Codex

Click **Open in Codex app** on the Oobeya screen, press Enter and allow the command it runs. Codex CLI has no open link; use the commands instead:

```bash
codex mcp add oobeya --url https://<your-oobeya-address>/mcp
codex mcp login oobeya
```

Allow access on the Oobeya screen that opens.

### Cursor and VS Code

1. Click **Add to Cursor** or **Add to VS Code** on the Oobeya screen. The app opens and asks you to confirm.
2. When the app connects, the Oobeya sign-in screen opens in your browser. Allow access there.

{% hint style="info" %}
Every AI agent in VS Code (GitHub Copilot, Claude, Codex and others) uses the MCP servers added to VS Code, so adding Oobeya once is enough.
{% endhint %}

### Devin (Windsurf)

Click **Add to Devin** on the Oobeya screen and confirm, or use the terminal:

```bash
devin mcp add oobeya https://<your-oobeya-address>/mcp
devin mcp login oobeya
```

Allow access on the Oobeya screen that opens.

### GitHub Copilot

```bash
copilot mcp add --transport http oobeya https://<your-oobeya-address>/mcp
```

When Copilot connects, the Oobeya sign-in screen opens in your browser. Allow access there. The command adds Oobeya to the GitHub Copilot settings (`~/.copilot/mcp-config.json`), which Copilot CLI and the GitHub Copilot app both use.

### Gemini CLI, Grok Build and OpenCode

| AI tool    | Add the server                                                             | Sign in                                     |
| ---------- | -------------------------------------------------------------------------- | ------------------------------------------- |
| Gemini CLI | `gemini mcp add --transport http oobeya https://<your-oobeya-address>/mcp` | Start Gemini CLI and run `/mcp auth oobeya` |
| Grok Build | `grok mcp add --transport http oobeya https://<your-oobeya-address>/mcp`   | Opens automatically when Grok connects      |
| OpenCode   | `opencode mcp add oobeya --global --url https://<your-oobeya-address>/mcp` | `opencode mcp auth oobeya`                  |

Allow access on the Oobeya screen that opens.

## 3. Approve the Connection

The first time your AI tool connects, your browser opens the **Connect an application to Oobeya** screen. It shows the account you are signed in as, the Oobeya host and the application that asks for access.

* Click **Allow** to connect the tool.
* Click **Deny** if you did not start this connection yourself.

{% hint style="warning" %}
Only allow a connection that you started. The application will be able to read and change Oobeya data with your permissions.
{% endhint %}

## 4. Ask Questions

Ask in your own words and name the team, person or period you mean. When you give no period, Oobeya reports the last 90 days.

| Goal                                  | Example question                                                             |
| ------------------------------------- | ---------------------------------------------------------------------------- |
| Delivery performance                  | How did the Payments team do on DORA metrics in the last 90 days?            |
| Pull requests                         | Which pull requests of the Mobile team waited longest for review this month? |
| Sprints                               | How is the current sprint of the Checkout board going?                       |
| Code and work types                   | Show the work type breakdown of the Platform team and its members.           |
| One developer                         | Summarize my contributions in the last 30 days.                              |
| Work items                            | Which commits and pull requests belong to PAY-1234?                          |
| Team comparison                       | Compare the Web and Mobile teams on pull request metrics.                    |
| Understanding a number                | Why is our lead time for changes so high? Explain how it is calculated.      |
| Setup (administrators and team leads) | Add Jane Doe to the Backend team.                                            |

The Oobeya server also offers ready-made prompts for common tasks: a team report, sprint health, a team comparison, a developer profile and the onboarding of a new Oobeya installation. Your AI tool lists them with the prompts or slash commands of the Oobeya server.

{% hint style="info" %}
Every number in an answer comes from Oobeya. If an answer contains a figure without a period or a source, ask the tool which Oobeya report it used.
{% endhint %}

## 5. What You Can See and Change

Your AI tool has exactly the access you have in Oobeya.

| You are             | You can read                                 | You can change                                   |
| ------------------- | -------------------------------------------- | ------------------------------------------------ |
| Admin or Super User | Everything                                   | Everything                                       |
| Team lead           | Your teams and their sub-teams               | Those teams, their developers and their analyses |
| Team member         | The teams you belong to and your own profile | Nothing                                          |

Users with the company role Team Lead, Manager or Director can also add developers.

When you ask for something you are not allowed to do, the tool answers that it is forbidden and nothing is changed. Ask your Oobeya administrator for the access, as you would for the UI.

## 6. Good to Know

* **Changes need your approval.** Before a change, the tool tells you what it will do, and your AI tool asks you to approve the call. Deletions need your explicit yes.
* **Never type a password or token into the chat.** A task that needs a secret, such as connecting a new integration, gives you a link to the Oobeya screen where you enter it.
* **Large reports can take a moment.** For a very large team or a long period the tool may answer that Oobeya is still calculating the report. Ask again after about a minute. A sub-team or a shorter period answers faster.
* **Your prompts are not sent to Oobeya.** Oobeya receives only the requests your AI tool makes. The answers Oobeya returns are processed by your AI tool and its model provider.

## 7. Disconnect

1. In Oobeya, open **Profile → AI access (MCP)**.
2. Under **Connected apps**, find the tool and click **Revoke access**.

The tool loses access within a minute. To connect again, sign in from the tool as in step 2. You can also remove the server from the tool itself, for example with `claude mcp remove oobeya` in Claude Code.

## 8. Troubleshooting

| Symptom                                                       | What to do                                                                                    |
| ------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| The **AI access (MCP)** tab says the MCP server is turned off | Ask your Oobeya administrator to enable it                                                    |
| The tool cannot reach the MCP address                         | Check that your computer can open Oobeya in the browser; connect to the office network or VPN |
| The sign-in screen does not open                              | Run the sign-in command of your tool again, or sign in from inside the tool                   |
| The tool does not show Oobeya after you added it              | Close and reopen the tool, or start a new session                                             |
| The tool answers "forbidden"                                  | You do not have the Oobeya permission for that team or action                                 |
| A report is "still being calculated"                          | Ask again after about a minute, or ask for a sub-team or a shorter period                     |
| The tool asks you to sign in again                            | Your connection expired or was revoked; sign in again                                         |

## FAQ

**Do I need a separate account?** No. You sign in with your Oobeya account, with the same method you use for the Oobeya UI.

**Can my AI tool change data in Oobeya?** Only what you are allowed to change, and only after you approve the call in your AI tool.

**Can I connect more than one tool?** Yes. Each tool appears as its own entry under Connected apps and can be removed separately.

**Are the numbers the same as in the Oobeya UI?** Yes. The tool reads the same reports that the UI shows.

## Next Steps

* Start with a question about your own team, for example its pull request metrics in the last 90 days.
* Ask the tool to explain a metric you want to understand better.
