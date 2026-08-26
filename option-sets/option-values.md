---
description: >-
  Adding, bulk-adding, reordering, and pricing the individual choices inside a
  selection option — plus the characters you cannot use.
icon: list-ul
---

# Working with option values

Selection-style options — dropdowns, radio buttons, checkboxes, buttons, swatches — are lists. Each entry in the list is an **option value**. This page covers everything that is true of option values whatever type they belong to.

Input-style options such as Text or Number have no option values, because the customer types instead of choosing

## The three rules for a value

{% hint style="warning" %}
**A value cannot be empty.**

**Values must be unique within the option.** The check ignores capitalisation and surrounding spaces, so `Red` and `red` count as the same value.

**A value cannot contain any of these characters:** `,` `:` `"` `'` `|`
{% endhint %}

The reason for the character restriction is that values are packed into the order record alongside other data, and those characters are used as separators there.

The one exception is **Product links**, where values are products you pick rather than text you type, so the uniqueness check does not apply.

## Adding values

### One at a time

Select **Add value**. A new empty row is appended. Type the value, then set its price or image if it needs one.

### Many at once

Select **Bulk add**, then paste your list into the box — **one value per line**. Select **Select** and every line becomes a row, appended to whatever is already there.

Bulk add checks the whole list before it will accept it:

* Blank lines are ignored, and leading and trailing spaces are trimmed.
* If any line contains a blocked character, the whole paste is rejected with the reason.
* If any line duplicates another line, **or duplicates a value already in the table**, the paste is rejected.

Fix the reported problem in the box and it accepts immediately.

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Bulk Add Values dialog with several values pasted one per line"><figcaption><p>Bulk add takes one value per line and appends them to the existing list.</p></figcaption></figure>

## Help text on a value

Each value can carry its own short explanation, shown next to that choice rather than under the whole option. Use the **Action** column and select **Add help text**.

This is useful for explaining what a choice means or what it costs you in lead time — `Adds 3 working days`, for example.

Most selection types support per-value help text. **Select**, **Product links**, and **Tabs** support help text at the option level only.

## Pricing a value

Selecting the **Price** cell opens the add-on dialog, which offers three modes:

<table><thead><tr><th width="270">Mode</th><th>Use it when</th></tr></thead><tbody><tr><td><strong>Use existing product</strong></td><td>You already sell the thing. Price and stock come from that product's variant.</td></tr><tr><td><strong>Automatically generate product</strong></td><td>You want stock tracking without building a product by hand. The app creates one at the price you type.</td></tr><tr><td><strong>Add price</strong></td><td>You just want to add money. No product, no stock. Not supported on Shopify POS.</td></tr></tbody></table>

Values with no price are free.

See [Add-on pricing](../add-on-pricing/) for all three in depth, and [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md) for how the charge scales with quantity.

## Colours and images on a value

Swatch-style options add a **Color** or **Image** column, controlled by the option's **Swatch style** setting:

* **Color** — pick one colour, or two for a split swatch.
* **Image** — upload an image, or reuse one of the product's own images.

See [Swatch style](../option-types/shared-settings/swatch-style-and-previews.md#swatch-style), [Color swatch](../option-types/selection-types/color-swatch.md), and [Image swatch](../option-types/selection-types/image-swatch.md).

## Translating values

If your storefront has more than one language, values can be translated per language using the language switcher in the builder. The **Name** of the option stays untranslated so your order records remain consistent.

See [Translate option content](../translations/translate-option-content.md).
