---
description: >-
  The simplest way to charge — add money to the order with no product behind it,
  and the two things it cannot do.
icon: dollar-sign
---

# Add price directly

The **Add price** mode does exactly what it says: it increases what the customer pays, with no Shopify product involved.

It is the right choice for services — engraving labour, express production, a design fee — where there is nothing to run out of and nothing to ship separately.

## Steps

{% stepper %}
{% step %}
### Open the price field

On an input type, that is **Price** under **Add-on Settings** on **Basic Settings**. On a selection type, it is the **Price** cell on the option value's row. See [Where you can set add-ons](where-you-can-set-add-ons.md).
{% endstep %}

{% step %}
### Choose the Add price tab

The dialog opens with three tabs. **Add price** is the third.

A note confirms what it does: it increases the price of the main product without creating an add-on product.
{% endstep %}

{% step %}
### Enter the amount

Type the amount in your store's currency. Negative amounts are rejected.
{% endstep %}

{% step %}
### Select Select

The dialog closes and the price is attached.
{% endstep %}

{% step %}
### Set how it scales

On **Advanced Settings**, the **Advanced settings** dropdown decides whether the charge follows the product quantity, applies once, or is driven by something the customer enters. See [Advanced add-on modes](advanced-add-on-modes.md).
{% endstep %}

{% step %}
### Save and test on your storefront

Add the product to a cart and check the total. The charge is applied at checkout — see [How pricing is applied](how-pricing-is-applied.md).
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: addon-add-price-tab | App admin → builder → dialog Add-on Configuration | Tab "Add price" đang chọn, có banner giải thích và ô Price | Khoanh tab Add price và ô giá -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Add price tab of the add-on dialog with a price entered"><figcaption><p>One field, no product — the simplest of the three modes.</p></figcaption></figure>

## What the customer sees

The add-on amount is shown beside the option, in the format set by your store-wide settings — `(+ $5.00)` by default. The product price shown on the page can also update to include it, depending on your settings.

There is **no separate cart line**. The charge is folded into the main item's price, so the cart shows one line at the higher amount, with the option details listed underneath.

For many merchants that is the appeal: the cart stays simple.

See [Add-on price display settings](price-display-settings.md).

## What it cannot do

{% hint style="warning" %}
**No Shopify POS support.** Charges added this way do not work in the Shopify POS app. If an option set is published to the POS channel, use one of the product-backed modes instead. See [POS limitations](../pos/limitations.md).

**No stock, and therefore no out-of-stock handling.** There is no product, so nothing to count. The [Out of stock options](../option-types/shared-settings/out-of-stock-options.md) setting has nothing to act on.
{% endhint %}

It also has no SKU, no weight, and no separate line in your Shopify product reporting. If any of those matter, use [Automatically generate a product](auto-generate-a-product.md) instead — it takes the same amount of effort to set up.

## When Add price is the right answer

<table><thead><tr><th width="330">Add-on</th><th>Why Add price fits</th></tr></thead><tbody><tr><td>Engraving labour</td><td>Nothing physical is consumed</td></tr><tr><td>Express production</td><td>A scheduling promise, not an item</td></tr><tr><td>Artwork setup or proofing fee</td><td>A service</td></tr><tr><td>A custom-colour surcharge</td><td>You are charging for effort, not for a product</td></tr><tr><td>A small handling fee</td><td>No stock, no shipping weight</td></tr></tbody></table>

## When to use something else

<table><thead><tr><th width="330">Add-on</th><th>Use instead</th></tr></thead><tbody><tr><td>Gift wrap, boxes, ribbon — anything you can run out of</td><td><a href="auto-generate-a-product.md">Automatically generate a product</a></td></tr><tr><td>Something you already sell</td><td><a href="use-an-existing-product.md">Use an existing product</a></td></tr><tr><td>Anything you also sell in person</td><td>Either product-backed mode</td></tr><tr><td>Anything that changes the shipping weight</td><td>Either product-backed mode</td></tr><tr><td>Anything you want to see in Shopify product reports</td><td>Either product-backed mode</td></tr></tbody></table>

## Examples

**A flat engraving fee**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Option</td><td><code>Engraving text</code>, a Text option</td></tr><tr><td>Price</td><td><strong>Add price</strong> $5.00</td></tr><tr><td>Advanced settings</td><td><strong>Default</strong> — one charge per bracelet</td></tr></tbody></table>

**Engraving by the character**

Same option, **Price** $0.50, **Advanced settings** set to **Per character**, with a **Max character** of `20` so the maximum charge is $10.00.

**Express production, once per order**

A Switch labelled `Express production`, **Add price** $10.00, **Advanced settings** **One time charge** — so somebody buying three items pays it once.

**A tiered service charge**

A Radio button with `Standard` free, `Priority` at $8.00, `Same day` at $20.00, all three using **Add price**.

## Notes

* Negative amounts are rejected.
* A price attached to a **default value** is charged as soon as the page loads. See [Required field and default value](../option-types/shared-settings/required-and-default-value.md#default-value).
* A hidden option is not charged — hiding an option with a conditional rule removes its price.
* On a multi-select option, every selected value with a price is charged. Cap it with [Max selections](../option-types/shared-settings/limits.md#min-and-max-selections).

## Troubleshooting

<details>
<summary>The price does not appear on the product page</summary>

Check **Show add-on for inputs** and **Show add-on for options** in **Settings > Settings > Add-on price**. They control whether the preview is displayed at all. See [Add-on price display settings](price-display-settings.md).
</details>

<details>
<summary>The product price on the page does not change</summary>

That is **Add add-on price to the product price** in the same settings. With it off, the add-on is shown separately instead of being folded into the displayed price.
</details>

<details>
<summary>Nothing is charged at checkout</summary>

Check the option is not hidden by a conditional rule, and that the option set is saved and active. If it still does not charge, see [How pricing is applied](how-pricing-is-applied.md).
</details>

<details>
<summary>It does not work in POS</summary>

Expected — **Add price** is not supported there. Switch the affected values to a product-backed mode.
</details>

<details>
<summary>Out of stock options does nothing</summary>

There is no product, so no stock. Use a product-backed mode if you need stock behaviour.
</details>
