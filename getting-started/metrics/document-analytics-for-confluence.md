---
description: >-
  Confluence documentation activity, content freshness, contribution patterns,
  and Space health.
---

# Document Analytics for Confluence

Document Analytics shows documentation activity, content freshness, contribution patterns, and Confluence Space health. Metrics may be available at organization, Space, team, and contributor levels.

See [Document Analytics - Confluence](https://docs.oobeya.io/document-analytics/document-analytics-confluence).

### Organization and Space Overview

| Metric                     | What it measures                                                                    |
| -------------------------- | ----------------------------------------------------------------------------------- |
| **Total Spaces**           | Total number of Confluence Spaces included in the analysis.                         |
| **Active Spaces**          | Number of Spaces with qualifying documentation activity during the selected period. |
| **Inactive Spaces**        | Number of Spaces without qualifying activity during the selected period.            |
| **Total Pages**            | Total number of analyzed Confluence pages.                                          |
| **Total Contributors**     | Number of contributors associated with analyzed content.                            |
| **Active Contributors**    | Number of contributors who created or updated content during the selected period.   |
| **Pages per Space**        | Average or total number of pages within each Space.                                 |
| **Contributors per Space** | Number of active contributors associated with each Space.                           |
| **Space Activity Score**   | Relative indicator representing documentation activity within a Space.              |
| **Space Ranking**          | Ranking of Spaces based on selected activity, freshness, or health indicators.      |

### Documentation Activity Metrics

| Metric                            | What it measures                                                              |
| --------------------------------- | ----------------------------------------------------------------------------- |
| **Pages Created**                 | Number of pages created during the selected period.                           |
| **Pages Updated**                 | Number of unique pages updated during the selected period.                    |
| **Page Update Count**             | Total number of page-update activities.                                       |
| **Content Activity**              | Combined view of page creation and update activity.                           |
| **Page Creation Trend**           | Change in newly created pages over time.                                      |
| **Page Update Trend**             | Change in page-update activity over time.                                     |
| **Space Activity Trend**          | Change in documentation activity for a Space over time.                       |
| **Contributor Activity**          | Number of page creation and update activities attributed to each contributor. |
| **Contribution Distribution**     | Distribution of documentation activity across contributors.                   |
| **Pages Created per Contributor** | Average or individual number of pages created by contributors.                |
| **Pages Updated per Contributor** | Average or individual number of pages updated by contributors.                |

### Freshness and Documentation Health

| Metric                             | What it measures                                                                                                                        |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Documentation Health Score**     | Composite indicator summarizing freshness, maintenance activity, contributor participation, and other configured documentation signals. |
| **Fresh Pages**                    | Number of pages updated within the configured freshness period.                                                                         |
| **Fresh Content Rate (%)**         | Percentage of analyzed pages classified as fresh.                                                                                       |
| **Stale Pages**                    | Number of pages not updated within the configured stale-content threshold.                                                              |
| **Stale Content Rate (%)**         | Percentage of analyzed pages classified as stale.                                                                                       |
| **Average Page Age**               | Average age of analyzed pages since creation.                                                                                           |
| **Average Time Since Last Update** | Average elapsed time since pages were last updated.                                                                                     |
| **Oldest Page Update Age**         | Longest elapsed time since a page was updated.                                                                                          |
| **Pages Needing Attention**        | Number of pages identified as stale, inactive, or requiring review.                                                                     |
| **Spaces Needing Attention**       | Number of Spaces with low activity, stale content, or other documentation-health risks.                                                 |

### Team and Ownership Indicators

| Metric                             | What it measures                                                                |
| ---------------------------------- | ------------------------------------------------------------------------------- |
| **Mapped Teams**                   | Number of Oobeya teams associated with analyzed Confluence Spaces.              |
| **Spaces with Team Mapping**       | Number of Spaces connected to at least one Oobeya team.                         |
| **Spaces without Team Mapping**    | Number of Spaces without an assigned team relationship.                         |
| **Pages by Team**                  | Documentation pages attributed to each mapped team.                             |
| **Activity by Team**               | Documentation creation and update activity attributed to each team.             |
| **Contributors by Team**           | Active documentation contributors grouped by team.                              |
| **Team-to-Space Relationships**    | Distribution of mapped team relationships across Spaces.                        |
| **Documentation Coverage by Team** | Visibility into whether mapped teams maintain active and current documentation. |

{% hint style="info" %}
Freshness and health results depend on the configured stale-content period and the availability of Confluence history and contributor data.
{% endhint %}
