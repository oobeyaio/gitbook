---
description: >-
  This symptom refers to a high level of vulnerabilities as reported by the
  static code analysis tool Sonar.
---

# S7- High vulnerabilities on Sonar

### **Why is this a symptom?**

This symptom refers to a high level of vulnerabilities as reported by the static code analysis tool Sonarqube/SoanrCloud. Vulnerabilities are security weaknesses in the code that can be exploited by attackers to gain unauthorized access or control of the system.&#x20;

High vulnerabilities can be an indication of poor coding practices, lack of attention to security, or lack of time dedicated to addressing vulnerabilities. High vulnerabilities can lead to increased risk of security breaches, decreased system reliability, and decreased trust in the system. It can also lead to decreased code quality, increased risk of defects, and decreased developer productivity.&#x20;

High vulnerabilities can be considered a symptom of the development process, indicating that the team may need to focus on improving their coding practices, increasing time dedicated to addressing vulnerabilities, and paying attention to security best practices.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #security\_risk
{% endhint %}

### **Possible Causes**

* Lack of attention to security
* Lack of time dedicated to addressing vulnerabilities
* Use of poor secure coding practices
* Lack of training or knowledge on secure coding practices
* Lack of established security review processes

### **Improvement Areas**

* Increase the focus on security
* Prioritize the reduction of vulnerabilities
* Implement tools and processes to identify and track vulnerabilities
* Encourage collaboration and knowledge sharing on secure coding practices
* Encourage and facilitate the use of security testing tools
* Regularly review and update secure coding policies and procedures

### **Detection Method**

Oobeya detects this symptom if the level of vulnerabilities on Sonar for the selected period exceeds the specified threshold.

**Formula:** (sonar\_vulnerabilities) > (threshold) in the selected period

**Example:** The team has **more than 0** open vulnerabilities on Sonar.

