---
description: >-
  Oobeya tracks deployment pipelines and calculates accurate DORA Metrics from
  commit to prod deployment (not PR Merged). No changes required to pipelines;
  effortlessly integrates with current tools.
icon: github
---

# How To Calculate DORA Metrics for GitHub

{% hint style="info" %}
Oobeya integrates seamlessly with GitLab + GitHub + Jira + Sonar + GitLab CI + GitHub Actions + Jenkins + TeamCity + Azure DevOps + NewRelic, and many more…
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

### How To Calculate DORA Metrics for GitHub

**1. Go to Coding, Review & Delivery (Analytics section of the left menu).**

<figure><img src="https://images.tango.us/workflows/d37824ac-e844-4087-8bf5-7ea7077720c5/steps/dd72f76c-1906-4375-9d28-8f07da78a9a4/eca86372-e01e-40a9-85a2-2ba00136ebec.png?fm=png&#x26;crop=focalpoint&#x26;fit=crop&#x26;fp-x=0.2406&#x26;fp-y=0.2433&#x26;fp-z=2.0536&#x26;w=1200&#x26;mark-w=0.2&#x26;mark-pad=0&#x26;mark64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmsucG5n&#x26;ar=1920%3A976" alt=""><figcaption><p>Oobeya's Gitwiser home page</p></figcaption></figure>

**2. Click on "GitHub" or "GitHubEnterprise"**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FMWUTIRCeHfXo5oI4UYnP%2Fimage.png?alt=media&#x26;token=c7172b56-c8ae-420a-ae2a-31ea5b95a750" alt=""><figcaption><p>Select Addon</p></figcaption></figure>

**3. Select the Data Source you added** [**before**](https://docs.oobeya.io/integrations/adding-new-integration/adding-a-new-data-source)**:**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FvEaXHrdPvGSqtpy882rL%2Fimage.png?alt=media&#x26;token=47a6ca0b-84a7-4773-9a23-dcf4e94a2908" alt=""><figcaption></figcaption></figure>

**4. Select your GitHub Organization from the Organization list**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FcpSzn0L9clfhvSPaQGXE%2Fimage.png?alt=media&#x26;token=68827d86-475f-495a-bff6-273988c2953a" alt=""><figcaption></figcaption></figure>

**5. Select your coding repository from the list.**

**Select your deployment branch --> master, main, release, prod, etc.**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F3iQItxdWnmCZ7tr2XeCc%2Fimage.png?alt=media&#x26;token=d5aba8d3-b425-4295-a90b-db379213419e" alt=""><figcaption></figcaption></figure>

**6. Select the "Deployment Analytics" option to calculate DORA Metrics**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F4dMBkLfsQsTXEGIgkyc2%2Fimage.png?alt=media&#x26;token=d13766ab-5e0d-4c5f-8d6b-3fe172f55aee" alt=""><figcaption></figcaption></figure>

**7. Select your CI/CD tool from the list**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FHD0q5zFpNdGjMyTuNHEC%2Fimage.png?alt=media&#x26;token=33635c41-ab72-4725-95a1-442568a58916" alt=""><figcaption></figcaption></figure>

**8. For GitHub Actions, Select Data Source, Organization, Repository, and Workflow for your Deployment Pipelines**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F7vY8A0gYdzhrrCCvA0vt%2Fimage.png?alt=media&#x26;token=166abcd0-d244-46eb-a438-0390ed723307" alt=""><figcaption><p>GitHub x GitHub Actions DORA Metrics</p></figcaption></figure>

**9. Auto Failure Detection Options:**

**Select your incident source (NewRelic, DataDog, etc.) and enter your hotfix patterns to automatically detect production failures**

Learn more: [How to Effectively Detect Production Failures](https://oobeya.io/blog/dora-metrics-tracking-how-to-effectively-detect-production-failures/)

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FF3cdBdnotMuVQxAwc9d0%2Fimage.png?alt=media&#x26;token=eb5903c4-afc3-4b7e-a091-4aeac2ffda51" alt=""><figcaption><p>DORA Auto Failure Detection</p></figcaption></figure>

**10. Click on Start Analysis**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fu4wo0umXVtJLwvjGn5p3%2Fimage.png?alt=media&#x26;token=2530268d-56b5-441f-b2c2-68207e6634cd" alt=""><figcaption></figcaption></figure>

**11. Gitwiser Analysis has started. Click on the "Return to page" button and wait for the results**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fl8rJfGvSioUs7w4vTRY2%2Fimage.png?alt=media&#x26;token=41bcc8ef-6ea5-4670-a44a-53c09f1c3cda" alt=""><figcaption></figcaption></figure>

**12. Click on the "Deployments (DORA)" tab and see the DORA Metrics**

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F3GVaVfH1I1wvjoykKkh0%2Fimage.png?alt=media&#x26;token=adebbd31-2865-49aa-bd2d-70d02dc4cb15" alt=""><figcaption><p>Oobeya GitHub DORA Metrics</p></figcaption></figure>

***
