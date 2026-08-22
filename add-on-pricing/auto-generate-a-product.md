---
description: >-
  Type a price and let the app create the add-on product for you — what it makes,
  how it names it, and how to keep it out of your storefront browsing.
icon: wand-magic-sparkles
---

# Automatically generate a product

You type a price; the app creates a Shopify product to carry it. You get everything a real product gives you — stock, SKU, weight, POS support, proper reporting — without building the product by hand.

For most physical add-ons this is the mode to use.

## Steps

{% stepper %}
{% step %}
### Open the price field

**Price** under **Add-on Settings** for an input type, or the **Price** cell on an option value's row for a selection type.
{% endstep %}

{% step %}
### Choose the Automatically generate product tab

A note confirms what will happen: enter the price and the app will generate a product as the add-on product.
{% endstep %}

{% step %}
### Check the titles

**Product title** and **Variant title** are shown but not editable — they are derived from your option:

* **Product title** comes from the option's **Label**
* **Variant title** comes from the option value's name, or from the option itself on an input type

That is why it is worth setting a sensible **Label** before generating. `Frame colour` produces a readable product; `Select` does not.
{% endstep %}

{% step %}
### Enter the price

In your store's currency. Negative amounts are rejected.
{% endstep %}

{% step %}
### Select Select, then Save the option set

The product is created after you save — not while the dialog is open.
{% endstep %}

{% step %}
### Reload the page

Once the product exists, the values table gains a **Product** column with a link that opens it in Shopify admin. If the link is not there yet, reload — creation happens in the background and takes a moment.
{% endstep %}

{% step %}
### Set up its inventory

