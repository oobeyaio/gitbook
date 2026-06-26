---
description: >-
  This symptom refers to a high number of pull requests that are large in size
  and contain a lot of changes.
---

# S11 - Oversize Pull Requests

### **Why is this a symptom?**

This symptom refers to a high number of pull requests that are large in size and contain a lot of changes.&#x20;

Oversize pull requests can be an indication of a lack of established processes for breaking down large changes into smaller chunks. Oversized pull requests are more difficult to review and have more risk.

Oversized pull requests can lead to poor-quality code being merged into the main codebase, an increased risk of defects, and reviewer bottlenecks. They can also lead to decreased developer productivity, long code review times, slow delivery cycles, a reduction in code review depth, and difficulty reviewing and testing the changes.

Oversize pull requests can be considered a symptom of the development process, indicating that the team may need to focus on breaking down large changes into smaller chunks, and paying attention to code review best practices.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #quality\_risk, #bottleneck, #large\_deploy\_risk
{% endhint %}

### **Possible Causes**

* Lack of established processes for breaking down large changes
* Lack of experience in working in smaller chunks
* Lack of planning and estimation
* Lack of attention to code review best practices
* Insufficient training or knowledge of the code review process

### **Improvement Areas**

* Establish clear processes for breaking down large changes
* Regularly review and update the code review process (set and review an oversized PR limit)
* Provide training or knowledge on the code review process
* Improve planning and estimation skills

### **Detection Method**

Oobeya detects this symptom if the number of oversized pull requests for the selected period exceeds the specified threshold.

**Formula:** (oversize\_pr) > (threshold) in the selected period

**Example:** In the past **3 months**, the team has merged **more than 5** oversized pull requests.
