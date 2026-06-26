---
description: >-
  This symptom refers to the percentage of deployments that result in failures
  or incidents in production. It can lead to customer dissatisfaction, decreased
  user trust, and increased operational costs.
---

# S14- High Change Failure Rate (DORA)

### **Why is this a symptom?**

A high change failure rate (DORA) refers to the percentage of deployments that result in failures or incidents in production. It indicates the stability and reliability of the software systems being developed and delivered. A high change failure rate can lead to customer dissatisfaction, decreased user trust, and increased operational costs.

**Impact:** Increased system instability, reduced reliability, and potential disruption to end-users or customers.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #quality\_risk, #low\_productivity, #poor\_customer\_satisfaction, #inefficiencies, #low\_job\_satisfaction
{% endhint %}

### **Possible Causes**

* Inadequate code review process: Insufficient attention to code quality, lack of thorough reviews, or a lack of a standardized code review process can contribute to higher failure rates.
* Insufficient testing coverage: Incomplete or inadequate testing strategies, including lack of automated testing or inadequate test coverage, can increase the likelihood of failures in production.
* High technical debt: Accumulated technical debt, such as outdated or poorly maintained code, can introduce instability and increase the likelihood of production failures.
* Lack of knowledge-sharing: Limited knowledge-sharing within the team can result in a lack of awareness about potential issues or best practices, leading to higher failure rates.
* Ineffective communication and collaboration: Poor communication and collaboration among team members can lead to misunderstandings, misaligned expectations, and ultimately, higher failure rates.

### **Improvement Areas**

* Strengthening code review practices: Implementing stricter code review processes, ensuring comprehensive reviews, and emphasizing code quality can help identify and address potential issues before they reach production.
* Enhancing testing strategies: Investing in automated testing, increasing test coverage, and implementing robust testing methodologies can improve the effectiveness of testing and reduce failures.
* Managing technical debt: Prioritizing and addressing technical debt through refactoring, code cleanup, and architectural improvements can reduce the risk of failures caused by accumulated debt.
* Promoting knowledge-sharing: Encouraging knowledge-sharing among team members through pair programming, documentation, and regular knowledge-sharing sessions can enhance understanding and awareness of potential issues.
* Fostering a culture of collaboration: Emphasizing effective communication, fostering collaboration among team members, and promoting cross-functional teamwork can improve coordination and alignment, reducing the likelihood of failures.

### **Detection Method**

Oobeya detects this symptom if the Change Failure Rate metric is more than the specified threshold in the selected period.

**Formula:** (change\_failure\_rate) > (threshold) in the selected period

**Example:** In the past **3 months**, the Change Failure Rate is **more than 20%**.

