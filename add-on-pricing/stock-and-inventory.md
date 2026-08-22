---
description: Track how many add-ons you have left, and control what shoppers see when one runs out.
icon: warehouse
---

# Stock and inventory

An add-on backed by a Shopify product can be counted. That turns "we have run out of gift boxes" from a problem you discover at packing time into something the storefront handles by itself.

## What you need first

Stock only exists where a product exists. So the mode you chose matters:

<table><thead><tr><th width="290">Mode</th><th>Stock?</th></tr></thead><tbody><tr><td><a href="use-an-existing-product.md">Use existing product</a></td><td><strong>Yes</strong> — the linked variant's inventory</td></tr><tr><td><a href="auto-generate-a-product.md">Automatically generate product</a></td><td><strong>Yes</strong> — but tracking must be turned on first</td></tr><tr><td><a href="add-price-directly.md">Add price</a></td><td><strong>No.</strong> There is no product, so nothing to count</td></tr></tbody></table>

If you need stock behaviour and your values use **Add price**, change them to a product-backed mode.

## Setting it up

{% stepper %}
{% step %}
### Open the add-on product in Shopify admin

For a generated product, use the **Product** link in the option values table. For a linked product, open it from your catalogue.
{% endstep %}

{% step %}
### Turn on inventory tracking

On the variant, enable tracking and enter your quantity.

Generated products arrive with tracking off, so this step is what makes everything below work.
{% endstep %}

{% step %}
### Set it to stop selling when out of stock

Change the variant's inventory policy so Shopify stops selling at zero.

{% hint style="warning" %}
Generated products are created with the opposite policy — they keep selling when out of stock. That is the safe default, but it means nothing changes on your storefront when the quantity hits zero until you change this.
{% endhint %}
{% endstep %}

{% step %}
### Set the option's Out of stock options

Back in the app, on the option's **Advanced Settings**, choose what shoppers see: **Show**, **Hide**, **Blur**, or **Strike-through**. See [Out of stock options](../option-types/shared-settings/out-of-stock-options.md).
{% endstep %}

{% step %}
### Test it

Set the quantity to zero in Shopify, reload a product page, and confirm the value behaves as configured. Then put the quantity back.
{% endstep %}
{% endstepper %}

## What shoppers see when something runs out

<table><thead><tr><th width="200">Setting</th><th>Result</th></tr></thead><tbody><tr><td><strong>Show</strong></td><td>No change. The value stays selectable — which means they can order what you cannot supply</td></tr><tr><td><strong>Hide</strong></td><td>The value disappears from the list</td></tr><tr><td><strong>Blur</strong></td><td>Faded and not selectable. Best for colour and image swatches</td></tr><tr><td><strong>Strike-through</strong></td><td>Crossed out and not selectable. Best for text choices</td></tr></tbody></table>

## How the counting works

Each option value points at one **variant**. Selling that add-on draws down that variant's inventory, exactly as a direct sale of the product would.

That has three consequences worth knowing:

<table><thead><tr><th width="290">Situation</th><th>What happens</th></tr></thead><tbody><tr><td>An option value points at a variant of a product you also sell directly</td><td>Both routes share one inventory figure. Usually what you want</td></tr><tr><td>Two option sets link to the same product</td><td>They share its stock. Duplicating an option set does not duplicate its add-on products</td></tr><tr><td>A generated product has one variant per priced option value</td><td>Each value has its own independent quantity</td></tr></tbody></table>

## Keeping the counts honest

<table><thead><tr><th width="290">Habit</th><th>Why</th></tr></thead><tbody><tr><td>Find your generated products by the <code>globo-product-options</code> tag</td><td>It is the only reliable way to see them all at once</td></tr><tr><td>Set a low-stock alert where your tools allow it</td><td>Add-ons run out quietly — nobody notices ribbon until it is gone</td></tr><tr><td>Use <strong>Blur</strong> rather than <strong>Hide</strong> for colours</td><td>Shoppers can see the colour exists and may come back for it</td></tr><tr><td>Put "back in stock soon" in the value's own help text</td><td>Turns a dead end into a reason to return. See <a href="../concepts/option-values.md">Working with option values</a></td></tr><tr><td>Review after a busy period</td><td>Add-on stock is the easiest thing to forget to restock</td></tr></tbody></table>

## Weight, SKU, and tax

Because add-ons are real products, they also carry the rest of a product's properties — and those are worth setting:

<table><thead><tr><th width="230">Property</th><th>Why it matters</th></tr></thead><tbody><tr><td>Weight</td><td>Shipping rates calculated by weight will be wrong if your add-ons weigh nothing</td></tr><tr><td>SKU</td><td>Your fulfilment and stock systems need something to match on</td></tr><tr><td>Tax setting</td><td>Some add-ons are taxed differently from the product they attach to</td></tr><tr><td>Cost per item</td><td>Lets you see the real margin on personalised orders</td></tr></tbody></table>

All of them are set on the product in Shopify admin, not in this app.

## Notes

* Stock is checked when the product page loads, against live inventory.
* A value linked to a sold-out **variant** is out of stock even when other variants of that product have stock.
* Deleting an option set does not delete its add-on products, and does not release their stock. See [Duplicate and delete](../option-sets/duplicate-and-delete.md).
* **Out of stock options** is plan-gated. See [Compare plans](../plans/compare-plans.md).
* Use **Sync Add-on data** in the builder's more-actions menu if an add-on product's details look stale in the app.

## Troubleshooting

<details>
<summary>Out-of-stock handling does nothing</summary>

Three things, in order: the values must be product-backed rather than **Add price**; the variant must have inventory tracking on; and its policy must be set to stop selling at zero. Generated products need the last two doing by hand.
</details>

<details>
<summary>Shoppers can still buy add-ons I have run out of</summary>

The variant is still set to continue selling when out of stock. Change the policy in Shopify.
</details>

<details>
<summary>A value shows as unavailable when I have stock</summary>

Check the specific variant the value points at, not the product as a whole. Reopen the price dialog to see which variant is selected.
</details>

<details>
<summary>Two option sets are eating the same stock</summary>

They link to the same product. If you need separate counts, generate a product for one of them.
</details>

<details>
<summary>Shipping is undercharging on personalised orders</summary>

Your add-on products have no weight. Set it on each variant in Shopify.
</details>

<details>
<summary>I cannot find my add-on products</summary>

Filter your Shopify products by the tag `globo-product-options`.
</details>

## Next steps

* [Out of stock options](../option-types/shared-settings/out-of-stock-options.md) — the display setting in full.
* [Automatically generate a product](auto-generate-a-product.md)
* [Merge main product and add-ons](merge-as-bundle.md)
