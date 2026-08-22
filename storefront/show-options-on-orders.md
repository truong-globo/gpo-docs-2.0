---
description: Where option details appear automatically, and how to add them to packing slips, invoices, and notification emails.
icon: file-lines
---

# Show options on orders

The choices a customer makes travel with their order automatically. This page covers where they already appear, and the few places that need a small piece of Liquid to show them.

## Where they appear with no setup

Option values are attached to the cart line as **line item properties** — Shopify's own mechanism for custom order details. So anywhere Shopify already displays line item properties, your options appear:

<table><thead><tr><th width="290">Place</th><th>Shows</th></tr></thead><tbody><tr><td>The cart page</td><td>Each option's <strong>Name</strong> and the customer's value, under the item</td></tr><tr><td>Checkout</td><td>The same</td></tr><tr><td>The order in Shopify admin</td><td>The same, per line item</td></tr><tr><td>Order confirmation emails</td><td>Usually, depending on your notification templates</td></tr><tr><td>Uploaded files</td><td>As links, so your team can download the originals</td></tr></tbody></table>

The label shown is the option's **Name**, not its Label — which is why the Name matters. `Engraving text: Forever yours` is actionable; `text: Forever yours` is not. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).

<!-- SCREENSHOT: store-order-details | Shopify admin → 1 order có option | Line item với danh sách option properties bên dưới | Khoanh phần properties -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="An order in Shopify admin showing a line item with its option details listed underneath"><figcaption><p>Option details reach the order with no configuration.</p></figcaption></figure>

## Where they need a small addition

Packing slips, printed invoices, and some notification emails use templates you control. If yours does not already print line item properties, add a snippet to it.

The snippet is the same in every case:

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

Two things it does that matter:

* **It skips properties whose name starts with an underscore.** Those are the app's internal properties, which link add-ons to their parent item and carry pricing data. They are not for your team to read. See [Line item properties](../reference/line-item-properties.md).
* **It renders uploaded files as links** rather than as long addresses, so a packing slip stays readable.

{% hint style="info" %}
It must go **inside** the template's loop over line items, where `line_item` exists. Pasting it outside that loop renders nothing.
{% endhint %}

## Packing slips

Shopify's own Order Printer app produces packing slips from templates you can edit.

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

Put it where you want the option details to appear — usually directly under each item's title.
{% endstep %}

{% step %}
### Save, then print a real order

Print an order that actually has options, and check every option appears and no underscore-prefixed properties leak through.
{% endstep %}
{% endstepper %}

If you use a different packing slip or fulfilment app, the same snippet works wherever that app lets you edit a Liquid template with `line_item` in scope.

## Printed invoices

The same approach. Open your invoice template — in Order Printer or whichever app produces them — and paste the snippet inside the line item loop.

## Order confirmation emails and staff notifications

Shopify's notification emails are templates you can edit.

{% stepper %}
{% step %}
### Open your notifications

In Shopify admin, go to **Settings** > **Notifications**.
{% endstep %}

{% step %}
### Choose the notification to edit

**Order confirmation** for the customer's copy. **New order** for the notification your staff receive.
{% endstep %}

{% step %}
### Find the line item loop

Look for where the template loops over the order's line items and prints each title.
{% endstep %}

{% step %}
### Paste the snippet inside that loop

Then save.
{% endstep %}

{% step %}
### Send yourself a test

Shopify can send a preview. Better still, place a real test order with options and check the email that arrives.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
Editing notification templates is editing your own store's email. Copy the existing template somewhere safe before you change it, so you can put it back.

If you would rather not, we can supply ready-made versions of these templates — see [Contact support](../help/contact-support.md).
{% endhint %}

## The alternative: let an automation do it

If editing templates is not appealing, a [workflow](../automations/README.md) achieves much of the same result with no Liquid at all:

<table><thead><tr><th width="290">Workflow</th><th>Result</th></tr></thead><tbody><tr><td><a href="../automations/email-notification.md">Email notification</a></td><td>Emails you every order with its options, in a format you control</td></tr><tr><td><a href="../automations/update-order-notes.md">Update order notes</a></td><td>Writes the options into the order's notes — and the note already appears on packing slips, invoices, and emails in most templates</td></tr><tr><td><a href="../automations/update-order-tags.md">Update order tags</a></td><td>Tags the order by the option chosen, so you can filter and route orders</td></tr></tbody></table>

**Update order notes** is the neat trick here. Most templates already print the order note, so writing options into the note puts them on your paperwork without touching a template.

## Notes

* Option details on an order are a record of that order. Renaming an option later does not change orders already placed.
* Uploaded files stay available from the order in Shopify admin.
* Add-on products appear as their own line items unless you merge them. See [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).
* Properties whose name begins with an underscore are internal. Do not print them, and do not rely on them.

## Troubleshooting

<details>
<summary>Options appear in the cart but not on my packing slip</summary>

Your packing slip template does not print line item properties. Add the snippet above, inside the line item loop.
</details>

<details>
<summary>The snippet renders nothing</summary>

It is outside the line item loop, so `line_item` does not exist there. Move it inside.
</details>

<details>
<summary>Odd technical entries appear on my paperwork</summary>

Your template is printing every property, including the internal ones. Use the snippet above — it skips names beginning with an underscore.
</details>

<details>
<summary>Uploaded files show as long unreadable addresses</summary>

The snippet renders them as links. If you wrote your own loop, add the same handling.
</details>

<details>
<summary>Option names on orders are unhelpful</summary>

They are the options' **Name** values. Set them to something readable — for future orders. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).
</details>

<details>
<summary>I would rather not edit templates</summary>

Use an [Update order notes](../automations/update-order-notes.md) workflow, or ask support for ready-made templates.
</details>
