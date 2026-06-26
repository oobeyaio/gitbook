---
description: >-
  Oobeya tracks deployment pipelines and calculates accurate DORA Metrics from
  commit to prod deployment (not PR Merged). No changes are required to
  pipelines; simply integrate with current tools.
icon: windows
---

# How To Calculate DORA Metrics for Azure DevOps

{% hint style="info" %}
[Oobeya](https://oobeya.io/) integrates seamlessly with GitLab + GitHub + Jira + Sonar + GitLab CI + GitHub Actions + Jenkins + TeamCity + Azure DevOps, and many more…&#x20;
{% endhint %}

You can calculate [DORA Metrics](https://oobeya.io/dora-metrics-four-key/) with cross-platform analysis as well:

* Azure DevOps Repos x Jenkins
* Azure DevOps Repos x GitLab CI
* Azure DevOps Repos x GitHub Actions
* Azure DevOps Repos x TeamCity
* GitHub x Azure DevOps Releases
* and more...

Learn below how to calculate DORA Metrics for **Azure DevOps Repos + Azure DevOps Release**.

\*\*\*

## How To Calculate DORA Metrics for Azure DevOps

#### 1. Go to Gitwiser's main page.

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/dd72f76c-1906-4375-9d28-8f07da78a9a4/eca86372-e01e-40a9-85a2-2ba00136ebec.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.2406&#x26;fp-y=0.2433&#x26;fp-z=2.0536&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption><p>Oobeya's Gitwiser home page</p></figcaption></figure>

#### 2. Click on "AzureDevops"

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/0ee19424-37fb-4ba7-8e21-65a3b6f30cd5/094525b2-177f-4cba-9ed1-bf8596972472.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.4811&#x26;fp-y=0.2843&#x26;fp-z=1.7679&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption><p>Select your Addon</p></figcaption></figure>

#### 3. Click on "Git"

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/89b83550-0c59-4ee3-a4c9-751ad9b17b50/f3faa826-b7a0-4b7c-8ae3-f9bc38a5af35.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5045&#x26;fp-y=0.2982&#x26;fp-z=2.1521&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 4. Select your Data Source

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/5eb240c7-c801-4759-a5de-5be7627ea927/e81d412d-08dc-4084-ba5f-58b1e9692302.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5173&#x26;fp-y=0.3747&#x26;fp-z=1.4060&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 5. Select your Project from the project list

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/0e42d8f3-071b-4307-9506-26753b89594c/c7aa4d3d-29d4-4dd7-b174-9337f0fa6c16.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5049&#x26;fp-y=0.3162&#x26;fp-z=2.4060&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 6. Select your Code Repository from the list

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/707b25d1-0b8d-45ef-a85d-25f8d2212e82/976ee056-35f4-4316-b9c4-ddf57b236f12.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5062&#x26;fp-y=0.3114&#x26;fp-z=2.4060&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 7. Select your deployment branch --> master, main, release, prod, etc.

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/39038e64-938d-421f-9752-f4f6f5eb5288/03ac2bfe-7094-4f90-a6c5-05dd7905284b.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5078&#x26;fp-y=0.2998&#x26;fp-z=2.7706&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 8. Select the "Deployment Analytics" option to calculate DORA Metrics

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/6dab4baf-2aab-4ebc-be9e-ee231ab981c1/162033b5-f4e0-4707-96b5-b422d5934d56.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5052&#x26;fp-y=0.3333&#x26;fp-z=2.1829&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 9. Select your CI/CD tool from the list

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/9997f177-ba69-46fc-8845-3434874e8885/2fde9d5e-bede-424f-af61-1bcc68fde7af.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5057&#x26;fp-y=0.4998&#x26;fp-z=2.0000&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 10. Select Data Source, Project, and Environment for your Deployments

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/456fa909-68d6-4161-be09-6cd788a2190f/2ef70013-22ef-4a0c-b3fd-53050f5269bb.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5095&#x26;fp-y=0.6917&#x26;fp-z=2.4427&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 11. Click on Start Analysis

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/6b384fef-9dac-4627-82ac-4bc34875ea25/4af5f849-c938-4925-8298-4f4ec4efd414.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5017&#x26;fp-y=0.7287&#x26;fp-z=2.8872&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 12. Gitwiser Analysis has started. Click on the "Return to page" button and wait for the results

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/06068892-da3a-4f46-b6e6-e98029d3c95a/bc7f7696-44dd-4179-9ff5-1d85c14367c4.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5000&#x26;fp-y=0.5000&#x26;fp-z=1.0000&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption></figcaption></figure>

#### 13. Click on the "Deployment Analytics" tab and see the DORA Metrics

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/d31095d9-6dea-4196-b088-1228ba4a1612/0c181850-432f-4a04-98b2-588cc891af51.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.5000&#x26;fp-y=0.5000&#x26;fp-z=1.0000&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1816%3A948" alt=""><figcaption></figcaption></figure>

***
