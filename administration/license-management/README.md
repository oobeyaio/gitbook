---
description: Learn about Oobeya License Management.
icon: file-certificate
---

# License Management

Oobeya needs a valid license key to run. The license is bound to your Oobeya installation through its **Server ID**, and it defines the license type, the expiry date, the features you can use, and, for limited licenses, how many teams, users, and analyses you can create.

To open the page, sign in with an **Administrator** account, select **Administration** in the left menu, then **License Management** in the **Platform** section.

<figure><img src="https://images.gitbook.com/__img/dpr=2,width=760,onerror=redirect,format=auto,signature=360470707/https%3A%2F%2Ffiles.gitbook.com%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FVjZ4dLgzPRyNyJrOqhZt%2Fadmin-license.png%3Falt%3Dmedia%26token%3D60e0ba30-593f-4a2a-a694-f2e63dfce1a6" alt="Administration, License Management page with Server ID, license type, expiry date, license key field, and licensed features"><figcaption><p>Administration > License Management. Server ID and dates are sample values.</p></figcaption></figure>

### What the page shows

| Area                  | What it shows                                                                                                                                                                                                                                                                                                                                |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Server ID**         | The unique ID of your Oobeya installation. Share it with the Oobeya Sales Team to get a license for this server. Use the copy button next to it.                                                                                                                                                                                             |
| **License Type**      | The type of the active license (for example **PAID**).                                                                                                                                                                                                                                                                                       |
| **Expiry Date**       | The last day the license is valid.                                                                                                                                                                                                                                                                                                           |
| **License Key**       | The field where you enter a new or renewed key. Click **Save** to apply it or **Reset** to clear your changes. See [Updating The License Key](https://docs.oobeya.io/administration/license-management/updating-the-license-key).                                                                                                            |
| **License Limits**    | Shown for limited licenses: the maximum team, user, profile, league, dashboard, Git analysis, and board analysis counts, and the available add-ons. You cannot create more items than these limits allow.                                                                                                                                    |
| **Licensed Features** | The modules your license covers, such as Dashboards, Organization, Developer Heatmap, Resource Allocation, Trend Reports, Test Analytics, Problem Analytics, Analysis Efficiency, AI Usage, DevEx Surveys, Document Analytics, and Individual Scorecard. A module that is not licensed shows **Not licensed** with a **Contact Sales** link. |

{% hint style="info" %}
A licensed feature can still be turned off for your organization in **Administration** > **Feature Management**.
{% endhint %}

### Expiry notices

Before the license expires, Oobeya shows a notice that the license will expire soon, with the expiry date and a **Contact Sales** link. After the expiry date, Oobeya shows that the license has expired and you can no longer use Oobeya until a renewed key is saved.

To renew, contact the [Oobeya Sales Team](https://oobeya.io/contact-sales/) with your Server ID, then [update the license key](https://docs.oobeya.io/administration/license-management/updating-the-license-key).

### Error messages

| Message                                              | What to do                                                                                                                                   |
| ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Invalid license key.**                             | Check that you pasted the whole key without extra spaces or line breaks.                                                                     |
| **This license key does not belong to this server.** | The key was created for another Server ID. Send the Server ID shown on this page to the Oobeya Sales Team and ask for a key for this server. |
| **The license key could not be saved.**              | Check the key and try again. If it keeps failing, contact Oobeya support.                                                                    |
