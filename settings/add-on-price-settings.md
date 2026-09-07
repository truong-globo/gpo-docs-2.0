---
description: The Add-on price section, covering how extra charges are displayed and how add-on lines appear in the cart.
icon: tags
---

# Add-on price settings

**Settings** > **Settings** > **Add-on price** contains seven store-wide settings that control how add-on charges are *displayed*. The amounts charged are set on the options themselves.

The settings are documented in full under [Add-on price display settings](../add-on-pricing/price-display-settings.md). This page summarizes them.

## The settings

<table><thead><tr><th width="290">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Add-on money format</strong></td><td><strong>Without currency</strong></td><td>Whether amounts include your currency code</td></tr><tr><td><strong>Add-on label format</strong></td><td><code>(+ {{addon}})</code></td><td>The wrapper around the amount</td></tr><tr><td><strong>Show add-on for inputs</strong></td><td>On</td><td>Whether Text, Textarea, and Number options show their price</td></tr><tr><td><strong>Show add-on for options</strong></td><td>On</td><td>Whether selection types show theirs</td></tr><tr><td><strong>Show add-on message</strong></td><td>On</td><td>A summary message about selections adding to the price</td></tr><tr><td><strong>Add add-on price to the product price</strong></td><td><strong>On</strong> for new stores</td><td>Whether the displayed product price rises as the customer chooses</td></tr><tr><td><strong>Merge Main product &amp; Add-on products</strong></td><td><strong>On</strong> for new stores</td><td>Whether add-ons appear as part of the item in the cart, or as separate lines</td></tr></tbody></table>

## The two most important settings

**Add add-on price to the product price** controls whether customers see one running total or a base price plus extras. With it on, and an option carrying a priced [default value](../option-types/shared-settings/required-and-default-value.md#default-value), the product price is higher than your listed price as soon as the page loads. This is the most common reason customers ask why a product costs more than advertised.

**Merge Main product & Add-on products** controls whether the cart displays one customized item or an itemized list. Use merging for heavily configured products, and separate lines for add-ons that are substantial items on their own. See [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).

## What is not here

<table><thead><tr><th width="290">Setting</th><th>Where it is</th></tr></thead><tbody><tr><td>The price itself</td><td>On each option, or each option value. See <a href="../add-on-pricing/where-you-can-set-add-ons.md">Where you can set add-ons</a></td></tr><tr><td>How a charge scales with quantity</td><td>The option's <strong>Advanced settings</strong>. See <a href="../add-on-pricing/advanced-add-on-modes.md">Advanced add-on modes</a></td></tr><tr><td>The add-on message's wording</td><td><strong>Settings &gt; Translations</strong>, per language</td></tr><tr><td>Cart controls for add-on lines</td><td><strong>Settings &gt; General &gt; Cart page</strong>. See <a href="../storefront/cart-page.md">Cart page</a></td></tr></tbody></table>
