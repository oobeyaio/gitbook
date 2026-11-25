---
description: Learn about how to configure LDAP / Active Directory on QA Dashboard...
icon: user-group
---

# LDAP / Active Directory Integration

### **OVERVIEW**

**LDAP / AD integration** allows users to log in to Oobeya with their LDAP / AD credentials.

When a user logs in to Oobeya via LDAP connection, the account of the user is created on Oobeya with the **least privilege**. Then you need to define the required permissions for the users.

You can also **import users from LDAP / AD**. [_See the documentation_](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/importing-a-new-user-from-ldap-ad) for detailed information.

You can deactivate user accounts that you do not want to log in to the Oobeya. Click [here ](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/deactivating-a-user)to learn how to deactivate a user account.

### **1. ENABLING LDAP AUTHENTICATION**

1\. Select **Administration** in the left menu, then **Authentication** in the **Platform** section.

2\. Open the **LDAP** tab.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FDa4ol0C1eo55KexQJfIg%2Ffile.png?alt=media)

3\. Click the switch to enable LDAP authentication.

### **2. CONFIGURING LDAP**

1\. After enabling LDAP authentication, fill in the form with your own LDAP configuration.

![](https://firebasestorage.googleapis.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2F7amKVKT1ucohK7KBGdXf%2Ffile.png?alt=media)

2\. Click the **"Save"** button.

* **Hostname:** Hostname or IP address of the server running LDAP. _(Example: ldap.mydomain.com)_
* **Port:** Port of the server running LDAP.
* **User DN:** _Bind DN_, A read only user that can perform LDAP searches. _(Example: cn=user,dc=domain,dc=name)_
* **Password:** Password of the bind user.
* **Base DN:** Root LDAP node from which to search for users and groups. _(Example: cn=users,dc=mydomain,dc=com)_

### WHAT'S NEXT?

* [Importing a new user from LDAP / AD](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/importing-a-new-user-from-ldap-ad)
