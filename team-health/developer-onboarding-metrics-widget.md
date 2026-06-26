---
description: >-
  Learn how to feed onboarding data into Oobeya and interpret the Developer
  Onboarding Metrics widget.
---

# Developer Onboarding Metrics Widget

The **Developer Onboarding Metrics** widget helps teams understand how effectively new developers onboard into their teams. It combines hire date, first commit, early task effort, and support data to show how quickly developers become active and how much support they need during onboarding.

The widget is available on the **Team Scorecard** screen and can be filtered by the selected team and date range.

### What the widget shows

The widget provides both a summary view and a developer-level table.

It tracks the following metrics:

| Metric                | Description                                                                                                  |
| --------------------- | ------------------------------------------------------------------------------------------------------------ |
| Hires                 | Number of developers hired within the selected period.                                                       |
| Avg. Commit Days      | Average number of days between hire date and first commit.                                                   |
| Avg. Effort Fit (%)   | Average ratio of estimated effort to actual effort for the developer's first four completed tasks.           |
| Avg. Support Requests | Average number of support requests created before the first commit.                                          |
| Avg. Total Support    | Average total number of support requests and incidents created before the first commit.                      |
| Terminations          | Number of developers whose termination date falls within the selected period.                                |
| Terminated            | Percentage of terminated developers who left within the first half of the selected period after being hired. |

{% hint style="info" %}
All averages exclude developers whose corresponding field has no data.
{% endhint %}

### Prerequisites

Before using the Developer Onboarding Metrics widget, make sure that:

1. The user exists in Oobeya.
2. The user has a developer profile.
3. The developer profile is linked to the relevant version control and issue tracking accounts.
4. The developer is assigned to at least one team.
5. API requests include the following header:

```http
Oobeya-API-Key: <your-key>
```

### Data Integration Flow

To populate the widget, follow these steps:

1. Register the developer's hire date and termination date.
2. Retrieve the developer's first commit data from Oobeya.
3. Calculate onboarding support metrics in your own ticketing system.
4. Push the calculated support metrics to Oobeya.
5. View the consolidated report in the widget.

### Step 1: Register Hire and Termination Dates

#### Create a new user

Use the following endpoint to create a new user with hire and termination information.

```http
POST /apis/v1/users
Content-Type: application/json
Oobeya-API-Key: <your-key>
```

```json
{
  "username": "jane.doe",
  "email": "jane.doe@company.com",
  "fullName": "Jane Doe",
  "roles": ["ROLE_USER"],
  "hireDate": "2024-08-17T00:00:00+03:00",
  "terminationDate": null
}
```

#### Update an existing user

Use the following endpoint to add or update hire and termination dates for an existing user.

```http
PUT /apis/v1/users/{userId}
Content-Type: application/json
Oobeya-API-Key: <your-key>
```

```json
{
  "username": "jane.doe",
  "email": "jane.doe@company.com",
  "fullName": "Jane Doe",
  "roles": ["ROLE_USER"],
  "hireDate": "2024-08-17T00:00:00+03:00",
  "terminationDate": "2025-08-17T00:00:00+03:00"
}
```

| Field             | Description                                                                                    |
| ----------------- | ---------------------------------------------------------------------------------------------- |
| `hireDate`        | Developer's hire date in ISO 8601 format. Required for onboarding metrics.                     |
| `terminationDate` | Developer's termination date in ISO 8601 format. Send `null` if the developer is still active. |

### Step 2: Retrieve First Commit Data

After users are registered, Oobeya can return each developer's first commit based on their hire date.

```http
GET /apis/v1/reports/onboarding/first-commits?hireDateFrom=2024-08-17T00:00:00+03:00
Oobeya-API-Key: <your-key>
```

| Parameter      | Description                                                              |
| -------------- | ------------------------------------------------------------------------ |
| `hireDateFrom` | Returns first commit data for users whose hire date is after this value. |

#### Example response

```json
[
  {
    "userId": "60a1b2c3d4e5f6a7b8c9d0e1",
    "developerId": "60a1b2c3d4e5f6a7b8c9d0e2",
    "username": "jane.doe",
    "userEmail": "jane.doe@company.com",
    "fullName": "Jane Doe",
    "hireDate": "2025-03-17T00:00:00",
    "firstCommitDate": "2025-03-24T09:14:33",
    "firstCommitSha": "a3f9d1e2b7c04..."
  }
]
```

Use the `username`, `userEmail`, and `firstCommitDate` values to calculate support request and incident counts in your own ticketing system.

{% hint style="info" %}
First commit data is calculated by Oobeya. You do not need to push it back.
{% endhint %}

### Step 3: Push Onboarding Support Metrics

Support request and incident metrics are calculated on the customer side, using ticketing system data.

Once calculated, these values can be pushed to Oobeya.

#### Single metric upsert

```http
POST /apis/v1/reports/onboarding/metrics
Content-Type: application/json
Oobeya-API-Key: <your-key>
```

```json
{
  "username": "jane.doe",
  "email": "jane.doe@company.com",
  "type": "REQUEST",
  "count": 3
}
```

#### Bulk metric upsert

