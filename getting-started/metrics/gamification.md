---
description: >-
  Points, rounds, leagues, and rankings built from selected Oobeya metrics and
  manually defined KPIs.
---

# Gamification

Gamification converts selected Oobeya metrics and manually defined KPIs into configurable points, rounds, leagues, and rankings. It can use metrics from Project Management, Development Analytics, Pull Request Analytics, Code Quality, Security, Engineering Symptoms, and manually defined KPIs.

See [Gamification](https://docs.oobeya.io/gamification/gamification).

### Gamification Outputs

| Metric                       | What it measures                                                         |
| ---------------------------- | ------------------------------------------------------------------------ |
| **Metric Result**            | Actual value of the selected engineering metric for a scoring round.     |
| **Metric Threshold**         | Configured value range used to assign points.                            |
| **Metric Points**            | Points earned from a metric based on its scoring thresholds.             |
| **Manual KPI Points**        | Points manually entered and approved by a league referee.                |
| **Round Score**              | Total points earned by a team during a scoring round.                    |
| **Approved Round Score**     | Round Score after referee review and approval.                           |
| **Cumulative Score**         | Total points accumulated across completed rounds.                        |
| **Team Rank**                | Position of a team based on cumulative or selected-round score.          |
| **League Ranking**           | Ranking of all participating teams within a league.                      |
| **Maximum Available Points** | Maximum points a team can earn under the configured rules.               |
| **Achievement Rate (%)**     | Earned points relative to the maximum available points, where displayed. |

{% hint style="info" %}
Gamification scores are derived outputs. The underlying engineering metrics retain their original definitions and units.
{% endhint %}
