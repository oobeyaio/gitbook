---
description: >-
  This symptom refers to a high level of technical debt, as reported by the
  static code analysis tool Sonar.
---

# S6- High technical debt on Sonar

### **Why is this a symptom?**

This symptom refers to a high level of technical debt, as reported by the static code analysis tool Sonarqube/SonarCloud. Technical debt is a measure of the cost of maintaining a codebase, including the cost of fixing defects and adding new features.&#x20;

High technical debt can be an indication of poor coding practices, lack of attention to code quality, or lack of time dedicated to code maintenance.&#x20;

High technical debt can lead to increased maintenance costs, reduced code maintainability, and decreased ability to add new features in the future. It can also lead to decreased code quality, increased risk of defects and vulnerabilities, and a decrease in developer productivity.&#x20;

High technical debt can be considered a symptom of the development process, indicating that the team may need to focus on improving their coding practices, increasing time dedicated to code maintenance, and paying down the debt.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #quality\_risk, #low\_productivity, #slow\_delivery, #low\_developer\_satisfaction
{% endhint %}

### **Possible Causes**

* Lack of attention to code quality
* Pressure to meet deadlines
* Lack of time dedicated to code maintenance
* Use of poor coding practices
* Lack of training or knowledge on good coding practices
* Lack of established code review processes

### **Improvement Areas**

* Increase the focus on code quality
* Prioritize the reduction of technical debt
* Incorporate code review and maintenance into the development process
* Encourage collaboration and knowledge sharing on clean code
* Encourage and facilitate refactoring within the team

### **Detection Method**

Oobeya detects this symptom if the level of technical debt on Sonar for the selected period exceeds the specified threshold.

**Formula:** (sonar\_technical\_debt) > (threshold) in the selected period

**Example:** During each of the **last 3 months**, the team has consistently had **more than 180 minutes** of technical debt on Sonar.

