---
description: >-
  How planned workload and engineering capacity are distributed across projects
  and contributors.
---

# Resource Allocation

Resource Allocation shows how planned workload and engineering capacity are distributed across projects and contributors. Utilization and allocation can be calculated by work-item count or by estimated effort.

See [Resource Allocation](https://docs.oobeya.io/allocations/resource-allocation).

### Overview Metrics

| Metric                           | What it measures                                                                                               |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Total Projects**               | Number of projects included in Resource Allocation analysis.                                                   |
| **Total Resources**              | Number of contributors included in the analysis.                                                               |
| **Utilization by Effort (%)**    | Resource utilization calculated using estimated effort.                                                        |
| **Utilization by Count (%)**     | Resource utilization calculated using work-item count.                                                         |
| **Resource Status Distribution** | Distribution of resources classified as Underutilized, Optimally Utilized, Slightly Overloaded, or Overloaded. |
| **Planned Work Items**           | Number of work items assigned to a resource or team.                                                           |
| **Delivered Work Items**         | Number of work items completed by a resource or team.                                                          |
| **Planned Effort**               | Estimated effort assigned to a resource or team.                                                               |
| **Delivered Effort**             | Estimated effort completed by a resource or team.                                                              |
| **Team Average Capacity**        | Delivered work divided by the number of contributors in the team.                                              |

### Resource Utilization Metrics

| Metric                            | What it measures                                                                      |
| --------------------------------- | ------------------------------------------------------------------------------------- |
| **Resource Utilization (%)**      | Planned work assigned to a resource relative to the team's average delivery capacity. |
| **Team Utilization (%)**          | Aggregated utilization level of a team.                                               |
| **Underutilized Resources**       | Resources whose utilization is below the configured lower threshold.                  |
| **Optimally Utilized Resources**  | Resources operating within the configured optimal range.                              |
| **Slightly Overloaded Resources** | Resources above the optimal range but below the highest overload threshold.           |
| **Overloaded Resources**          | Resources whose utilization exceeds the configured overload threshold.                |

Default calculation:

```
Team Average Capacity =
Delivered Work Items / Number of Contributors
```

```
Resource Utilization (%) =
Planned Work Items / Team Average Capacity × 100
```

Default classification:

| Utilization   | Status              |
| ------------- | ------------------- |
| **≤ 85%**     | Underutilized       |
| **85%-110%**  | Optimally Utilized  |
| **110%-130%** | Slightly Overloaded |
| **> 130%**    | Overloaded          |

Thresholds can be customized by administrators.

### Project Allocation Metrics

| Metric                                | What it measures                                                             |
| ------------------------------------- | ---------------------------------------------------------------------------- |
| **Project Allocation (%)**            | Percentage of a contributor's planned work assigned to a particular project. |
| **Allocation by Work-Item Count (%)** | Project allocation calculated using planned work-item count.                 |
| **Allocation by Effort (%)**          | Project allocation calculated using estimated effort.                        |
| **Projects per Contributor**          | Number of projects to which a contributor is allocated.                      |
| **Contributors per Project**          | Number of contributors allocated to a project.                               |
| **Allocation Distribution**           | Distribution of contributor capacity across projects.                        |

Calculation:

```
Project Allocation (%) =
Planned Items for the Contributor in the Project
/
Total Planned Items for the Contributor Across All Projects
× 100
```
