---
description: Workflows that run after an order arrives — email yourself, write the options into the order notes, or tag the order.
icon: bolt
---

# Overview

An automation runs when a customer places an order containing app options. Three kinds are available, and between them they solve the problem of getting option details to the people who have to act on them.

## The three workflows

<table><thead><tr><th width="230">Workflow</th><th width="290">What it does</th><th>How many</th></tr></thead><tbody><tr><td><a href="email-notification.md">Email notification</a></td><td>Emails you the order and the options chosen</td><td>One</td></tr><tr><td><a href="update-order-notes.md">Update order notes</a></td><td>Writes the options into the order's notes</td><td>One</td></tr><tr><td><a href="update-order-tags.md">Update order tags</a></td><td>Tags the order — a fixed tag, or the value the customer chose</td><td>As many as you like</td></tr></tbody></table>

<!-- SCREENSHOT: auto-templates | App admin → Automations → Workflow templates | 3 thẻ workflow với icon và mô tả | Không khoanh -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The three workflow templates with their descriptions"><figcaption><p>Three workflow types, added from the workflow templates screen.</p></figcaption></figure>

## Which one you want

<table><thead><tr><th width="330">You want</th><th>Use</th></tr></thead><tbody><tr><td>To know immediately when a personalised order comes in</td><td><a href="email-notification.md">Email notification</a></td></tr><tr><td>Option details on your packing slips and invoices without editing templates</td><td><a href="update-order-notes.md">Update order notes</a> — most templates already print the note</td></tr><tr><td>To filter or route orders by what was chosen</td><td><a href="update-order-tags.md">Update order tags</a></td></tr><tr><td>To flag every order that has options at all</td><td><a href="update-order-tags.md">Update order tags</a> with a fixed tag</td></tr><tr><td>Your production team to see the options in their own tools</td><td><a href="update-order-notes.md">Update order notes</a>, or tags they can filter on</td></tr></tbody></table>

{% hint style="info" %}
**Update order notes** is the most quietly useful of the three. Because most packing slip, invoice, and email templates already print the order note, writing options into the note puts them on all your paperwork without touching a single Liquid template. See [Show options on orders](../storefront/show-options-on-orders.md).
{% endhint %}

## Before you start

### Order data access

Workflows read order details, so the app asks for access to your order data — including customer data — the first time you open **Automations**.

The app explains what it is asking for and confirms the data is used only for this feature and is not distributed. Select **Update** to approve, and Shopify shows its own approval screen, exactly like the original install.

Until you approve it, workflows cannot run.

### Plan

Automations are plan-gated. If the page shows an upgrade prompt, see [Compare plans](../plans/compare-plans.md).

## Adding a workflow

{% stepper %}
{% step %}
### Open Automations

From the app menu.
{% endstep %}

{% step %}
### Select Add workflow

The workflow templates screen lists the three types, with the maximum number of each you can have.
{% endstep %}

{% step %}
### Choose a type

The workflow editor opens.
{% endstep %}

{% step %}
### Give it a name and configure it

Each type has its own settings — see its page.
{% endstep %}

{% step %}
### Test it

Email notification sends a test email. The other two run against a real recent order without changing it. Use this rather than waiting for a real order.
{% endstep %}

{% step %}
### Set the status to Active and save

Workflows have their own **Active** and **Draft** status, separate from your option sets.
{% endstep %}
{% endstepper %}

## Managing them

The **Automations** list shows each workflow's name, type, status, and creation date, with actions to **Edit**, **Duplicate**, and **Delete**.

Duplicating is useful for order tags, where you may want several rules — one per option you care about.

## Notes

* Workflows run on orders that contain app options. An order with no options does not trigger them.
* They run after the order is created, so there is a short delay before an email arrives or a tag appears.
* A workflow set to **Draft** does nothing.
* Workflows are configured per store, and are not included in option set or settings exports.
