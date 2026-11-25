---
description: >-
  If set to enabled, Gitwiser checks repositories periodically. Reanalyze
  processes are performed automatically if there are new commits, pull requests,
  and deployments on checked repositories.
icon: clock-rotate-left
---

# Setting Automated Reanalyze For Gitwiser

When **Development Automated Reanalysis** is enabled, Oobeya checks the analyzed repositories periodically and reanalyzes them automatically if there are new commits, pull requests, or deployments.

1. Sign in with an **Administrator** account and select **Administration** in the left menu.
2. In the **Analytics** section, select **Coding, Review & Delivery**.
3. On the **Git Analytics** tab, turn on **Development Automated Reanalysis**.
4. Select a reanalyze period from the list.
5. Click **Save**.

Oobeya checks and analyzes repositories at the following times if there are new commits, pull requests, and deployments:

* 15 Minutes: \*:00, \*:15, \*:30, \*:45
* 30 Minutes: \*:00, \*:30
* 1 Hour: \*:00
* 6 Hours: 00:00, 06:00, 12:00, 18:00
* 12 Hours: 00:00, 12:00
* 24 Hours: 00:00
