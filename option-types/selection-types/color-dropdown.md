---
description: >-
  A dropdown with a colour chip beside every entry — for long colour lists that
  would take too much space as a swatch grid.
icon: droplet
---

# Color dropdown

A [Dropdown](dropdown.md) where each entry carries a colour chip. It is the compact answer to a long colour list: forty colours as a swatch grid dominate the page, but as a dropdown they take one line.

## What customers see

A field showing the current colour and its name. Opening it lists every colour with a chip beside its name, searchable if you turn search on.

<!-- SCREENSHOT: type-colordropdown-storefront | Storefront → trang sản phẩm | Color dropdown đang mở, mỗi entry có chip màu + tên | Khoanh vùng dropdown đang mở -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An open colour dropdown on a storefront product page with a colour chip beside each name"><figcaption><p>A colour chip beside the name means shoppers do not have to imagine what "Sage" is.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until a colour is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#swatch-style">Swatch style</a></td><td><strong>Color</strong> or <strong>Image</strong>. Starts on <strong>Color</strong>.</td></tr><tr><td><strong>Option values</strong></td><td>The colours, with a <strong>Color</strong> column for each. Single or split two-colour chips. See <a href="../../option-sets/option-values.md">Working with option values</a>.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#allow-multiple">Allow multiple</a></td><td>Lets the shopper choose several colours.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-selections">Min selections</a> / <a href="../shared-settings/limits.md#min-and-max-selections">Max selections</a></td><td>Shown once <strong>Allow multiple</strong> is on.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>The unselected prompt.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Preselects a colour.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How the add-on scales with quantity.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#search-suggestion">Search suggestion</a></td><td>Adds a search box. Worth turning on past about fifteen colours.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#not-allow-deselect">Not allow deselect</a></td><td>Stops the shopper clearing their choice. Single-select only.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#color-preview">Color preview</a></td><td>Previews the chosen colour applied to a text option.</td></tr><tr><td><strong>Select text box</strong></td><td>Which text option the preview applies to. Appears once <strong>Color preview</strong> is on.</td></tr><tr><td><a href="../shared-settings/out-of-stock-options.md">Out of stock options</a></td><td>How sold-out colours look.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

### Color preview

Turning on **Color preview** and pointing **Select text box** at a [Text](../input-types/text.md) option in the same option set gives you "see your engraving in the colour you chose" without the full Personalizer.

Use it when the colour applies to text — thread colour, ink colour, foil colour. See [Swatch style and previews](../shared-settings/swatch-style-and-previews.md#color-preview).

## Personalizer Settings

Supported as an **image layer**: each colour value can carry an image that appears on the product photo when chosen. Settings are image shape, background mode, size, position, rotation, clip area, and customer controls.

Useful when each colour has a photograph of the product in that colour. See [Image layers](../../personalizer/image-layers.md).

## Add-on pricing

Prices belong to each colour value. A premium finish can cost more than a standard one, and each value can use a different mode.

Linking values to add-on products is what makes **Out of stock options** meaningful — sold-out colours can then be blurred or hidden automatically. See [Stock and inventory](../../add-on-pricing/stock-and-inventory.md).

## Color dropdown or Color swatch?

<table><thead><tr><th width="230"></th><th width="230">Color dropdown</th><th>Color swatch</th></tr></thead><tbody><tr><td>Space used</td><td>One line, closed</td><td>A grid, always open</td></tr><tr><td>Colour names visible</td><td>Yes, beside each chip</td><td>On hover, as a tooltip</td></tr><tr><td>Search</td><td>Yes</td><td>No</td></tr><tr><td>Slider layout</td><td>No</td><td>Yes</td></tr><tr><td>Best for</td><td>Twenty or more colours, or named colours</td><td>Under twenty, where seeing them all matters</td></tr></tbody></table>

If your colours have names that mean something — `Antique brass`, `Sage` — the dropdown is better, because the name and the chip are shown together. If the colour itself is the whole message, the swatch grid is better.

## Examples

**Forty thread colours**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Thread colour</code></td></tr><tr><td>Swatch style</td><td><strong>Color</strong></td></tr><tr><td>Search suggestion</td><td>On</td></tr><tr><td>Not allow deselect</td><td>On</td></tr><tr><td>Required field</td><td>On</td></tr><tr><td>Color preview</td><td>On, pointing at <code>Embroidered name</code></td></tr></tbody></table>

**Two-tone finishes**

Each value set to a two-colour split chip, so `Black and gold` shows both.

**Colours with different prices**

Standard colours free, metallics priced through **Automatically generate product** so you can track their stock.

## Limits and notes

* Available on the Advanced plan.
* Works in Shopify POS.
* No slider or collapsible layout — a dropdown is already compact.
* Colour chips are set per value in the values table, not globally.
* Colours on screen will not match a physical product exactly. Say so in help text if colour accuracy matters.

## Troubleshooting

<details>
<summary>The values table has no Color column</summary>

**Swatch style** is set to **Image**. Switch it to **Color**.
</details>

<details>
<summary>Chips are all the same colour</summary>

The values still have their default colour. Set each one in the **Color** column.
</details>

<details>
<summary>Color preview does nothing</summary>

Set **Select text box** as well, and make sure that text option exists in the same option set.
</details>

<details>
<summary>Sold-out colours are still selectable</summary>

**Out of stock options** is on **Show**, or the values have no add-on product behind them. See [Out of stock options](../shared-settings/out-of-stock-options.md).
</details>

<details>
<summary>Color dropdown is greyed out</summary>

It is on the Advanced plan. See [Compare plans](../../plans/compare-plans.md).
</details>
