---
description: >-
  Helps visualize developer activities to detect workload imbalances and
  unhealthy work practices.
---

# Activity Heatmap

The Oobeya **Activity Heatmap** module visualizes the daily activities of software development teams, helping analyze **workload distribution**, **contribution diversity**, and **developer experience**. It scores various activities such as commits, pull requests (code reviews), code changes, and comments, and presents trends over time in a heatmap format.

With this module, you can:

* Identify overloaded or under-contributing developers.
* Detect unbalanced workload distributions.
* Encourage fairer task sharing within teams.

***

### 1. Key Features

* Analysis by daily, weekly, monthly, quarterly, or custom time range
* Tracking of PR, commit, code line changes, and code review comments
* Color-coded heatmap view by developer
* Developer Work Log with detailed contribution analysis
* Team selection and role-based filtering
* Working days filter (configured under Admin Panel > General Settings)

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FnEJ2Mw9DOl1Yt1LU0XiI%2Fimage.png?alt=media&#x26;token=6524f1c1-2b3b-4bcd-827f-d53644ea5972" alt=""><figcaption><p>Activity Heatmap Overview</p></figcaption></figure>

***

### 2. Scoring Mechanism

In the **Activity Heatmap** module, developer activities are calculated using data from different contribution types and normalized for visualization in the heatmap.

#### 2.1. Daily Normalization & Z-Score

1. The highest-scoring developer each day is taken as the 100% reference.
2. Other developers are scaled against this maximum → `rank_ratio`.
3. Daily contributions are normalized.
4. The average ratio and standard deviation of all developers are calculated.
5. Ratios are converted to **z-scores** and normalized into the 0–100 range.
6. These scores are mapped into color tones in the heatmap.

#### 2.2. Activity-Based Score Formulas

**2.2.1. Commit Activities**

```
COMMIT_SCORE = (COMMITS × commit_coeff) +
               (LINES_ADDED × added_coeff) +
               (LINES_DELETED × deleted_coeff) +
               (LINES_EDITED × edited_coeff)
```

**2.2.2. Pull Request Activities**

```
PR_OPEN_SCORE        = PRs Created × pr_open_coeff
PR_REVIEW_SCORE      = PR Reviews × pr_review_coeff
PR_APPROVAL_SCORE    = PR Approvals × pr_approve_coeff
PR_NEEDS_WORK_SCORE  = PR Needs Work × pr_needs_work_coeff
PR_COMMENT_SCORE     = PR Comments × pr_comment_coeff
```

**2.2.3. Total Score**

```
TOTAL_RANK_SCORE = COMMIT_SCORE + PR_OPEN_SCORE + PR_REVIEW_SCORE +
                   PR_APPROVAL_SCORE + PR_NEEDS_WORK_SCORE + PR_COMMENT_SCORE
```

**2.2.4. Heatmap Visualization**

* Normalized scores are mapped into color tones.
* Darker tones represent higher activity, lighter tones represent lower activity.

{% hint style="info" %}
This mechanism ensures **fair comparisons** across teams, allows organizations to adjust the impact of different activity types, and provides results that are easy to track visually.
{% endhint %}

***

### 3. Admin Panel Settings

Weight values are assigned to different activities. These coefficients determine how each activity type influences the overall heatmap score and visualization.

**Location:** `Administration > Activity Heatmap`

#### Coefficient Settings

For each activity type, you can define its weight on the total score.

<table><thead><tr><th width="211.52728271484375">Activity</th><th width="395.47412109375">Description</th><th>Default</th></tr></thead><tbody><tr><td>Commits</td><td>Number of commits made</td><td>2.0</td></tr><tr><td>Lines Added</td><td>Number of lines of code added</td><td>0.1</td></tr><tr><td>Lines Deleted</td><td>Number of lines of code deleted</td><td>0.1</td></tr><tr><td>Lines Edited</td><td>Number of lines of code modified</td><td>0.1</td></tr><tr><td>PRs Created</td><td>Number of pull requests created</td><td>1.0</td></tr><tr><td>PR Reviews</td><td>Number of code reviews performed</td><td>1.5</td></tr><tr><td>PR Approvals</td><td>Number of pull requests approved</td><td>0.25</td></tr><tr><td>PR Needs Work</td><td>Number of pull requests sent back for changes</td><td>0.5</td></tr><tr><td>PR Comments</td><td>Number of comments made on pull requests</td><td>1.0</td></tr></tbody></table>

<figure><img src="https://your-link.com/activity_heatmap_admin.png" alt=""><figcaption><p>Admin Panel – Activity Coefficients</p></figcaption></figure>

***

### 4. Dashboard Components

The **Activity Heatmap Dashboard** consists of multiple components to analyze daily developer activities from different perspectives. Each component visualizes contribution types, trends over time, and distribution within teams.

#### 4.1. Activity Heatmap

**Activity Heatmap** is the core component that visualizes developers’ daily activities. Each cell represents a developer’s contribution score for a given day.

