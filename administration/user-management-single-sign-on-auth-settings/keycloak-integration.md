---
description: >-
  This guide explains how to integrate Keycloak with Oobeya to enable Single
  Sign-On (SSO) authentication for your users.
icon: asterisk
---

# Keycloak Integration

### Overview

By integrating Keycloak as an identity provider, Oobeya can authenticate users via your existing IAM setup, improving security, user experience, and centralized access management.

***

### Prerequisites

Before you begin, make sure you have:

* Access to a **Keycloak instance** with admin privileges
* Access to **Oobeya Admin Panel**
* Your **Keycloak Base URL**
* Your **Oobeya Base URL**

***

### Part 1: Configure Keycloak

#### Step 1: Create a New Client

1. Log in to the **Keycloak Admin Console**
2. Select your **Realm** (or create a new one)
3. Navigate to **Clients** from the left menu
4. Click **Create**

***

#### Step 2: General Settings

Configure the client with the following values:

<table><thead><tr><th width="303.906982421875">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Client ID</td><td><code>oobeya-client</code></td></tr><tr><td>Name</td><td>Oobeya (optional)</td></tr><tr><td>Description</td><td>Integration with Oobeya platform (optional)</td></tr><tr><td>Always display in UI</td><td>On</td></tr></tbody></table>

***

#### Step 3: Access Settings

| Setting                         | Value                        | Example                                            |
| ------------------------------- | ---------------------------- | -------------------------------------------------- |
| Root URL                        | `{{YOUR_OOBEYA_BASE_URL}}`   | [https://app.oobeya.io](https://app.oobeya.io/)    |
| Home URL                        | `{{YOUR_OOBEYA_BASE_URL}}/*` | [https://app.oobeya.io/](https://app.oobeya.io/)\* |
| Valid Redirect URIs             | `{{YOUR_OOBEYA_BASE_URL}}/*` | [https://app.oobeya.io/](https://app.oobeya.io/)\* |
| Valid Post Logout Redirect URIs | Optional                     | Leave empty or define explicitly                   |
| Web Origins                     | `{{YOUR_OOBEYA_BASE_URL}}`   | Add dev URLs if required                           |
| Admin URL                       | `{{YOUR_OOBEYA_BASE_URL}}`   | [https://app.oobeya.io](https://app.oobeya.io/)    |

***

#### Step 4: Capability Configuration

Set authentication flows as follows:

* **Client Authentication:** On
* **Authorization:** Off
* **Authentication Flow:**
  * ✅ Standard Flow
  * ⛔ All others disabled

> ⚠️ **Important:** Only **Standard Flow** should be enabled for Oobeya.

***

#### Step 5: Client Credentials

1. Open the **Credentials** tab
2. Copy the **Client Secret**
3. Store it securely — it will be required in Oobeya

***

### Part 2: Configure Oobeya

#### Step 1: Open Keycloak Settings

1. Log in to Oobeya as an **Administrator**
2. Navigate to **Settings > Keycloak Authentication**

***

#### Step 2: Enable Keycloak Authentication

Enable the toggle:

> **Configure Keycloak settings to authenticate users**

***

#### Step 3: Connection Settings

Fill in the required fields:

<table><thead><tr><th width="209.48736572265625">Field</th><th>Description</th><th>Example</th></tr></thead><tbody><tr><td>Base URL</td><td>Keycloak server URL</td><td><a href="https://keycloak.company.com/">https://keycloak.company.com</a></td></tr><tr><td>Callback URL</td><td>Oobeya callback endpoint</td><td><code>{{YOUR_OOBEYA_BASE_URL}}/callback</code></td></tr><tr><td>Realm</td><td>Keycloak realm name</td><td>oobeya</td></tr><tr><td>Client ID</td><td>Must match Keycloak</td><td>oobeya-client</td></tr><tr><td>Client Secret</td><td>From Keycloak</td><td>********</td></tr></tbody></table>

***

#### Step 4: User Management Options

**Do not allow login if user does not exist in Oobeya**

* **Default:** Enabled
* Requires users to be pre-created in Oobeya

**Create a profile for every user logging in via Keycloak**

* **Default:** Enabled
* Automatically creates user profiles on first login

**Recommended Configurations**

* **Controlled access:** Enable both options
* **Automatic provisioning:** Disable user existence check, enable profile creation

***

#### Step 5: Save Configuration

* Review all settings
* Click **Save** to apply
* Use **Reset** to discard changes

***

### Part 3: Test the Integration

#### Authentication Test

1. Log out of Oobeya
2. Open the Oobeya login page
3. Click **Login with Keycloak**
4. Authenticate via Keycloak
5. Verify successful redirect to Oobeya

***

#### Verify User Creation

1. Log in as an Oobeya admin
2. Open **Users** section
3. Confirm Keycloak users are listed (if auto-provisioning is enabled)

***

### Troubleshooting

* Ensure redirect URLs match exactly
* Verify realm and client ID consistency
* Check Keycloak logs for authentication errors
* Validate client secret correctness

***

If you need help, contact **Oobeya Support** or your solution partner.
