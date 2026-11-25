---
description: >-
  See how much of your new code is AI-assisted, which AI tools and models
  produced it, and how it relates to commit and line activity.
icon: coin-blank
---

# AI Usage

**AI Usage** (in the **AI Hub** section of the left menu) brings **AI code attribution**, **token usage**, and **SDLC metrics** together for end-to-end AI visibility. Where [AI Impact](https://docs.oobeya.io/ai-impact/ai-impact-overview) relates assistant adoption to engineering outcomes, AI Usage shows how much AI-written code actually reached commits.

{% hint style="info" %}
Line-level AI attribution comes from [Blamely AI](https://blamely.ai/docs/welcome) (backed by Oobeya), which records the AI or human origin of each line on developers' machines and stores it in Git notes. Without attribution data, the attribution widgets stay empty while commit and line activity are still shown.
{% endhint %}

### Filters

Filter by **team**, **member**, and **repository**, choose **Daily**, **Weekly**, or **Monthly**, and set the date range.

### What the page shows

| Section                   | What it shows                                                                                                                         |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **AI-assisted share**     | The percentage of new code that was AI-assisted, with total lines and AI-attributed lines.                                            |
| **AI Tool Usage**         | Share of AI-attributed lines per tool.                                                                                                |
| **AI Model Usage**        | Share of AI-attributed lines per model.                                                                                               |
| **Generation Type Mix**   | How the lines were produced.                                                                                                          |
| **Total Tokens**          | Token usage and its distribution.                                                                                                     |
| **Suggested / Accepted**  | Suggested and accepted lines and the overall acceptance rate, with a table per tool (lines, suggested, accepted, rate, total tokens). |
| **Commit Activity Trend** | Commit volume over time and the AI share of commits.                                                                                  |
| **Line Activity Trend**   | Lines added over time and the AI share of added lines.                                                                                |
| **Commit History**        | Commit-level detail. **Bulk Merge** is available from this table.                                                                     |

{% hint style="info" %}
AI Usage can be turned on or off for the organization in **Administration** > **Feature Management** (**Modules**).
{% endhint %}

### Related

* [AI Impact Overview](https://docs.oobeya.io/ai-impact/ai-impact-overview)
* [AI Cost & Credits](https://docs.oobeya.io/ai-impact/ai-cost-and-credits)
