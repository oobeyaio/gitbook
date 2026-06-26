---
description: >-
  Oobeya utilizes a role-based access control system to manage user permissions
  and define responsibilities within your organization.
---

# Understanding Roles in Oobeya

### Application/System Roles

Application Roles are pre-defined roles within Oobeya that manage the permissions of users. They determine what a user can access and what operations they can perform within the application. The default Application Role is **Role User**.

<figure><img src="../../.gitbook/assets/image (430).png" alt=""><figcaption><p>Oobeya Application Roles</p></figcaption></figure>

***

### Available Application Roles

#### **1. Role User (Default)**

&#x20;This is the default role assigned to new users.

* **Permissions**:
  * Can access dashboards and team scorecards that are shared with them.
  * Can access their own scorecard.
* **Restrictions**:
  * Cannot access private dashboards not shared with them.
  * Cannot perform administrative operations.

***

#### **2. Role Admin**

Users with this role have full administrative rights within Oobeya.

* **Permissions**:
  * Can manage all operations, including:
    * Adding and managing integrations.
    * Managing data sources.
    * Accessing admin settings.
  * Can access all dashboards, analytics, and scorecards.
* **Ideal for**: Administrators who need full control over the Oobeya environment.

***

#### **3. Role Executive**

Designed for executive-level users who need insight into team and individual performance.

* **Permissions**:
  * Can access all Team and Individual Scorecards.
* **Restrictions**:
  * Cannot access admin settings.
  * Cannot manage integrations or data sources.
* **Ideal for**: Executives and managers who need to access all data without administrative capabilities.

***

#### **4. Role Superuser**

* **Description**: A system role specifically for on-premise instances (the first user) of Oobeya

***

### Summary

By effectively managing Application Roles, you can ensure that users have appropriate access levels and that their responsibilities within Oobeya align with their roles in your organization.

* **Role User**: Default role with limited access; can view shared dashboards, teams, and individual scorecards.
* **Role Admin**: Full access to all features and settings; can manage integrations and data sources.
* **Role Executive**: Access to all team and individual scorecards; cannot access admin settings.
* **Role Superuser**: System role for on-premise instances.
