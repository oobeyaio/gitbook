---
icon: plug-circle-check
---

# Adding New Integration

Since Oobeya 2.1, all integrations and their data sources live on a single **Integrations** page. There is no separate Marketplace, Data Sources page, or install step: select a tool and add its data source.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MGIlBSTjQtZxUoFwUx4%2Fuploads%2FHse7i91bO4p05dwNDfRr%2Fintegrations-page.png?alt=media&#x26;token=7c6d68c4-3f16-4465-8558-24bd70761735" alt="Oobeya Integrations page with tools grouped by category"><figcaption><p>The Integrations page groups every supported tool by category.</p></figcaption></figure>

{% stepper %}
{% step %}
#### Open Integrations

Sign in with an **Administrator** or **Super User** account and select **Integrations** in the **Administration** section of the left menu. [Installing an Addon](https://docs.oobeya.io/integrations/adding-new-integration/installing-an-addon) explains the page and what changed in 2.1.
{% endstep %}

{% step %}
#### Add a data source

Select the tool's card and fill in the connection form. See [Adding a New Data Source](https://docs.oobeya.io/integrations/adding-new-integration/adding-a-new-data-source).
{% endstep %}

{% step %}
#### Test and save

Click **Test Connection**, then **Add**. You can re-check, edit, or delete the data source later. See [Updating and Deleting Data Sources](https://docs.oobeya.io/integrations/adding-new-integration/updating-and-deleting-data-sources).
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Tool-specific steps, such as which token to create and which permissions it needs, are in the [Integration Catalog](https://docs.oobeya.io/integrations/all-integrations).
{% endhint %}
