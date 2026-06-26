---
description: >-
  This symptom refers to a high number of pull requests that are submitted and
  merged quickly, without adequate code review and testing.
---

# S10 - Lightning Pull Requests

### **Why is this a symptom?**

This symptom refers to a high number of pull requests that are submitted and merged quickly, without adequate code review and testing.&#x20;

Lightning pull requests can be an indication of a lack of established code review processes, lack of attention to code quality, or lack of team cohesion.&#x20;

Lightning pull requests can lead to poor-quality code being merged into the main codebase, increased risk of defects, and decreased code maintainability. It can also lead to decreased developer productivity and a lack of accountability among the team.&#x20;

Lightning pull requests can be considered a symptom of the development process, indicating that the team may need to focus on improving their code review processes, increasing time dedicated to review and testing, and paying attention to code quality best practices.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #quality\_risk
{% endhint %}

### **Possible Causes**

* Lack of established code review process
* Lack of time dedicated to code review
* High pressure to meet deadlines
* Lack of attention to code quality
* Lack of team cohesion
* Lack of clear communication of the code review process
* Lack of team accountability
* Insufficient training or knowledge on the code review process

### **Improvement Areas**

* Establish a clear code review process
* Allocate sufficient time for code review
* Encourage collaboration and knowledge sharing
* Regularly review and update the code review process
* Provide training or knowledge on the code review process

### **Detection Method**

Oobeya detects this symptom if the number of lightning pull requests for the selected period exceeds the specified threshold.

**Formula:** (lightning\_pr) > (threshold) in the selected period

**Example:** In the past **3 months**, the team has merged **more than 5 lightning pull requests** in **less than 2 minutes**.
