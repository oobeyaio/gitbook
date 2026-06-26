# Total Code Quality Index (TCQI)

The **Total Code Quality Index (TCQI)** is a composite metric in Oobeya that quantifies code quality by analyzing SonarQube issue data through multiple lenses: **severity**, **category impact** (security, reliability, maintainability), **remediation effort**, and **codebase volume**. It provides engineering leaders with a clear, standardized, and customizable way to monitor and improve software quality.

***

## What TCQI Measures

The TCQI goes beyond raw issue counts. It evaluates:

* **How risky issues are**, based on severity and fix effort.
* **What impact they have** across key quality dimensions.
* **How clean the codebase is** by factoring in total code volume.
* **How the project compares to an ideal maximum** through normalization.

This results in a set of actionable, easy-to-compare indices:

* **Total Code Quality Index (TCQI)**
* **Security Index**
* **Reliability Index**
* **Maintainability Index**

***

## Core Concepts

**TCQI** is built on **three core inputs** from SonarQube:

<table><thead><tr><th width="214.99365234375">Dimension</th><th>Description</th></tr></thead><tbody><tr><td><strong>Severity</strong></td><td>Indicates how critical an issue is (Blocker, High, Medium, etc.).</td></tr><tr><td><strong>Quality Categories</strong></td><td>Reflects the issue’s domain: <strong>Security</strong>, <strong>Reliability</strong>, <strong>Maintainability</strong>. An issue may belong to more than one category.</td></tr><tr><td><strong>Remediation Effort</strong></td><td>The estimated time required to fix the issue (e.g., 10 minutes, 8 hours, etc.).</td></tr></tbody></table>

These inputs are transformed into scores using **configurable coefficients** defined by your organization.

***

## Configurable Coefficients

All coefficients can be customized in **Admin Settings > Code Quality > Code Quality Index**.

#### 🔸 Severity Coefficients

| Severity | Coefficient |
| -------- | ----------- |
| High     | 0.6         |
| Medium   | 0.3         |
| Low      | 0.1         |

#### 🔸 Quality Category Coefficients

| Category        | Coefficient |
| --------------- | ----------- |
| Security        | 0.55        |
| Reliability     | 0.35        |
| Maintainability | 0.1         |

***

## Step-by-Step Calculation

### 1. **Calculate Issue Risk Scores**

Each issue is scored independently per quality category it belongs to:

```
Issue_Risk_Score = Severity_Coefficient × Category_Coefficient × Remediation_Effort
```

Because issues may belong to multiple categories, the same issue may contribute to multiple risk scores (e.g., both Security and Reliability).

***

### 2. **Calculate Project-Level Category Risk Scores**

For each category:

```
Project Category Risk Score = Sum(Issue Risk for that category)

Project Security Risk Score = Sum(Security_Issue_Risk_Score)
Project Reliability Risk Score = Sum(Reliability_Issue_Risk_Score)
Project Maintainability Risk Score = Sum(Maintainability_Issue_Risk_Score)
```

***

### 3. **Final** Total Code Quality Index (**TCQI) Formula**

```
Total_Risk_Score = Sum(Issue_Risk_Score)

TCQI = 5 × (1− (Total_Risk_Score / (Lines_of_Code + Total_Risk_Score)​)
```

***

## Why Use TCQI?

* **Standardized and Scalable**: Works across small and large codebases alike.
* **Actionable**: Highlights critical areas in security, reliability, or maintainability.
* **Customizable**: Adapt coefficients to align with your company’s engineering standards.
* **Measurable Over Time**: Track quality regressions or improvements release by release.

***

## Where to Configure

To tailor the TCQI model to your organization:

Go to:\
&#xNAN;**`Admin Settings > Code Quality > Code Quality Index`**

There, you can:

* Define severity weights
* Set quality category priorities

***

## Summary

Oobeya’s Total Code Quality Index provides a **balanced, flexible, and insightful view** of your engineering organization’s code health. It connects static code analysis to strategic engineering decisions—helping you drive long-term quality improvements.