```http
POST /apis/v1/reports/onboarding/metrics/bulk
Content-Type: application/json
Oobeya-API-Key: <your-key>
```

```json
{
  "items": [
    {
      "username": "jane.doe",
      "email": "jane.doe@company.com",
      "type": "REQUEST",
      "count": 3
    },
    {
      "username": "jane.doe",
      "email": "jane.doe@company.com",
      "type": "INCIDENT",
      "count": 4
    },
    {
      "username": "john.smith",
      "email": "john.smith@company.com",
      "type": "REQUEST",
      "count": 5
    },
    {
      "username": "john.smith",
      "email": "john.smith@company.com",
      "type": "INCIDENT",
      "count": 6
    }
  ]
}
```

| Field      | Description                                                             |
| ---------- | ----------------------------------------------------------------------- |
| `username` | Oobeya first tries to match the user by username.                       |
| `email`    | Used as a fallback if the username cannot be matched.                   |
| `type`     | Use `REQUEST` for support requests and `INCIDENT` for incident tickets. |
| `count`    | Pre-calculated ticket count from the customer's ticketing system.       |

{% hint style="info" %}
These endpoints use upsert logic. Calling the endpoint again with a new count replaces the previous value.
{% endhint %}

### Step 4: Read the Consolidated Report

After the data is pushed, you can retrieve the consolidated onboarding report.

```http
GET /apis/v1/reports/onboarding/metrics/report?hireDateFrom=2024-08-17T00:00:00+03:00
Oobeya-API-Key: <your-key>
```

This endpoint joins user data, first commit data, effort data, and custom onboarding metrics. It returns one row per developer.

This is the same data source used by the widget table.

### Metric Definitions

#### Time to First Commit

Measures how many calendar days passed between the developer's hire date and first Git commit.

```
Commit Days = First Commit Date - Hire Date
```

The widget header shows the average across developers who have first commit data.

#### First Four Tasks Effort Fit

Measures whether the developer completed their first four assigned tasks within the estimated effort.

```
Effort Fit (%) = Target Effort / Actual Effort × 100
```

| Field         | Description                                                  |
| ------------- | ------------------------------------------------------------ |
| Target Effort | Sum of estimated effort for the first four qualifying tasks. |
| Actual Effort | Sum of actual effort for the same tasks.                     |

Tasks without both estimated effort and actual effort values are excluded.

A value below `100%` means the actual effort was higher than the estimated effort.

#### Support Requests

The number of request tickets opened by the developer between their hire date and first commit date.

Examples can include access requests, environment setup issues, or other onboarding-related requests.

This value is calculated in the customer's ticketing system and pushed to Oobeya with:

```json
"type": "REQUEST"
```

#### Support Incidents

The number of incident tickets opened by the developer between their hire date and first commit date.

This value is calculated in the customer's ticketing system and pushed to Oobeya with:

```json
"type": "INCIDENT"
```

#### Total Support

Total Support is calculated automatically by Oobeya.

```
Total Support = Support Requests + Support Incidents
```

#### Terminated

The **Terminated** value shows whether a developer left within the first half of the selected date range after being hired.

For example:

| Selected Period | Terminated = Yes if the developer left within |
| --------------- | --------------------------------------------- |
| 1 year          | 6 months after hire date                      |
| 6 months        | 3 months after hire date                      |
| 3 months        | 1.5 months after hire date                    |

This helps identify early turnover during the onboarding period.

### Table Columns

| Column            | Description                                                                                      |
| ----------------- | ------------------------------------------------------------------------------------------------ |
| Name              | Developer's full name.                                                                           |
| Role              | Developer's role or title.                                                                       |
| Teams             | Teams the developer belongs to.                                                                  |
| Hiring Date       | Developer's hire date.                                                                           |
| First Commit Date | Date and time of the developer's first commit.                                                   |
| Commit Days       | Number of calendar days from hire date to first commit.                                          |
| Target Effort     | Sum of estimated effort for the developer's first four qualifying tasks.                         |
| Actual Effort     | Sum of actual effort for the same tasks.                                                         |
| Effort Fit (%)    | Target effort as a percentage of actual effort.                                                  |
| Support Requests  | Number of request tickets before first commit.                                                   |
| Support Incidents | Number of incident tickets before first commit.                                                  |
| Total Support     | Sum of support requests and incidents.                                                           |
| Termination Date  | Developer's termination date, if available.                                                      |
| Terminated        | Shows whether the developer left within the first half of the selected period after being hired. |

### Excel Export

The widget includes an Excel export option.

The exported file contains one row per developer and includes the same columns shown in the widget table.

{% hint style="info" %}
The Excel export does not include the summary header. It only includes developer-level rows.
{% endhint %}

### Missing Data Behavior

If data is missing, the widget displays `-`.

| Missing Data                                   | Widget Behavior                                                  |
| ---------------------------------------------- | ---------------------------------------------------------------- |
| No first commit data                           | First commit related fields show `-`.                            |
| No support metrics pushed                      | Support Requests, Support Incidents, and Total Support show `-`. |
| No tasks with both estimated and actual effort | Effort related fields show `-`.                                  |
| Missing values in summary calculations         | `-` values are excluded from averages.                           |
