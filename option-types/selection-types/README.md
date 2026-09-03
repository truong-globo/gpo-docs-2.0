---
description: >-
  The 11 option types where the customer chooses from a list you define — and
  how they differ from each other.
icon: hand-pointer
---

# Selection types

Selection types present a list of **option values** you define. The customer chooses one, or several. Every one of them can carry a different price, and every one can be linked to a real product for stock.

## Eleven option types

<table><thead><tr><th width="210">Type</th><th>Looks like</th><th>Reach for it when</th></tr></thead><tbody><tr><td><a href="select.md">Select</a></td><td>The browser's own dropdown</td><td>You want something plain and dependable</td></tr><tr><td><a href="dropdown.md">Dropdown</a></td><td>A styled dropdown</td><td>You want search, swatches, or the live preview</td></tr><tr><td><a href="color-dropdown.md">Color dropdown</a></td><td>A dropdown with a colour per entry</td><td>Many colours, little vertical space</td></tr><tr><td><a href="image-dropdown.md">Image dropdown</a></td><td>A dropdown with a picture per entry</td><td>Many designs, little vertical space</td></tr><tr><td><a href="radio-button.md">Radio button</a></td><td>A vertical list, one choice</td><td>Values have long names or their own help text</td></tr><tr><td><a href="checkbox.md">Checkbox</a></td><td>A list, several choices</td><td>A menu of optional extras</td></tr><tr><td><a href="button.md">Button</a></td><td>A row of buttons</td><td>Short values such as sizes</td></tr><tr><td><a href="color-swatch.md">Color swatch</a></td><td>A grid of colour chips</td><td>Colour is the choice, and you want it visible</td></tr><tr><td><a href="image-swatch.md">Image swatch</a></td><td>A grid of pictures</td><td>Patterns, materials, or designs you photograph</td></tr><tr><td><a href="font-picker.md">Font picker</a></td><td>A list of fonts, drawn in those fonts</td><td>The customer chooses the lettering</td></tr><tr><td><a href="product-links.md">Product links</a></td><td>Links to other products</td><td>You want to send them elsewhere, not collect a choice</td></tr></tbody></table>

## The capability matrix

This is the fastest way to pick between them.

<table><thead><tr><th width="170">Type</th><th width="110">Multiple</th><th width="110">Search</th><th width="130">Swatch style</th><th width="130">Out of stock</th><th width="130">Slider layout</th><th>Personalizer</th></tr></thead><tbody><tr><td>Select</td><td>Yes</td><td>No</td><td>No</td><td>No</td><td>No</td><td>No</td></tr><tr><td>Dropdown</td><td>Yes</td><td>Yes</td><td>Default, Image</td><td>Yes</td><td>No</td><td>Yes</td></tr><tr><td>Color dropdown</td><td>Yes</td><td>Yes</td><td>Color, Image</td><td>Yes</td><td>No</td><td>Yes</td></tr><tr><td>Image dropdown</td><td>Yes</td><td>Yes</td><td>Images only</td><td>Yes</td><td>No</td><td>Yes</td></tr><tr><td>Radio button</td><td>No</td><td>No</td><td>Default, Color, Image</td><td>Yes</td><td>No</td><td>Yes</td></tr><tr><td>Checkbox</td><td>Always</td><td>No</td><td>Default, Color, Image</td><td>Yes</td><td>No</td><td>Yes</td></tr><tr><td>Button</td><td>Yes</td><td>No</td><td>Default, Image</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>Color swatch</td><td>Yes</td><td>No</td><td>Color, Image</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>Image swatch</td><td>Yes</td><td>No</td><td>Images only</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>Font picker</td><td>Yes</td><td>Yes</td><td>No</td><td>No</td><td>No</td><td>No</td></tr><tr><td>Product links</td><td>No</td><td>No</td><td>No</td><td>Yes</td><td>No</td><td>No</td></tr></tbody></table>

The following selection types also offer **Not allow deselect**, which prevents the shopper from clearing their choice once selected: **Dropdown**, **Color dropdown**, **Image dropdown**, **Button**, **Color swatch**, and **Image swatch**. This setting is available when **Allow multiple** is off. See [Selection behaviour](../shared-settings/selection-behaviour.md).

## What they all share

* **Option values** — the list itself, with per-value prices, colours, images, and help text. See [Working with option values](../../option-sets/option-values.md).
* [Label](../shared-settings/labels-and-visibility.md#label), [Name](../shared-settings/labels-and-visibility.md#name), [Hidden label](../shared-settings/labels-and-visibility.md#hidden-label)
* [Required field](../shared-settings/required-and-default-value.md#required-field) and [Default value](../shared-settings/required-and-default-value.md#default-value) — except Product links, which collects nothing
* [Help text](../shared-settings/placeholder-and-help-text.md#help-text) and its [position](../shared-settings/placeholder-and-help-text.md#help-text-position)
* [Conditional logic](../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic)
* The add-on **Advanced settings** dropdown — see [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md)
* [Column width](../shared-settings/direction-width-and-css.md#column-width) and [HTML class](../shared-settings/direction-width-and-css.md#html-class)

## Where the price lives

On a selection type, the price belongs to **each option value -** not to the option. That is the important structural difference from the input types: different choices usually cost different amounts.

You set it in the values table's **Price** column, and each value can use a different mode — one linked to an existing product, app-generated, or a plain price. See [Where you can set add-ons](../../add-on-pricing/where-you-can-set-add-ons.md).

Values with no price are free.

## Swatch style crosses the boundaries

**Swatch style** controls how an option looks, independently of how it behaves. A Checkbox can look like color chips, while a Button can display images. The option type controls the _selection behavior_; the style controls the _appearance_.

So don’t choose **Color swatch** simply because you want to show colors. Choose it when you want a grid layout with slider support. If you want colors in a vertical list with help text for each value, use a Radio button with **Swatch style** set to **Color**. See [Swatch style and previews](../shared-settings/swatch-style-and-previews.md).

## Notes

* **Product links** is the exception: it does not collect an answer and is not supported on Shopify POS. We recommend using only one **Product links** option per option set. See [Product links](product-links.md).
* For long lists, consider three approaches: add [search](../shared-settings/selection-behaviour.md#search-suggestion), use a [collapsible layout or slider](../shared-settings/collapsible-layouts-and-sliders.md), or split the list across two options using [conditional logic](../../conditional-logic/).
