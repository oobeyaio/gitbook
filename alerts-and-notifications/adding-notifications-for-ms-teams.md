---
description: Learn about how to add notifications for Microsoft Teams channels...
---

# Adding Notifications for MS Teams

## **OVERVIEW**

[Oobeya](https://oobeya.io/) integrates with **Microsoft Teams** to send notification messages and reports to your channels. See the steps below to add _channels, connectors, and incoming webhooks_ for MS Teams.

{% hint style="info" %}
After creating incoming webhooks, you can connect the Oobeya notification service with Microsoft Teams.
{% endhint %}

## **1. CREATING A NEW TEAM CHANNEL ON** MS TEAMS :speech\_balloon:&#x20;

1. Go to **Microsoft Teams** and open the _**Teams**_ tab.
2. Click the **"Add channel"** option to create a new Teams channel.

![](<../.gitbook/assets/image (174).png>)

3\. Enter the channel name and select the privacy option.

![](<../.gitbook/assets/image (296).png>)

4\. Add members to the channel and close the popup.

![](<../.gitbook/assets/image (163).png>)

## **2. ADDING CONNECTORS / WEBHOOKS TO THE TEAM** :electric\_plug:&#x20;

1. Select the **"Connectors"** option for the channel.

![](<../.gitbook/assets/image (115).png>)

2\. Click the **Configure** button for the **Incoming Webhook**.

![MS Teams Connectors](<../.gitbook/assets/image (324).png>)

3\. Enter a name for the connector (e.g. _qa-dashboard_) and upload an icon (optional). Then click **Create**.

![](<../.gitbook/assets/image (287).png>)

4\. Copy the **Webhook URL**. It will be used for the Oobeya notification configuration.&#x20;

![Copy incoming webhook URL](<../.gitbook/assets/image (148).png>)

5\. You can find your configured Incoming Webhook URLs on the connectors popup when needed.

![MS Teams Configured Connectors](<../.gitbook/assets/image (72).png>)

## **3. ADDING NOTIFICATIONS ON QA DASHBOARD** :bell:&#x20;

1. Open the **Profiles & Teams**. Select the **Teams** tab to add a team notification.
2. Click the **Add Notification** button and configure the notification settings.

![](<../.gitbook/assets/image (187).png>)

3\. You can test the connection via the "Send Notification Now" button.

4\. Click **Add** to save the notification settings.

{% hint style="success" %}
**That's it!** Now you have a scheduled notifier for your **Microsoft Teams** channel.&#x20;
{% endhint %}
