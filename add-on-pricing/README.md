---
description: >-
  Charge extra for the choices customers make - including three different ways
  to do this, and choosing the right one depends on how you want the charge to
  work.
icon: tags
---

# Overview

Add-on pricing turns an option from simple information into an additional charge. For example, a customer selects gift wrapping and $3.00 is added to the price, enters an engraving message and $5.00 is added, or chooses a premium fabric with an additional cost.

The app gives you three ways to apply these charges. Choosing the right method from the start can save you a lot of rework. The key difference is whether a real Shopify product is used behind the add-on. This affects inventory tracking, Shopify POS compatibility, and how the add-on appears in the order.

## The three ways

Every price field in the app opens the same dialog, which contains these three tabs.

<table><thead><tr><th width="230">Mode</th><th width="230">What it does</th><th>Behind the scenes</th></tr></thead><tbody><tr><td><strong>Use existing product</strong></td><td>Links to a product and variant you already sell. The add-on costs the same as that variant.</td><td>Your own product</td></tr><tr><td><strong>Automatically generate product</strong></td><td>You enter a price, and the app creates a product for the add-on.</td><td>A product the app creates and manages</td></tr><tr><td><strong>Add price</strong></td><td>Adds an extra charge to the order. Nothing else is created or linked.</td><td>No product at all</td></tr></tbody></table>

## Compare them properly

Use this table to choose the right pricing method before you start building.

<table><thead><tr><th width="290"></th><th width="170">Use existing product</th><th width="170">Automatically generate</th><th>Add price</th></tr></thead><tbody><tr><td>Where the price comes from</td><td>The linked variant</td><td>You type it</td><td>You type it</td></tr><tr><td>Creates a product in your catalogue</td><td>No — uses an existing one</td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Stock can be tracked</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Works with <strong>Out of stock options</strong></td><td><strong>Yes</strong></td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Has its own SKU, weight, and tax setting</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Appears as its own cart line</td><td>Yes</td><td>Yes</td><td>No — folded into the main item's price</td></tr><tr><td>Can be merged visually with the main item</td><td>Yes</td><td>Yes</td><td>Not applicable</td></tr><tr><td>Supported in Shopify POS</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td><td><strong>No</strong></td></tr><tr><td>Effort to set up</td><td>Medium — you need the product</td><td>Low</td><td>Lowest</td></tr><tr><td>Effort to maintain</td><td>Low</td><td>Low</td><td>None</td></tr></tbody></table>

## Which one should I use?

<table><thead><tr><th width="330">Your add-on is…</th><th>Use</th></tr></thead><tbody><tr><td>A physical thing you already sell — a gift box, a spare part</td><td><strong>Use existing product</strong></td></tr><tr><td>A physical thing you do not sell separately, but need to count — ribbons, boxes, engraving plates</td><td><strong>Automatically generate product</strong></td></tr><tr><td>A service with no inventory to track or run out of—such as engraving, expedited production, or a design fee.</td><td><strong>Add price</strong></td></tr><tr><td>Something you also sell in person through Shopify POS</td><td>Either product-backed mode. <strong>Not Add price</strong></td></tr><tr><td>Something you want reported separately in your Shopify sales reports</td><td>Either product-backed mode</td></tr><tr><td>Something with different weights that affect shipping</td><td>Either product-backed mode</td></tr></tbody></table>

{% hint style="info" %}
When in doubt, choose **Automatically generate product**. It costs nothing extra, gives you stock tracking and POS support if you need them later, and ensures the add-on is included properly in your Shopify reports. Choose **Add price** only when there is genuinely nothing to track or count.
{% endhint %}

## Pages in this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Where you can set add-ons</strong></td><td>Option level against value level, and which types support which.</td><td><a href="where-you-can-set-add-ons.md">where-you-can-set-add-ons.md</a></td></tr><tr><td><strong>Add price directly</strong></td><td>The simplest mode, and its one significant limitation.</td><td><a href="add-price-directly.md">add-price-directly.md</a></td></tr><tr><td><strong>Use an existing product</strong></td><td>Linking a product and variant you already sell.</td><td><a href="use-an-existing-product.md">use-an-existing-product.md</a></td></tr><tr><td><strong>Automatically generate a product</strong></td><td>What the app creates, how it names the products, and how to keep them out of your storefront.</td><td><a href="auto-generate-a-product.md">auto-generate-a-product.md</a></td></tr><tr><td><strong>Advanced add-on modes</strong></td><td>All eight quantity modes, each with a worked calculation.</td><td><a href="advanced-add-on-modes.md">advanced-add-on-modes.md</a></td></tr><tr><td><strong>Dimension add-on formula</strong></td><td>Calculate the price from measurements the customer enters.</td><td><a href="dimension-formula.md">dimension-formula.md</a></td></tr><tr><td><strong>Stock and inventory</strong></td><td>Turning on tracking, and what happens when something runs out.</td><td><a href="stock-and-inventory.md">stock-and-inventory.md</a></td></tr><tr><td><strong>Merge main product and add-ons</strong></td><td>Showing add-ons as part of the item rather than separate lines.</td><td><a href="merge-as-bundle.md">merge-as-bundle.md</a></td></tr><tr><td><strong>Add-on price display settings</strong></td><td>How prices are shown on the product page.</td><td><a href="price-display-settings.md">price-display-settings.md</a></td></tr><tr><td><strong>How pricing is applied</strong></td><td>Why the product page shows a preview while checkout shows the final price.</td><td><a href="how-pricing-is-applied.md">how-pricing-is-applied.md</a></td></tr><tr><td><strong>Limitations</strong></td><td>What add-on pricing cannot do, so you know the limitations before you build.</td><td><a href="limitations.md">limitations.md</a></td></tr></tbody></table>

## The one thing to understand

The price shown on the product page is a **preview**, calculated in the shopper’s browser. The actual charge is applied by Shopify at checkout.

This is not a workaround—it’s how Shopify works, and it’s what keeps the pricing secure from tampering. It also explains several things that might otherwise seem confusing: why add-on products appear as separate cart lines, why the displayed total can be configured independently, and why shoppers cannot change the price in their browser.

See [How pricing is applied](how-pricing-is-applied.md).