* **Color Intensity**: The cell’s color reflects the developer’s performance level that day. Darker tones represent higher activity, lighter tones lower activity.
* **Normalized Scores**: Daily scores are normalized against the highest contribution of the day, ensuring fair comparisons between developers and across days.
* **Time Filters**: Analysis can be done daily, weekly, monthly, or within custom date ranges.

{% hint style="info" %}
The Activity Heatmap helps teams visually detect workload imbalances and quickly identify potential overload or low participation.
{% endhint %}

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FdzrUeZKfzaFD1eAfaVBn%2Fimage.png?alt=media&#x26;token=f314684d-e1d1-4008-aa3b-8a186e77f3a3" alt=""><figcaption><p>Activity Heatmap</p></figcaption></figure>

#### 4.2. Developer Work Log

The **Developer Work Log** provides a detailed list of daily activities for each developer within the selected date range. It provides the raw data behind the scores displayed in the heatmap in a tabular format.

This section shows:

* **Total score by developer** (normalized)
* **Total activity counts** (commits, PRs, comments, etc.)
* **Daily contribution cells** with activity counts and corresponding points

{% hint style="info" %}
The goal is not only to view general scores, but also to analyze in detail which days each developer was more active and which types of contributions they focused on.
{% endhint %}

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Frw1yvXBqpUwtR0KZJARR%2Fimage.png?alt=media&#x26;token=147fe9f8-45f8-46c4-9084-d62661fc99be" alt=""><figcaption><p>Developer Work Log</p></figcaption></figure>

#### 4.3. Filters

The **Activity Heatmap** module offers various filtering options to enable more focused and meaningful analysis:

* **Working Days**: Ensures scores are calculated only based on your company’s defined working days (e.g., Monday–Friday). Configurable in **Admin > General Settings**.
* **Team Selection**: Select one or more teams to view only their activities in the heatmap.
* **Role Filter**: Choose specific roles (e.g., Developer, QA) to include only those roles in the analysis. Non-development contributions can be excluded.
* **Activity Type**: Select desired activity types (commits, PR creation, reviews, comments, etc.) to filter the heatmap by those contributions.

{% hint style="info" %}
With these filters, teams can gain more precise and targeted insights for specific time periods, roles, or activity types.
{% endhint %}

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FG2L0nFndIQtLHR7Azfy0%2Fimage.png?alt=media&#x26;token=fb40c6c8-62e3-476c-8cf4-87458a748cc9" alt="" width="461"><figcaption><p>Module Filters</p></figcaption></figure>

***

### 5. Data Sources

The **Activity Heatmap** module aggregates data from different development tools and contribution types to calculate developer activities.

* **Commits**: Commit records from Git repositories (_Azure DevOps, GitHub, GitLab, Bitbucket, Gitea_)
* **Code Changes**: Lines added, deleted, and modified
* **Pull Requests**: Created PRs (GitHub, GitLab, Bitbucket, Azure Repos, etc.)
* **Code Reviews**: Reviews performed, PR approvals, or rejections
* **Comments**: Comments made on pull requests
* **Developer Profiles**: Only developers defined in Oobeya are included in the analysis

{% hint style="info" %}
Data from these sources is weighted with the coefficients defined in the admin panel and converted into the total score.
{% endhint %}

***

### 6. Recommended Use Cases

The **Activity Heatmap** module can be used in different scenarios to make team activities fairer, more balanced, and more effective:

<table><thead><tr><th width="201.9287109375">Scenario</th><th>Benefit</th></tr></thead><tbody><tr><td><strong>Sprint Reviews</strong></td><td>Analyzes contribution intensity at the end of a sprint, supporting healthier retrospectives.</td></tr><tr><td><strong>Workload Balance</strong></td><td>Identifies overloaded or low-participation team members to rebalance task assignments.</td></tr><tr><td><strong>Engagement &#x26; Motivation</strong></td><td>Helps spot developers with consistently low contributions and supports motivation-boosting actions.</td></tr><tr><td><strong>PR Review Culture</strong></td><td>Measures the review culture of teams through PR reviews, comments, and approvals.</td></tr><tr><td><strong>Performance Improvement</strong></td><td>Tracks collaboration and contribution diversity to uncover training and coaching needs.</td></tr></tbody></table>

{% hint style="info" %}
This module is not only for measuring individual performance but also a powerful team management tool for monitoring **engagement levels** and **workload balance**.
{% endhint %}

***

### 7. FAQ (Frequently Asked Questions)

<details>

<summary>Why are some developers not visible?</summary>

Only developers registered in the Oobeya platform and assigned to active teams are included in the analysis.

</details>

<details>

<summary>How are scores calculated?</summary>

Each activity contribution is multiplied by the coefficients defined in the admin panel. These scores are then normalized daily.

</details>

<details>

<summary>What does the working days filter do?</summary>

It excludes non-working days (such as weekends) from the analysis.

</details>
