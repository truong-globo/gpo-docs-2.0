---
description: Track how many add-ons you have left, and control what customers see when one runs out.
icon: warehouse
---

# Stock and inventory

An add-on backed by a Shopify product has its own inventory. When the add-on runs out, the storefront can hide or mark the option automatically, instead of the shortage being discovered when you pack the order.

## What you need first

Inventory exists only where a product exists, so the pricing mode you selected determines whether inventory is available:

<table><thead><tr><th width="290">Mode</th><th>Stock?</th></tr></thead><tbody><tr><td><a href="use-an-existing-product.md">Use existing product</a></td><td><strong>Yes</strong> — the linked variant's inventory</td></tr><tr><td><a href="auto-generate-a-product.md">Automatically generate product</a></td><td><strong>Yes</strong> — but tracking must be turned on first</td></tr><tr><td><a href="add-price-directly.md">Add price</a></td><td><strong>No.</strong> There is no product, so nothing to count</td></tr></tbody></table>

If you need inventory behavior and your values use **Add price**, change them to a product-backed mode.

## Setting it up

{% stepper %}
{% step %}
### Open the add-on product in Shopify admin

For a generated product, use the **Product** link in the option values table. For a linked product, open it from your catalog.
{% endstep %}

{% step %}
### Turn on inventory tracking

On the variant, enable inventory tracking and enter your quantity.

Generated products are created with tracking disabled, so this step is required for the rest of the setup to work.
{% endstep %}

{% step %}
### Set it to stop selling when out of stock

Change the variant's inventory policy so Shopify stops selling at zero.

{% hint style="warning" %}
Generated products are created with the opposite policy, so they continue selling when out of stock. This is the safe default, but it means nothing changes on your storefront when the quantity reaches zero until you change this setting.
{% endhint %}
{% endstep %}

{% step %}
### Set the option's Out of stock options

In the app, on the option's **Advanced Settings**, select what customers see: **Show**, **Hide**, **Blur**, or **Strike-through**. See [Out of stock options](../option-types/shared-settings/out-of-stock-options.md).
{% endstep %}

{% step %}
### Test it

Set the quantity to zero in Shopify, reload a product page, and check that the value is displayed as configured. Then restore the quantity.
{% endstep %}
{% endstepper %}

## What customers see when something runs out

<table><thead><tr><th width="200">Setting</th><th>Result</th></tr></thead><tbody><tr><td><strong>Show</strong></td><td>No change. The value stays selectable — which means they can order what you cannot supply</td></tr><tr><td><strong>Hide</strong></td><td>The value disappears from the list</td></tr><tr><td><strong>Blur</strong></td><td>Faded and not selectable. Best for color and image swatches</td></tr><tr><td><strong>Strike-through</strong></td><td>Crossed out and not selectable. Best for text choices</td></tr></tbody></table>

## How the counting works

Each option value links to one **variant**. Selling the add-on reduces that variant's inventory, in the same way as a direct sale of the product.

This has three consequences:

<table><thead><tr><th width="290">Situation</th><th>What happens</th></tr></thead><tbody><tr><td>An option value points at a variant of a product you also sell directly</td><td>Both routes share one inventory figure. Usually what you want</td></tr><tr><td>Two option sets link to the same product</td><td>They share its stock. Duplicating an option set does not duplicate its add-on products</td></tr><tr><td>A generated product has one variant per priced option value</td><td>Each value has its own independent quantity</td></tr></tbody></table>

## Keeping the counts accurate

<table><thead><tr><th width="290">Habit</th><th>Why</th></tr></thead><tbody><tr><td>Find your generated products by the <code>globo-product-options</code> tag</td><td>It is the only reliable way to see them all at once</td></tr><tr><td>Set a low-stock alert where your tools allow it</td><td>Add-ons run out quietly — nobody notices ribbon until it is gone</td></tr><tr><td>Use <strong>Blur</strong> rather than <strong>Hide</strong> for colors</td><td>Customers can see the color exists and may come back for it</td></tr><tr><td>Put "back in stock soon" in the value's own help text</td><td>Turns a dead end into a reason to return. See <a href="../option-sets/option-values.md">Working with option values</a></td></tr><tr><td>Review after a busy period</td><td>Add-on stock is the easiest thing to forget to restock</td></tr></tbody></table>

## Weight, SKU, and tax

Add-ons are real products, so they also have the other properties of a product. Set the following:

<table><thead><tr><th width="230">Property</th><th>Why it matters</th></tr></thead><tbody><tr><td>Weight</td><td>Shipping rates calculated by weight will be wrong if your add-ons weigh nothing</td></tr><tr><td>SKU</td><td>Your fulfilment and stock systems need something to match on</td></tr><tr><td>Tax setting</td><td>Some add-ons are taxed differently from the product they attach to</td></tr><tr><td>Cost per item</td><td>Lets you see the real margin on personalized orders</td></tr></tbody></table>

All of these are set on the product in Shopify admin, not in the app.

## Notes

* Inventory is checked against live values when the product page loads.
* A value linked to a sold-out **variant** is out of stock, even when other variants of that product are in stock.
* Deleting an option set does not delete its add-on products or change their inventory. See [Duplicate and delete](../option-sets/duplicate-and-delete.md).
* **Out of stock options** may not be available on all plans. See [Compare plans](../plans/compare-plans.md).
* If an add-on product's details are out of date in the app, use **Sync Add-on data** in the builder's more-actions menu.
