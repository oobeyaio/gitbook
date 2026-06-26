---
description: >-
  This symptom refers to a situation where software changes are not deployed to
  production frequently. It indicates a potential bottleneck or inefficiency in
  the deployment process.
---

# S13- Low Deployment Frequency (DORA)

### **Why is this a symptom?**

Low deployment frequency (DORA) refers to a situation where software changes are not deployed to production frequently. This symptom indicates a potential bottleneck or inefficiency in the deployment process. Teams may face challenges in delivering changes to production environments, which can result in slower software delivery cycles and longer lead times for deploying new features or bug fixes.

**Impact:** Reduced agility in delivering value to users, slower feedback loops, and delayed realization of business benefits.

{% hint style="info" %}
**Level:** Team Level, System Level

**Potential Complications:** #slow\_delivery, #slow\_time\_to\_market, #poor\_customer\_satisfaction, #inefficiencies, #delay\_in\_delivery, #high\_lead\_time
{% endhint %}

### **Possible Causes**

* Inadequate resource allocation: Insufficient resources, such as limited team capacity or lack of infrastructure, can lead to delays in deploying code changes.
* Complex and lengthy deployment processes: Cumbersome and time-consuming deployment processes, involving multiple manual steps or dependencies, can hinder the frequency of deployments.
* High technical debt: Accumulated technical debt, including code that is hard to maintain or modify, can slow down the deployment process and reduce frequency.
* Limited test automation: Insufficient automated testing practices and reliance on manual testing can prolong the deployment cycle and decrease the frequency of releases.
* Ineffective release management: Poor release coordination, insufficient planning, or inadequate release management practices can result in delays and infrequent deployments.
* Lack of collaboration and communication: Inadequate collaboration and communication between teams involved in the deployment process can cause delays and reduced frequency.
* Risk-averse culture: A risk-averse culture that prioritizes stability over speed can lead to cautious deployment practices and lower deployment frequency.
* Inefficient code review and quality assurance: Lengthy or ineffective code review processes, coupled with inadequate quality assurance practices, can delay deployments and decrease frequency.

### **Improvement Areas**

* Enhancing infrastructure and resource allocation: Ensure sufficient resources are allocated to support frequent deployments, including robust infrastructure, suitable hardware, and adequate team capacity.
* Streamlining deployment processes: Identify and remove unnecessary steps, automate manual tasks, and simplify the overall deployment process to increase efficiency and speed.
* Reducing technical debt: Address technical debt by refactoring code, eliminating code smells, improving code quality, and adopting best practices to make the codebase more maintainable and deployable.
* Increasing test automation coverage: Invest in automated testing frameworks and tools to improve test coverage and reduce the time required for manual testing, enabling faster and more frequent deployments.
* Implementing effective release management practices: Develop a well-defined release management strategy that includes clear planning, coordination, and communication to enable smoother and more frequent deployments.
* Cultivating a DevOps culture: Foster a culture of collaboration, shared responsibility, and continuous improvement across development, operations, and other teams involved in the deployment process to promote a faster and more frequent release cycle.
* Prioritizing stability and reliability: Balance the need for speed with a focus on stability and reliability by implementing robust monitoring, error tracking, and incident management practices to minimize risks associated with frequent deployments.
* Optimizing code review and quality assurance: Streamline code review processes, establish clear guidelines, and ensure thorough quality assurance to expedite the review cycle and enhance the overall deployment frequency.
* Leveraging deployment automation tools: Explore and adopt deployment automation tools and technologies, such as continuous integration and continuous deployment (CI/CD) pipelines, to streamline and accelerate the deployment process.

### **Detection Method**

Oobeya detects this symptom if the Deployment Frequency metric is less than the specified threshold in the selected period.

**Formula:** (deployment\_frequency) < (threshold) in the selected period

**Example:** In the past **3 months**, the Deployment Frequency metric is **less than 0.2 days**.

