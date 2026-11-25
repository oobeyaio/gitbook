# Problem Analytics

**Problem Analytics** (the **Problem Management** page) tracks problems across teams and applications. It gives visibility into resolution times, SLA performance, severity, status, and trends from creation to resolution.

{% hint style="info" %}
Problem Analytics can be turned on or off for the organization in **Administration** > **Feature Management** (**Modules**).
{% endhint %}

### Applications

The main page lists the analyzed **Applications** with their **Open**, **Closed**, and **Total** problems and the **Updated Date**. From the **Actions** column you can refresh an analysis (it updates the data since the last analysis) or delete it.

### Problem Detail

Open an application to see its **Problem Detail** page: resolution times, SLA breaches, reopenings, status and severity distributions, and open problems. Group the charts **Daily**, **Weekly**, or **Monthly**.

| Widget                          | What it shows                                                                                                                                                                                                                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Summary cards**               | **Problems** created in the selected period, average **Resolution Time** (from creation until first marked as Closed), **SLA Breach** (share of resolved problems that exceeded the SLA target of their severity), and **Reopens** (times problems were reopened after being closed). |
| **Open Problems Trend**         | How the number of open problems changes over time, grouped by severity.                                                                                                                                                                                                               |
| **Problem Distribution Chart**  | Problems grouped by Type, Main Type, Severity, Priority, or Category. Rejected problems are not included.                                                                                                                                                                             |
| **Problem Status Distribution** | The number of problems in each status category (To Do, In Progress, Closed, Rejected).                                                                                                                                                                                                |
| **Resolution Time Accuracy**    | Estimated versus actual resolution time, showing whether problems were resolved within the expected duration (over or under estimate).                                                                                                                                                |
| **Problem Details**             | The problems themselves. Open a problem to see its **Problem History**: who changed which field, the old and new values, and when.                                                                                                                                                    |

### Status and severity mapping (administrators)

**Administration** > **Problem Management** (**Analytics** section) maps the values of your tool to the categories Problem Analytics uses:

* **Problem Status Mapping**: map your work item states to **To Do**, **In Progress**, **Done**, and **Rejected**. Select an existing state or type a new one and press Enter. States that are not mapped are listed; problems in those states are excluded from calculations until you map them. Since Oobeya 2.1 the states come from the status definitions of your tool, and an **Unmapped** option can be selected in each category.
* **Problem Severity Mapping**: map your severity values to **Blocker**, **Critical**, **High**, **Medium**, **Low**, and **Info**, and set the **SLA Target** (in hours) for each level. SLA Breach is calculated from these targets.

Click **Save** after each change.
