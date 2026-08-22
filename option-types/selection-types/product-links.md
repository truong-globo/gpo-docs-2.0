---
description: >-
  Send shoppers to other products instead of collecting a choice — five display
  styles, and the two limits to know about.
icon: link
---

# Product links

The odd one out among the selection types. Product links does not collect an answer — it shows a set of other products and takes the shopper to the one they select.

Use it when the "options" are really separate products: different sizes sold as their own listings, colours that are separate items, a family of related models.

{% hint style="warning" %}
Two limits, and the app tells you both when you add the option:

* **Only one Product links field per option set is recommended.** More than one can conflict.
* **Not supported on the Shopify POS app.** Avoid it if you take orders in person. See [POS limitations](../../pos/limitations.md).
{% endhint %}

## What customers see

A set of choices in the style you pick. Selecting one navigates to that product's page.

<!-- SCREENSHOT: type-productlinks-storefront | Storefront → trang sản phẩm | Product links dạng button, mỗi button là 1 sản phẩm khác | Khoanh riêng nhóm product links -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Product links shown as a row of buttons on a storefront product page"><figcaption><p>Each choice is a link to another product, not an option on this one.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name recorded internally.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><strong>Display style</strong></td><td>How the links are presented. Five choices — see below.</td></tr><tr><td><strong>Option values</strong></td><td>The products themselves, selected from your catalogue.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>The unselected prompt, for the dropdown style.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

There is no **Required field** and no **Default value** — nothing is being collected, so neither would mean anything.

### Display style

<table><thead><tr><th width="230">Style</th><th>Looks like</th><th>Best for</th></tr></thead><tbody><tr><td><strong>Dropdown</strong></td><td>A list</td><td>Many products, little space</td></tr><tr><td><strong>Radio</strong></td><td>A vertical list</td><td>Products whose names need reading</td></tr><tr><td><strong>Button</strong></td><td>A row of buttons</td><td>Short names such as sizes. This is the default</td></tr><tr><td><strong>Color Swatch</strong></td><td>A grid of colour chips</td><td>Colour variations sold as separate products</td></tr><tr><td><strong>Image Swatch</strong></td><td>A grid of pictures</td><td>Visually distinct products</td></tr></tbody></table>

The style only changes the appearance. The behaviour is the same in all five: selecting a value navigates to that product.

### Option values

Values are products you select from your catalogue rather than text you type. Each value carries the product, its handle, its image, and — for the swatch styles — a colour or image.

Because the values are products, the uniqueness rule that applies to other option types' values does not apply here.

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/out-of-stock-options.md">Out of stock options</a></td><td>How a linked product looks when it is out of stock: <strong>Show</strong>, <strong>Hide</strong>, <strong>Blur</strong>, or <strong>Strike-through</strong>.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

**Out of stock options** is genuinely useful here: it reads the linked product's real availability, so you are not sending shoppers to a page they cannot buy from.

## Add-on pricing and Personalizer

Neither applies. Product links does not add anything to the cart — it moves the shopper to a different product page, where that product's own price and options take over.

## Product links or Shopify variants?

If the products are genuinely variations of one thing — the same item in three colours — Shopify's own variants are almost always better. They keep the shopper on one page, share reviews, share the URL, and swap images natively.

Product links is for when the items really are separate products:

<table><thead><tr><th width="290">Situation</th><th>Use</th></tr></thead><tbody><tr><td>Same product, three colours</td><td>Shopify variants</td></tr><tr><td>Same product, twelve colours and four sizes, past Shopify's variant limit</td><td>Separate products, joined with Product links</td></tr><tr><td>A family of related but distinct models</td><td>Product links</td></tr><tr><td>Bundle sizes sold as their own listings</td><td>Product links</td></tr><tr><td>An option that changes the price of <em>this</em> product</td><td>An <a href="../../add-on-pricing/README.md">add-on</a>, not a link</td></tr></tbody></table>

## Examples

**Sizes sold as separate products**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Size</code></td></tr><tr><td>Display style</td><td><strong>Button</strong></td></tr><tr><td>Option values</td><td>The three size products</td></tr><tr><td>Out of stock options</td><td><strong>Strike-through</strong></td></tr><tr><td>Help text</td><td><code>Each size is its own product page.</code></td></tr></tbody></table>

**Colours as separate products**

**Display style** **Color Swatch**, one value per colour product, so the grid reads exactly like a normal colour swatch even though each chip is a link.

**A model family**

**Display style** **Image Swatch** with a photo of each model.

## Limits and notes

* Available on paid plans.
* **Not supported on Shopify POS.**
* Only one Product links option per option set is recommended.
* No required field, default value, add-on price, or Personalizer.
* Selecting a value navigates away from the current page, so anything the shopper filled in on this page is lost. Put Product links **above** your other options, or in a [Section](../static-types/section.md) of its own at the top, so it reads as navigation rather than as part of the form.
* Linked products are ordinary products with their own option sets — remember to apply the right ones to them too.

## Troubleshooting

<details>
<summary>The option does not appear in POS</summary>

Product links is not supported there. Remove it from option sets published to POS, or accept that it is web-only.
</details>

<details>
<summary>Two Product links options conflict</summary>

Only one per option set is supported. Remove the extra one.
</details>

<details>
<summary>Shoppers lose what they typed when they select a link</summary>

Expected — selecting a link is navigation. Move the Product links option to the top of the form so it is used before anything is filled in.
</details>

<details>
<summary>A linked product page has no options</summary>

Option sets apply per product. Make sure your product rules cover the linked products too. See [Assign to products](../../option-sets/assign-to-products.md).
</details>

<details>
<summary>Out-of-stock products are still linked</summary>

**Out of stock options** is on **Show**. Change it to **Hide**, **Blur**, or **Strike-through**.
</details>

<details>
<summary>I wanted the choice to change this product's price</summary>

That is an add-on, not a link. See [Add-on pricing](../../add-on-pricing/README.md).
</details>
