---
description: >-
  Let users sign in to Oobeya with their Okta accounts (single sign-on over
  SAML).
---

# Okta Integration

Oobeya supports single sign-on with **Okta** over **SAML**. Users sign in with their Okta account; Oobeya still decides what each user can see through its own roles.

### 1. Prepare a SAML application in Okta

In the Okta Admin Console, create a **SAML 2.0** application for Oobeya and assign the users or groups who should sign in to Oobeya. From the application, collect:

* the **single sign-on URL** of the application (users are sent here when they click **Sign in with Okta**),
* the **identity provider issuer**,
* the **X.509 signing certificate**,
* the names of the attributes that carry the user's **first name**, **last name**, and **e-mail**.

{% hint style="info" %}
The values that Okta needs about Oobeya (for example, where Okta sends the SAML response) depend on your installation. Ask the Oobeya team for them if you do not have them.
{% endhint %}

### 2. Configure Okta in Oobeya

1. Sign in to Oobeya with an **Administrator** account.
2. Select **Administration** in the left menu, then **Authentication** in the **Platform** section.
3. Open the **Okta** tab and turn on **Let users sign in to Oobeya with their Okta accounts**.
4. Fill in the fields (all are required):

| Field                    | Value                                                            |
| ------------------------ | ---------------------------------------------------------------- |
| **SSO URL**              | The single sign-on URL of the Okta application.                  |
| **ID Provider URL**      | The identity provider issuer.                                    |
| **First Name Attribute** | The name of the Okta attribute that carries the first name.      |
| **Last Name Attribute**  | The name of the Okta attribute that carries the last name.       |
| **Email Attribute**      | The name of the Okta attribute that carries the e-mail address.  |
| **SP Provider XML**      | The X.509 signing certificate used to validate Okta's responses. |

5. Click **Save**.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FQjdhF0GSCZ7V0H3tMzUS%2Fadmin-authentication.png?alt=media&#x26;token=510ba551-2f00-4677-accc-9e65e1353658" alt="Administration > Authentication page with the sign-in provider tabs"><figcaption><p>Administration > Authentication. Each sign-in provider has its own tab.</p></figcaption></figure>

Once Okta is enabled, the Oobeya sign-in page shows a **Sign in with Okta** button.

### Related

* [Microsoft Entra (Azure AD) Integration](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/azure-ad-integration)
* [Keycloak Integration](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/keycloak-integration)
* [LDAP / Active Directory Integration](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/configuring-ldap-active-directory)
* [Understanding Roles in Oobeya](https://docs.oobeya.io/administration/user-management-single-sign-on-auth-settings/understanding-roles-in-oobeya)
