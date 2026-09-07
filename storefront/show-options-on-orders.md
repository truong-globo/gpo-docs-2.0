---
description: Where option details appear automatically, and how to add them to packing slips, invoices, and notification emails.
icon: file-lines
---

# Show options on orders

A customer's choices are stored with their order automatically. This page covers where they appear without any setup, and the few places that need a small piece of Liquid.

## Where they appear without setup

Option values are attached to the cart line as **line item properties**, which is Shopify's own mechanism for custom order details. Your options appear anywhere Shopify already displays line item properties:

<table><thead><tr><th width="290">Place</th><th>Shows</th></tr></thead><tbody><tr><td>The cart page</td><td>Each option's <strong>Name</strong> and the customer's value, under the item</td></tr><tr><td>Checkout</td><td>The same</td></tr><tr><td>The order in Shopify admin</td><td>The same, per line item</td></tr><tr><td>Order confirmation emails</td><td>Usually, depending on your notification templates</td></tr><tr><td>Uploaded files</td><td>As links, so your team can download the originals</td></tr></tbody></table>

The label displayed is the option's **Name**, not its Label. This is why the Name matters: `Engraving text: Forever yours` tells your team what to do, and `text: Forever yours` does not. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).

<!-- SCREENSHOT: store-order-details | Shopify admin → 1 order có option | Line item với danh sách option properties bên dưới | Khoanh phần properties -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="An order in Shopify admin showing a line item with its option details listed underneath"><figcaption><p>Option details reach the order with no configuration.</p></figcaption></figure>

## Where they need a small addition

Packing slips, printed invoices, and some notification emails use templates you control. If your template does not already print line item properties, add a snippet to it.

The same snippet works in all of these templates:

```liquid
<div class="gpo-properties">
  {% assign property_size = line_item.properties | size %}
  {% if property_size > 0 %}
    {% for p in line_item.properties %}
      <div class="gpo-property">
        {% assign first_character_in_key = p.first | truncate: 1, '' %}
        {% unless p.last == blank or first_character_in_key == '_' %}
          <span>{{ p.first }}: </span>
          {%- if p.last contains '/uploads/' -%}
            <a href="{{ p.last }}">{{ p.last | split: '/' | last }}</a>
          {%- else -%}
            <span>{{ p.last }}</span>
          {%- endif -%}
        {% endunless %}
      </div>
    {% endfor %}
  {% endif %}
</div>
```

The snippet does two things:

* **It skips properties whose name starts with an underscore.** Those are the app's internal properties, which link add-ons to their parent item and carry pricing data. Your team does not need to read them. See [How it works](../reference/how-it-works.md).
* **It displays uploaded files as links** rather than as long addresses, so a packing slip stays readable.

{% hint style="info" %}
The snippet must go **inside** the template's loop over line items, where `line_item` exists. Outside that loop, it displays nothing.
{% endhint %}

## Packing slips

Shopify's Order Printer app produces packing slips from templates you can edit.

{% stepper %}
{% step %}
### Open Order Printer

In Shopify admin, go to **Apps** and open **Order Printer**.
{% endstep %}

{% step %}
### Open the packing slip template

**Manage templates**, then the packing slip template.
{% endstep %}

{% step %}
### Paste the snippet inside the line item loop

Put it where you want the option details to appear, usually directly below each item's title.
{% endstep %}

{% step %}
### Save, then print a real order

Print an order that has options, and check that every option appears and that no properties beginning with an underscore are printed.
{% endstep %}
{% endstepper %}

If you use a different packing slip or fulfillment app, the same snippet works in any Liquid template where `line_item` is available.

## Printed invoices

Use the same approach. Open your invoice template, in Order Printer or whichever app produces your invoices, and paste the snippet inside the line item loop.

## Order confirmation emails and staff notifications

Shopify's notification emails are also templates you can edit.

{% stepper %}
{% step %}
### Open your notifications

In Shopify admin, go to **Settings** > **Notifications**.
{% endstep %}

{% step %}
### Choose the notification to edit

Select **Order confirmation** for the customer's copy, or **New order** for the notification your staff receive.
{% endstep %}

{% step %}
### Find the line item loop

Find the part of the template that loops over the order's line items and prints each title.
{% endstep %}

{% step %}
### Paste the snippet inside that loop

Then save the template.
{% endstep %}

{% step %}
### Send yourself a test

Shopify can send a preview. It is better to place a test order with options and check the email that arrives.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
These templates are your store's own emails. Copy the existing template somewhere safe before you change it, so you can restore it.

If you would rather not edit them yourself, support can supply ready-made versions of these templates. See [Contact support](../help/contact-support.md).
{% endhint %}

## Alternative: use an automation

If you would rather not edit templates, a [workflow](../automations/README.md) produces much of the same result without any Liquid:

<table><thead><tr><th width="290">Workflow</th><th>Result</th></tr></thead><tbody><tr><td><a href="../automations/email-notification.md">Email notification</a></td><td>Emails you every order with its options, in a format you control</td></tr><tr><td><a href="../automations/update-order-notes.md">Update order notes</a></td><td>Writes the options into the order's notes — and the note already appears on packing slips, invoices, and emails in most templates</td></tr><tr><td><a href="../automations/update-order-tags.md">Update order tags</a></td><td>Tags the order by the option chosen, so you can filter and route orders</td></tr></tbody></table>

**Update order notes** is the most useful of these. Most templates already print the order note, so writing the options into the note puts them on your paperwork without editing a template.

## Notes

* Option details on an order are a record of that order. Renaming an option later does not change orders that have already been placed.
* Uploaded files stay available from the order in Shopify admin.
* Add-on products appear as their own line items unless you merge them. See [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).
* Properties whose name begins with an underscore are internal to the app. Do not print them or build processes around them.
