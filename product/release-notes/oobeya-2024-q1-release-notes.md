---
description: Check out the new features and improvements we've released for you.
---

# 🎁 Oobeya 2024 Q1 - Release Notes

&#x20;:tada: We're thrilled to unveil the latest features and enhancements in [Oobeya](https://oobeya.io)'s 2024 Quarter 1 release! Dive into the exciting new integrations, powerful enhancements, and innovative features designed to elevate your software development and delivery experience.

## ​🎁 NEW FEATURES & IMPROVEMENTS

### **Development Analytics & DORA Metrics**

* **Trunk-based Deployment Analysis**: Introduced support for trunk-based analysis practice within the Oobeya Deployment API, enabling teams to analyze deployments directly from their mainline branches, streamlining deployment tracking and DORA metrics accuracy.
*   **Jenkins Integration Enhancements**: Added support for the Multibranch Pipeline projects and the ability to specify job names for CI and CD pipelines separately, enhancing Jenkins integration flexibility for deployment tracking and DORA metrics calculation.<br>

    <figure><img src="../../.gitbook/assets/image (410).png" alt=""><figcaption><p>Jenkins DORA Metrics</p></figcaption></figure>
* **Commit Navigation in DORA Deployment Table**: Deployments now include direct links to the commit lists, making it easier to trace changes and review specific commits associated with deployments.
* **Detailed Work Items Tooltip**: The DORA Deployment Table now displays extended details for related work items, including ID, type, title, and creation date, offering a more comprehensive understanding of deployment impacts.

<figure><img src="../../.gitbook/assets/image (411).png" alt=""><figcaption><p>DORA Deployment list</p></figcaption></figure>

* **Release Strategy Selection**: Users can now select a release strategy (e.g., Long-lived branches, Git Tags, Gitflow release branch pattern) for more precise DORA metric calculations, accommodating various workflow preferences.

<figure><img src="../../.gitbook/assets/image (412).png" alt=""><figcaption><p>Release strategy for DORA Metrics calculation</p></figcaption></figure>

* **Parametric Work Type Calculation**: Introduced a customizable threshold for Git Analytics Work Type Calculation (default: 21 days), allowing teams to define what constitutes each type of work according to their specific processes.

<figure><img src="../../.gitbook/assets/image (413).png" alt=""><figcaption><p>Git Analytics Work Type</p></figcaption></figure>

### **Symptoms**

* **Unreviewed Pull Requests**: Now shows root causes for the S9 symptom, providing insights into why pull requests may be overlooked, alongside a count of detected root causes for all symptoms, enhancing issue diagnosis.

<figure><img src="../../.gitbook/assets/image (414).png" alt=""><figcaption><p>Symptomatic Pull Requests</p></figcaption></figure>

### **UI/UX Enhancements**

* **Enhanced Percentage Display**: For metrics comparison, values greater than 500% are now displayed as "500+%", improving readability for significant changes.

### **Administration**

* **User Activity Tracking**: Enhanced admin features to include analytics on user login patterns, session durations, and more, aiding in understanding and improving user engagement.

<figure><img src="../../.gitbook/assets/image (415).png" alt=""><figcaption><p>User analytics</p></figcaption></figure>

* **Team Insights Access Control**: Implemented access restrictions for Team Insights and Analytics, ensuring that team-specific data is only visible to authorized users, enhancing privacy and security.
* **Agile Analytics Enhancements**: Agile boards' analyses are now more secure, automatically hiding from users without explicit board permissions, ensuring sensitive information remains confidential and accessible only to authorized users.
* **Development Analytics Permissions**: Similar to Agile Analytics, any analysis tied to repositories will not be displayed to users lacking the necessary repository permissions, reinforcing data privacy and integrity.

### **Integrations**

* **Appdynamics SaaS Cloud:** Appdynamics' SaaS and on-premises solutions are now fully integrated with Oobeya.
* **Jira Server Enhancements**: Jira Server & Data Center can now connect via API tokens.
* **GitHub App**: Released a dedicated GitHub App to streamline integration and data collection from GitHub repositories, detailed at [Oobeya GitHub Integration](https://docs.oobeya.io/integrations/all-integrations/scm-addons/step-by-step-integration-instructions-for-the-oobeya-github-application).

### **Team Analytics & Agile Analytics**

* Enhanced insights into team performance with features like **Pull Request Comment Count** on the Merged Pull Requests widget.
* **Agile Analytics** improvements include new metrics to track the duration issues stay in a column and the frequency of status reversions (e.g., transitions from test to in progress), offering deeper insights into project flow and efficiency.

We're committed to delivering tools that empower your teams and improve your overall Oobeya experience. If you have any questions or feedback, our support team is ready to assist you. Your feedback is invaluable to our continuous improvement, so we welcome any insights or suggestions you may have.

***

### :person\_running: SEE OOBEYA IN ACTION!

{% hint style="info" %}
Do you want to see all the new features in action and discuss the product roadmap?

Click and [**book a demo**](https://oobeya.io/schedule-a-new-demo/?utm_source=releasenotes\&utm_medium=june2022) now.
{% endhint %}

