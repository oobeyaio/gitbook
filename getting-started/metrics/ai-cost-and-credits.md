---
description: >-
  AI coding assistant spend and credit consumption by organization, team, user,
  model, product, repository, and cost center.
---

# AI Cost and Credits

The AI Cost and Credits module gives financial visibility into AI coding assistant consumption at organization, team, user, model, product, repository, and cost-center levels. It can also compare AI spend with engineering outcome metrics.

See [AI Cost and Credits](https://docs.oobeya.io/ai-impact/ai-cost-and-credits).

### Summary Metrics

| Metric                          | What it measures                                                     |
| ------------------------------- | -------------------------------------------------------------------- |
| **Total Users**                 | Number of users represented in the selected AI cost and credit data. |
| **AI Credit Pool Value**        | Monetary value of the organization's available AI credit pool.       |
| **Total AI Credits Used**       | Total number of AI credits consumed during the selected period.      |
| **Remaining AI Credits**        | Unused credits remaining in the configured credit pool.              |
| **Total Gross Cost**            | Total cost before discounts or adjustments.                          |
| **Discount Amount**             | Total discount applied to AI usage charges.                          |
| **Net Cost**                    | Cost after discounts and adjustments.                                |
| **Applied Cost per Credit**     | Monetary rate applied to each AI credit.                             |
| **Remaining Credit Pool Value** | Monetary value of credits remaining in the configured pool.          |
| **Credit Utilization Rate (%)** | Percentage of the total credit pool consumed.                        |
| **Cost per User**               | Average or individual AI cost attributed to a user.                  |
| **Credits per User**            | Average or individual AI credits consumed by a user.                 |

Where the standard AI credit rate is configured as USD 0.01:

```
AI Cost (USD) = AI Credits × 0.01
```

The actual rate may differ based on product configuration, provider pricing, contract terms, discounts, and imported billing data.

### Cost and Credit Breakdown Metrics

| Metric                      | What it measures                                                             |
| --------------------------- | ---------------------------------------------------------------------------- |
| **Cost by User**            | AI cost attributed to each user.                                             |
| **Credits by User**         | AI credits consumed by each user.                                            |
| **Cost by Team**            | AI cost aggregated by mapped Oobeya team.                                    |
| **Credits by Team**         | AI credits aggregated by team.                                               |
| **Cost by Organization**    | AI cost aggregated by source organization.                                   |
| **Credits by Organization** | AI credits aggregated by source organization.                                |
| **Cost by Product**         | AI cost grouped by AI coding assistant product.                              |
| **Credits by Product**      | AI credits grouped by product.                                               |
| **Cost by SKU**             | Cost grouped by provider SKU.                                                |
| **Credits by SKU**          | Credit usage grouped by provider SKU.                                        |
| **Cost by Model**           | AI cost grouped by language model.                                           |
| **Credits by Model**        | Credit consumption grouped by language model.                                |
| **Model Usage Share (%)**   | Percentage of total AI consumption attributed to each model.                 |
| **Cost by Repository**      | AI cost associated with each repository, where repository data is available. |
| **Credits by Repository**   | AI credit usage associated with each repository.                             |
| **Cost by Cost Center**     | AI cost aggregated by mapped cost center.                                    |
| **Credits by Cost Center**  | AI credit usage aggregated by cost center.                                   |

### Cost Trend Metrics

| Metric                               | What it measures                                                           |
| ------------------------------------ | -------------------------------------------------------------------------- |
| **Daily Credit Consumption**         | AI credits consumed per day.                                               |
| **Monthly Credit Consumption**       | AI credits consumed per month.                                             |
| **Credit Consumption Trend**         | Change in credit usage over time.                                          |
| **Daily AI Cost**                    | AI cost generated per day.                                                 |
| **Monthly AI Cost**                  | AI cost generated per month.                                               |
| **AI Cost Trend**                    | Change in AI cost over time.                                               |
| **Average Daily Cost**               | Average AI cost generated per day.                                         |
| **Average Monthly Cost**             | Average AI cost generated per month.                                       |
| **Projected Period Cost**            | Estimated cost for the full reporting period based on current consumption. |
| **Budget or Pool Consumption Trend** | Progress of cost or credit consumption against the configured pool.        |

### Estimated Token Metrics

Detailed input, output, and cached-token telemetry may not be provided directly by every AI coding assistant.

When estimated token reporting is enabled, Oobeya may display:

| Metric                          | What it measures                                                                              |
| ------------------------------- | --------------------------------------------------------------------------------------------- |
| **Estimated Total Token Usage** | Estimated number of tokens represented by the observed AI cost and model-pricing assumptions. |
| **Estimated Input Tokens**      | Estimated input-token volume.                                                                 |
| **Estimated Output Tokens**     | Estimated output-token volume.                                                                |
| **Estimated Cached Tokens**     | Estimated token volume served from provider cache.                                            |
| **Estimated Token Range**       | Low, expected, and high token-usage estimates based on pricing and usage assumptions.         |
| **Estimation Confidence**       | Confidence indicator associated with the available model, feature, and pricing information.   |

{% hint style="info" %}
Estimated token metrics are estimates, not provider-reported exact telemetry. They must always be labeled as **Estimated**.
{% endhint %}

### Cost and Engineering Impact Analysis

The module can compare AI cost and credit consumption with engineering outcome metrics.

| Analysis                                | What it measures                                                                         |
| --------------------------------------- | ---------------------------------------------------------------------------------------- |
| **AI Cost vs. Adoption Rate**           | Compares financial consumption with AI adoption.                                         |
| **AI Cost vs. Acceptance Rate**         | Compares cost with suggestion or line acceptance.                                        |
| **AI Cost vs. Coding Efficiency**       | Examines whether cost changes coincide with changes in Coding Efficiency.                |
| **AI Cost vs. Coding Impact**           | Compares AI spend with the scope and impact of development activity.                     |
| **AI Cost vs. Code Churn**              | Examines whether increased AI consumption coincides with more or less short-term rework. |
| **AI Cost vs. Pull Request Cycle Time** | Compares AI spend with pull request review and merge speed.                              |
| **AI Cost vs. Lead Time for Changes**   | Compares cost with end-to-end delivery time.                                             |
| **AI Cost vs. Deployment Frequency**    | Compares AI spend with production delivery frequency.                                    |
| **AI Cost vs. Change Failure Rate**     | Examines the relationship between AI spend and delivery stability.                       |
| **AI Cost vs. Time to Restore Service** | Compares AI spend with production restoration performance.                               |
| **AI Cost vs. Technical Debt**          | Examines whether AI consumption coincides with changes in technical debt.                |
| **AI Cost vs. Code Quality**            | Compares AI spend with quality, security, reliability, and maintainability indicators.   |

{% hint style="info" %}
Correlation does not prove causation. These analyses are intended to identify patterns that should be investigated together with team context, workflow changes, and sample size.
{% endhint %}