This is the step people skip. See [Turning on stock tracking](#turning-on-stock-tracking) below.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: addon-auto-generate | App admin → builder → dialog Add-on Configuration | Tab "Automatically generate product": banner, Product title và Variant title readonly, ô Price | Khoanh ô Price và 2 field readonly -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Automatically generate product tab showing read-only titles and a price field"><figcaption><p>The titles come from your option, so name the option well before generating.</p></figcaption></figure>

## What the app creates

Knowing this makes the products much less mysterious when you find them in your catalogue.

<table><thead><tr><th width="230">Property</th><th>Value</th></tr></thead><tbody><tr><td>Title</td><td>The option's <strong>Label</strong></td></tr><tr><td>Variants</td><td>One per priced option value, named after that value. An input type gets a single variant</td></tr><tr><td>Status</td><td><strong>Active</strong></td></tr><tr><td>Sales channels</td><td>Published, so it can be purchased through the widget</td></tr><tr><td>Tags</td><td><code>globo-product-options</code>, plus an identifier for the option it belongs to</td></tr><tr><td>Inventory policy</td><td>Set to continue selling when out of stock — so by default it never blocks a sale</td></tr></tbody></table>

{% hint style="info" %}
The `globo-product-options` tag is the useful part. It is how you find every generated product at once, and how you exclude them from automated collections. Search your Shopify products for that tag to see them all.
{% endhint %}

One product is created per option, with one variant per priced value. So an [Image swatch](../option-types/selection-types/image-swatch.md) with twelve priced fabrics becomes one product with twelve variants — not twelve products. Options with a very large number of priced values are split across more than one product.

## Turning on stock tracking

Generated products are created so that they never block a sale. That is the safe default, but it means **out-of-stock behaviour does nothing until you change it**.

{% stepper %}
{% step %}
### Open the product in Shopify admin

Use the **Product** link in the values table, or search your products for the `globo-product-options` tag.
{% endstep %}

{% step %}
### Turn on inventory tracking

On the variant, enable tracking and enter your quantity.
{% endstep %}

{% step %}
### Set it to stop selling when out of stock

Change the variant's policy so Shopify does not continue selling once the quantity reaches zero.
{% endstep %}

{% step %}
### Set the option's Out of stock options

Back in the app, set [Out of stock options](../option-types/shared-settings/out-of-stock-options.md) to **Hide**, **Blur**, or **Strike-through** so shoppers can see what has run out.
{% endstep %}

{% step %}
### Test it

Set the quantity to zero and check the value behaves as you configured on the storefront.
{% endstep %}
{% endstepper %}

Full detail: [Stock and inventory](stock-and-inventory.md).

## Keeping them out of the way

Generated products are published so they can be bought, which means they can also be found by browsing — the most common complaint about this mode.

<table><thead><tr><th width="290">Problem</th><th>Fix</th></tr></thead><tbody><tr><td>They appear in automated collections</td><td>Add a condition to those collections excluding the tag <code>globo-product-options</code></td></tr><tr><td>They appear in storefront search</td><td>Exclude them in whatever controls your search — a search app's settings, or your theme's search template</td></tr><tr><td>They clutter your product list in admin</td><td>Filter or sort by tag. There is no need to delete them</td></tr><tr><td>They appear in a sitemap or feed</td><td>Exclude by tag in the tool that builds it</td></tr></tbody></table>

{% hint style="warning" %}
Do not **unpublish** them from the Online Store. A product that is not published to the Online Store cannot be added to the cart there, which breaks the add-on. Exclude them from collections and search instead — that hides them from browsing while keeping them purchasable.
{% endhint %}

## When to use it, and when not

<table><thead><tr><th width="330">Use it when</th><th>Use something else when</th></tr></thead><tbody><tr><td>The add-on is physical and you want to count it</td><td>It is a service with nothing to count — <a href="add-price-directly.md">Add price</a></td></tr><tr><td>You do not already sell it separately</td><td>You do — <a href="use-an-existing-product.md">Use an existing product</a></td></tr><tr><td>You sell in person through POS</td><td>Never <strong>Add price</strong> for POS</td></tr><tr><td>You want add-ons in your Shopify reporting</td><td></td></tr><tr><td>The add-on has weight that affects shipping</td><td></td></tr></tbody></table>

## Examples

**Gift wrap with real stock**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Option</td><td><code>Gift wrap</code>, a Checkbox with one value</td></tr><tr><td>Price</td><td><strong>Automatically generate product</strong> $3.00</td></tr><tr><td>Advanced settings</td><td><strong>One time charge</strong></td></tr><tr><td>After saving</td><td>Turn on inventory tracking, enter your box count, set the policy to stop selling at zero</td></tr><tr><td>Out of stock options</td><td><strong>Hide</strong></td></tr></tbody></table>

**Twelve premium colours, each with its own stock**

A [Color swatch](../option-types/selection-types/color-swatch.md) where each premium value is generated at its own price. One product, twelve variants, twelve independent stock figures.

**An engraving plate**

A Text option for the engraving, with the price generated so the metal plate itself is counted.

## Notes

* The product is created after you **save**, in the background. It is not instant.
* Editing the price in the app updates the generated variant.
* Renaming the option's **Label** does not rename the existing product — the product keeps the title it was created with.
* Deleting the option set does **not** delete the generated products. They stay in your catalogue. See [Duplicate and delete](../option-sets/duplicate-and-delete.md).
* Duplicating an option set does not duplicate the products — both sets point at the same ones and share their stock.
* If a generated product looks out of step with the app, use **Sync Add-on data** in the builder's more-actions menu.

## Troubleshooting

<details>
<summary>No product appeared</summary>

Save the option set first, then reload the page — creation happens in the background after saving. Also check the price field actually holds a value.
</details>

<details>
<summary>The product has a useless name like "Select"</summary>

It was created from the option's **Label** at the time. Rename the option for future clarity, and rename the product itself in Shopify admin — the link is not by name, so renaming is safe.
</details>

<details>
<summary>Generated products show up in my collections</summary>

Exclude the tag `globo-product-options` in those collections' conditions.
</details>

<details>
<summary>Out-of-stock handling does nothing</summary>

Inventory tracking is off, or the variant is still set to continue selling when out of stock. Both need changing — see [Turning on stock tracking](#turning-on-stock-tracking).
</details>

<details>
<summary>Customers can buy add-ons I have run out of</summary>

Same cause. The default policy is to keep selling.
</details>

<details>
<summary>I deleted the generated product by mistake</summary>

Reopen the option's price dialog and set the price again, then save — a new product is generated. Any stock figure you had is gone.
</details>

<details>
<summary>I have dozens of generated products and cannot tell them apart</summary>

Filter your Shopify products by the `globo-product-options` tag, and give your options meaningful labels before generating in future.
</details>
