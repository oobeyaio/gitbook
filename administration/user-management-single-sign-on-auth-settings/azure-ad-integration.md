---
description: Learn about Azure Active Directory & Oobeya integration.
icon: windows
---

# Microsoft Entra (Azure AD) Integration

## **OVERVIEW**

**Azure Active Directory integration** allows users to log in to [Oobeya](https://oobeya.io/) with their AD credentials.

When a user logs in to Oobeya via Azure AD connection, the account of the user is created on Oobeya with the **least privilege**. Then you need to define the required permissions for the users.

You can also **import users from Azure AD**. [_See the documentation_](importing-a-new-user-from-ldap-ad.md) for detailed information.

You can deactivate user accounts that you do not want to log in to the Oobeya. Click [here ](deactivating-a-user.md)to learn how to deactivate a user account.

## 1. CREATING THE OOBEYA APPLICATION IN AZURE AD

1. Open the directory page, select the "**App Registration**" in the sidebar (left) and then click "**New Registration**".&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FqDmOkIUM37rsXrKXt3Uh%2Ffile.png?alt=media)

2\. Fill in the required areas and click to "**Register**" button.&#x20;

![Inserting image...](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FdZnDEhS5wOH5h6uCVuri%2Ffile.png?alt=media)

3\. Click on the details of the registration you have just created, and then note the "**Tenant ID**" and "**Client ID**" to use in Oobeya later.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FcjlgHZCTNLezAt8p7We2%2Ffile.png?alt=media)

4\. Now, click on the "**Certificates & Secrets**" in the sidebar, and then click the "**New Client Secret**" button. You will use "**Value**" as the third parameter in Oobeya (**Client Secret**).&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FEyOa1IdTdsZDZZKhk1eV%2Ffile.png?alt=media)

5\. Check and configure the **API permission:**

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2Fb8oMZrGBPrHd11aVds3X%2Ffile.png?alt=media)

## 2. CONFIGURING AZURE AD ON OOBEYA

1. Everything is ready. Now, open the Oobeya and then click the **Administration** in the sidebar as in the following:

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FwjbbvAnuBDqVAGEBYbay%2Ffile.png?alt=media)

2\. Click the "**Go to Admin Settings**" button.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F2NNyPx0Hya8DwrnwLKO0%2Ffile.png?alt=media)

3\. In the "**General settings**" click the "**Azure AD Settings**" tab, enable the configuration by turning the switch on, fill in the required areas and then click the "**Save**" button.&#x20;

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FkeNcCp8wFjw7a13PyXZw%2Ffile.png?alt=media)
