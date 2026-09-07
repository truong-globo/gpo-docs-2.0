---
description: Send customers to other products instead of collecting a choice.
icon: link
---

# Product links

Product links is the exception among the selection types, because it does not collect an answer. It displays a set of other products and takes the customer to the product they select.

Use it when the options are separate products, such as sizes sold as individual listings, colors sold as separate products, or a family of related models.

{% hint style="warning" %}
The app displays two important limitations when you add this option:

* **Only one Product links field per option set is recommended.** Using more than one can cause conflicts.
* **Not supported on the Shopify POS app.** Avoid it if you take orders in person. See [POS limitations](../../pos/limitations.md).
{% endhint %}

## What customers see

A set of choices in the style you select. Selecting one opens that product's page.

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name recorded internally.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><strong>Display style</strong></td><td>How the links are presented. Five choices — see below.</td></tr><tr><td><strong>Option values</strong></td><td>The products themselves, selected from your catalog.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>The unselected prompt, for the dropdown style.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

There is no **Required field** and no **Default value**, because nothing is collected.

### Display style

<table><thead><tr><th width="230">Style</th><th>Looks like</th><th>Best for</th></tr></thead><tbody><tr><td><strong>Dropdown</strong></td><td>A list</td><td>Many products, little space</td></tr><tr><td><strong>Radio</strong></td><td>A vertical list</td><td>Products whose names need reading</td></tr><tr><td><strong>Button</strong></td><td>A row of buttons</td><td>Short names such as sizes. This is the default</td></tr><tr><td><strong>Color Swatch</strong></td><td>A grid of color chips</td><td>Color variations sold as separate products</td></tr><tr><td><strong>Image Swatch</strong></td><td>A grid of pictures</td><td>Visually distinct products</td></tr></tbody></table>

The style changes the appearance only. The behavior is the same in all five: selecting a value opens that product.

### Option values

Values are products selected from your catalog rather than text you enter. Each value includes the selected product, its handle, and its image. For the swatch styles, it can also include a color or image.

Because these values are products, the uniqueness rule that applies to option values elsewhere does not apply here.

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/out-of-stock-options.md">Out of stock options</a></td><td>How a linked product looks when it is out of stock: <strong>Show</strong>, <strong>Hide</strong>, <strong>Blur</strong>, or <strong>Strike-through</strong>.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

**Out of stock options** is useful here, because it reads the linked product's real availability and prevents you from sending customers to a product they cannot buy.

## Add-on pricing and Personalizer

Neither applies. Product links does not add anything to the cart. It sends the customer to a different product page, where that product's own price and options apply.

## Product links or Shopify variants?

If the products are variations of one item, such as the same item in three colors, use Shopify's own variants instead. They keep the customer on one page, share reviews and the URL, and change the product images natively.

Use Product links when the items are separate products:

<table><thead><tr><th width="290">Situation</th><th>Use</th></tr></thead><tbody><tr><td>Same product, three colors</td><td>Shopify variants</td></tr><tr><td>Same product, twelve colors and four sizes, past Shopify's variant limit</td><td>Separate products, joined with Product links</td></tr><tr><td>A family of related but distinct models</td><td>Product links</td></tr><tr><td>Bundle sizes sold as their own listings</td><td>Product links</td></tr><tr><td>An option that changes the price of <em>this</em> product</td><td>An <a href="../../add-on-pricing/">add-on</a>, not a link</td></tr></tbody></table>

## Examples

**Sizes sold as separate products**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Size</code></td></tr><tr><td>Display style</td><td><strong>Button</strong></td></tr><tr><td>Option values</td><td>The three size products</td></tr><tr><td>Out of stock options</td><td><strong>Strike-through</strong></td></tr><tr><td>Help text</td><td><code>Each size is its own product page.</code></td></tr></tbody></table>

**Colors as separate products**

**Display style** set to **Color Swatch**, with one value for each color product, so the grid looks like a normal color swatch even though each chip is a link.

**A model family**

**Display style** set to **Image Swatch**, with a photo of each model.

## Notes

* Available on paid plans.
* **Not supported on Shopify POS.**
* Only one Product links option per option set is recommended.
* No required field, default value, add-on price, or Personalizer.
* Selecting a value opens another page, so anything the customer entered on the current page is lost. Put Product links **above** your other options, or in its own [Section](../static-types/section.md) at the top, so it reads as navigation rather than as part of the form.
* Linked products are normal products with their own option sets, so check that the correct option sets apply to them.
