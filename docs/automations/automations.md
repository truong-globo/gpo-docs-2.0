---
description: >-
  Workflows that run after an order arrives, to email you, write the options
  into the order notes, tag the order, or copy uploaded files to Google Drive.
icon: bolt
---

# Overview

An automation runs when a customer places an order containing app options. There are four types, and together they get the option details, and the files, to the people who have to act on them.

## The four workflows

The **Add workflow** screen splits them into two groups: **Order updates**, which add the selected options to the order in Shopify, and **Notifications and sync**, which send option data by email or copy uploaded files to cloud storage.

<table><thead><tr><th width="200">Workflow</th><th width="170">Group</th><th width="290">What it does</th><th>How many</th></tr></thead><tbody><tr><td><a href="update-order-notes.md">Order notes update</a></td><td>Order updates</td><td>Writes the selected options into the order's notes, so they sit with the order in your admin</td><td>One</td></tr><tr><td><a href="update-order-tags.md">Order tags update</a></td><td>Order updates</td><td>Turns the selected options into order tags, so you can filter and search orders by them</td><td>As many as you like</td></tr><tr><td><a href="email-notification.md">Email notification</a></td><td>Notifications and sync</td><td>Emails you the selected options as soon as the order comes in</td><td>One</td></tr><tr><td><a href="google-drive-sync/">Google Drive sync</a></td><td>Notifications and sync</td><td>Copies customer-uploaded files to your Drive, one folder per order</td><td>One</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/placeholder.png" alt="The four workflow templates with their descriptions"><figcaption><p>The workflow types, added from the workflow templates screen.</p></figcaption></figure>

## Which workflow to use

<table><thead><tr><th width="330">You want</th><th>Use</th></tr></thead><tbody><tr><td>To know immediately when a personalized order comes in</td><td><a href="email-notification.md">Email notification</a></td></tr><tr><td>Option details on your packing slips and invoices without editing templates</td><td><a href="update-order-notes.md">Order notes update</a> — most templates already print the note</td></tr><tr><td>To filter or route orders by what was chosen</td><td><a href="update-order-tags.md">Order tags update</a></td></tr><tr><td>To flag every order that has options at all</td><td><a href="update-order-tags.md">Order tags update</a> with a fixed tag</td></tr><tr><td>Your production team to see the options in their own tools</td><td><a href="update-order-notes.md">Order notes update</a>, or tags they can filter on</td></tr><tr><td>The photos and artwork customers upload, in a folder your team can open</td><td><a href="google-drive-sync/">Google Drive sync</a></td></tr></tbody></table>

{% hint style="info" %}
**Order notes update** is the most useful of the four for most stores. Most packing slip, invoice, and email templates already print the order note, so writing the options into the note puts them on all your paperwork without editing a Liquid template. See [Show options on orders](../storefront-display-and-design/show-options-on-orders/).
{% endhint %}

## Before you start

### Order data access

Workflows read order details, so the app requests access to your order data, including customer data, the first time you open **Automations**.

The app explains what it is requesting and confirms that the data is used only for this feature and is not distributed. Select **Update** to approve. Shopify then displays its own approval screen, the same as during the original install.

Workflows cannot run until you approve this.

### Plan

Automations may not be available on all plans. If the page displays an upgrade prompt, see [Compare plans](../plans-and-billing/compare-plans.md).

## Adding a workflow

{% stepper %}
{% step %}
### Open Automations

From the app menu.
{% endstep %}

{% step %}
### Select Add workflow

The workflow templates screen lists the four types under their two groups, with the maximum number of each you can create. A type you have already used up is marked **Limit reached**.
{% endstep %}

{% step %}
### Choose a type

The workflow editor opens.
{% endstep %}

{% step %}
### Name it and configure it

Each type has its own settings. See the page for that type.
{% endstep %}

{% step %}
### Test it

Email notification sends a test email. The other three run against a recent order. Test the workflow rather than waiting for a real order.
{% endstep %}

{% step %}
### Set the status to Active and save

Workflows have their own **Active** and **Draft** status, separate from the status of your option sets.
{% endstep %}
{% endstepper %}

## Managing workflows

The **Automations** list displays each workflow's name, type, status, and creation date, with actions to **Edit**, **Duplicate**, and **Delete**.

Duplicating is useful for order tags, where you may want one workflow for each option you filter on.

## Notes

* Workflows run on orders that contain app options. An order without options does not trigger them.
* Google Drive sync needs a connected Google account as well as a saved workflow. See [Google Drive sync](google-drive-sync/).
* They run after the order is created, so an email or a tag appears a short time later.
* A workflow set to **Draft** does not run.
* Workflows are configured per store, and are not included in option set or settings exports.
