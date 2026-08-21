---
description: A size table built from one of thirteen presets or from scratch, opened from a link on the product page.
icon: table-cells
---

# Size chart

A size table. Start from one of thirteen presets for common garment types, or build your own, and it opens from a link on the product page.

If you sell anything worn, this is the static type that most reduces returns.

## What customers see

A link with your chart header. Selecting it opens the table at the width you set.

<!-- SCREENSHOT: type-sizechart-storefront | Storefront → trang sản phẩm | Link mở size chart và bảng size đã mở | Khoanh link và bảng -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A size chart opened from a link on a storefront product page"><figcaption><p>A size chart in the option form, where the shopper is actually choosing a size.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Chart title</strong></td><td>The heading inside the chart. Starts as <code>Size chart</code>.</td></tr><tr><td><strong>Chart header</strong></td><td>The link text on the product page. Starts as <code>Size guides</code>.</td></tr><tr><td><strong>Chart content</strong></td><td>The table itself. Pick a preset or build your own — see below.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide the link.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Chart icon</strong></td><td>An icon beside the link, from the app's icon picker. A ruler is the obvious choice.</td></tr><tr><td><strong>Chart width</strong></td><td>The width of the opened chart in pixels. Starts at <code>600</code>.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and the width of the link, not the chart.</td></tr></tbody></table>

## The presets

Selecting a preset fills the table with a standard set of measurements for that garment type, which you then edit to your own sizing.

<table><thead><tr><th width="230">Preset</th><th width="230">Preset</th><th>Preset</th></tr></thead><tbody><tr><td>Blank</td><td>Men's Bottoms</td><td>Bra</td></tr><tr><td>Jacket</td><td>Women's Bottoms</td><td>Bikini</td></tr><tr><td>Men's Tops</td><td>Men's Shoes</td><td>Pet Clothing</td></tr><tr><td>Women's Tops</td><td>Women's Shoes</td><td>Pet Collar</td></tr><tr><td>Dress</td><td></td><td></td></tr></tbody></table>

**Blank** gives you an empty table to build from scratch.

{% hint style="warning" %}
A preset is a starting point, not your sizing. Replace every number with your own measurements — a chart that does not match what you ship causes the returns it was meant to prevent.
{% endhint %}

{% stepper %}
{% step %}
### Choose the closest preset

The table fills with that garment type's usual measurements.
{% endstep %}

{% step %}
### Replace the numbers with your own

Edit the cells directly in the table editor.
{% endstep %}

{% step %}
### Add or remove rows and columns

Match your real size range, and add any measurement your customers ask about — sleeve length, inside leg, chest at the widest point.
{% endstep %}

{% step %}
### Say which units you are using

Put it in the **Chart title** or in a header row. `Measurements in cm` removes the most common question.
{% endstep %}

{% step %}
### Check it on a phone

Wide tables are hard on small screens. If it is cramped, reduce the number of columns rather than the width.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: type-sizechart-presets | App admin → builder → option Size chart | Danh sách 13 preset dạng icon để chọn | Khoanh vùng chọn preset -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The size chart preset picker in the builder showing the garment type options"><figcaption><p>Thirteen presets, including Blank for building your own.</p></figcaption></figure>

## Where to put it

Directly beside the size option, not at the bottom of the form. A shopper deciding between M and L wants the chart in that moment, and will not scroll to find it.

Two arrangements that work:

* The size option, then the size chart link immediately below it.
* A collapsed [Section](section.md) labelled `Size guide` right after the size option.

## Examples

**A garment with your own sizing**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Chart header</td><td><code>Size guide</code></td></tr><tr><td>Chart title</td><td><code>Measurements in cm</code></td></tr><tr><td>Chart content</td><td>From the <strong>Women's Tops</strong> preset, edited to your sizing</td></tr><tr><td>Chart icon</td><td>A ruler</td></tr><tr><td>Chart width</td><td><code>700</code></td></tr></tbody></table>

**Two charts on one product**

One Size chart for clothing measurements and a second for shoe sizes, each shown by conditional logic depending on which product type the shopper picked.

**A pet product**

From the **Pet Collar** preset, with your own neck measurements and a note on how to measure.

## Limits and notes

* Available on the Advanced plan.
* Works in Shopify POS.
* Collects nothing, so it never reaches the cart or order.
* Content is translatable per storefront language — worth doing, since units differ by market. See [Translate option content](../../translations/translate-option-content.md).
* One table per Size chart option. For several tables, add several options and reveal them with conditional logic.

## Troubleshooting

<details>
<summary>Choosing a preset replaced what I had written</summary>

Presets fill the table. Choose the preset first, then edit.
</details>

<details>
<summary>The table is cramped on mobile</summary>

Reduce the number of columns. Width alone will not fix a table with eight measurements on a phone.
</details>

<details>
<summary>Shoppers still order the wrong size</summary>

Check the chart matches what you ship, state the units, and say how to measure. Also make sure the link sits beside the size option rather than at the bottom of the form.
</details>

<details>
<summary>I need two charts for different product types</summary>

Add two Size chart options and use conditional logic to show the right one.
</details>

<details>
<summary>Size chart is greyed out</summary>

It is on the Advanced plan. See [Compare plans](../../plans/compare-plans.md).
</details>

## Next steps

* [Pop-up modal](pop-up-modal.md) — for non-table content.
* [Tabs](tabs.md) — chart plus care plus delivery in one place.
* [Conditional logic](../../conditional-logic/README.md) — the right chart for the right product.
