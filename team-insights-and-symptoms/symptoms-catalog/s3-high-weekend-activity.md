---
description: >-
  This symptom refers to a consistently high level of activity on weekends,
  indicating that team members are working outside of regular work hours.
---

# S3- High weekend activity

### **Why is this a symptom?**

This symptom refers to a consistently high level of activity on weekends, indicating that team members are working outside of regular work hours. This could be due to pressure to meet deadlines, an excessively demanding workload, or a lack of support from management. High weekend activity can lead to burnout, reduced productivity, and decreased job satisfaction.

If team members have coding and review activities over the weekend, it can be considered a symptom of the development process.&#x20;

{% hint style="info" %}
**Level:** Team Level

**Potential Complications:** #burnout, #low\_productivity, #low\_job\_satisfaction
{% endhint %}

### **Possible Causes**

* Lack of resources
* Pressure to meet deadlines
* Excessively demanding workload
* Lack of support from management
* Poor planning process

### **Improvement Areas**

* Review and redistribute workloads as needed
* Set clear deadlines and expectations
* Ensure team members have sufficient support and resources to complete their tasks during regular work hours
* Review past instances of high weekend activity to identify patterns and root causes

### **Detection Method**

Oobeya detects this symptom if the level of activity on weekends for the selected period exceeds the specified threshold.

**Formula:** (weekend\_commits, weekend\_PRs) > 0 in selected period

**Example:** In the past **3 months**, **more than 5 commits** and **pull request activities** were detected.

