---
description: What the customer and your team see after a personalised item is added to the cart.
icon: cart-shopping
---

# Designs in cart and orders

A personalised design is only useful if it reaches the person who has to make it. This page covers what happens after **Add to cart**.

## What the customer sees in the cart

The item appears with its option details listed underneath — the text they typed, the design they chose, the file they uploaded — exactly as any other option would.

Personalised items additionally offer a way to look at the design they created. The wording is part of the widget text and reads **Preview Your Design** by default.

## Preview mode

How that design is presented is a store-wide setting.

**Settings** > **Settings** > **General** > **Cart page** > **Personalize preview mode**

<table><thead><tr><th width="230">Mode</th><th width="290">Behaviour</th><th>Use when</th></tr></thead><tbody><tr><td><strong>View in modal</strong></td><td>The design opens in a dialog on the cart page. The default</td><td>Almost always. The shopper checks it without leaving the cart</td></tr><tr><td><strong>Download file</strong></td><td>The design is downloaded as a file</td><td>Customers need to keep or forward a copy — approving artwork with a colleague, for instance</td></tr></tbody></table>

**View in modal** is the better default: a shopper who has to download a file to check their own order is a shopper who might not bother.

This setting is plan-gated. See [Compare plans](../plans/compare-plans.md).

<!-- SCREENSHOT: pp-cart-preview | Storefront → trang cart | Line item có option details và link "Preview Your Design", modal preview đã mở | Khoanh link và modal -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A cart line with its option details and the design preview open in a modal"><figcaption><p>The customer can check their design from the cart before paying.</p></figcaption></figure>

## Letting customers change their mind

**Show "Edit Options" button in cart** — also in **Settings** > **Settings** > **General** > **Cart page** — lets shoppers reopen the option form from the cart and change their choices, including their personalisation.

For personalised products this is worth having. Somebody who spots a typo in their engraving after adding to cart would otherwise have to remove the item and start again — and some of them will simply leave.

It is plan-gated. See [Cart page](../storefront/cart-page.md).

## What you see on the order

The order in Shopify admin shows the item with its option details: the text, the chosen values, and links to any uploaded files.

That is what your production team works from. Two things make the difference between an order they can act on and one they have to ask about:

<table><thead><tr><th width="290">Do this</th><th>Because</th></tr></thead><tbody><tr><td>Give every option a readable <strong>Name</strong></td><td>The Name is what appears on the order. <code>Engraving text: Forever yours</code> is actionable; <code>text: Forever yours</code> is not. See <a href="../option-types/shared-settings/labels-and-visibility.md">Label and Name</a></td></tr><tr><td>Include everything production needs as an option</td><td>If the font matters, ask for it as a <a href="../option-types/selection-types/font-picker.md">Font picker</a> option so it is recorded, rather than relying on a default nobody wrote down</td></tr></tbody></table>

## Getting the details out of Shopify admin

Three routes, depending on how your team works:

<table><thead><tr><th width="290">Route</th><th>Good for</th></tr></thead><tbody><tr><td>Reading the order in Shopify admin</td><td>Low volume. Nothing to set up</td></tr><tr><td>Order confirmation emails, invoices, and packing slips</td><td>Anybody who works from printed paperwork. Option details appear automatically. See <a href="../storefront/show-options-on-orders.md">Show options on orders</a></td></tr><tr><td>An <a href="../automations/README.md">automation</a></td><td>Higher volume — email yourself the options as each order arrives, or write them into the order notes so they appear everywhere the note does</td></tr></tbody></table>

For a personalisation business, the automations are worth setting up early. See [Email notification](../automations/email-notification.md) and [Update order notes](../automations/update-order-notes.md).

## Uploaded files

Files a customer uploaded are attached to the order, so your team can download the originals from the order in Shopify admin.

Two practical points:

* Ask for the resolution you need in the option's [help text](../option-types/shared-settings/placeholder-and-help-text.md#help-text). The preview will happily draw a small file that is useless for printing.
* Turning on the upload option's image editor means customers crop their own photos, so what you receive is closer to what you need. See [File upload](../option-types/input-types/file-upload.md).

## Set expectations about the preview

The preview is a representation, not a print proof. Screens are not colour-calibrated, and final placement can vary by a millimetre or two.

One line of help text prevents almost all disputes about this: *"The preview is a guide. Colours may vary slightly from your screen."*

If you sell high-value personalised items, consider adding your own proofing step — a [Switch](../option-types/input-types/switch.md) offering an emailed proof before production, priced or free.

## Notes

* Option values, including personalisation text, reach the order as line item properties. See [Line item properties](../storefront/show-options-on-orders.md).
* Add-on products attached to personalisation appear as their own cart lines unless you merge them. See [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).
* Orders already placed keep the option names they were placed with. Renaming an option later does not rewrite history.
* The **Preview Your Design** and **Your Design** wording is editable per language in **Settings > Translations**.

## Troubleshooting

<details>
<summary>There is no design preview in the cart</summary>

Check the item genuinely has a personalised option, and that **Personalize preview mode** is available on your plan.
</details>

<details>
<summary>The design downloads instead of opening</summary>

**Personalize preview mode** is set to **Download file**. Switch it to **View in modal**.
</details>

<details>
<summary>Customers cannot fix a typo without starting again</summary>

Turn on **Show "Edit Options" button in cart**.
</details>

<details>
<summary>My order line says "text" instead of something useful</summary>

The option's **Name** is still at its default. Set it to something readable — for future orders.
</details>

<details>
<summary>I cannot find the customer's uploaded file</summary>

It is attached to the order in Shopify admin, alongside the option details for that line item.
</details>

<details>
<summary>The customer says the product does not match the preview</summary>

Set expectations in help text, and consider offering a proofing step for high-value items.
</details>
