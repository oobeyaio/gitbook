---
icon: octagon-minus
---

# Git Analytics Exclusions

Gitwiser allows you to fine-tune your analytics by excluding unnecessary files, directories, or specific commits from the analysis. This ensures metrics are focused on meaningful contributions. Exclusions can be applied at a global level, repository level, or commit level.

| Example              | Scope                                                              |
| -------------------- | ------------------------------------------------------------------ |
| \*\*/\*.xml          | Excludes all _xml_ files from Gitwiser analysis.                   |
| \*\*/data.json       | Excludes all _data.json_ files from Gitwiser analysis.             |
| \*\*/\*sample\*/\*\* | Excludes directories that include "_sample_" in their folder name. |

***

#### 1- Global Exclusions (Admin Setting)

Admins can define exclusion patterns that apply to all repositories across the platform.

* Navigate to:\
  **Administration** → **Coding, Review & Delivery** (Analytics section) → **Git Analytics** tab
* In the **Exclusion List**, add glob patterns such as:\
  \*\*/_.aac → excludes all .aac files_\
  _\*\*/_.apng → excludes all .apng files
* Toggle **Reset Existing Analyses** if you want Gitwiser to reanalyze existing data based on new patterns.

📌 These exclusions are global and affect all repos.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fr6S1IAPmmBEEzOR5HUqa%2Fimage.png?alt=media&#x26;token=f096e7f2-3d56-49ee-bc69-ffac2d1a36d3" alt=""><figcaption></figcaption></figure>

***

#### 2- Repository-level Exclusions

You can configure exclusion patterns for a specific repository.

**If you're creating a new analysis:**

* During setup, you'll see the **Advanced Settings** step
* Add your file exclusion patterns there (e.g., \*\*/\*.xml, \*\*/\*sample\*/\*\*)

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FkWnFIkPwQ71kpc7ChRD8%2Fimage.png?alt=media&#x26;token=410ae19f-7b7c-41a2-a9f4-ca4c0b2d14ea" alt=""><figcaption></figcaption></figure>

**If the analysis already exists:**

* Go to:\
  **Gitwiser & DORA Metrics** → select the repository → **Git Analytics**
* Click the **three dots** (⋯) in the top-right corner of the **Git Analytics** page
* Select **Update Analysis**
* You'll be able to edit exclusion patterns here

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FQe2GC0ZJXef43moxinLU%2Fimage.png?alt=media&#x26;token=a7683009-d26b-429a-b01b-b5e41cdba266" alt=""><figcaption></figcaption></figure>

***

#### 3- Commit-level Exclusions

Specific commits can also be manually excluded from analytics.

* Navigate to:\
  **Gitwiser & DORA Metrics** → select the repository → **Git Analytics**
* Scroll to the **Contributions During the Selected Period** section
* Click **Exclude** next to the commit(s) you want to exclude
* Excluded commits appear in the **Excluded Commits** section at the bottom

🧠 Useful for filtering out noise like formatting commits, reverts, or merge commits.

<figure><img src="https://3582076375-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FBepLfpTqyw6wXRamZS3J%2Fimage.png?alt=media&#x26;token=f7e46393-e3e8-41c4-b66c-b1f77eab2588" alt=""><figcaption></figcaption></figure>

***

#### Conclusion

Using **Git Analytics Exclusions** effectively helps ensure your metrics reflect meaningful contributions by filtering out noise like binary files, test data, or irrelevant commits. Whether you're applying exclusions globally, per repository, or at the commit level, these tools give you full control over the scope of your analysis in Gitwiser. For best results, review and refine your exclusion patterns regularly based on your team's workflow.
