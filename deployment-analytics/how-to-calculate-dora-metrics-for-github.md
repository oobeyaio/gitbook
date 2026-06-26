---
description: >-
  Oobeya tracks deployment pipelines and calculates accurate DORA Metrics from
  commit to prod deployment (not PR Merged). No changes required to pipelines;
  effortlessly integrates with current tools.
icon: github
---

# How To Calculate DORA Metrics for GitHub

{% hint style="info" %}
Oobeya integrates seamlessly with GitLab + GitHub + Jira + Sonar + GitLab CI + GitHub Actions + Jenkins + TeamCity + Azure DevOps + NewRelic, and many more…&#x20;
{% endhint %}

You can calculate DORA Metrics with cross-platform analysis as well:

* GitHub x GitHub Actions
* GitHub x Jenkins
* GitHub x Azure DevOps Pipelines
* GitHub x Azure DevOps Releases
* GitHub x TeamCity
* and more...

Learn below how to calculate DORA Metrics for **GitHub + GitHub Actions**.

\*\*\*

## How To Calculate DORA Metrics for GitHub

#### 1. Go to Gitwiser's main page.

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/dd72f76c-1906-4375-9d28-8f07da78a9a4/eca86372-e01e-40a9-85a2-2ba00136ebec.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.2406&#x26;fp-y=0.2433&#x26;fp-z=2.0536&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption><p>Oobeya's Gitwiser home page</p></figcaption></figure>

#### 2. Click on "GitHub" or "GitHubEnterprise"&#x20;

<figure><img src="../.gitbook/assets/image (403).png" alt=""><figcaption><p>Select Addon</p></figcaption></figure>

#### 3. Select the Data Source you added [before](../integrations/adding-new-integration/adding-a-new-data-source.md):&#x20;

<figure><img src="../.gitbook/assets/image (376).png" alt=""><figcaption></figcaption></figure>

#### 4. Select your GitHub Organization from the Organization list

<figure><img src="../.gitbook/assets/image (367).png" alt=""><figcaption></figcaption></figure>

#### 5. Select your coding repository from the list.&#x20;

#### Select your deployment branch --> master, main, release, prod, etc.

<figure><img src="../.gitbook/assets/image (394).png" alt=""><figcaption></figcaption></figure>

#### 6. Select the "Deployment Analytics" option to calculate DORA Metrics

<figure><img src="../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure>

#### 7. Select your CI/CD tool from the list

<figure><img src="../.gitbook/assets/image (405).png" alt=""><figcaption></figcaption></figure>

#### 8. For GitHub Actions, Select Data Source, Organization, Repository, and Workflow for your Deployment Pipelines

<figure><img src="../.gitbook/assets/image (393).png" alt=""><figcaption><p>GitHub x GitHub Actions DORA Metrics</p></figcaption></figure>

#### 9. Auto Failure Detection Options:&#x20;

#### Select your incident source (NewRelic, DataDog, etc.) and enter your hotfix patterns to automatically detect production failures

Learn more: [How to Effectively Detect Production Failures](https://oobeya.io/blog/dora-metrics-tracking-how-to-effectively-detect-production-failures/)

<figure><img src="../.gitbook/assets/image (383).png" alt=""><figcaption><p>DORA Auto Failure Detection</p></figcaption></figure>

#### 10. Click on Start Analysis

<figure><img src="../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure>

#### 11. Gitwiser Analysis has started. Click on the "Return to page" button and wait for the results

<figure><img src="../.gitbook/assets/image (378).png" alt=""><figcaption></figcaption></figure>

#### 12. Click on the "Deployments (DORA)" tab and see the DORA Metrics

<figure><img src="../.gitbook/assets/image (406).png" alt=""><figcaption><p>Oobeya GitHub DORA Metrics</p></figcaption></figure>

***
