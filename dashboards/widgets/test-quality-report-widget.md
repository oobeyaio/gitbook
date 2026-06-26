---
description: Let's learn about the Test Quality Report widget.
---

# Test Quality Report Widget

## Introduction

The **Test Quality Report** widget provides an overview of the quality and effectiveness of your team's tests, with metrics calculated from data collected through SonarQube integration. It tracks key aspects of code coverage, including overall coverage and coverage of new code changes, to help teams monitor their testing strategies and ensure high-quality standards across development cycles.

By leveraging SonarQube data, the widget offers a comprehensive view of test results, helping teams quickly identify areas for improvement, such as insufficient coverage or failed tests. With this insight, teams can take targeted actions to improve code reliability, reduce technical debt, and maintain robust quality control practices.

Key features of the Test Quality Report widget include:

* **Test Coverage**: Displays the percentage of code covered by tests.
* **Line Coverage**: Shows the percentage of code lines with corresponding tests.
* **New Code Coverage**: Focuses on coverage for new code changes, ensuring that recent updates are thoroughly tested.
* **Test Results**: Summarizes test outcomes, including the number of passed and failed tests.

This widget is essential for keeping track of your codebase’s health and optimizing your test coverage and testing efforts over time.

***

## 1- Team Unit Test Coverage&#x20;

This is the primary window displaying the test quality metrics for various teams. Here are the key components visible in this section:

<figure><img src="../../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure>

* **Coverage on New Code**: A high-level view of how much of the new code is covered by tests across the teams.&#x20;
* **Line Coverage on New Code**: This metric measures the percentage of new code lines covered by tests.
* **New Lines to Cover**: This section gives a total of **new lines** that need to be covered.
* **Coverage (%)**: Shows the overall test coverage percentage across all code lines.
* **Line Coverage (%)**: Displays the percentage of lines covered.
* **Lines to Cover**: Displays the total number of lines that still need coverage.
* **Passed Tests**: The total number of tests passed across all teams.
* **Failed Tests**: The number of failed tests.

**Team-Level Breakdown**: Below the team overview, each team has its own metrics. Each line shows the team’s specific data, including test coverage and the number of passed/failed tests.

***

## 2- Analysis Unit Test Coverage&#x20;

This section provides a more detailed breakdown of unit test coverage for different analyses, focusing on specific reports and codebases:

<figure><img src="../../.gitbook/assets/image (457).png" alt=""><figcaption></figcaption></figure>

* **Coverage on New Code (%)**: Like the previous section, it shows how much of the new code is covered by tests.
* **Line Coverage on New Code (%)**: Focuses on the line-level coverage of new code.
* **New Lines to Cover**: Shows the number of new lines that need coverage.
* **Coverage (%)**: The overall coverage of code in the analysis.
* **Line Coverage (%)**: The line coverage percentage.
* **Lines to Cover**: The total lines that still need to be covered.
* **Passed Tests**: Total number of passed tests.
* **Failed Tests**: Number of failed tests.

**Analysis-Specific Data**: Each Sonarqube analysis is listed with specific coverage, passed tests, failed tests, and coverage percentage data. These analyses show how well the tests are covering the code in individual projects or branches.

***

## **3- Team Unit Test Coverage Report (Chart View)**

The **Team Unit Test Coverage Report** provides a graphical representation of test coverage trends over time, helping teams track their testing progress and identify areas for improvement. This section includes a bar chart that displays key metrics related to test coverage for each month.

<figure><img src="../../.gitbook/assets/image (458).png" alt=""><figcaption></figcaption></figure>

**Trends Over Time**:

* The **x-axis** represents months, allowing teams to track coverage changes over time.
* The **y-axis** represents the scale of each metric in terms of lines or percentage, making it easy to assess how coverage metrics have shifted over the months.

This chart enables teams to spot trends in their test coverage, identify areas that require attention, and make data-driven decisions to improve their testing efforts.

***

## Metric Definitions

#### **Coverage on New Code (%)**

**Formula**: (New Covered Condition + New Covered Lines) / (New Condition to Cover + New Lines to Cover) × 100\
**Definition**: The percentage of new code (both conditions and lines) that has been covered by tests. It combines the coverage of new conditions and new lines.

#### **Line Coverage on New Code (%)**

**Formula**: New Covered Lines / New Lines to Cover × 100\
**Definition**: The percentage of new lines covered by tests out of the total new lines in the codebase.

#### **New Lines to Cover**

**Formula**: Sum of new lines to cover values\
**Definition**: The total number of new lines in the codebase that require coverage through unit tests.

#### **Coverage (%)**

**Formula**: (Covered Condition (CT) + Covered Lines (LC)) / (Condition to Cover (B) + Lines to Cover (EL)) × 100\
**Definition**: The combined coverage percentage of conditions and lines in the codebase. It indicates how much of the codebase has been covered by unit tests.

#### **Line Coverage (%)**

**Formula**: Covered Lines / Lines to Cover × 100\
**Definition**: The percentage of covered lines relative to the total lines that need to be covered by tests.

#### **Lines to Cover**

**Formula**: Sum of lines to cover values\
**Definition**: The total number of lines in the codebase that still need to be covered by tests.

#### **Passed Tests**

**Formula**: Sum of passed test values\
**Definition**: The total number of tests that passed during the testing cycle.

#### **Failed Tests**

**Formula**: Sum of failed test values\
**Definition**: The total number of tests that failed during the testing cycle.

#### **Team Count**

**Definition**: Displays the number of teams added in the analysis. If a team has a sub-team, it shows the count of sub-teams included.

#### **Total Lines**

**Definition**: The total number of lines in the codebase.

#### **Status**

**Definition**: Indicates whether the last scan in SonarQube was successful or failed.

***

### **Conclusion**

The **Test Quality Report Widget** is an essential tool for teams looking to maintain high standards of code quality. By providing insights into test coverage, both overall and on new code, as well as tracking test results, this widget empowers teams to continuously monitor and improve their testing efforts.

With data collected via SonarQube integration, the widget offers reliable, up-to-date metrics that can help identify gaps in coverage, track trends over time, and ensure that both new and existing code are thoroughly tested. Teams can use the **Test Quality Report Widget** to make informed decisions, reduce technical debt, and foster a culture of quality within the development process.

By regularly reviewing the metrics and trends presented in the widget, you can ensure that your test coverage is improving, issues are detected early, and your codebase remains reliable and maintainable.

