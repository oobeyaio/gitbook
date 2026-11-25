---
description: >-
  Technical debt, security, reliability, maintainability, and codebase health
  from SonarQube or SonarCloud.
---

# Code Quality Analytics

Code Quality Analytics uses SonarQube or SonarCloud data to show technical debt, security, reliability, maintainability, and codebase health. It also includes the Total Code Quality Index (TCQI).

See [Total Code Quality Index](https://docs.oobeya.io/quality-analytics/total-code-quality-index-tcqi).

### Core Quality Metrics

| Metric                           | What it measures                                                                                |
| -------------------------------- | ----------------------------------------------------------------------------------------------- |
| **Technical Debt - Overall**     | Estimated remediation time required to fix all maintainability issues in the analyzed codebase. |
| **Technical Debt - New Period**  | Technical debt introduced during the selected period or on new code.                            |
| **Technical Debt per Developer** | Technical debt attributed to each developer based on source-control author information.         |
| **Added Technical Debt**         | Technical debt introduced during the selected period.                                           |
| **Code Quality Issues**          | Total number of quality issues detected by the connected code-quality platform.                 |
| **Bugs**                         | Number of reliability issues.                                                                   |
| **Vulnerabilities**              | Number of security issues.                                                                      |
| **Code Smells**                  | Number of maintainability issues.                                                               |
| **Duplicated Lines (%)**         | Percentage of code identified as duplicated.                                                    |
| **Test Coverage (%)**            | Percentage of analyzed code covered by tests.                                                   |
| **Lines of Code**                | Total analyzed codebase size used as an input for normalization and quality analysis.           |

### Severity and Risk Metrics

| Metric                                      | What it measures                                                                      |
| ------------------------------------------- | ------------------------------------------------------------------------------------- |
| **Blocker Issues**                          | Number of issues classified at the highest configured severity.                       |
| **High-Severity Issues**                    | Number of issues classified as high severity.                                         |
| **Medium-Severity Issues**                  | Number of issues classified as medium severity.                                       |
| **Low-Severity Issues**                     | Number of issues classified as low severity.                                          |
| **Security Severity - Blocker, Overall**    | Total blocker-level security issues in the analyzed codebase.                         |
| **Security Severity - High, Overall**       | Total high-severity security issues in the analyzed codebase.                         |
| **Security Severity - Blocker, New Period** | New blocker-level security issues introduced during the selected period.              |
| **Security Severity - High, New Period**    | New high-severity security issues introduced during the selected period.              |
| **Issue Risk Score**                        | Risk score calculated using issue severity, quality category, and remediation effort. |
| **Project Security Risk Score**             | Aggregated security risk for the analyzed project.                                    |
| **Project Reliability Risk Score**          | Aggregated reliability risk for the analyzed project.                                 |
| **Project Maintainability Risk Score**      | Aggregated maintainability risk for the analyzed project.                             |

The Issue Risk calculation follows this structure:

```
Issue Risk =
Severity Coefficient
× Quality Category Coefficient
× Remediation Coefficient
```

### Total Code Quality Index Metrics

| Metric                              | What it measures                                                                                                                |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Total Code Quality Index - TCQI** | Composite quality score based on issue severity, security, reliability, maintainability, remediation effort, and codebase size. |
| **Security Index**                  | Normalized score representing the security health of the codebase.                                                              |
| **Reliability Index**               | Normalized score representing reliability health.                                                                               |
| **Maintainability Index**           | Normalized score representing maintainability health.                                                                           |
| **Security Score / Rating**         | Overall security rating provided by the connected quality platform.                                                             |
| **Reliability Score / Rating**      | Overall reliability rating provided by the connected quality platform.                                                          |
| **Maintainability Score / Rating**  | Overall maintainability rating provided by the connected quality platform.                                                      |
| **TCQI Trend**                      | Change in Total Code Quality Index over time.                                                                                   |
| **Security Index Trend**            | Change in the Security Index over time.                                                                                         |
| **Reliability Index Trend**         | Change in the Reliability Index over time.                                                                                      |
| **Maintainability Index Trend**     | Change in the Maintainability Index over time.                                                                                  |

{% hint style="info" %}
TCQI coefficients can be configured under the Code Quality administration settings.
{% endhint %}
