---
icon: code-branch
---

# Git Analytics - Metric Definitions

## Git Analytics - Work Type Metrics

Git Analytics tools analyze all atomic software development activities and generate metrics to help teams better understand the development process.&#x20;

[Oobeya](https://oobeya.io/) analyzes all commits in a coding repository and runs an algorithm to identify the work type of each code change. These work-type metrics shouldn't be used as a target for development teams, it's just a tool that enables them to identify the signals of their development process. Oobeya leverages these metrics to detect symptoms of the development process. See the related symptoms below:

{% content-ref url="../../team-insights-and-symptoms/symptoms-catalog/s1-recurring-high-rework-rate.md" %}
[s1-recurring-high-rework-rate.md](../../team-insights-and-symptoms/symptoms-catalog/s1-recurring-high-rework-rate.md)
{% endcontent-ref %}

{% content-ref url="../../team-insights-and-symptoms/symptoms-catalog/s2-recurring-high-cognitive-load.md" %}
[s2-recurring-high-cognitive-load.md](../../team-insights-and-symptoms/symptoms-catalog/s2-recurring-high-cognitive-load.md)
{% endcontent-ref %}

<figure><img src="../../.gitbook/assets/image (408).png" alt=""><figcaption><p>Git Analytics Work Types</p></figcaption></figure>

### 1. New Work&#x20;

"New work" is a measure of how much new and fresh work has been done in a given period. The interest in new work in organizations depends on the type of product and work (new projects, maintenance projects, transformation, etc.).

For a task to be considered "new work", the code snippets should not replace others, but rather be written from scratch and independently. Lines added as part of an existing change (git hunk) do not count as new work.

### 2. Refactor&#x20;

Developing new features and maintaining existing code often requires revisiting old (legacy) code snippets. As codebases age, preserving code and keeping things up to date are critical goals for organizations.&#x20;

For work in Oobeya to be considered a "Refactor", at least 3 weeks (industry standard) should have passed since the last addition or modification of old work.&#x20;

In teams with a high refactor rate, managers (Product Owners, Team Leaders, etc.) need to balance such tasks proportionally with new features. Having high technical debt is undesirable, but having a stagnant (unimproved) product is even worse. The code refactor rate is an important indicator of the project's health.

### 3. Help Others

It is a measure of how much a software developer has helped to maintain and/or fix another developer's recent code (in 3 weeks).

For work in Oobeya to count as "help others", the block of code worked on together should not be older than 3 weeks. (If it's older than 3 weeks, it's considered a refactoring activity).

The Help Others ratio provides insight into the team's collaborative (pair) working culture and knowledge sharing within the team.

### 4. Churn / Rework

Code complexity, leaving technical debt, or rewriting/deleting code shortly after it is written is considered a natural part of the development process. Engineers often test different solutions, iterate, and investigate a problem.

Churn levels vary among teams, individuals, project types, and where those projects are in the development life cycle. Different individuals and teams may have different levels of churn based on their workflows and the types of projects they are working on (i.e. a new problem, a known issue, a quick fix, etc.).

Tracking the churn value by iteration in Oobeya provides early visibility into issues that arise during development phases (lack of analysis, lack of know-how, high technical debt, workload distribution, etc.).

For a task in Oobeya to be considered Churn/Rework, the changes must be made by the same person and on a block of code no older than 3 weeks. (If it's older than 3 weeks, it's considered a refactor).

***

### Coding Efficiency&#x20;

Percentage of productive work. It is calculated by the sum of New Work + Refactor + Help Others.

This metric is measured and displayed at different levels (commit level, individual level, team level) in Oobeya. Tracking the Coding Efficiency metric enables early detection of symptoms that arise during development periods and helps team leaders improve the developer experience and reduce friction.

### Impact Score

The Impact Score is an approximate measure of how much cognitive load the engineer performed when developing a commit. It is measured and shown at different levels in Oobeya (commit level, individual level, team level).

Oobeya identifies the cognitive load of team members during development cycles by tracking the Impact Score.

Team and individual health symptoms (burnout, overload, etc.) and working practice symptoms (knowledge silos, etc.) are identified by utilizing the Impact Score. See the related symptom below:

{% content-ref url="../../team-insights-and-symptoms/symptoms-catalog/s2-recurring-high-cognitive-load.md" %}
[s2-recurring-high-cognitive-load.md](../../team-insights-and-symptoms/symptoms-catalog/s2-recurring-high-cognitive-load.md)
{% endcontent-ref %}

***

### Setting The Threshold For Work Type Calculation

Oobeya analyzes commit activities by running an algorithm to identify the type of work for each code change. The algorithm's default threshold is 21 days (3 weeks), but users can customize it for their specific use cases. To change the threshold:

1. Navigate to Administration > Gitwiser & DORA Metrics > Git Analytics.
2. Set the threshold for Git work type calculation. (Default value: 21 days)

{% hint style="warning" %}
Changing this parameter will delete all commits and reanalyze them. Please note that analyzing all repositories will take time.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>
