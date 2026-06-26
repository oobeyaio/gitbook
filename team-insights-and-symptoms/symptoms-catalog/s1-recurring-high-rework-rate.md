---
description: >-
  This symptom refers to a high rate of coding that needs to be redone or
  corrected. This could be due to a lack of clear requirements, inadequate
  testing, or a failure to follow established processes.
---

# S1- Recurring high rework rate

### **Why is this a symptom?**

This symptom refers to a high rate of coding that needs to be redone or corrected. This could be due to a lack of clear requirements, inadequate testing, or a failure to follow established processes.&#x20;

Rework, by definition, wastes time and resources. A high rework rate is costly, time-consuming, and can cause delays, leading to frustration among team members.

{% hint style="info" %}
**Level:** Team Level

**Potential Complications:** #low\_efficiency, #slow\_delivery, #dissatisfaction
{% endhint %}

### **Possible Causes**

* Lack of clear requirements
* User stories with no clear Definition of Done
* High technical debt & complexity, low-quality code
* Lack of domain knowledge
* Lack of knowledge-sharing culture
* Inadequate testing
* Failure to follow established processes

### **Improvement Areas**

* Clarify requirements/user stories
* Improve testing processes at the development level
* Establish clear processes for analysis, development, and review
* Provide additional training as needed
* Review past instances of rework to identify patterns and root causes
* Improve knowledge-sharing culture and practices within the team

### **Detection Method**

Oobeya detects this symptom if the rework rate for recurring periods exceeds the specified threshold.

**Formula:** (churn% > \[churn\_threshold]%) x\[specified\_period] recurring periods

**Example:** During each of the **last 3 months**, the team has consistently had a **rework rate** of **more than 20%**.

