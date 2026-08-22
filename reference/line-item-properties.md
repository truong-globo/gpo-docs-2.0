---
description: >-
  Every property the app writes on a cart line, what it means, and which ones to
  print on your paperwork.
icon: tags
---

# Line item properties

Shopify lets an app attach extra information to a cart line as **line item properties** — a list of name and value pairs. That is how the customer's answers reach the order.

You mostly do not need to think about this. It matters in two situations: printing options on your own paperwork, and diagnosing something with a developer.

## The one rule

**Properties whose name starts with an underscore are internal. Do not print them.**

Shopify treats a leading underscore as "hidden", so its own admin and checkout screens keep them out of the way. Custom templates do not always follow suit, which is why odd technical lines sometimes appear on packing slips.

The snippet in [Show options on orders](../storefront/show-options-on-orders.md) skips them.

## The two kinds

<table><thead><tr><th width="290">Kind</th><th>Name</th><th>Example</th></tr></thead><tbody><tr><td><strong>Your options</strong></td><td>The option's <strong>Name</strong></td><td><code>Engraving text</code> → <code>Forever yours</code></td></tr><tr><td><strong>The app's bookkeeping</strong></td><td>Starts with <code>_</code></td><td><code>_gpo_product_group</code> → <code>1703752870644</code></td></tr></tbody></table>

The first kind is what you want on your paperwork, and the reason it is worth setting the **Name** on every option rather than leaving `text` or `checkbox`. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).

## Properties on the main product line

<table><thead><tr><th width="290">Property</th><th>Meaning</th></tr></thead><tbody><tr><td>Your option names</td><td>One per answered option, using its <strong>Name</strong> and the customer's answer</td></tr><tr><td><code>_has_gpo</code></td><td>The option set that produced this line. Its presence is how the app recognises its own lines — in the cart, in <strong>Edit Options</strong>, and in your analytics</td></tr><tr><td><code>_gpo_product_group</code></td><td>An identifier linking this line to its add-on lines. This is what makes an add-on belong to a particular main item, rather than just being in the same cart</td></tr><tr><td><code>_gpo_personalize</code></td><td>Present when the line was personalised. It is what makes the design preview available from the cart and the order</td></tr><tr><td><code>_gpo_options</code></td><td>A structured copy of the answers, written when there are <strong>Add price</strong> add-ons or when add-on lines are being merged</td></tr><tr><td><code>_gpo_addon_products</code></td><td>A structured copy of the add-on products, written in the same circumstances</td></tr><tr><td><code>_gpo_addon_price</code></td><td>Added at checkout, recording the <strong>Add price</strong> amount that was applied. It is where the add-on revenue figure in <a href="../option-sets/analytics.md">Analytics</a> comes from</td></tr></tbody></table>

## Properties on add-on product lines

A product-backed add-on is its own cart line — a real product being bought. These properties tie it back to the main item and record how it was configured.

<table><thead><tr><th width="290">Property</th><th>Meaning</th></tr></thead><tbody><tr><td><code>_gpo_parent_product_group</code></td><td>Points at the main line's <code>_gpo_product_group</code>. This pairing is what lets the app treat them as one purchase — and what <a href="../add-on-pricing/merge-as-bundle.md">Merge main product and add-ons</a> relies on</td></tr><tr><td><code>_gpo_field_name</code></td><td>Which option produced this add-on, by its <strong>Name</strong> — so you can tell which question a charge came from</td></tr></tbody></table>

## The advanced-mode markers

One of these appears on an add-on line when the option uses a mode other than **Default**. It records the base quantity the mode was configured with, so the quantity survives a cart edit.

<table><thead><tr><th width="290">Property</th><th>Set by</th></tr></thead><tbody><tr><td><code>_gpo_one_time_charge</code></td><td><strong>One time charge</strong></td></tr><tr><td><code>_gpo_quantity_fixed</code></td><td><strong>Fixed quantity</strong>, and <strong>Fixed quantity (by customer)</strong></td></tr><tr><td><code>_gpo_quantity_dynamic</code></td><td><strong>Dynamic quantity</strong>, and <strong>Dynamic quantity (by customer)</strong></td></tr><tr><td><code>_gpo_quantity_mix</code></td><td><strong>Mixed quantity</strong></td></tr><tr><td><code>_gpo_per_character</code></td><td><strong>Per character</strong></td></tr></tbody></table>

None appears on **Default**, which needs no marker — it simply follows the main product's quantity. See [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md).

{% hint style="info" %}
These markers are why changing the main product's quantity in the cart keeps the add-on quantities correct. A cart app that strips properties when it rewrites lines can break that — see [Theme and third-party notes](../integrations/theme-and-third-party-notes.md).
{% endhint %}

## What a real cart looks like

A customer buys one custom bike with a `Classic Racer` seat and leather upholstery. Three cart lines:

**Line 1 — the bike**

| Property | Value |
| -------- | ----- |
| `Handlebars` | `Straight` |
| `Frame Finish` | `Black` |
| `Seat Type` | `Custom - Classic Racer` |
| `Seat Finish` | `Leather Upholstered` |
| `_has_gpo` | the option set |
| `_gpo_product_group` | a group identifier |

**Line 2 — the seat upgrade**

| Property | Value |
| -------- | ----- |
| `_gpo_parent_product_group` | the same group identifier |
| `_gpo_field_name` | `Seat Type` |

**Line 3 — the upholstery**

| Property | Value |
| -------- | ----- |
| `_gpo_parent_product_group` | the same group identifier |
| `_gpo_field_name` | `Seat Finish` |

Only line 1 has anything worth printing. Lines 2 and 3 carry the charges, and their own product titles already say what they are.

That is exactly what [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md) tidies up for the customer's benefit.

## Printing them

Options appear automatically in:

* The cart page and cart drawer
* Shopify admin's order page
* Shopify's own order confirmation and packing slip defaults

They may **not** appear in a custom packing slip, an invoice app, or a fulfilment export, because those print what their template tells them to.

Two ways to fix that:

<table><thead><tr><th width="290">Approach</th><th>When</th></tr></thead><tbody><tr><td>Add the Liquid snippet to the template</td><td>You can edit it, and want the options laid out properly. See <a href="../storefront/show-options-on-orders.md">Show options on orders</a></td></tr><tr><td>Write the options into the order note</td><td>You cannot edit the template. Most of them already print the note. See <a href="../automations/update-order-notes.md">Update order notes</a></td></tr></tbody></table>

## Notes

* Only answered options become properties. An empty optional field writes nothing.
* Hidden options write nothing, which is also why they are not charged.
* A **Paragraph** or **Heading** collects no answer, so it writes nothing.
* The **Name** is captured when the item is added to the cart. Renaming an option later does not change existing orders.
* Uploaded files appear as a link to the file.

## Troubleshooting

<details>
<summary>Odd technical lines on my paperwork</summary>

The template is printing every property. Skip names beginning with `_` — the snippet in [Show options on orders](../storefront/show-options-on-orders.md) does.
</details>

<details>
<summary>Order lines read "text" or "checkbox"</summary>

Those are the options' **Name** values at their defaults. Set them properly. It applies to future orders only.
</details>

<details>
<summary>No properties at all on a line</summary>

The item was not added through the widget — usually a quickview or a sticky add-to-cart bar that bypassed it, or an accelerated checkout button. See [Cart and checkout problems](../help/troubleshooting-cart-checkout.md).
</details>

<details>
<summary>An add-on line has lost its link to the main item</summary>

Its `_gpo_parent_product_group` is missing, which means something rewrote the line. Usually another cart app.
</details>
