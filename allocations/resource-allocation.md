---
icon: chart-pie-simple-circle-dollar
---

# Resource Allocation

The **Resource Allocation** module in Oobeya enables teams to analyze workload distribution and project allocations, supporting more efficient resource management. It helps ensure that teams work in a balanced way based on their capacity, task load, and project priorities.

With this module, engineering leaders can:

* Visualize team capacities,
* Identify **overloaded** or **underutilized** teams and contributors,
* Improve **resource planning** based on real-time data.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FCUkEIJHKY0630CDvJNl9%2FScreenshot%202025-07-31%20at%2014.25.10.png?alt=media&#x26;token=e6ed5831-e348-4768-ba46-95f1c34e59b1" alt=""><figcaption><p>Resource Allocations Module</p></figcaption></figure>

***

### Prerequisites

Before using the Resource Allocation module, make sure the following conditions are met:

* [x] **Project Management tool integration is active**: The module pulls data from the project management tools like Jira or Azure Boards via Oobeya's AgileSpace module.
* [x] **Projects are analyzed on AgileSpace**: Ensure your Jira or Azure Boards projects are being actively analyzed in AgileSpace.
* [x] **Contributor Profiles are created**: Every contributor involved in project delivery work must have a contributor profile in Oobeya.
* [x] **Accounts are merged (if needed)**: Duplicate Jira/Azure Boards accounts should be merged to avoid miscalculations.
* [x] **Relevant roles are configured**: Only selected roles (e.g., Developer) are included in allocation calculations. Roles can be managed via `Administration > Resource Allocations`. [See the details below](resource-allocation.md#admin-settings).
* [x] **Exclude unnecessary work item types**: Go to  `Administration > AgileSpace > Work Item Type Exclusion` to exclude irrelevant work item types (e.g., questions, comments) from the analysis to improve accuracy.

***

### Key Concepts

* **Resource**: A contributor involved in the development process (e.g., developer, QA, analyst).
* **Project**: The initiative or product being worked on. The module integrates with Jira and Azure Boards.
* **Project Allocation %**: Represents the ratio of effort or tasks a contributor is assigned to a specific project.
* **Resource Utilization %**: Indicates how much of the assigned work a resource was able to deliver.

***

### How It Works

**Overview Panel**

The module provides a summary across the entire organization or selected units:

* **Total Projects**
* **Total Resources**
* **Utilization by Effort (%)**
* **Utilization by Count (%)**
* **Resource Status Chart**

Both utilization metrics help visually identify **workload imbalances** or **inefficient use of capacity**.

***

### **1. Resource Utilization (%) Calculation**

Resource utilization indicates how full a team or individual is compared to their actual delivery capacity. It helps you evaluate:

* Are teams or individuals **underloaded**?
* Are they operating at an **optimal level**?
* Are they **overloaded**?

**Formula:**

```
Utilization (%) = (Planned Work Items / Team Average Capacity) × 100
```

**Team Average Capacity** is calculated as:

```
Team Average Capacity = Delivered Work Items / Number of Contributors
```

**Example:**

* Total Delivered Work Items: 100
* Team Members: 5
* Planned Work Items for Dev-A: 25

→ Team Avg Capacity = 100 / 5 = 20\
→ Dev-A’s Utilization = (25 / 20) × 100 = **125%**

**Interpretation:**

| Utilization % (default) | Status              |
| ----------------------- | ------------------- |
| ≤ 85%                   | Underutilized       |
| 85% – 110%              | Optimally Utilized  |
| 110% – 130%             | Slightly Overloaded |
| > 130%                  | Overloaded          |

{% hint style="info" %}
These default thresholds can be customized via `Administration > Resource Allocations`.
{% endhint %}

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F3r0TB3AGR9HFPAxoL6t8%2Fimage.png?alt=media&#x26;token=62870473-afab-41ee-94ef-b0725e2905c1" alt=""><figcaption><p>Resource Status</p></figcaption></figure>

***

### 2. Project Allocation (%) Calculation

Project allocation indicates how much of a contributor’s time and effort is assigned to a particular project.

This is especially helpful for tracking contributors working on multiple projects simultaneously.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FwgVUIve0jogp3Hj9lVrm%2Fimage.png?alt=media&#x26;token=708b2c90-1d1a-409e-ab6a-e2d3474758e5" alt=""><figcaption><p>Project Allocation</p></figcaption></figure>

**Formula:**

```
Project Allocation (%) =
(Planned Items for This Project by Person / Total Planned Items by Person Across All Projects) × 100
```

**Example:**

* Planned Tasks for Jane in Project A: 5
* Total Planned Tasks for Jane Across All Projects: 10

→ Project Allocation = (5 / 10) × 100 = **50%**

This means 50% of Jane's effort is allocated to Project A.

***

### Additional Notes

* Data is retrieved from AgileSpace (Oobeya’s Agile analytics module).
* Only selected roles (e.g., Developer) are included in calculations. Manage role settings via `Administration > Resource Allocations`.
* The module supports toggling between **Item Count** and **Effort** (story points or time estimates).
* For accurate results, ensure contributor profiles are created in Oobeya and merged if necessary.

***

### Admin Settings

Oobeya provides configuration options for administrators to tailor the module’s behavior, such as defining resource status thresholds and selecting which roles are included in the analysis.

***

#### **1. Resource Allocation Thresholds**

These thresholds define how resource utilization is classified:

| Category                | Description                                              | Default (%) |
| ----------------------- | -------------------------------------------------------- | ----------- |
| **Underutilized**       | Below this rate, resources are considered underutilized. | 85          |
| **Optimally Utilized**  | Within this range, resources are considered balanced.    | 110         |
| **Slightly Overloaded** | Between optimal and heavily overloaded.                  | 130         |
| **Overloaded**          | Above this rate, resources are marked as overloaded.     | >130        |

> Each threshold is explained via tooltip icons next to the fields.

* **Reset**: Reverts to default values.
* **Save**: Saves your custom threshold settings.

***

#### **2. Allocation Roles (Role-Based Exclusions)**

This setting lets you control which contributor roles are included in Resource Allocation analytics.

* For example: If only the `Developer` role is selected, only those contributors’ workloads are analyzed.
* This excludes non-engineering roles such as QA, Analyst, Management, Support, etc.

**Use Case:**\
If a project manager wants to evaluate only developer productivity, excluding other roles results in more meaningful insights.

{% hint style="info" %}
This setting affects the entire organization and can only be modified by users with admin privileges.
{% endhint %}



