---
description: >-
  Your personal Oobeya home page: what needs your attention, what is going well,
  and where to go next, shaped by your role and your teams.
---

# Home Page

Oobeya opens with a personal home page. It brings together the things that need your attention, what is going well, and the pages you use most, so you can see where to start without opening every report.

What you see depends on your company role, your teams and your Oobeya permissions. Every number on the page comes from the same data as the rest of Oobeya, and each section links to the page where you can act on it.

{% hint style="info" %}
Available from **Oobeya 2.1**.
{% endhint %}

## Your Role Shapes the Page

The home page follows the **company role** in your Oobeya profile and the teams you belong to or lead.

| You are                                                                                      | Your home page focuses on                                                                                             |
| -------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Developer** (and any role that does not lead a team)                                       | Your own work: your coding activity, the quality of the code you changed, your wins, and the symptoms of your team    |
| **Team lead** (for example Team Lead, Tech Lead, Scrum Master, Agile Coach, Project Manager) | The teams you lead: their symptoms, delivery and DORA metrics                                                         |
| **Manager or director** (for example Manager, Director, Tribe Lead, CTO, VP)                 | All the teams you lead across the organization: DORA levels across teams, active symptoms and your organization table |
| **Administrator** (application role)                                                         | Everything above for your company role, plus the setup items that need an administrator                               |

{% hint style="info" %}
If your home page shows the wrong view, check the company role and teams in your profile. Only an administrator can change your company role.
{% endhint %}

## The Header

The header shows your name, photo, company role and teams. From here you can:

* Open **My scorecard** or **Edit profile**.
* Change the **language** of Oobeya: English, Español, Polski, Português do Brasil or Türkçe. The change applies at once and is kept the next time you sign in.
* Choose the **period** for the whole page: the last 7, 30, 90, 180 or 365 days.
* Open **Customize your homepage** with the gear button (see [Customize Your Home Page](home-page.md#customize-your-home-page)).

**My tools** lists the repositories, boards, pipelines, code quality projects and AI tools of your teams, with a link to each tool. Select **Show my tools** to open the list. Tools appear here once they are selected in your team scorecard.

## Action Items

**Action items** lists what is waiting for you or your team, the most urgent first. Items are grouped into tabs:

| Tab          | What it contains                                                                                                                          |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Symptoms** | Active team symptoms, such as unreviewed pull requests or a recurring high rework rate                                                    |
| **Delivery** | Delivery and DORA items of your teams                                                                                                     |
| **Setup**    | Setup steps that are still missing for your teams                                                                                         |
| **For me**   | Items about your own work, such as security or reliability issues in code you changed                                                     |
| **Admin**    | Administrators only: for example data sources that fail their connection check, accounts that are not merged, or Git analyses that failed |

You can filter the list by **severity** (Critical, Warning, Info), by **status**, and, if you lead several teams, by **team**. Select **Details** to see more, and use the button on the right, such as **Open in team**, **See issues** or **Review accounts**, to go to the page where you can fix it.

Each item also has your own **status**: **Open**, **On it**, **Done** or **Won't fix**. Items marked Done or Won't fix are dimmed and move to the end of the list. The status is for your own follow-up: it does not change anything in Oobeya, and it is saved in your browser.

## Wins

**Wins** shows what is going well in the selected period, for example a coding efficiency that rose, a rework rate below the company average, an improved lead time or an Elite DORA level. Filter the wins by category to see one area at a time.

## Shortcuts and Get Involved

**Shortcuts** keeps the pages you use most one click away. Select **Edit** to choose your shortcuts.

**Get involved** points to:

* **Gamification**.
* **Surveys**: open surveys for you, and **Create a survey** if you can create one.
* **Connect your AI tool (MCP)**: whether an AI tool is connected to your Oobeya account, with a link to connect one. See [Using Oobeya from Your AI Tool (MCP)](/broken/pages/7b86def1736f4e977a2f570a49ab51f4485c2936).

## Team and Organization Sections

Further down, the home page summarizes your teams. Which sections you see depends on your role.

* **DORA levels across teams**: how many of your teams are at Elite, High, Medium or Low for each DORA metric.
* **Active symptoms**: the number of active symptoms, how many are critical, and the areas they are in, such as code review, development or delivery.
* **Wins and action items**: open items and wins side by side for each area, with the area that is going best and the one with the most to do.
* **My Organization**: the DORA levels and active symptoms of each team you lead. Expand a team to see its sub-teams.
* **My coding** (developers): what kind of work you do compared with the company average (new work, refactoring, helping others, rework), where your commits went, and the quality of the code you changed.

## Customize Your Home Page

Select the gear button in the header to open **Customize your homepage**.

* Turn off the sections you don't need, for example Wins, Shortcuts, DORA levels across teams or the teams table. Administrators can also turn off the admin tasks in Action items.
* Select **Edit layout** to arrange the sections.
* Select **Reset to default** to bring back the original page.

Your choices are saved in this browser.

## FAQ

**Why don't I see the Admin tab?** The Admin tab is shown only to users with the Admin application role.

**Why is My tools empty?** My tools lists the tools that are selected in your team scorecard. Ask your team lead or administrator to select the repositories, boards and code quality projects of your team.

**Why do I see a developer home page although I lead a team?** The view follows the company role in your profile. Ask an administrator to update your company role.

**Does marking an item Done change anything in Oobeya?** No. The status is your own follow-up and is saved in your browser. The item disappears from the list when the underlying problem is solved.
