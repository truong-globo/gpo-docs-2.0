---
description: Write the options a customer chose into the order's notes — the easiest way to get them onto all your paperwork.
icon: note-sticky
---

# Update order notes

Writes the chosen options into the order's note field in Shopify.

This is the most useful automation for most shops, for one reason: **most packing slip, invoice, and notification templates already print the order note**. So writing options into the note puts them on all your paperwork without editing a single template.

You can have one order notes workflow.

## Settings

<table><thead><tr><th width="290">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Content (HTML)</strong></td><td>The template for what is written into the note. Accepts Liquid variables</td></tr><tr><td><strong>Keep existing order notes</strong></td><td>When on, the app adds a new line below whatever is already in the note instead of replacing it</td></tr></tbody></table>

<!-- SCREENSHOT: auto-order-notes | App admin → Automations → workflow Order notes update | Editor Content (HTML), checkbox Keep existing order notes, nút Test và Revert to default | Khoanh editor và checkbox -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The order notes workflow with its content editor and the keep existing notes option"><figcaption><p>One template, and one decision about whether to overwrite.</p></figcaption></figure>

## Keep existing order notes

{% hint style="warning" %}
Turn this **on** if anything else writes to your order notes — a checkout note field where customers leave delivery instructions, or another app.

With it off, the app replaces the note, and a customer's own message is lost. That is a real problem, because the thing most likely to be in a note is the customer asking for something.
{% endhint %}

With it on, the app appends its content on a new line, so both survive.

## The content template

**Content (HTML)** is a Liquid template. The default lists each line item and its options, which is what most shops want.

The full variable list is available from the page, and documented in [Liquid variables reference](liquid-variables-reference.md).

Keep it compact. A note is displayed in a small box in Shopify admin and printed in a small box on paperwork, so a long template is harder to read than a short one. Aim for one line per option.

**Revert to default** restores the original template if you break it, and asks you to confirm first.

## Testing

**Test** opens a list of your fifty most recent orders. Choose one and the workflow runs against it, so you can see exactly what the note will look like.

Test with an order that actually has options. An order without them produces an empty result and tells you nothing.

## Why this is worth doing

<table><thead><tr><th width="290">Without it</th><th>With it</th></tr></thead><tbody><tr><td>Option details are on the order, but not on your printed paperwork unless you edit templates</td><td>They appear anywhere the order note is printed — usually packing slips, invoices, and emails</td></tr><tr><td>Editing packing slip and email templates means Liquid</td><td>No template editing at all</td></tr><tr><td>Warehouse staff open Shopify admin to read the options</td><td>They read the packing slip</td></tr></tbody></table>

Compare with editing templates directly, which gives you more control over placement: [Show options on orders](../storefront/show-options-on-orders.md).

## Notes

* One order notes workflow per store.
* It runs shortly after the order is created, so the note appears a moment later — not instantly.
* A workflow set to **Draft** does nothing.
* Requires order data access, approved once when you first open **Automations**.
* It writes to the order note. It does not change line items, prices, or anything else about the order.

## Troubleshooting

<details>
<summary>The note is empty</summary>

The order had no app options, or the workflow is **Draft**. Use **Test** against an order you know has options.
</details>

<details>
<summary>A customer's own note disappeared</summary>

**Keep existing order notes** was off, so the app replaced it. Turn it on. Notes already overwritten cannot be recovered.
</details>

<details>
<summary>The note is very long and hard to read</summary>

Shorten the template. One line per option is enough for most paperwork.
</details>

<details>
<summary>The note does not appear on my packing slip</summary>

Most templates print the order note, but not all. Check your packing slip template includes it, or add the option details directly — see [Show options on orders](../storefront/show-options-on-orders.md).
</details>

<details>
<summary>The formatting looks wrong on printed paperwork</summary>

Notes are usually printed as plain text, so HTML formatting may be stripped. Keep the template simple: line breaks rather than tables.
</details>

<details>
<summary>I broke the template</summary>

**Revert to default**.
</details>

## Next steps

* [Update order tags](update-order-tags.md)
* [Liquid variables reference](liquid-variables-reference.md)
* [Show options on orders](../storefront/show-options-on-orders.md)
