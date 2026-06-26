---
description: >-
  The objective of this document is to guide you through the process of setting
  up development analytics on Oobeya.
---

# Setting Up Development Analytics And DORA Metrics

**Oobeya Development Analytics** (Gitwiser) module offers comprehensive insights into the development process, providing visibility into the coding, code review, and delivery cycles. Through Development Analytics, Oobeya analyzes **all development activities, including commits, pull requests,** and **deployments**, offering valuable insights. By leveraging Development Analytics, teams can identify bottlenecks, pinpoint problematic areas, and enhance engineering productivity and efficiency.

## Initializing Oobeya Development Analytics In 6 Steps

* Click the **"Gitwiser"** icon on the left sidebar. Then click the **"New Analysis"** button.
* Select the Version Control System tool (Github, GitLab, Azure DevOps, Bitbucket, Gitea).
* Follow the steps below to start analyzing the software development process historically:

### Step 1: Repository

Select the data source, project, repository, and branch information. This step ensures accurate analysis of the coding repository including commits, pull requests, and metadata, enabling comprehensive insights into the development workflow.

### Step 2: CI/CD Flow

Choose the CI/CD strategy that aligns with your development workflow. This step enables Oobeya to understand how software development processes are managed and integrated, enabling accurate tracking and analysis from code commit to deployment.

* [ ] We don’t have a CI/CD flow or we don’t want to analyze deployments
* [ ] We have a single pipeline for both CI and CD deployments
* [ ] We have separate pipelines for CI and CD deployments

### Step 3: Deployment

Provide details about your deployment pipeline, including environments, deployment process, and relevant tools. This information helps Oobeya to accurately track and analyze deployment activities, DORA Metrics, and their impact on software delivery performance.

### Step 4: Incident Detection

Specify incident sources, such as incident management tools and hotfix branch naming conventions. This step is essential for enabling Oobeya to automatically detect, track, and accurately calculate DORA Metrics such as Change Failure Rate and Time to Restore Service.

### Step 5: Advanced Settings

Fine-tune the analytics process by selecting related teams and defining the date range for analysis. Customize settings to focus on specific data and time frames relevant to your needs, enhancing the accuracy and relevance of the insights gained from the analytics process.

### Step 6: Finish

Review and confirm the summary of selections and settings made in the previous steps. Click 'Finish' to start the analytics process and gain insights into your software development and delivery performance.

***

Once the analysis is completed, you can see the results on the **Development Analytics** page. Click on the repository name and navigate to the analytics result.

***

### Notes

* Make sure to select the correct Source Code Management tool and provide accurate details about your project's coding repository.
* When choosing a CICD strategy, ensure it aligns with your delivery workflow to avoid inaccurate analytics and DORA Metrics.
* Provide accurate details of your production deployment pipeline to ensure precise measurement of DORA Metrics.
* Select the appropriate development practice (trunk-based or pull request based) for accurate metric calculation.
* Integrate incident tracking tools and specify incident detection sources to accurately calculate the Change Failure Rate and Time to Restore Service metrics of DORA.
* Use caution when fine-tuning settings, as incorrect configurations may lead to inaccurate analysis results.

### Tips for Efficiency

* Double-check the accuracy of the information you provide at each step to avoid errors.
* Take advantage of tutorials and resources provided by Oobeya to maximize your use of the platform.
* Contact Oobeya via their website ([oobeya.io](http://oobeya.io/)) if you have any questions or need further assistance.
