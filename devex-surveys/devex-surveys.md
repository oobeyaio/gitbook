---
icon: square-poll-vertical
---

# DevEx Surveys

**DevEx Surveys** (since Oobeya 2.1) measures how engineers experience their work. Start from a ready-to-use Oobeya survey or build your own, send it to teams, developers, or developer tags, and follow scores, participation, and benchmarks by team. Results sit next to the delivery and quality metrics of the same teams.

You find DevEx Surveys in the **Engagement** section of the left menu:

| Page                                                  | Who uses it                      | What it shows                                                                                                                          |
| ----------------------------------------------------- | -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **My Surveys**                                        | Everyone                         | Surveys waiting for your answers and the ones you completed, with confidentiality, period, and your answer status.                     |
| **Survey List**                                       | Survey owners and administrators | All surveys with status, teams, confidentiality, source (Oobeya template or your own), number of questions, period, and participation. |
| **Survey Dashboard** (Developer Experience Dashboard) | Survey owners and administrators | Results across teams: company score, participation, topic scores, benchmarks, and answer sentiment.                                    |

{% hint style="info" %}
DevEx Surveys can be turned on or off for the organization in **Administration** > **Feature Management** (**Modules**).
{% endhint %}

### Ready-to-use Oobeya surveys

Each Oobeya survey comes with curated questions, a recommended cadence, and an estimated answer time of 1–7 minutes:

| Survey                    | Recommended cadence                          |
| ------------------------- | -------------------------------------------- |
| Developer Experience Core | Monthly                                      |
| SDLC Maturity             | Quarterly                                    |
| AI Engineering Maturity   | Quarterly                                    |
| AI Readiness Assessment   | On demand                                    |
| Engineering Team Health   | Monthly                                      |
| Team Operating Model      | Quarterly                                    |
| Code Review Effectiveness | Monthly                                      |
| Engineering Quality       | Quarterly                                    |
| Wellbeing Pulse           | Weekly (five questions, always confidential) |

Oobeya surveys include a benchmark, so each topic score can be compared with a reference value.

### Creating a survey

1. Open **Survey List** or **Survey Dashboard** and click **Create**.
2. Pick an Oobeya template or one of your own templates.
3. Choose who receives the survey: teams, developers, or developer tags.
4. Set a date range or a recurring schedule.
5. Review the survey and publish it.

Participants see pending surveys in a banner and in in-app notifications. Answers are saved as they go. Recurring surveys appear in the list with their cadence and run number (for example, _Weekly · #5_).

#### Your own templates and questions

Use **Templates** to build your own surveys and **Question Bank** to manage questions. Supported question types are **Likert**, **Yes/No**, **NPS**, and **open text**.

### Reading the results

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FN3lhB6Cf8841rUYfoTCP%2Fdevex-dashboard.png?alt=media&#x26;token=b5b30538-2d0f-4d61-a181-2929033f93b0" alt="Developer Experience Dashboard with company score, participation, and topic results"><figcaption><p>Survey Dashboard: score, participation, and benchmark at a glance.</p></figcaption></figure>

Filter the dashboard by **Team** and date range. The **Survey Overview** has two tabs:

* **Score & Participation**: the **General Company Score** (0–100, with a status such as _Needs attention_), the participation rate over time, active surveys, total responses, average completion rate, and the engagement trend compared with the previous period.
* **Topic Results**: scores by topic.

Below the overview:

* **Completion**: the share of invited people who completed the survey.
* **Topics vs Benchmark**: how many topics meet their benchmark and how many are below it.
* **Answer Sentiment**: the share of positive and negative answers.
* **How are we doing across topics?**: a table of topics with score, trend, benchmark, number of questions, sentiment, and comments. The table can be exported.

The results of a single survey also show the strongest question, the question that needs attention, the largest gap to benchmark, and comment themes.

### Confidentiality

A survey is either **Confidential** or **Identified**:

* **Confidential**: results are visible only to authorized roles, and never show who gave which answer. Only aggregated results are shown.
* **Identified**: answers can be attributed to respondents.

### Survey settings (administrators)

**Administration** > **Survey Settings** (**Insights & AI** section) holds the defaults for new surveys. Each survey can override them when it is created.

| Setting                               | Description                                                                                                                                                                                                                      |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Default confidentiality mode**      | Confidential or Identified.                                                                                                                                                                                                      |
| **Roles that can see survey results** | For example Admin and Survey owner. In confidential surveys these roles see results but never who gave which answer.                                                                                                             |
| **Answering**                         | Allow respondents to change their answers until the survey closes.                                                                                                                                                               |
| **Delivery Channels**                 | Email.                                                                                                                                                                                                                           |
| **Default Reminder Schedule**         | Initial invitation when the survey opens, a reminder a set number of days after start, a reminder a set number of hours before closing, and a final-day reminder. Reminders go only to people who have not completed the survey. |
| **Notifications**                     | E-mails sent when a survey is created, closed, or deleted, or when everyone has answered, and who receives them.                                                                                                                 |

{% hint style="info" %}
Invitations and reminders are sent by e-mail, so the mail server must be configured in **Administration** > **Notifications** (SMTP).
{% endhint %}
