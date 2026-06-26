---
description: >-
  This symptom refers to a high level of code quality bugs as reported by the
  static code analysis tool Sonar.
---

# S8- High code quality bugs on Sonar

### **Why is this a symptom?**

This symptom refers to a high level of code quality bugs as reported by the static code analysis tool Sonarqube/SonarCloud.&#x20;

Code quality bugs are issues in the code that can negatively impact the maintainability, performance, or functionality of the system.&#x20;

High code quality bugs can be an indication of poor coding practices, lack of attention to code quality, or lack of time dedicated to code review and maintenance.&#x20;

High code quality bugs can lead to increased maintenance costs, reduced code maintainability, and decreased ability to add new features in the future. It can also lead to decreased code quality, increased risk of defects, and decreased developer productivity.&#x20;

High code quality bugs can be considered a symptom of the development process, indicating that the team may need to focus on improving their coding practices, increasing time dedicated to code review and maintenance, and paying attention to code quality best practices.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #quality\_risk
{% endhint %}

### **Possible Causes**

* Lack of attention to code quality
* Lack of time dedicated to code review and maintenance
* Use of poor coding practices
* Lack of training or knowledge on good coding practices
* Lack of established code review processes

### **Improvement Areas**

* Increase the focus on code quality
* Prioritize the reduction of code-quality bugs
* Implement tools and processes to identify and track vulnerabilities
* Encourage collaboration and knowledge sharing on secure coding practices
* Encourage and facilitate automated testing

### **Detection Method**

Oobeya detects this symptom if the level of bugs on Sonar for the selected period exceeds the specified threshold.

**Formula:** (sonar\_bugs) > (threshold) in the selected period

**Example:** The team has **more than 0** open code quality bugs on Sonar.
