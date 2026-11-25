---
description: Learn about how to manage existing Data Sources...
icon: plug-circle-minus
---

# Updating and Deleting Data Sources

Data sources need attention when, for example:

* a token expires or is revoked,
* the server's domain name changes,
* the service account's password or permissions change.

Oobeya checks the connection of every data source each night. Failed checks show on the tool's card on the **Integrations** page (**N failed**) and in a banner at the top of the page.

### Opening a tool's data sources

1. Select **Integrations** in the **Administration** section of the left menu.
2. Click the tool's card. The **Manage Data Sources** window lists its data sources.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FITAgI7q2VVeVGS1730DJ%2Fdatasource-list.png?alt=media&#x26;token=39b5353d-8708-45b9-add2-9586456d8332" alt="Manage Data Sources window with the data source list"><figcaption><p>The data source list of a tool, with the actions of each data source.</p></figcaption></figure>

Each data source has these actions:

| Icon   | Action                                                                                                                                       |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Reload | **Check now**: runs the connection check for this data source. When a check fails, the list shows how long the data source has been failing. |
| Pencil | **Edit**: opens the form to update the data source.                                                                                          |
| Trash  | **Delete**: deletes the data source after confirmation.                                                                                      |

To check every data source of every tool at once, click **Check all now** at the top right of the Integrations page.

### Updating a data source

1. Open the tool's data sources and click the **edit** (pencil) icon.
2. Change the fields you need. The form also shows the **Data Source ID**, which you can copy (some API calls and support requests need it).
3. Click **Test Connection**, then **Update**.

### Deleting a data source

{% hint style="warning" %}
Deleting a data source cannot be undone. Analyses that use it stop receiving data.
{% endhint %}

1. Open the tool's data sources and click the **delete** (trash) icon.
2. In the **Delete Data Source** window, type the data source name to confirm, then click **Delete**.

When you delete the last data source of a tool, the tool's card goes back to **Not connected**.

### What's next?

* [Adding a New Data Source](https://docs.oobeya.io/integrations/adding-new-integration/adding-a-new-data-source)
