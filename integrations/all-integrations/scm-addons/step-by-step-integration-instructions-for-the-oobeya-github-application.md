---
icon: github
cover: ../../../.gitbook/assets/Screen Shot 2024-02-09 at 14.25.07.png
coverY: -83.01866666666666
layout:
  width: default
  cover:
    visible: true
    size: hero
    mask: none
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Step-by-Step Integration Instructions for the Oobeya GitHub Application

There are three options to integrate Oobeya with GitHub. This guide will provide detailed instructions on how to integrate Oobeya with GitHub using Option 1 and Option 2.

1. **Option 1:** Use the Official Oobeya GitHub App from the GitHub Marketplace. This option provides a straightforward integration process by installing the official Oobeya GitHub App and selecting it when creating a data source in Oobeya.
2. **Option 2:** Register your own GitHub application. This option offers more flexibility and customization by allowing you to create your own GitHub App, and configure settings.
3. **Option 3:** Use a [Personal Access Token for the integration](github-integrations.md).

***

## **Option 1:** Using the Official Oobeya GitHub App&#x20;

Utilize the[ official Oobeya GitHub App ](https://github.com/marketplace/oobeya-dora-metrics)available on the GitHub Marketplace to seamlessly integrate [Oobeya](https://oobeya.io) with your GitHub repositories and workflows. Simply install the application from the GitHub App Marketplace, grant the necessary permissions, and select the Oobeya GitHub App option when [creating a data source](../../adding-new-integration/adding-a-new-data-source.md) within Oobeya. This straightforward approach ensures smooth integration and access to [Oobeya's features](https://oobeya.io/oobeya-metric-definitions/). See the step-by-step integration guide below:

### Step 1: Install the Oobeya GitHub App

1. Go to the [Oobeya DORA Metrics GitHub App Marketplace page ](https://github.com/marketplace/oobeya-dora-metrics)and install the application.&#x20;
2. You will be prompted to choose which repositories to integrate with Oobeya. You can select all repositories or choose specific ones.
3.  After selecting the repositories, grant the necessary permissions requested by Oobeya.<br>

    <figure><img src="../../../.gitbook/assets/image (50).png" alt=""><figcaption><p>Oobeya DORA Metrics GitHub Application<br></p></figcaption></figure>

### Step 2: Create a Data Source in Oobeya

1. Navigate to the Oobeya **Data Sources** page. Look for the GitHub integration and select it.
2.  When [adding the data source](../../adding-new-integration/adding-a-new-data-source.md) in Oobeya, select "Oobeya GitHub App" as the "version".<br>

    <figure><img src="../../../.gitbook/assets/image (54).png" alt="" width="334"><figcaption><p>Select Oobeya GitHub App</p></figcaption></figure>
3. Enter the name of the data source.
4. Click the "Request GitHub Permission" button.
5.  Grant the required permissions on the GitHub website. Then you'll be redirected to the Oobeya screen.<br>

    <figure><img src="../../../.gitbook/assets/image (51).png" alt="" width="563"><figcaption></figcaption></figure>
6.  Select the newly created data source from the list and click the "Test Connection" button to see if it works properly.<br>

    <figure><img src="../../../.gitbook/assets/image (52).png" alt="" width="332"><figcaption><p>Test Connection</p></figcaption></figure>

***

## **Option 2:** Registering Your Own GitHub Application

Register your own GitHub Application to integrate with Oobeya for more flexibility and customization. By creating your own GitHub App, you can tailor the integration to suit your specific requirements and preferences. Navigate to your GitHub account settings, register a new GitHub App, configure the required permissions, and specify the Client ID and Client Secret within the Oobeya data source settings. This option offers greater control over the integration process, allowing you to manage the connection between Oobeya and GitHub according to your needs. See the step-by-step integration guide below:

### Step 1: Create a New GitHub App

1. Navigate to the **Settings** page on GitHub.
   * To register an application for a **personal account**, click on the "Developer settings" tab.
   * To register an application for an **Organization**, go to the "Organizations" tab from the left menu, then click on the "Settings" button next to the organization name.
2. On the left menu, click on "Developer settings".
3. On the left menu, click on "GitHub Apps".
4. Click on the "New GitHub App" button.
5. Fill in the required fields (GitHub App name, Homepage URL, Callback URL) with your information.
   * For the **Callback URL** field, enter the following URL: {OOBEYA\_DOMAIN}/api/platform/datasources/github \
     (e.g., https://customer.oobeya.io/api/platform/datasources/github).
6. Click the "Save Changes" button to save your changes.
7.  Open the "Permissions & events" tab from the left menu and select the following permissions as **"Read-only"** for the Actions, Administration, Code, Deployments, Issues, Members, Metadata, Organization Administration, Organization Events, Organization Projects, and Pull Requests.<br>

    <figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption><p>Permissions for your own GitHub App</p></figcaption></figure>



### Step 2: Integrate the GitHub App with Oobeya

1. Navigate to the Oobeya **Data Sources** page. Look for the GitHub integration and select it.
2. When [adding the data source](../../adding-new-integration/adding-a-new-data-source.md) for GitHub, select **"GitHub Own GitHub App"** as the "version".
3. Enter the **GitHub App Client ID** and **Client Secret** of the newly registered GitHub application.
4. Finally, click the "Request GitHub Permission" button to add the new data source.<br>

<figure><img src="../../../.gitbook/assets/image (55).png" alt="" width="329"><figcaption><p>Create your own application on GitHub and register it to Oobeya</p></figcaption></figure>

***

## Troubleshooting

* If you encounter issues with the integration, check the permissions granted during the installation process. Ensure Oobeya has access to the necessary data.
* Consult the Oobeya support documentation or contact the Oobeya support team or your assigned Customer Success Engineer for specific issues related to the Oobeya platform.

***

## **What's Next? 🎯**&#x20;

By following these instructions, you will be able to effortlessly integrate the Oobeya GitHub Application into your Oobeya account. This integration will greatly enhance your development workflow by providing you with valuable metrics and data, including [DORA metrics](https://oobeya.io/dora-metrics-four-key/) and [pull request metrics](https://oobeya.io/oobeya-metric-definitions/).

If you are not using Oobeya, feel free to [contact us](https://oobeya.io/contact/) to learn more about Oobeya GitHub integration and explore Oobeya's powerful DORA Metrics tool.

## **Next Steps** :dart:&#x20;

* [Network Access Requirements ](../../network-access-requirements.md)
* [Create a new Gitwiser Analysis](../../../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
