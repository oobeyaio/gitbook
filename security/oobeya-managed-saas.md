---
description: Learn more about Oobeya Managed SaaS offering.
icon: cloud
---

# Oobeya Managed SaaS

## Oobeya Managed SaaS (Private Cloud) offering provides a **single-tenant SaaS environment** for each customer.

This means each customer has their own dedicated instance of the software and its supporting infrastructure. Unlike a shared tenant (multi-tenant) model where multiple customers' data and resources are hosted on the same server/cluster, a single-tenant architecture ensures that your data is isolated from other customers' data. This isolation provides several benefits:

* **Enhanced Security:** By not sharing resources with other tenants, the risk of data leakage or cross-tenant attacks is significantly reduced. Each tenant's environment can be secured according to their specific security policies and compliance requirements.
* **Customization and Control:** Since the environment is exclusive, customers have greater flexibility to customize the software and infrastructure according to their unique business processes and needs. This includes the ability to implement custom security policies, compliance measures, and integrations with other tools.
* **Performance Reliability:** In a single-tenant setup, customers do not have to worry about the "noisy neighbor" effect, where the activities of one tenant can impact the performance of others on the same server. Each customer enjoys the full resources of their dedicated environment, leading to more predictable and reliable performance.

## How does Oobeya preserve the data? Where and how the data is hosted?

Oobeya preserves customer data by hosting it on **MongoDB** in a **single-tenant SaaS environment**. This setup provides a **secure, isolated database** and **network** for each customer, **ensuring data integrity** and **security.** Here's how Oobeya manages data preservation and security:

* **Isolated Databases:** Each customer's data is stored in a separate MongoDB database. This isolation not only enhances security by separating your data from that of other customers but also allows for tailored database management practices that align with individual security and compliance needs.
* **Secure Hosting Environment:** The data is hosted and managed within a secure, single-tenant environment. This means that each customer's data storage and processing resources are not shared with others, minimizing the risk of unauthorized access or data breaches.
* **Compliance and Security Customization:** Given the isolated nature of each tenant's environment, customers have the ability to implement their own security measures and comply with specific regulations. Oobeya's infrastructure supports customization in terms of access controls, and other security protocols.
* **Integration with SDLC Tooling:** For customers integrating Oobeya with their software development lifecycle (SDLC) tools, such as GitHub, Azure DevOps, Jira, Jenkins, and Sonar, Oobeya ensures that the data flowing from these integrations is securely managed and preserved within the isolated, single-tenant environment. This approach allows for seamless and secure data exchange between Oobeya and your software engineering ecosystem, ensuring that all relevant data is accurately captured, stored, and available for your team's use.

In summary, Oobeya's approach to data hosting and preservation is designed **to** **ensure maximum security, performance,** and **flexibility for its customers**. By leveraging a single-tenant SaaS model and hosting data on MongoDB within this isolated environment, **Oobeya offers a secure, customizable, and reliable solution** that meets the diverse needs of its customers.
