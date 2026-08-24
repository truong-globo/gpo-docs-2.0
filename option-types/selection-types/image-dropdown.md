---
description: >-
  A dropdown with a picture beside every entry, and an option to show the chosen
  image outside the closed field.
icon: image
---

# Image dropdown

A [Dropdown](dropdown.md) where each entry carries a picture. Use it when the choice is visual but the list is too long for a swatch grid — thirty print designs, twenty fabric patterns, a catalogue of frame styles.

## What customers see

A field showing the current choice. Opening it lists every entry with its picture, searchable if you turn search on. With **Image display outside dropdown** on, the chosen picture is also shown beside the closed field.

<!-- SCREENSHOT: type-imagedropdown-storefront | Storefront → trang sản phẩm | Image dropdown đang mở, mỗi entry có ảnh nhỏ + tên | Khoanh vùng dropdown đang mở -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An open image dropdown on a storefront product page with a thumbnail beside each entry"><figcaption><p>A picture per entry, without the vertical cost of a swatch grid.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until something is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><strong>Option values</strong></td><td>The choices, each with an <strong>Image</strong> column. Upload a picture, or reuse one of the product's own images. See <a href="../../option-sets/option-values.md">Working with option values</a>.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#allow-multiple">Allow multiple</a></td><td>Lets the shopper choose several.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-selections">Min selections</a> / <a href="../shared-settings/limits.md#min-and-max-selections">Max selections</a></td><td>Shown once <strong>Allow multiple</strong> is on.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>The unselected prompt.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Preselects a value.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

There is no **Swatch style** setting on this type — it is always images.

## Advanced Settings

<table><thead><tr><th width="290">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How the add-on scales with quantity.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#search-suggestion">Search suggestion</a></td><td>Adds a search box to the list.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#not-allow-deselect">Not allow deselect</a></td><td>Stops the shopper clearing their choice. Single-select only.</td></tr><tr><td><strong>Image display outside dropdown</strong></td><td>Shows the chosen image beside the closed field, so the choice stays visible without reopening the list. Off by default.</td></tr><tr><td><a href="../shared-settings/out-of-stock-options.md">Out of stock options</a></td><td>How sold-out entries look.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

### Image display outside dropdown

Worth turning on for anything where the shopper will want to keep looking at what they chose while they fill in the rest of the form — a print design, a fabric, a frame.

Without it, the closed field shows only the value's name, and the shopper has to reopen the list to remind themselves what it looked like.

## Personalizer Settings

Supported as an **image layer**. Each value's image can be drawn onto the product photo when it is selected, with image shape, background mode, size, position, rotation, a clip area, and customer controls.

This is the combination behind "choose a design and see it on the product": an Image dropdown for the list, Personalizer for the preview. See [Image layers](../../personalizer/image-layers.md).

## Add-on pricing

Prices belong to each value, so different designs can cost different amounts. Linking values to add-on products gives each design its own stock, which then drives **Out of stock options**.

See [Add-on pricing](../../add-on-pricing/README.md).

## Image dropdown or Image swatch?

<table><thead><tr><th width="230"></th><th width="230">Image dropdown</th><th>Image swatch</th></tr></thead><tbody><tr><td>Space used</td><td>One line, closed</td><td>A grid, always open</td></tr><tr><td>Names shown</td><td>Beside each picture</td><td>On hover</td></tr><tr><td>Search</td><td>Yes</td><td>No</td></tr><tr><td>Slider layout</td><td>No</td><td>Yes</td></tr><tr><td>Picture size</td><td>Small thumbnails</td><td>Adjustable, plus a zoom tooltip</td></tr><tr><td>Best for</td><td>Twenty or more designs</td><td>Under twenty, where the picture is the whole decision</td></tr></tbody></table>

If shoppers need to compare pictures side by side, use [Image swatch](image-swatch.md). If they arrive knowing roughly what they want and need to find it, use this.

## Examples

**Thirty print designs**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Print design</code></td></tr><tr><td>Option values</td><td>Thirty entries, each with its artwork image</td></tr><tr><td>Search suggestion</td><td>On</td></tr><tr><td>Image display outside dropdown</td><td>On</td></tr><tr><td>Required field</td><td>On</td></tr><tr><td>Personalizer</td><td>On, so the design appears on the product photo</td></tr></tbody></table>

**Fabric swatches with different prices**

Standard fabrics free, premium ones priced through **Automatically generate product** so each has its own stock.

**Frame styles**

Values with photographs of each moulding, **Image display outside dropdown** on, **Not allow deselect** on.

## Limits and notes

* Available on the Advanced plan.
* Works in Shopify POS.
* Always image-based — there is no text-only or colour mode.
* Every value needs an image. Without one the entry shows a blank.
* Use consistently sized, consistently lit images. A list of mismatched crops looks careless.
* No slider or collapsible layout.

## Troubleshooting

<details>
<summary>Entries have no picture</summary>

Upload an image on each value in the values table's **Image** column, or reuse a product image.
</details>

<details>
<summary>The chosen picture disappears when the list closes</summary>

Turn on **Image display outside dropdown**.
</details>

<details>
<summary>Thumbnails look stretched</summary>

Your uploaded images have inconsistent proportions. Crop them to a consistent shape before uploading.
</details>

<details>
<summary>I want bigger pictures</summary>

Use [Image swatch](image-swatch.md), which has adjustable swatch sizes and a zooming tooltip.
</details>

<details>
<summary>The design does not appear on the product photo</summary>

Turn on **Personalizer Settings** and configure a background for the option set. See [Choosing the background](../../personalizer/setup.md#choosing-the-background).
</details>
