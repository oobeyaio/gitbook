---
description: >-
  This symptom refers to a high number of pull requests that have not been
  reviewed by other team members.
---

# S9 - Unreviewed Pull Requests

### **Why is this a symptom?**

This symptom refers to a high number of pull requests that have not been reviewed by other team members.&#x20;

Pull requests are a way for developers to submit their changes for review and merge them into the main codebase. Unreviewed pull requests can be an indication of a lack of established code review processes, lack of time dedicated to code review, or lack of team cohesion.&#x20;

Unreviewed pull requests can lead to poor-quality code being merged into the main codebase, increased risk of defects, and decreased code quality and maintainability. It can also lead to decreased developer productivity and a lack of accountability among the team.&#x20;

Unreviewed pull requests can be considered a symptom of the development process, indicating that the team may need to focus on improving their code review processes and increasing time dedicated to code review.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #quality\_risk
{% endhint %}

### **Possible Causes**

* Lack of established code review process
* Lack of time dedicated to code review
* Lack of team cohesion
* Lack of clear communication of the code review process
* Lack of team accountability
* The high workload on the team

### **Improvement Areas**

* Establish a clear code review process
* Prioritize code review
* Encourage collaboration and knowledge sharing
* Regularly review and update the code review process
* Encourage the team to work together
* Provide training or knowledge on the code review process

### **Detection Method**

Oobeya detects this symptom if the number of unreviewed pull requests for the selected period exceeds the specified threshold.

**Formula:** (unreviewed\_pr) > (threshold) in the selected period

**Example:** In the past **3 months**, the team has merged **more than 0** unreviewed pull requests.
