---
description: Alignment, tooltips, showing the selected value, and limiting the widget's height.
icon: sliders
---

# Widget behavior

Four settings in **Settings** > **Settings** > **General** > **Widget Settings** that change how the widget behaves rather than how it looks. All store-wide.

## Alignment

<table><thead><tr><th width="180">Tab</th><td>General &gt; Widget Settings</td></tr><tr><th>Default</th><td><strong>Left</strong></td></tr></thead></table>

<table><thead><tr><th width="230">Choice</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>Left</strong></td><td>Left-aligned. Correct for left-to-right languages</td></tr><tr><td><strong>Center</strong></td><td>Centred, in either reading direction</td></tr><tr><td><strong>Right</strong></td><td>Right-aligned without changing reading direction</td></tr><tr><td><strong>Right to left</strong></td><td>Full right-to-left layout, for Arabic and Hebrew storefronts</td></tr></tbody></table>

**Right to left** is the important one — it flips the whole widget's layout, not just its text alignment. See [Right-to-left and non-Latin text](../translations/rtl-and-non-latin.md).

## Show tooltip when hovering over options

<table><thead><tr><th width="180">Default</th><td>On</td></tr></thead></table>

Shows the option value's name when a shopper hovers a swatch. Without it, swatch names are invisible.

Leave it on. A grid of colour chips with no names forces shoppers to guess, and it is the only way they can find out what "the third green one" is called.

Related: [Image swatch](../option-types/selection-types/image-swatch.md) can also show a zoomed image in its tooltip, controlled per option. See [Tooltip style](../option-types/shared-settings/swatch-style-and-previews.md#tooltip-style).

{% hint style="warning" %}
Hover does not exist in the same way on touch devices. Anything a mobile shopper must know belongs in per-value help text rather than a tooltip. See [Working with option values](../option-sets/option-values.md).
{% endhint %}

## Display selected value next to label

<table><thead><tr><th width="180">Default</th><td>On</td></tr></thead></table>

Shows the chosen value beside the option's label — `Colour: Sage` rather than just `Colour`.

Worth keeping on, especially for swatches. It gives the shopper a written confirmation of what they picked, which a highlighted chip alone does not, and it is the easiest way for them to check their choices before adding to cart.

## Limit widget height

<table><thead><tr><th width="180">Default</th><td>Off</td></tr></thead></table>

Turning it on reveals **Fixed height**, a value in pixels. The widget is capped at that height and scrolls inside it.

<table><thead><tr><th width="290">Use it when</th><th>Avoid it when</th></tr></thead><tbody><tr><td>A very long option set pushes <strong>Add to cart</strong> far down the page</td><td>The widget is a reasonable length already</td></tr><tr><td>Your theme's layout needs a predictable height</td><td>You have not tried <a href="../option-types/static-types/section.md">Sections</a> and <a href="../conditional-logic/README.md">conditional logic</a> first</td></tr></tbody></table>

{% hint style="info" %}
This is a blunt instrument. A scrollbar inside a page that also scrolls is confusing, and shoppers miss options inside it — particularly on a phone.

Try these first: group options into collapsible [Sections](../option-types/static-types/section.md); reveal options only when relevant with [conditional logic](../conditional-logic/README.md); use [collapsible layouts or sliders](../option-types/shared-settings/collapsible-layouts-and-sliders.md) for long value lists; and set [column widths](../option-types/shared-settings/direction-width-and-css.md#column-width) so short fields share a row.

All four make the form genuinely shorter. A height limit only hides it.
{% endhint %}

<!-- SCREENSHOT: store-widget-behavior | App admin → Settings → General → Widget Settings | Alignment, Show tooltip, Display selected value, Limit widget height | Khoanh nhóm 4 setting -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The widget behaviour settings for alignment, tooltips, selected value, and height limit"><figcaption><p>Four behaviour settings, all store-wide.</p></figcaption></figure>

## Two more settings on the same page

Not strictly behaviour, but they live in the same section and are worth knowing:

<table><thead><tr><th width="290">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Auto-scroll to first error message</strong></td><td>Under <strong>Product page</strong>. On by default. Scrolls the page to the first problem when add to cart is blocked. Keep it on — without it a shopper sees nothing happen</td></tr><tr><td><strong>File preview</strong></td><td>Under <strong>Product page</strong>. Whether an uploaded image shows as a thumbnail or a link. See <a href="../option-types/input-types/file-upload.md">File upload</a></td></tr></tbody></table>

## Notes

* All store-wide, applying to every option set.
* Alignment cannot be set per language. For a store selling in both directions, use [custom CSS](custom-css.md).
* These are behaviour settings. Appearance is in **Design** — see [Colors](colors.md) and [Borders and typography](borders-and-typography.md).

## Troubleshooting

<details>
<summary>Swatch names do not appear on hover</summary>

Turn on **Show tooltip when hovering over options**. On a touch device, hover behaves differently — use per-value help text instead.
</details>

<details>
<summary>Shoppers cannot tell what they selected</summary>

Turn on **Display selected value next to label**, and make **Swatch border active** clearly distinct. See [Colors](colors.md#swatches).
</details>

<details>
<summary>The widget scrolls inside itself and shoppers miss options</summary>

Turn **Limit widget height** off, and shorten the form properly with sections and conditional logic.
</details>

<details>
<summary>The widget reads left to right on my Arabic storefront</summary>

Set **Alignment** to **Right to left**.
</details>

<details>
<summary>Add to cart is blocked and nothing seems to happen</summary>

Turn on **Auto-scroll to first error message** so the page moves to the problem.
</details>
