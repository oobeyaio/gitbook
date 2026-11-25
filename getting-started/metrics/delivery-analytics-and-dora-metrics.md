---
description: >-
  Software delivery performance - the four key DORA metrics, delivery flow, and
  deployment and incident volume.
---

# Delivery Analytics and DORA Metrics

Delivery Analytics connects source code management, CI/CD, deployment, and incident data to measure software delivery performance.

See [DORA Metrics Introduction](https://docs.oobeya.io/deployment-analytics/dora-metrics-introduction) and [Deployment Analytics](https://docs.oobeya.io/gitwiser-repo-analytics/deployment-analytics-dora-metrics).

### Four Key DORA Metrics

| Metric                             | What it measures                                                                                        |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Lead Time for Changes**          | Time from a code commit or development change until that change is successfully deployed to production. |
| **Deployment Frequency**           | How often the team successfully deploys changes to production.                                          |
| **Change Failure Rate (%)**        | Percentage of production deployments that result in a failure or incident.                              |
| **Time to Restore Service / MTTR** | Time required to restore service after a production failure.                                            |

### Delivery Flow Metrics

| Metric                  | What it measures                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------ |
| **Development Time**    | Time between the first commit and merge of the related pull request or change.       |
| **Waiting for Deploy**  | Time between the pull request merge and the start of the deployment pipeline.        |
| **Deployment Duration** | Time between the deployment pipeline start and successful completion.                |
| **Lead Time Breakdown** | Breakdown of Lead Time for Changes into development, waiting, and deployment phases. |
| **Deploy Size**         | Number of commits and pull requests included in a deployment package.                |
| **Average Deploy Size** | Average number of commits and pull requests delivered per deployment.                |

### Deployment and Incident Volume

| Metric                                 | What it measures                                                                  |
| -------------------------------------- | --------------------------------------------------------------------------------- |
| **Number of Deployments**              | Total number of detected successful production deployments.                       |
| **Number of Contributors**             | Number of contributors whose changes were included in deployments.                |
| **Deployments Leading to an Incident** | Number of deployments associated with a production incident or failure.           |
| **Production Incidents**               | Number of incidents included in Change Failure Rate and restoration calculations. |
| **Successful Deployments**             | Number of production deployments completed without a detected failure.            |
| **Failed Changes**                     | Number of production changes associated with an incident or rollback condition.   |
| **Deployment Frequency Trend**         | Change in successful deployment frequency over time.                              |
| **Change Failure Rate Trend**          | Change in the percentage of failed production changes over time.                  |
| **Lead Time Trend**                    | Change in Lead Time for Changes over time.                                        |
| **Time to Restore Service Trend**      | Change in restoration time over time.                                             |

{% hint style="info" %}
Change Failure Rate and Time to Restore Service require a correctly configured failure-detection source and production deployment mapping.
{% endhint %}
