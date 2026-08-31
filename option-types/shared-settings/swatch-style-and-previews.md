---
description: >-
  Swatch style, swatch and tooltip image sizes, and the color and font preview
  settings that let a shopper see a choice before making it.
icon: palette
---

# Swatch style and previews

Five settings that decide whether a choice appears as text, as a color, or as a picture — and how much detail the shopper can see before selecting.

**Swatch style** is the one to start with, because changing it also changes the columns in the option values table.

## Swatch style

Turns a plain list of choices into color or image swatches.

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Depends on the option type — see below</td></tr><tr><td>Available on</td><td>Checkbox, Radio button, Button, Dropdown, Color dropdown, Color swatch</td></tr></tbody></table>

The choices offered differ by type, because some types already imply a style:

<table><thead><tr><th width="230">Type</th><th width="290">Choices</th><th>Default</th></tr></thead><tbody><tr><td>Checkbox, Radio button</td><td><strong>Default</strong>, <strong>Color</strong>, <strong>Image</strong></td><td><strong>Default</strong></td></tr><tr><td>Button, Dropdown</td><td><strong>Default</strong>, <strong>Image</strong></td><td><strong>Default</strong></td></tr><tr><td>Color dropdown, Color swatch</td><td><strong>Color</strong>, <strong>Image</strong></td><td><strong>Color</strong></td></tr><tr><td>Image dropdown, Image swatch</td><td colspan="2">No choice — always images</td></tr></tbody></table>

**What each choice does**

<table><thead><tr><th width="180">Choice</th><th>Result</th><th>Values table gains</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>Text only, in the type's normal appearance</td><td>Nothing</td></tr><tr><td><strong>Color</strong></td><td>Each value shows a color chip</td><td>A <strong>Color</strong> column, where you set one color, or two for a split swatch</td></tr><tr><td><strong>Image</strong></td><td>Each value shows a picture</td><td>An <strong>Image</strong> column, where you upload an image or reuse one of the product's own images</td></tr></tbody></table>

**How it behaves**

* Set the style before filling in your values. Changing it afterwards changes which columns the values table has. See [Working with option values](../../option-sets/option-values.md).
* The option type still controls the selection behavior. A **Checkbox** set to **Color** is a row of color swatches that allows multiple selections; a **Radio button** set to **Color** allows one.

{% hint style="info" %}
If a swatch layout is what you want from the start, use [Color swatch](../selection-types/color-swatch.md) or [Image swatch](../selection-types/image-swatch.md) instead. They are built for it and offer the sizing and slider settings below, which Checkbox and Radio button do not.
{% endhint %}

## Swatch image width and height

The size each swatch image is displayed at.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><code>60</code> px each</td></tr><tr><td>Available on</td><td>Image swatch</td></tr></tbody></table>

**How it behaves**

* Values are in pixels, and control display size only. The uploaded file is unchanged.
* Width and height are independent, so swatches can be rectangular for non-square products such as a fabric strip or a nameplate.
* Larger swatches read better on mobile, but push the **Add to cart** button further down the page.

**Typical sizes**

<table><thead><tr><th width="230">Situation</th><th>Size</th></tr></thead><tbody><tr><td>Color or material chips</td><td><code>40</code>–<code>60</code></td></tr><tr><td>Patterns or prints where detail matters</td><td><code>80</code>–<code>120</code></td></tr><tr><td>Product photographs used as choices</td><td><code>120</code> or more, with a slider layout</td></tr><tr><td>Long lists with many values</td><td>Smaller, plus a tooltip that zooms</td></tr></tbody></table>

For many large swatches, pair the size with a [slider or collapsible layout](collapsible-layouts-and-sliders.md) so the list stays compact.

## Tooltip style

What the shopper sees when they hover over a swatch.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>Text</strong></td></tr><tr><td>Available on</td><td>Image swatch</td></tr></tbody></table>

<table><thead><tr><th width="200">Choice</th><th>Shows on hover</th></tr></thead><tbody><tr><td><strong>Text</strong></td><td>The value's name</td></tr><tr><td><strong>Text &#x26; image</strong></td><td>The value's name plus a larger version of the swatch image</td></tr></tbody></table>

**How it behaves**

* **Text & image** reveals **Tooltip image width** and **Tooltip image height**, both `150` px by default. They size the zoomed image only, not the swatch.
* Whether tooltips appear at all is also controlled store-wide by **Show tooltip when hovering over options** in **Settings > Settings > General**. See [Widget behavior](../../storefront/widget-behavior.md).

**When to use it**

Use **Text & image** when you need a long list of choices and shoppers still need to see detail: keep the swatches small so the list stays short, and let the tooltip do the zooming.

{% hint style="warning" %}
Hover does not exist on touch devices. Do not put information a mobile shopper needs into a tooltip — put it in the value's own help text instead. See [Working with option values](../../option-sets/option-values.md).
{% endhint %}

## Color preview

Shows a live preview of the color the shopper picked or entered.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Off</td></tr><tr><td>Available on</td><td>Color picker, Color dropdown, Color swatch</td></tr></tbody></table>

**How it behaves**

Turning it on reveals **Select text box**, where you choose one of the option set's text options. The text the shopper typed into that option is then previewed in the color they chose.

**When to use it**

Engraved or printed text where the ink color is a separate choice. The shopper types their message in one option, picks a color in another, and sees the message in that color.

For drawing the shopper's text onto the product photo itself, use the [Personalizer](../../personalizer/README.md) rather than this setting.

## Font preview

Renders each font in the list in that font.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Off</td></tr><tr><td>Available on</td><td>Font picker</td></tr></tbody></table>

**When to use it**

Turn it on for any font picker. A list of font names in a single typeface asks the shopper to imagine the result; a list drawn in each font does not.

The trade-off is loading time: the browser loads every font in the list, so a picker with thirty fonts renders more slowly. Keep the list to fonts you can actually produce. See [Font picker](../selection-types/font-picker.md).

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The Swatch style setting on a Checkbox option offering Default, Color, and Image"><figcaption><p>Swatch style changes both the storefront appearance and the values table.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An image swatch hovered on the storefront showing a zoomed tooltip image"><figcaption><p>Text &#x26; image tooltips let small swatches carry large detail.</p></figcaption></figure>
