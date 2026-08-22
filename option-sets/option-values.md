---
description: >-
  Adding, bulk-adding, reordering, and pricing the individual choices inside a
  selection option — plus the characters you cannot use.
icon: list-ul
---

# Working with option values

Selection-style options — dropdowns, radio buttons, checkboxes, buttons, swatches — are lists. Each entry in the list is an **option value**. This page covers everything that is true of option values whatever type they belong to.

Input-style options such as Text or Number have no option values, because the customer types instead of choosing.

## The option values table

When you select a selection-style option, its choices appear in a table. The columns you get depend on the option type.

<table><thead><tr><th width="170">Column</th><th>What it is</th></tr></thead><tbody><tr><td>Drag handle</td><td>Grab it and drag to reorder. The table order is the order shoppers see.</td></tr><tr><td><strong>Color</strong> / <strong>Image</strong></td><td>Only on swatch-style options. Set the colour or upload the image for that choice.</td></tr><tr><td><strong>Value</strong></td><td>The text of the choice. This is what shoppers read and what lands on the order.</td></tr><tr><td><strong>Price</strong></td><td>The add-on for this choice. Selecting the cell opens the add-on dialog with its three modes.</td></tr><tr><td><strong>Product</strong></td><td>Appears once the value is linked to an add-on product. Opens that product in Shopify admin.</td></tr><tr><td><strong>Action</strong></td><td>Add help text for this value, or delete the row.</td></tr></tbody></table>

Below the table are three controls: **Add value**, **Bulk add**, and **Delete all option values**.

<!-- SCREENSHOT: concept-ov-table | App admin → builder → 1 option kiểu Checkbox hoặc Dropdown | Bảng Option values đầy đủ cột + 3 nút Add value / Bulk add / Delete all option values | Khoanh hàng nút ở dưới bảng -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="An option values table with its columns and the Add value, Bulk add, and Delete all buttons below it"><figcaption><p>Every selection option is managed from this table.</p></figcaption></figure>

## The three rules for a value

{% hint style="warning" %}
**A value cannot be empty.**

**Values must be unique within the option.** The check ignores capitalisation and surrounding spaces, so `Red` and `red ` count as the same value.

**A value cannot contain any of these characters:** `,` `:` `"` `'` `|`
{% endhint %}

The reason for the character restriction is that values are packed into the order record alongside other data, and those characters are used as separators there.

The one exception is **Product links**, where values are products you pick rather than text you type, so the uniqueness check does not apply.

### Working around a blocked character

<table><thead><tr><th width="240">You wanted</th><th>Write this instead</th></tr></thead><tbody><tr><td><code>Blue, large</code></td><td><code>Blue - large</code> or <code>Blue / large</code></td></tr><tr><td><code>Size: XL</code></td><td><code>Size XL</code>, and put the word "Size" in the option's <strong>Label</strong></td></tr><tr><td><code>Men's</code></td><td><code>Mens</code></td></tr><tr><td><code>10" x 12"</code></td><td><code>10in x 12in</code></td></tr></tbody></table>

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

<!-- SCREENSHOT: concept-ov-bulk-add | App admin → builder → dialog Bulk Add Values | Textarea nhiều dòng giá trị + nút Select | Không khoanh (modal đơn) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Bulk Add Values dialog with several values pasted one per line"><figcaption><p>Bulk add takes one value per line and appends them to the existing list.</p></figcaption></figure>

### Starting over

**Delete all option values** empties the table. You are asked to confirm first.

{% hint style="danger" %}
Deleting values also removes their add-on prices, images, and help text. Any conditional logic rule that referenced a deleted value stops matching — check your rules afterwards. See [Troubleshooting conditional logic](../conditional-logic/troubleshooting.md).
{% endhint %}

## Ordering values

Drag rows by the handle on the left. The order in the table is exactly the order shoppers see, top to bottom or left to right depending on the option's layout.

Some orderings are worth thinking about:

* Put your most popular choice first — many shoppers take the first plausible option.
* For sizes, use natural order (`S`, `M`, `L`, `XL`), not alphabetical.
* Put free choices before paid ones so the cheapest option reads as the default.

## Help text on a value

Each value can carry its own short explanation, shown next to that choice rather than under the whole option. Use the **Action** column and select **Add help text**.

This is useful for explaining what a choice means or what it costs you in lead time — `Adds 3 working days`, for example.

Most selection types support per-value help text. **Select**, **Product links**, and **Tabs** support help text at the option level only.

## Pricing a value

Selecting the **Price** cell opens the add-on dialog, which offers three modes:

<table><thead><tr><th width="270">Mode</th><th>Use it when</th></tr></thead><tbody><tr><td><strong>Use existing product</strong></td><td>You already sell the thing. Price and stock come from that product's variant.</td></tr><tr><td><strong>Automatically generate product</strong></td><td>You want stock tracking without building a product by hand. The app creates one at the price you type.</td></tr><tr><td><strong>Add price</strong></td><td>You just want to add money. No product, no stock. Not supported on Shopify POS.</td></tr></tbody></table>

Values with no price are free.

See [Add-on pricing](../add-on-pricing/README.md) for all three in depth, and [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md) for how the charge scales with quantity.

## Colours and images on a value

Swatch-style options add a **Color** or **Image** column, controlled by the option's **Swatch style** setting:

* **Color** — pick one colour, or two for a split swatch.
* **Image** — upload an image, or reuse one of the product's own images.

See [Swatch style](../option-types/shared-settings/swatch-style-and-previews.md#swatch-style), [Color swatch](../option-types/selection-types/color-swatch.md), and [Image swatch](../option-types/selection-types/image-swatch.md).

## Translating values

If your storefront has more than one language, values can be translated per language using the language switcher in the builder. The **Name** of the option stays untranslated so your order records remain consistent.

See [Translate option content](../translations/translate-option-content.md).

## Troubleshooting

<details>
<summary>"Value must be unique"</summary>

Two rows have the same value once capitalisation and spaces are ignored. Look for a trailing space, or for `Red` and `RED` in the same table.
</details>

<details>
<summary>"Value can't contain any of the following characters , : " ' |"</summary>

Remove the character — see the substitutions table above. Commas and apostrophes are the usual culprits.
</details>

<details>
<summary>Bulk add refuses my whole list</summary>

One bad line blocks the entire paste. The error names the problem — a blocked character or a duplicate. Note that a duplicate can be against a value already in the table, not just within your pasted list.
</details>

<details>
<summary>My values are in the wrong order on the storefront</summary>

Storefront order follows table order exactly. Drag the rows into the order you want and save. If it looks scrambled, check whether you are looking at a slider layout, which lays values out in rows — see [Swatch slider](../option-types/shared-settings/collapsible-layouts-and-sliders.md#slider-settings).
</details>

<details>
<summary>A value is greyed out or crossed through on the storefront</summary>

That value is linked to an add-on product that is out of stock, and the option's **Out of stock options** setting decides how it looks. See [Out of stock options](../option-types/shared-settings/out-of-stock-options.md#out-of-stock-options).
</details>
