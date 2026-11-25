---
description: Learn about Azure Active Directory & Oobeya integration.
icon: windows
---

# Microsoft Entra (Azure AD) Integration

### **OVERVIEW**

**Azure Active Directory integration** allows users to log in to [Oobeya](https://oobeya.io/) with their AD credentials.

When a user logs in to Oobeya via Azure AD connection, the account of the user is created on Oobeya with the **least privilege**. Then you need to define the required permissions for the users.

You can also **import users from Azure AD**. [_See the documentation_](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/importing-a-new-user-from-ldap-ad) for detailed information.

You can deactivate user accounts that you do not want to log in to the Oobeya. Click [here ](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/deactivating-a-user)to learn how to deactivate a user account.

### 1. CREATING THE OOBEYA APPLICATION IN AZURE AD

1. Open the directory page, select the "**App Registration**" in the sidebar (left) and then click "**New Registration**".

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FqDmOkIUM37rsXrKXt3Uh%2Ffile.png?alt=media)

2\. Fill in the required areas and click to "**Register**" button.

![Inserting image...](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FdZnDEhS5wOH5h6uCVuri%2Ffile.png?alt=media)

3\. Click on the details of the registration you have just created, and then note the "**Tenant ID**" and "**Client ID**" to use in Oobeya later.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FcjlgHZCTNLezAt8p7We2%2Ffile.png?alt=media)

4\. Now, click on the "**Certificates & Secrets**" in the sidebar, and then click the "**New Client Secret**" button. You will use "**Value**" as the third parameter in Oobeya (**Client Secret**).

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FEyOa1IdTdsZDZZKhk1eV%2Ffile.png?alt=media)

5\. Check and configure the **API permission:**

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fb8oMZrGBPrHd11aVds3X%2Ffile.png?alt=media)

### 2. CONFIGURING AZURE AD ON OOBEYA

1. In Oobeya, select **Administration** in the left menu, then **Authentication** in the **Platform** section.
2. Open the **Microsoft Entra ID** tab and turn on **Let users sign in to Oobeya with their Microsoft Entra ID accounts**.
3. Fill in **Tenant ID**, **Client ID**, and **Client Secret** from the app registration above. **Email Key**, **Given Name Key**, and **Family Name Key** are optional claim names.
4. Optionally, turn on **Automatically remove user accounts from Oobeya if removed from Microsoft Entra ID**.
5. Click **Save**.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FQjdhF0GSCZ7V0H3tMzUS%2Fadmin-authentication.png?alt=media&#x26;token=510ba551-2f00-4677-accc-9e65e1353658" alt="Administration > Authentication, Microsoft Entra ID tab"><figcaption><p>Administration > Authentication > Microsoft Entra ID.</p></figcaption></figure>
