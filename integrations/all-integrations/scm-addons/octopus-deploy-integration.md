---
description: >-
  Learn about Octopus Deploy & Oobeya Integration. This guide will walk you
  through the steps required to integrate Octopus Deploy with Oobeya.
icon: octopus-deploy
---

# Octopus Deploy Integration

### 1. Getting the Integration URL

* Retrieve the base URL for your Octopus Deploy server directly from your browser. This URL is the address shown in the browser's address bar (e.g. `https://<your-octopus-server>`).

***

### 2. Getting the Integration API Key

1. Log in to **Octopus Deploy**.
2. Click on your **profile icon** at the bottom left of the sidebar.
3. Select **My profile** from the menu.

<figure><img src="../../../.gitbook/assets/image (539).png" alt="" width="188"><figcaption></figcaption></figure>

4. On the **My Profile** page, go to the **My API Keys** tab.
5. Click **New API Key** to generate a new API key.
6. Copy the generated key — you will need it to configure the data source in Oobeya.

<figure><img src="../../../.gitbook/assets/image (540).png" alt=""><figcaption></figcaption></figure>

> **Note:** API keys allow automated tools like Oobeya to connect to Octopus without recording your personal password. Store the key securely, as it will only be shown once.

***

### 3. Navigate to the Data Sources Screen in Oobeya

1. **Log in to Oobeya** with an Administrator account.
2. From the left menu, select **Data Sources**.
3. Choose the relevant category — **SCM & CI/CD** — from the **Categories** panel.
4. Locate **Octopus Deploy** in the list of available data sources.

<figure><img src="../../../.gitbook/assets/image (541).png" alt="" width="375"><figcaption></figcaption></figure>

***

### 4. Create Data Source and Test Connection

1. Click on **Octopus Deploy** to open the **Manage Data Sources: Octopus Deploy** window.
2. **Create a new data source**:
   * Select your **Octopus** version from the version dropdown (e.g. Octopus v1).
   * Fill out the form using the URL and API key/token obtained in the previous steps.
   * You can assign any name for the **Data Source Name** field.
3. **Test the connection**:
   * Click the **Test Connection** button to verify the connection with Octopus Deploy.
   * Once you see **Test Connection Succeeded**, click **Add** to save the data source.

<figure><img src="../../../.gitbook/assets/image (542).png" alt="" width="375"><figcaption></figcaption></figure>

***

### Ready to Connect 🐙

Your Oobeya instance is now connected to your Octopus Deploy account. You can begin tracking and analyzing your deployment processes with Oobeya's analysis tools.

### **Ready to Connect** :rocket:&#x20;

Now Oobeya is connected to your own Octopus Deploy account/server to enable you to track accurate DORA metrics calculated by Oobeya Deployment Analytics.

## **Next Steps** :dart:&#x20;

* [Network Access Requirements ](../../network-access-requirements.md)
* [Create a new Gitwiser Analysis](../../../gitwiser-repo-analytics/settings-for-git-analytics/initialize-development-analytics.md)
