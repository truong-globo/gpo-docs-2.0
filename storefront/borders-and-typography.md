---
description: Border weight and corner radius for the three control families, and the four text styles.
icon: text-height
---

# Borders and typography

Two groups in **Settings** > **Settings** > **Design**. Both store-wide.

## Borders

Three control families, each with a size and a radius.

<table><thead><tr><th width="230">Family</th><th>Covers</th></tr></thead><tbody><tr><td><strong>Input</strong></td><td>Text fields, number fields, textareas</td></tr><tr><td><strong>Dropdown</strong></td><td>Dropdowns and select fields</td></tr><tr><td><strong>Swatch</strong></td><td>Colour and image swatches, and buttons</td></tr></tbody></table>

Each takes:

<table><thead><tr><th width="230">Value</th><th width="150">Default</th><th>What it does</th></tr></thead><tbody><tr><td>Size</td><td><code>1</code></td><td>Border thickness in pixels</td></tr><tr><td>Radius</td><td><code>2</code></td><td>Corner rounding in pixels</td></tr></tbody></table>

### Matching your theme

Border radius is the setting that most often gives away a widget as an add-on. A theme with fully rounded buttons and a widget with square fields looks wrong even when every colour matches.

<table><thead><tr><th width="290">Your theme's controls</th><th>Set radius to roughly</th></tr></thead><tbody><tr><td>Sharp, square corners</td><td><code>0</code></td></tr><tr><td>Slightly softened</td><td><code>2</code> to <code>4</code></td></tr><tr><td>Noticeably rounded</td><td><code>8</code> to <code>12</code></td></tr><tr><td>Pill-shaped</td><td>A large value, around <code>50</code></td></tr></tbody></table>

Copy the values from your theme's own settings rather than guessing.

A thicker **Swatch** border makes the selected state easier to see, which is worth a point or two on its own. See [Colors](colors.md#swatches).

## Typography

Four text styles, each with a font, a weight or variant, and a size.

<table><thead><tr><th width="230">Style</th><th>Applies to</th></tr></thead><tbody><tr><td><strong>Label text</strong></td><td>Option labels</td></tr><tr><td><strong>Main text</strong></td><td>What the customer types, and option values</td></tr><tr><td><strong>Help text</strong></td><td>Help text throughout</td></tr><tr><td>The fourth style</td><td>The add-on total line</td></tr></tbody></table>

Each style offers:

<table><thead><tr><th width="290">Control</th><th>What it does</th></tr></thead><tbody><tr><td>Font family</td><td>A font from the app's list</td></tr><tr><td>Font variant</td><td>The weight or style — regular, 600, and so on. The available variants depend on the font</td></tr><tr><td>Font size</td><td>In pixels</td></tr><tr><td>Custom font</td><td>Switch to one of your uploaded fonts instead. See <a href="../settings/custom-fonts.md">Custom fonts</a></td></tr></tbody></table>

### Getting typography right

{% stepper %}
{% step %}
### Use your theme's fonts, not similar ones

Two similar sans-serifs on one page look like a mistake. Match exactly, or use one font for everything.
{% endstep %}

{% step %}
### Make labels heavier than values

A heavier label and a regular value gives the form a clear reading order. That is why the label style starts at a heavier variant than the others.
{% endstep %}

{% step %}
### Keep help text smaller, but not too small

A point or two below the main text. Below about 12 pixels it stops being read at all, which defeats the purpose.
{% endstep %}

{% step %}
### Check non-Latin scripts

Many fonts have no Arabic, Hebrew, Thai, or CJK glyphs, and missing glyphs fall back to a system font. See <a href="../translations/rtl-and-non-latin.md">Right-to-left and non-Latin text</a>.
{% endstep %}

{% step %}
### Check on a phone

Text that is comfortable on a monitor can be tight on a phone.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: store-borders-typography | App admin → Settings → Design | Nhóm Border (3 family với size/radius) và nhóm Typography (4 style) | Khoanh 2 nhóm -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The border and typography settings groups in the Design tab"><figcaption><p>Three border families and four text styles, all store-wide.</p></figcaption></figure>

## Notes

* Both groups work alongside [Match theme style](match-your-theme-style.md) — use the switch as a base and adjust from here.
* Store-wide, with no per-option-set override. Use an [HTML class](../option-types/shared-settings/direction-width-and-css.md#html-class) and [custom CSS](custom-css.md) if you need one.
* The Personalizer's fonts are set per layer and are separate from these. See [Fonts](../personalizer/layer-settings/fonts.md).
* Custom fonts must be uploaded before they appear here. See [Custom fonts](../settings/custom-fonts.md).

## Troubleshooting

<details>
<summary>My font is not applying</summary>

Save, then reload a real product page — the builder preview uses the app's own styling. If it still does not apply, your theme's CSS may be more specific; override with [custom CSS](custom-css.md).
</details>

<details>
<summary>The variant I want is not listed</summary>

Variants depend on the font. Choose a font that has the weight you need, or upload it as a custom font.
</details>

<details>
<summary>Corners look wrong against my theme</summary>

Copy the radius from your theme's own settings rather than estimating.
</details>

<details>
<summary>Selected swatches are hard to see</summary>

Increase the **Swatch** border size and set a distinct **Swatch border active** colour.
</details>

<details>
<summary>Some characters render in a different font</summary>

The font lacks those glyphs. See [Right-to-left and non-Latin text](../translations/rtl-and-non-latin.md).
</details>
