---
description: Learn about Gitea & Oobeya Integration
icon: mug-tea
---

# Gitea Integration

This guide provides a step-by-step walkthrough to integrate your **Gitea** code review system with **Oobeya** to track engineering metrics and DORA analytics.

***

### 1. Create Gitea Access Tokens 🔑

To allow Oobeya to access your Gitea repositories, you need to generate an access token.

1. **Settings:** Click the user icon in the top-right corner of your Gitea UI, navigate to **Settings**.
2. **Generate Token:** Open the **"HTTP Credentials"** tab on the left sidebar and click the **"Generate New Password"** button.

<figure><img src="../../../.gitbook/assets/foto1.png" alt=""><figcaption></figcaption></figure>

3. **Secure Your Password:** Copy and save the generated password immediately. You will need this for the Oobeya data source configuration.

***

### 2. Install Gitea Add-on on Oobeya 🧩

Before connecting your data, ensure the Gitea integration is active in your Oobeya instance.

1. Log in to **Oobeya** with an **Administrator** account.
2. Navigate to **Integrations** from the side menu.
3. Locate the **Gitea** add-on and click the **"Install"** button.

<figure><img src="../../../.gitbook/assets/foto2.png" alt=""><figcaption></figcaption></figure>

***

### 3. Add A New Data Source 🔌

Now, connect your Gitea server to start fetching data.

1. Navigate to **Data Sources** and select **Gitea** from the SCM & CI/CD category.

<figure><img src="../../../.gitbook/assets/foto3 (1).png" alt=""><figcaption></figcaption></figure>

2. Click the **"New Data Source"** button and fill in the required fields:

* **Server URL:** Your Gitea instance URL (e.g., `https://gitea.yourdomain.com`).
* **Token:** The **Access Token** you generated in Step 1.
* Click **"Test Connection"** to verify the credentials.
* Once verified, click **"Add"** to finalize the setup.

***

### Ready to Connect 🚀

**Congratulations!** Oobeya is now connected to your Gitea server. It will begin pulling real-time statistics from your repositories to track development velocity, code review cycles, and team performance.
