---
description: >-
  This symptom refers to the significant amount of time it takes for code
  changes to progress from development to production.
---

# S12- High Lead Time For Changes (DORA)

### **Why is this a symptom?**

High Lead Time For Changes ([DORA Metrics](https://oobeya.io/dora-metrics-four-key/)) refers to the significant amount of time it takes for code changes to progress from development to production. It indicates delays and inefficiencies in the software delivery process, resulting in slower time-to-market for new features and bug fixes. This symptom is measured as part of the DORA Metrics, highlighting areas where improvements can be made in the development, testing, and deployment processes to reduce the time taken to deliver changes.

**Impact:** Delays in delivering new features, bug fixes, or improvements, leading to slower software delivery and potentially dissatisfied customers.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #slow\_delivery, #slow\_time\_to\_market, #poor\_customer\_satisfaction, #inefficiencies, #delay\_in\_delivery, #low\_job\_satisfaction, #low\_deploy\_frequency
{% endhint %}

### **Possible Causes**

* Inefficient code review process: Lengthy code review cycles, lack of clear guidelines or standards, and delays in providing feedback can contribute to increased lead time for changes.
* Manual and error-prone deployment processes: Reliance on manual deployment procedures, manual testing, or lack of automation in the deployment pipeline can lead to delays in releasing changes to production.
* Lack of test automation: Insufficient automated testing practices, limited test coverage, or slow and unreliable testing frameworks can prolong the time taken to validate changes.
* Technical debt and code complexity: Accumulated technical debt, including legacy code, poor architectural design, and code complexity, can make it more challenging to implement and deliver changes quickly.&#x20;
* Communication and coordination issues: Lack of effective collaboration and communication between development, QA, and operations teams can lead to delays and misalignment in the change deployment process.
* Dependencies and bottlenecks: Dependencies on external services, teams, or resources that experience delays or constraints can impact the lead time for changes.
* Inadequate infrastructure or tooling: Insufficient infrastructure resources, outdated or slow hardware, or limitations in the development or deployment tooling can contribute to longer lead times.
* Large and complex code changes - Oversize Pull Requests (Oobeya Symptom)

### **Improvement Areas**

* Streamline code review process: Implement efficient code review practices, such as smaller code review batches, clear guidelines, and timely feedback, to reduce review cycles and expedite approvals.
* Automate deployment pipelines: Invest in automated deployment pipelines to minimize manual intervention, reduce deployment bottlenecks, and speed up the delivery of changes to production.
* Optimize testing procedures: Enhance testing strategies, including automated testing frameworks, unit testing, integration testing, and performance testing, to identify and resolve issues earlier in the development cycle.
* Prioritize technical debt reduction: Allocate resources and efforts to address technical debt regularly, focusing on refactoring and code improvements to increase maintainability and agility in making changes.
* Enhance collaboration and communication: Foster strong collaboration between development, QA, and operations teams to ensure smooth coordination and minimize delays in the change deployment process.
* Implement feature toggles: Utilize feature toggles or feature flags to decouple code deployments from feature releases, enabling faster and safer delivery of changes.

### **Detection Method**

[Oobeya](https://oobeya.io/) detects this symptom if the Lead Time For Changes metric is more than the specified threshold in the selected period.

**Formula:** (lead\_time\_for\_changes) > (threshold) in the selected period

**Example:** In the past **3 months**, the Lead Time For Changes is **more than 5 days**.

