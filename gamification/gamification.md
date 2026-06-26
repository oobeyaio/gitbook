---
description: >-
  Automatically score engineering teams based on Engineering KPIs to boost
  performance and motivation.
icon: trophy
---

# Gamification

Oobeya’s **Gamification** module provides a point-based competitive structure to boost engineering team performance. It visualizes progress, increases motivation, and highlights achievements. With this feature, you can create leagues, define performance metrics (Engineering KPIs), compare team scores, and reward high performance.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FHxqtl9kUbZoescNlLyHO%2Fimage.png?alt=media&#x26;token=82ae69cf-b735-4068-9a28-2a236f56b75c" alt="Oobeya Gamification Module"><figcaption><p>Oobeya Gamification Module</p></figcaption></figure>

***

### Key Concepts

* **League**: A competition structure where teams collect points based on defined metrics.
* **Round**: Scoring periods executed at specific intervals (e.g., weekly, biweekly, monthly).
* **Referees**: Authorized users who supervise manual scoring and can update and approve results.
* **Points**: Numeric values assigned automatically or manually based on defined thresholds for KPIs.

***

### How It Works

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FPUVqWnP8mIFmBdiHB45D%2Fimage.png?alt=media&#x26;token=62c7cae1-2ed7-4c9f-8b90-a178eaca0906" alt=""><figcaption><p>Create New League - step by step</p></figcaption></figure>

{% stepper %}
{% step %}
### **1. League Setup**

Create a new league via:\
**Gamification > Leagues Management > New League**

Required fields:

* **League Name** and **Description**
* **Referees**: Minimum 1, maximum 5 users
* **Scoring Interval**: Weekly, biweekly, or monthly
* **Start / End Date** (optional)
* **League Logo** (optional)

{% hint style="info" %}
⚠️ If an end date is provided, it must be at least 28 days after the start date and no more than 365 days. If left empty, the league runs indefinitely.
{% endhint %}
{% endstep %}

{% step %}
**Metric Selection**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F6EQqYHGXqfsgctae262d%2Fimage.png?alt=media&#x26;token=4efa50ec-d3c9-42d4-baef-38980b19f421" alt=""><figcaption><p>Metric Selection</p></figcaption></figure>

Select which performance metrics will be scored. Categories include:

* **Project Management** (e.g., Lead Time, Predictability)
* **Development** (e.g., Rework Rate, Coding Efficiency)
* **Code Review**
* **Code Quality**
* **Security**
* **Symptoms**

{% hint style="info" %}
These metrics will be used for **automatic scoring**.
{% endhint %}
{% endstep %}

{% step %}
**KPI Scoring**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FQWGkELzEHWKpi2OU0HuL%2Fimage.png?alt=media&#x26;token=fd5d44fc-d66f-4a51-b38e-ce920dce41ab" alt=""><figcaption><p>KPI Scoring</p></figcaption></figure>

Define scoring thresholds for each metric. Example:

* Cycle Time < 3 days → 3 points
* 3–10 days → 1 point
* ≥10 days → 0 points

{% hint style="warning" %}
Ensuring logical consistency of thresholds is the user’s responsibility.
{% endhint %}
{% endstep %}

{% step %}
**Manual KPIs (Optional)**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F8qvsP4jiFxrZ43w8P2XP%2Fimage.png?alt=media&#x26;token=e2fc62eb-b679-4948-9ad0-a170f3b72cd0" alt=""><figcaption><p>Manual KPIs</p></figcaption></figure>

Define custom KPIs that will be scored manually by referees.

Each manual KPI requires:

* Label (Name)
* Description
* Maximum Points
{% endstep %}

{% step %}
**Team Selection**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FGQhq7q6JE4ArZKPVXDU1%2Fimage.png?alt=media&#x26;token=a13da56d-8eb4-4abc-8a3e-46dca80374b1" alt=""><figcaption><p>Team Selection</p></figcaption></figure>

Select which teams will participate in the league. Only teams with data available for the selected metrics can be added.
{% endstep %}

{% step %}
**Final Review and Start**

Review all settings and click **Create League** to launch.
{% endstep %}
{% endstepper %}

***

#### Round Management:

Each league generates a scoring **round** automatically based on the selected interval.

League referees manage rounds via:\
**League Management > Manage Rounds**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FmS5vgiEwenaAFnkiqdM5%2Fimage.png?alt=media&#x26;token=caad7134-81c2-481a-9514-162670fc7dcf" alt=""><figcaption><p>Manage Rounds</p></figcaption></figure>

**Round Details:**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FbXzMiU36AnTvTitQouek%2Fimage.png?alt=media&#x26;token=d076476f-bd62-40ef-b23a-7a6710ff08f5" alt=""><figcaption></figcaption></figure>

* **Round Date**: The date when scores are calculated.
* **States**:
  * `Scheduled for the next round`
  * `In Progress`
  * `Pending Approval`
  * `Approved`
  * `Failed`
  * `Cancelled`

Referees can **review, edit, and approve** round scores.

***

#### ✏️ Update Scores

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F4YW842xAinNry9mS3pDX%2Fimage.png?alt=media&#x26;token=0ad3bb66-c443-4dc2-a482-b7fb9d958724" alt=""><figcaption><p>Update Scores for a round</p></figcaption></figure>

For each KPI, referees can:

* View the actual value (Value)
* Check the automatically calculated score (Calculated Score)
* Manually update scores if needed (Update)
* Approve scores (Approve)

> Use the **Recalculate** button (top right) to refresh all automatic scores.

***

#### 📊 Leaderboard

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FEpKnYL0ahYogJXgWG8Cb%2Fimage.png?alt=media&#x26;token=1500f60a-2af6-45e8-ad9b-f622e41a2579" alt=""><figcaption><p>Leaderboard</p></figcaption></figure>

The leaderboard displays team rankings based on their total points:

* Track progress over time
* View historical rounds
* See which metrics contributed to team scores.

***

#### 🔐 Authorization

The following actions can only be performed by authorized users:

* Creating and editing leagues (Role: Gamification Admin)
* Defining metrics and scoring rules (Role: Gamification Admin)
* Approving round results (Role: League Referee)

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FTWLd8ShRmOvdnHYsHXGk%2Fimage.png?alt=media&#x26;token=f73a7ee9-709a-4404-bd1e-d7282aa9e519" alt=""><figcaption><p>Manage user roles</p></figcaption></figure>
