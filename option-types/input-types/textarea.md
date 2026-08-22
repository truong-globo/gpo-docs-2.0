---
description: >-
  A multi-line box for gift messages and instructions — the same settings as Text
  plus alignment, width, and height in the live preview.
icon: align-left
---

# Textarea

A multi-line box. Everything [Text](text.md) does, with room for line breaks.

Use it whenever the answer is a sentence or more: a gift message, care instructions, a description of a repair, a brief for a custom piece.

## What customers see

A taller box that accepts several lines, with your label above it and optionally a character counter below.

<!-- SCREENSHOT: type-textarea-storefront | Storefront → trang sản phẩm | 1 field Textarea nhiều dòng đã nhập vài dòng chữ, có counter | Khoanh riêng field Textarea -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A multi-line textarea on a storefront product page with a gift message typed into it"><figcaption><p>A textarea gives shoppers room for a real message.</p></figcaption></figure>

## Settings

Textarea has exactly the same settings as [Text](text.md), on both tabs:

<table><thead><tr><th width="240">Tab</th><th>Settings</th></tr></thead><tbody><tr><td><strong>Basic Settings</strong></td><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a>, <a href="../shared-settings/labels-and-visibility.md#name">Name</a>, <a href="../shared-settings/required-and-default-value.md#required-field">Required field</a>, <a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a>, <a href="../shared-settings/limits.md#min-and-max-character">Min character</a> and <a href="../shared-settings/limits.md#min-and-max-character">Max character</a>, <a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a>, <a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a>, <a href="../shared-settings/required-and-default-value.md#default-value">Default value</a>, <a href="../shared-settings/limits.md#character-counter">Character counter</a>, <a href="../shared-settings/conditional-logic-and-add-on-fields.md#price">Price</a>, <a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td></tr><tr><td><strong>Advanced Settings</strong></td><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> and <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a>, <a href="../shared-settings/text-input-rules.md#allowed-value">Allowed value</a>, <a href="../shared-settings/text-input-rules.md#text-transform">Text transform</a>, <a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a>, <a href="../shared-settings/prefix-suffix-and-icons.md#suffix">Suffix</a>, <a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix</a>, <a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a>, <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td></tr></tbody></table>

## The one real difference: the Personalizer

Text and Textarea diverge in the live preview, because one is a line and the other is a block.

<table><thead><tr><th width="250">Personalizer setting</th><th width="130">Text</th><th>Textarea</th></tr></thead><tbody><tr><td>Text color, Font size, Font style, Font family</td><td>Yes</td><td>Yes</td></tr><tr><td><strong>Text alignment</strong></td><td>No</td><td><strong>Yes</strong> — left, centre, or right</td></tr><tr><td><strong>Width</strong> and <strong>Height</strong></td><td>No</td><td><strong>Yes</strong> — the block the text wraps inside</td></tr><tr><td><strong>Curve</strong></td><td><strong>Yes</strong></td><td>No</td></tr><tr><td><strong>Auto-fit max width</strong></td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Position, opacity, rotation</td><td>Yes</td><td>Yes</td></tr><tr><td>Text effects</td><td>Yes</td><td>Yes</td></tr><tr><td>Clip area, customer controls</td><td>Yes</td><td>Yes</td></tr></tbody></table>

That means a Textarea layer is a text box you size and align, and the customer's lines wrap inside it. A Text layer is a single line you can bend along a curve.

See [Text layers](../../personalizer/text-layers.md) and [Position, size, and rotation](../../personalizer/position-size-rotation.md).

## Add-on pricing

Identical to Text, including the **Per character** mode. Bear in mind that a Textarea invites longer entries, so per-character pricing on a Textarea can add up fast — set a **Max character** as a ceiling.

For a gift message you generally want no charge at all, or one flat fee. See [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md).

## Examples

**Gift message, free**

<table><thead><tr><th width="270">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Gift message</code></td></tr><tr><td>Max character</td><td><code>200</code></td></tr><tr><td>Character counter</td><td><strong>Show</strong></td></tr><tr><td>Placeholder</td><td><code>Happy birthday, from all of us</code></td></tr><tr><td>Price</td><td>None</td></tr><tr><td>Conditional logic</td><td>Show when <strong>Gift wrap</strong> is selected</td></tr></tbody></table>

**Brief for a custom commission**

Min character `50` so you get something usable, max character `1000`, required on, help text `Tell us about the piece you have in mind — at least a couple of sentences.`

**Printed poem on a print**

Max character `400`, **Personalizer** on with **Text alignment** centre and a **Width** and **Height** matching the printable area.

## Limits and notes

* Available on all plans.
* Works in Shopify POS.
* Line breaks are preserved and travel through to the order.
* A very long entry is fine for the order but may not fit your printing area — set **Max character** to what you can actually produce.
* **Allowed value** and **Text transform** apply to the whole entry, including across line breaks.

## Troubleshooting

<details>
<summary>The box is too small or too large on the product page</summary>

Its height comes from your theme and the widget's styling. Adjust with [custom CSS](../../storefront/custom-css.md) using an [HTML class](../shared-settings/direction-width-and-css.md#html-class), or set **Column width** to change its width.
</details>

<details>
<summary>Line breaks are lost by the time the order reaches my team</summary>

The value keeps its line breaks. Some order-printing tools collapse them — check the tool rather than the option.
</details>

<details>
<summary>Per-character pricing produced a huge charge</summary>

A Textarea with no **Max character** and per-character pricing is unbounded. Set a maximum, or switch to a flat charge.
</details>

<details>
<summary>The preview text overflows its box</summary>

Textarea uses **Width** and **Height** rather than auto-fit. Increase them, reduce **Font size**, or lower **Max character**.
</details>

<details>
<summary>I want a curved message</summary>

**Curve** exists on Text only. Use a Text option for curved single lines.
</details>
