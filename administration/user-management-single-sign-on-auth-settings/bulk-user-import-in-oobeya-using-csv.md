---
icon: users-gear
---

# Bulk User Import in Oobeya Using CSV

Oobeya allows you to create multiple users simultaneously by importing a CSV file. The CSV file should contain information about each user in a specific format.

### CSV File Format

An example CSV file should look like this:

<pre class="language-csv"><code class="lang-csv">name,surname,email,companyRole,username,userType
<strong>Mike,Miller,mike.miller@oobeya.io,TEAM_LEAD,mike.miller,DB
</strong>John,Doe,john.doe@oobeya.io,MANAGER,john.doe,DB
Grace,Hopper,grace.hopper@oobeya.io,DEVELOPER,grace.hopper,DB
</code></pre>

#### Explanation of Fields

* **name**: First name of the user
* **surname**: Last name of the user
* **email**: Email address of the user
* **companyRole**: Role of the user within the company. You can select the proper Oobeya Company Roles from the list below:

```
DEVELOPER,
QA_ENGINEER,
DEVOPS_ENGINEER,
BUSINESS_ANALYST,
PROJECT_MANAGER,
SCRUM_MASTER,
PRODUCT_OWNER,
PRODUCT_MANAGER,
TEAM_LEAD,
MANAGER,
DIRECTOR,
EXECUTIVE_BOARD_MEMBER,
TECH_LEAD
```

* **username**: Username for logging into Oobeya
* **userType**: The type of user account. Use "DB" for standard database-authenticated users.

***

### Importing the CSV File

1. Navigate to _**Administration Panel > Go To Admin Settings**_.
2. Open _**Users & Groups**_.
3.  Click the **settings icon** and select **"Bulk Import From CSV"**.<br>

    <figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption><p>Bulk import</p></figcaption></figure>
4. Select your CSV file and click the '**Import**' button.

<figure><img src="../../.gitbook/assets/image (190).png" alt="" width="375"><figcaption><p>Import CSV file</p></figcaption></figure>

{% hint style="danger" %}
Please make sure that your CSV file does not include any syntax errors. Otherwise, you may view an error message.
{% endhint %}
