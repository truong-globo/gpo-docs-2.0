---
description: >-
  A grid of colour chips, with adjustable chip size, slider layouts, and a live
  colour preview for text.
icon: palette
---

# Color swatch

A grid of colour chips. Every colour is visible at once, which is what shoppers want when colour is the decision they came to make.

Use it when your palette is fixed and reasonably short. For a long list of named colours, [Color dropdown](color-dropdown.md) is more compact. For any colour at all, use [Color picker](../input-types/color-picker.md).

## What customers see

A grid of chips, each a single colour or split into two. Hovering shows the value's name, and the chosen chip is marked. With many colours you can present them as a slider instead.

<!-- SCREENSHOT: type-colorswatch-storefront | Storefront → trang sản phẩm | Grid color swatch, 1 chip đang chọn, 1 chip hết hàng bị blur, hover hiện tooltip tên màu | Khoanh riêng grid swatch -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A grid of colour swatches on a storefront product page with one selected and one blurred"><figcaption><p>All the colours at once — the reason to choose a swatch grid over a dropdown.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until a colour is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#swatch-style">Swatch style</a></td><td><strong>Color</strong> or <strong>Image</strong>. Starts on <strong>Color</strong>.</td></tr><tr><td><strong>Option values</strong></td><td>The colours, each with a <strong>Color</strong> column — one colour, or two for a split chip. See <a href="../../option-sets/option-values.md">Working with option values</a>.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#allow-multiple">Allow multiple</a></td><td>Lets the shopper choose several colours.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-selections">Min selections</a> / <a href="../shared-settings/limits.md#min-and-max-selections">Max selections</a></td><td>Shown once <strong>Allow multiple</strong> is on.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance for the whole option.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Preselects a colour.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="270">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How add-ons scale — including <strong>Mixed quantity</strong> when multiple is on.</td></tr><tr><td><strong>Swatch color width</strong> / <strong>Swatch color height</strong></td><td>The chip size in pixels. Both start at <code>32</code>.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#enable-custom-layout">Enable custom layout</a></td><td>Unlocks the layouts below.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#layout-type">Layout type</a></td><td><strong>Expand</strong>, <strong>Collapse</strong>, or <strong>Slider</strong>.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#scrolling">Scroll type</a>, <strong>Scroll height</strong>, <strong>Number of option values</strong></td><td>Scroll area for the Expand and Collapse layouts.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#slider-settings">Number of rows</a>, <strong>Swatches per row</strong>, <strong>Show navigation arrows</strong>, <strong>Show indicators</strong>, <strong>Slider style</strong></td><td>Slider layout settings.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#color-preview">Color preview</a></td><td>Previews the chosen colour applied to a text option.</td></tr><tr><td><strong>Select text box</strong></td><td>Which text option the preview applies to.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#not-allow-deselect">Not allow deselect</a></td><td>Stops the shopper clearing their choice. Single-select only.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#direction-style">Direction style</a></td><td><strong>Vertical</strong> or <strong>Horizontal</strong>.</td></tr><tr><td><a href="../shared-settings/out-of-stock-options.md">Out of stock options</a></td><td>How sold-out colours look. <strong>Blur</strong> works particularly well here.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the option-level help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

### Chip size

**Swatch color width** and **Swatch color height** are specific to this type — [Image swatch](image-swatch.md) has its own equivalents.

Both default to 32 pixels, which suits a plain colour chip. Make them larger when the colour is subtle or the palette has close shades; make them rectangular for something like a fabric strip.

Bear in mind that larger chips push the **Add to cart** button further down the page. Past about a dozen large chips, use the slider layout.

## Personalizer Settings

Supported as an **image layer**: each colour value can carry an image drawn onto the product photo when selected — typically a photograph of the product in that colour. Settings are image shape, background mode, size, position, rotation, clip area, and customer controls. See [Image layers](../../personalizer/layer-settings/image-layers.md).

## Add-on pricing

Prices belong to each colour. Standard colours free, premium finishes charged, is the usual arrangement.

Linking each colour to an add-on product gives each colour its own stock, which then drives **Out of stock options** — the cleanest way to show a temporarily unavailable colour without editing your option set. See [Stock and inventory](../../add-on-pricing/stock-and-inventory.md).

## Color swatch or Color dropdown?

<table><thead><tr><th width="230"></th><th width="230">Color swatch</th><th>Color dropdown</th></tr></thead><tbody><tr><td>All colours visible</td><td>Yes</td><td>No</td></tr><tr><td>Names visible</td><td>On hover</td><td>Beside each chip</td></tr><tr><td>Search</td><td>No</td><td>Yes</td></tr><tr><td>Slider layout</td><td>Yes</td><td>No</td></tr><tr><td>Vertical space</td><td>More</td><td>One line</td></tr><tr><td>Best for</td><td>Under twenty colours</td><td>Twenty or more, or named colours</td></tr></tbody></table>

## Examples

**Twelve paint colours**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Frame colour</code></td></tr><tr><td>Swatch style</td><td><strong>Color</strong></td></tr><tr><td>Swatch color width / height</td><td><code>40</code> / <code>40</code></td></tr><tr><td>Out of stock options</td><td><strong>Blur</strong></td></tr><tr><td>Not allow deselect</td><td>On</td></tr><tr><td>Required field</td><td>On</td></tr><tr><td>Each value</td><td>Linked to a generated add-on product for stock</td></tr></tbody></table>

**Forty colours as a slider**

**Enable custom layout** on, **Layout type** **Slider**, **Number of rows** `2`, **Swatches per row** `6.5`, **Show navigation arrows** **Show**.

**Two-tone finishes**

Each value set to a two-colour split chip.

**Thread colour with a live text preview**

**Color preview** on, **Select text box** pointing at your engraving text option.

## Limits and notes

* Available on all plans. Slider layout is separately plan-gated.
* Works in Shopify POS.
* Colours are set per value in the values table.
* Value names are shown on hover, so they still matter — a shopper on a phone may never see them, which is a reason to prefer [Color dropdown](color-dropdown.md) when names carry information.
* Screen colours do not match physical products exactly. Say so in help text if it matters.

## Troubleshooting

<details>
<summary>The values table has no Color column</summary>

**Swatch style** is set to **Image**. Switch it to **Color**.
</details>

<details>
<summary>All the chips look the same</summary>

The values still hold their default colour. Set each one.
</details>

<details>
<summary>The grid takes up too much of the page</summary>

Reduce the chip size, or use the **Slider** layout. See [Collapsible layouts and sliders](../shared-settings/collapsible-layouts-and-sliders.md).
</details>

<details>
<summary>Names do not appear on hover</summary>

Check **Show tooltip when hovering over options** in **Settings > Settings > General**.
</details>

<details>
<summary>Color preview does nothing</summary>

Set **Select text box** as well, pointing at a text option in the same option set.
</details>

<details>
<summary>Sold-out colours are still selectable</summary>

**Out of stock options** is on **Show**, or the values are priced with **Add price**, which has no stock.
</details>
