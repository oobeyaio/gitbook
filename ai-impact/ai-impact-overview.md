---
description: >-
  See how AI coding assistants relate to engineering outcomes: coding
  efficiency, delivery, code quality, and testing, compared with the previous
  period.
icon: chart-line-up-down
---

# AI Impact Overview

**AI Impact** (in the **AI Hub** section of the left menu) shows the adoption and impact of AI coding assistants on your teams' code and delivery. It combines data from your AI coding assistant integrations ([Claude Code](https://docs.oobeya.io/ai-impact/claude-code-ai-impact), [GitHub Copilot](https://docs.oobeya.io/ai-impact/github-copilot-ai-impact), [Cursor](https://docs.oobeya.io/integrations/all-integrations/ai-coding-assistants/cursor-integration), and [Codex](https://docs.oobeya.io/integrations/all-integrations/ai-coding-assistants/codex-integration)) with the Git, delivery, quality, and test data Oobeya already has for the same teams.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F6P7nD3lEjsKT4Mixy0c6%2Fai-impact-overview.png?alt=media&#x26;token=e2538ac8-8aa1-4964-ac3f-c31915cf07e6" alt="AI Impact overview with coding efficiency, outcome metrics, and Outcome Signals"><figcaption><p>AI Impact opens with an overview of outcomes compared with the previous period.</p></figcaption></figure>

### Filters and tabs

* **Team** and **Type** (AI assistant) filters at the top.
* **Working Days** switch, **Daily** / **Weekly** / **Monthly** granularity, and the date range.
* Three tabs:
  * **AI Impact**: the overview described below.
  * **Metrics**: usage and acceptance metrics of the assistants.
  * **Cost & Credits**: AI spending; see [AI Cost & Credits](https://docs.oobeya.io/ai-impact/ai-cost-and-credits).

### AI Impact Overview

Since Oobeya 2.1, AI Impact opens with an overview that answers _"How is AI-assisted development related to engineering outcomes?"_

* **Coding Efficiency** and **AI Suggestions & Acceptance**: the headline value, its change compared with the previous period of the same length, and the AI acceptance rate over the same period, with a trend chart of coding efficiency and accepted AI lines.
* **Outcome metrics**: coding efficiency, PR time to merge, bug count, and lead time for changes, each compared with the previous period; plus the security, maintainability, and reliability scores, technical debt, and unit test coverage.
* **Outcome Signals**: how many engineering outcome metrics moved favorably, stayed stable, or worsened compared with the previous period.
* Detailed charts grouped under the **Development**, **Delivery**, **Code Quality**, and **Testing** tabs.

#### High vs. low AI adoption teams

When the selected teams fall on both sides of the acceptance-rate threshold, Outcome Signals splits them into **high** and **low AI adoption** groups and compares coding efficiency, lead time for changes, PR time to merge, and bug count between the groups.

{% hint style="warning" %}
The comparison shows trends that occur together, not cause and effect.
{% endhint %}

#### Risks & Insights

**Risks & Insights** groups positive and negative findings. The **Tool Usage**, **User Metrics**, and **AI Assistant Users** tables are paginated, so large organizations can browse them quickly.

### Keeping AI data up to date

Administrators can turn on **Automated Reanalysis** in **Administration** > **AI Impact** (**Insights & AI** section). Oobeya then periodically checks the connected AI coding assistants for updates and reanalyzes AI Impact data. One reanalyze period applies to all assistants; recommended periods are every hour for Claude Code and daily at 6:00 AM for GitHub Copilot, Cursor, and Codex. Times follow the server time zone.

### Related

* [AI Usage](https://docs.oobeya.io/ai-impact/ai-usage)
* [AI Cost & Credits](https://docs.oobeya.io/ai-impact/ai-cost-and-credits)
* [Measuring the Impact of AI Coding Assistants](https://docs.oobeya.io/use-cases/measuring-the-impact-of-ai-coding-assistants)
