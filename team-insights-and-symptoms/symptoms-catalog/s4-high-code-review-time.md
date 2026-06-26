---
description: >-
  This symptom occurs when the review time of pull requests exceeds a predefined
  threshold, signaling potential inefficiencies in the code review process.
---

# S4 - High Code Review Time

### **Why is this a symptom?**

High Code Review Time is considered a symptom because it indicates potential bottlenecks and inefficiencies within the code review process, impacting the overall productivity and effectiveness of a development team. Extended code review periods may result in merging outdated or insufficiently reviewed code into the main branch, potentially leading to bugs and stability issues. Moreover, it can disrupt the rhythm of continuous integration and continuous deployment (CI/CD) practices, essential for agile and efficient software delivery.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #quality\_risk, #slow\_delivery, #delay\_in\_delivery, #low\_deploy\_frequency
{% endhint %}

### **Possible Causes**

* **Complex Code:** Pull requests that contain complex or large amounts of code may take longer to review thoroughly.
* **Lack of Automation:** Inadequate use of automated tools for static code analysis, testing, and style checks can increase the manual workload during reviews.
* **Insufficient Resources:** A lack of available reviewers or overburdened team members can significantly delay the review process.
* **Poor Communication:** Ineffective communication among team members can lead to misunderstandings and repeated review cycles.
* **Skill Discrepancies:** Variability in skill levels among developers and reviewers can result in slower review times, as less experienced members might require more time to understand or evaluate the code.

### **Improvement Areas**

* **Review Efficiency:** Focus on streamlining the review process through better guidelines, checklists, and pre-review preparations.
* **Automation Integration:** Implement or enhance the use of automated tools that can assist in identifying issues early and reduce the reliance on manual review.
* **Resource Allocation:** Ensure adequate allocation of human resources to handle the review workload effectively.
* **Feedback Mechanisms:** Establish robust feedback mechanisms to facilitate quick resolution of issues and continuous improvement in the review process.
* **Training and Development:** Regular training sessions and workshops to improve coding and review skills across the team.

### **Detection Method**

Oobeya detects this symptom if the number of stale pull requests for the selected period exceeds the specified threshold.

**Formula:** (number\_of\_stale\_pr) > (threshold) in the selected period

PR\_review\_time = PR\_merged - PR\_open

Stale PR: PR\_review\_time > stale\_threshold -> Stale PR detected

**Example:** In the past **6 months**, the team has merged **more than 0 stale pull requests** that have been reviewed **more than 3 days**.
