---
description: >-
  A single-line box for names, engravings, and short messages — with character
  limits, input rules, per-character pricing, and live preview support.
icon: font
---

# Text

A one-line box the customer types into. It is the most used type in the app, and the one most personalisation is built on.

Use it for anything short and singular: a name to engrave, two initials, a team number, a reference. For anything longer than a line, use [Textarea](textarea.md).

## What customers see

A single-line field with your label above it, optionally with a character counter, a prefix, and a suffix.

<!-- SCREENSHOT: type-text-storefront | Storefront → trang sản phẩm | 1 field Text có label, placeholder, help text và character counter | Khoanh riêng field Text -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A text field on a storefront product page with a label, placeholder, and character counter"><figcaption><p>A text option with a character counter and help text.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a></td><td>The text above the field.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>The name on the cart and order. Unique, no <code>.</code> <code>:</code> <code>"</code> <code>'</code> <code>\</code> <code>|</code>.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until something is typed.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label on the product page.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-character">Min character</a> / <a href="../shared-settings/limits.md#min-and-max-character">Max character</a></td><td>How short and how long the entry may be.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>Example text inside the empty field.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>A line of guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Pre-fills the field.</td></tr><tr><td><a href="../shared-settings/limits.md#character-counter">Character counter</a></td><td><strong>Show</strong> or <strong>Hide</strong> a live count as they type.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#price">Price</a></td><td>The add-on charge, under <strong>Add-on Settings</strong>.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide this option based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a></td><td>How the add-on scales — including <strong>Per character</strong>.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>The number used by the fixed and dynamic quantity modes.</td></tr><tr><td><a href="../shared-settings/text-input-rules.md#allowed-value">Allowed value</a></td><td>Restrict to letters, or letters and numbers.</td></tr><tr><td><a href="../shared-settings/text-input-rules.md#text-transform">Text transform</a></td><td>Force uppercase, lowercase, sentence case, or capitalised.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#suffix">Suffix</a></td><td>Fixed text after the field, such as a unit.</td></tr><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-icon">Prefix icon</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-text">Prefix text</a></td><td>An icon or short text inside the start of the field.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a></td><td>A CSS class for your own styling.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>How much width the field takes.</td></tr></tbody></table>

## Add-on pricing

The price belongs to the whole option, since there is one answer. All three add-on modes are available — link an existing product, generate one, or just add a price. See [Add-on pricing](../../add-on-pricing/README.md).

Text and Textarea are the only two types with the **Per character** advanced mode, which charges by how many characters the customer typed. It is the natural way to price engraving:

<table><thead><tr><th width="290">Configuration</th><th>Result for "Forever yours" (13 characters)</th></tr></thead><tbody><tr><td><strong>Price</strong> $0.50, mode <strong>Per character</strong></td><td>$6.50</td></tr><tr><td><strong>Price</strong> $5.00, mode <strong>Default</strong></td><td>$5.00 whatever they type</td></tr><tr><td><strong>Price</strong> $5.00, mode <strong>One time charge</strong></td><td>$5.00 even if they buy three bracelets</td></tr></tbody></table>

Pair **Per character** with a **Max character** so the charge has a ceiling. See [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md).

## Personalizer Settings

Text is fully supported by the live preview: the customer's words appear on the product photo as they type.

Its personalizer settings are colour, font size, font style, font family — default, a Google font, or one of your uploaded fonts — plus position, opacity, rotation, five text effects, a clip area, and which transformations the customer may apply.

Two settings are specific to Text and Number, because they are single-line: **Curve**, which bends the text along an arc, and **Auto-fit max width**, which shrinks the font when the text gets too long for the space. See [Curve and auto-fit width](../../personalizer/layer-settings/curve-and-auto-fit.md).

Full detail: [Product Personalizer](../../personalizer/README.md).

## Examples

**Engraving with a hard limit**

<table><thead><tr><th width="270">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Engraving text</code></td></tr><tr><td>Max character</td><td><code>15</code></td></tr><tr><td>Character counter</td><td><strong>Show</strong></td></tr><tr><td>Allowed value</td><td><strong>Letters &amp; numbers</strong></td></tr><tr><td>Text transform</td><td><strong>Capitalized</strong></td></tr><tr><td>Price</td><td><strong>Add price</strong> $5.00, mode <strong>Default</strong></td></tr><tr><td>Help text</td><td><code>Up to 15 letters and numbers. Engraved items cannot be returned.</code></td></tr></tbody></table>

**Two initials for a monogram**

Min character `2`, max character `3`, **Text transform** UPPERCASE, **Allowed value** Letters, required on.

**A team number on a jersey**

Max character `2`, **Allowed value** Letters & numbers, placeholder `10`, **Column width** 25% so it sits beside the name field.

## Notes
* Available on all plans.
* Works in Shopify POS.
* Character limits count spaces and punctuation.
* Validation runs on **Add to cart**, not while typing — the counter is what gives live feedback.
* An empty non-required Text option submits nothing, and no empty line appears on the order.
