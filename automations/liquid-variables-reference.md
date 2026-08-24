---
description: The Liquid variables available in email and order note templates.
icon: brackets-curly
---

# Liquid variables reference

Both the [email notification](email-notification.md) and [order notes](update-order-notes.md) templates accept Liquid variables. The app carries this list built in, reachable from the editor itself, so you never need to leave the page to check a name.

## General

Order-level values.

<table><thead><tr><th width="290">Variable</th><th>Contains</th></tr></thead><tbody><tr><td><code>{{ shop.name }}</code></td><td>Your shop's name</td></tr><tr><td><code>{{ order_number }}</code></td><td>The order number, without a prefix</td></tr><tr><td><code>{{ order_name }}</code></td><td>The order name, including the <code>#</code></td></tr><tr><td><code>{{ subtotal_price | money }}</code></td><td>Subtotal, formatted as money</td></tr><tr><td><code>{{ tax_price | money }}</code></td><td>Total tax</td></tr><tr><td><code>{{ total_price | money }}</code></td><td>Order total</td></tr></tbody></table>

## Shop details

<table><thead><tr><th width="290">Variable</th><th>Contains</th></tr></thead><tbody><tr><td><code>{{ shop.name }}</code></td><td>Your shop's name</td></tr><tr><td><code>{{ shop.admin_email }}</code></td><td>Your shop's email address</td></tr><tr><td><code>{{ shop.admin_name }}</code></td><td>The shop owner's name</td></tr></tbody></table>

## Customer details

<table><thead><tr><th width="290">Variable</th><th>Contains</th></tr></thead><tbody><tr><td><code>{{ customer_first_name }}</code></td><td>First name</td></tr><tr><td><code>{{ customer_last_name }}</code></td><td>Last name</td></tr><tr><td><code>{{ customer_name }}</code></td><td>Full name</td></tr><tr><td><code>{{ customer_email }}</code></td><td>Email address</td></tr><tr><td><code>{{ customer_phone }}</code></td><td>Phone number</td></tr></tbody></table>

## Line item details

Line items need a loop. Everything inside it uses `line`.

```liquid
{% for line in line_items %}
  {{ line.title }} × {{ line.quantity }}
  {% for p in line.properties %}
    {{ p.first }}: {{ p.last }}
  {% endfor %}
{% endfor %}
```

<table><thead><tr><th width="290">Variable</th><th>Contains</th></tr></thead><tbody><tr><td><code>{{ line.name }}</code></td><td>The item's name</td></tr><tr><td><code>{{ line.title }}</code></td><td>The product title</td></tr><tr><td><code>{{ line.variant_title }}</code></td><td>The variant title</td></tr><tr><td><code>{{ line.quantity }}</code></td><td>How many</td></tr><tr><td><code>{{ line.original_line_price | money }}</code></td><td>Price before discounts</td></tr><tr><td><code>{{ line.final_line_price | money }}</code></td><td>Price after discounts</td></tr><tr><td><code>{{ line.total_discount | money }}</code></td><td>Discount applied</td></tr><tr><td><code>{{ line.grams }}</code></td><td>Weight</td></tr><tr><td><code>{{ line.sku }}</code></td><td>SKU</td></tr><tr><td><code>{{ line.vendor }}</code></td><td>Vendor</td></tr><tr><td><code>{{ line.image | img_url }}</code></td><td>The item's image</td></tr></tbody></table>

## The properties loop

`line.properties` is where the options are. Each entry has a name and a value.

<table><thead><tr><th width="230">Inside the loop</th><th>Contains</th></tr></thead><tbody><tr><td><code>{{ p.first }}</code></td><td>The option's <strong>Name</strong> — which is why <a href="../option-types/shared-settings/labels-and-visibility.md">Name</a> matters</td></tr><tr><td><code>{{ p.last }}</code></td><td>What the customer entered or chose</td></tr></tbody></table>

{% hint style="warning" %}
**Skip properties whose name begins with an underscore.** Those are the app's internal properties — they link add-ons to their parent item and carry pricing data, and they are not for your team to read.
{% endhint %}

The pattern that handles both that and uploaded files:

```liquid
{% for p in line.properties %}
  {% assign first_char = p.first | truncate: 1, '' %}
  {% unless p.last == blank or first_char == '_' %}
    {{ p.first }}:
    {%- if p.last contains '/uploads/' -%}
      <a href="{{ p.last }}">{{ p.last | split: '/' | last }}</a>
    {%- else -%}
      {{ p.last }}
    {%- endif -%}
  {% endunless %}
{% endfor %}
```

Two things it does: it skips internal properties and empty values, and it renders an uploaded file as a link with a readable name rather than a long address.

See [Line item properties](../storefront/show-options-on-orders.md).

## A complete order note template

```liquid
{% for line in line_items %}
{{ line.title }} × {{ line.quantity }}
{% for p in line.properties %}{% assign fc = p.first | truncate: 1, '' %}{% unless p.last == blank or fc == '_' %}
- {{ p.first }}: {{ p.last }}
{% endunless %}{% endfor %}
{% endfor %}
```

Compact on purpose: order notes are displayed and printed in small boxes.

## Notes

* The variable list in the app is the authoritative one, and it is one click away in both editors.
* Money values need the `money` filter to be formatted — without it you get a raw number.
* Both templates have **Revert to default** if you break them.
* Order notes are often printed as plain text, so keep HTML formatting minimal there. Emails can carry more.

## Troubleshooting

<details>
<summary>A variable outputs nothing</summary>

Check the spelling against the list above, and that it is in the right scope — `line` only exists inside the line items loop.
</details>

<details>
<summary>Prices show as raw numbers</summary>

Add the `money` filter: `{{ total_price | money }}`.
</details>

<details>
<summary>Technical entries appear in my output</summary>

You are printing every property. Add the underscore check shown above.
</details>

<details>
<summary>Uploaded files show as long addresses</summary>

Use the file handling shown above to render them as links.
</details>

<details>
<summary>Option names read badly</summary>

They are the options' **Name** values. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).
</details>
