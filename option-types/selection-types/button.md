---
description: >-
  A row of tappable buttons — the most compact way to show short choices such as
  sizes, with slider support for long lists.
icon: square
---

# Button

A row of buttons, one per value. Every choice is visible and tappable in one gesture, which makes it the best type for short values on mobile.

It is the type Shopify shoppers are most used to seeing for sizes.

## What customers see

A row of buttons that wrap onto more rows as needed, or a slider if you configure one. With **Swatch style** set to **Image**, each button shows a picture instead of text.

<!-- SCREENSHOT: type-button-storefront | Storefront → trang sản phẩm | 1 hàng button size (S M L XL) với 1 button đang chọn và 1 button hết hàng bị strike-through | Khoanh riêng hàng button -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A row of size buttons on a storefront product page with one selected and one struck through"><figcaption><p>Short values as buttons — one tap, no opening or scrolling.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until one is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#swatch-style">Swatch style</a></td><td><strong>Default</strong> or <strong>Image</strong>.</td></tr><tr><td><strong>Option values</strong></td><td>The choices, with prices and their own help text. See <a href="../../concepts/option-values.md">Working with option values</a>.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#allow-multiple">Allow multiple</a></td><td>Lets the shopper choose several. Reveals the two limits below.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-selections">Min selections</a> / <a href="../shared-settings/limits.md#min-and-max-selections">Max selections</a></td><td>How many they must and may choose.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance for the whole option.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Preselects one or more values.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How add-ons scale — including <strong>Mixed quantity</strong> when multiple is on.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#enable-custom-layout">Enable custom layout</a></td><td>Unlocks the layouts below.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#layout-type">Layout type</a></td><td><strong>Expand</strong>, <strong>Collapse</strong>, or <strong>Slider</strong>.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#scrolling">Scroll type</a>, <strong>Scroll height</strong>, <strong>Number of option values</strong></td><td>Scroll area, for the Expand and Collapse layouts.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#slider-settings">Number of rows</a>, <strong>Swatches per row</strong>, <strong>Show navigation arrows</strong>, <strong>Show indicators</strong>, <strong>Slider style</strong></td><td>Slider layout settings.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#not-allow-deselect">Not allow deselect</a></td><td>Stops the shopper clearing their choice. Single-select only.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#direction-style">Direction style</a></td><td><strong>Vertical</strong> or <strong>Horizontal</strong>.</td></tr><tr><td><a href="../shared-settings/out-of-stock-options.md">Out of stock options</a></td><td>How sold-out values look.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the option-level help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

Button is one of only three types with a **Slider** layout, alongside [Color swatch](color-swatch.md) and [Image swatch](image-swatch.md).

## Personalizer Settings

Supported as an **image layer**: each value can draw an image onto the product photo when selected. Settings are image shape, background mode, size, position, rotation, clip area, and customer controls. See [Image layers](../../personalizer/image-layers.md).

## Add-on pricing

Prices belong to each value. With **Allow multiple** off, exactly one charge applies. With it on, every selected value is charged, and **Mixed quantity** becomes available.

See [Add-on pricing](../../add-on-pricing/README.md).

## Keep values short

Buttons size themselves to their text. Short values give you a tidy row; long ones give you a stack of full-width blocks that would have been better as a [Radio button](radio-button.md) list.

<table><thead><tr><th width="290">Works well as buttons</th><th>Better as radio buttons</th></tr></thead><tbody><tr><td><code>S</code> <code>M</code> <code>L</code> <code>XL</code></td><td><code>Standard delivery, 3–5 working days</code></td></tr><tr><td><code>10cm</code> <code>15cm</code> <code>20cm</code></td><td><code>Gift wrapped in recycled paper with a ribbon</code></td></tr><tr><td><code>Matt</code> <code>Gloss</code> <code>Satin</code></td><td><code>Premium service including insurance</code></td></tr><tr><td><code>1</code> <code>2</code> <code>3</code> <code>4</code></td><td>Anything needing its own help text</td></tr></tbody></table>

## Examples

**Sizes**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Size</code></td></tr><tr><td>Option values</td><td><code>S</code>, <code>M</code>, <code>L</code>, <code>XL</code>, each linked to an add-on product for stock</td></tr><tr><td>Required field</td><td>On</td></tr><tr><td>Not allow deselect</td><td>On</td></tr><tr><td>Out of stock options</td><td><strong>Strike-through</strong></td></tr><tr><td>Direction style</td><td><strong>Horizontal</strong></td></tr></tbody></table>

**Many sizes, as a slider**

Twenty sizes, **Enable custom layout** on, **Layout type** **Slider**, **Number of rows** `2`, **Swatches per row** `5.5`, **Show navigation arrows** **Show**.

**Quantity bands with prices**

Values `1 pack`, `3 pack`, `5 pack`, priced through **Use existing product** so each maps to a real SKU.

**Several finishes at once**

**Allow multiple** on, **Max selections** `2`, **Advanced settings** **Mixed quantity**.

## Limits and notes

* Available on all plans.
* Works in Shopify POS.
* Slider layout is plan-gated — see [Compare plans](../../plans/compare-plans.md).
* Per-value help text exists but is cramped inside a button. Radio buttons show it better.
* **Not allow deselect** disappears once **Allow multiple** is on.
* Values follow the order of the values table. For sizes, use natural order rather than alphabetical.

## Troubleshooting

<details>
<summary>Buttons wrap onto too many rows</summary>

The values are too long, or there are too many. Shorten them, use a **Slider** layout, or switch to a [Dropdown](dropdown.md).
</details>

<details>
<summary>The row looks cramped on mobile</summary>

Check the mobile preview in the builder. Reduce **Swatches per row** if using a slider, or shorten the value names.
</details>

<details>
<summary>Shoppers clear their size by accident</summary>

Turn on **Not allow deselect**.
</details>

<details>
<summary>Slider is missing from Layout type</summary>

Turn on **Enable custom layout** first, and check your plan includes the slider.
</details>

<details>
<summary>Sold-out sizes are still selectable</summary>

**Out of stock options** is on **Show**, or the values have no add-on product behind them.
</details>

## Next steps

* [Radio button](radio-button.md) — when values need explaining.
* [Collapsible layouts and sliders](../shared-settings/collapsible-layouts-and-sliders.md) — for long lists.
* [Image swatch](image-swatch.md) — when the choice is a picture.
