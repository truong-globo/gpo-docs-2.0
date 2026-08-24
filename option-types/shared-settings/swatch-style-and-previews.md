---
description: >-
  Swatch style, swatch and tooltip image sizes, and the colour and font preview
  settings that let a shopper see a choice before making it.
icon: palette
---

# Swatch style and previews

These settings decide whether a choice is shown as text, as a colour, or as a picture — and how big that picture is when the shopper looks closely.

## Swatch style

Turns a plain list of choices into colour or image swatches.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Depends on the type — see the table below</td></tr><tr><th>Available on</th><td>Checkbox, Radio button, Button, Dropdown, Color dropdown, Color swatch</td></tr></thead></table>

The choices offered differ by type, because some types already imply a style:

<table><thead><tr><th width="230">Type</th><th width="290">Choices</th><th>Default</th></tr></thead><tbody><tr><td>Checkbox, Radio button</td><td><strong>Default</strong>, <strong>Color</strong>, <strong>Image</strong></td><td><strong>Default</strong></td></tr><tr><td>Button, Dropdown</td><td><strong>Default</strong>, <strong>Image</strong></td><td><strong>Default</strong></td></tr><tr><td>Color dropdown, Color swatch</td><td><strong>Color</strong>, <strong>Image</strong></td><td><strong>Color</strong></td></tr><tr><td>Image dropdown, Image swatch</td><td colspan="2">No choice — always images</td></tr></tbody></table>

**What each choice does**

<table><thead><tr><th width="180">Choice</th><th>Result</th><th>Values table gains</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>Text only, in the type's normal appearance</td><td>Nothing</td></tr><tr><td><strong>Color</strong></td><td>Each value shows a colour chip</td><td>A <strong>Color</strong> column, where you set one colour or two for a split swatch</td></tr><tr><td><strong>Image</strong></td><td>Each value shows a picture</td><td>An <strong>Image</strong> column, where you upload an image or reuse one of the product's own images</td></tr></tbody></table>

Changing the style changes the columns in the option values table, so set the style first and then fill in the values. See [Working with option values](../../option-sets/option-values.md).

{% hint style="info" %}
This means a **Checkbox** can look like a row of colour swatches, and a **Button** can look like a row of images. The type controls the selection behaviour; **Swatch style** controls the appearance. If a swatch layout is what you want from the start, use [Color swatch](../selection-types/color-swatch.md) or [Image swatch](../selection-types/image-swatch.md), which are built for it.
{% endhint %}

## Swatch image width and height

The size each swatch image is displayed at.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><code>60</code> px each</td></tr><tr><th>Available on</th><td>Image swatch</td></tr></thead></table>

**How it behaves**

* Values are in pixels and control display size, not the uploaded file.
* Width and height are independent, so you can make swatches rectangular for non-square products — a fabric strip or a nameplate.
* Larger swatches read better on mobile but push the **Add to cart** button further down the page. If you need many large swatches, pair them with a [slider or collapsible layout](collapsible-layouts-and-sliders.md).

**Rough guidance**

<table><thead><tr><th width="230">Situation</th><th>Size</th></tr></thead><tbody><tr><td>Colour or material chips</td><td><code>40</code>–<code>60</code></td></tr><tr><td>Pattern or print swatches where detail matters</td><td><code>80</code>–<code>120</code></td></tr><tr><td>Product photographs as choices</td><td><code>120</code>+, with a slider layout</td></tr><tr><td>Long lists, many values</td><td>Smaller, plus a <a href="#tooltip-style">tooltip</a> with a zoomed image</td></tr></tbody></table>

## Tooltip style

What the shopper sees when they hover a swatch.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Text</strong></td></tr><tr><th>Available on</th><td>Image swatch</td></tr></thead></table>

<table><thead><tr><th width="200">Choice</th><th>Shows on hover</th></tr></thead><tbody><tr><td><strong>Text</strong></td><td>The value's name</td></tr><tr><td><strong>Text &amp; image</strong></td><td>The value's name plus a larger version of the swatch image</td></tr></tbody></table>

Choosing **Text & image** reveals two more settings, **Tooltip image width** and **Tooltip image height**, both `150` px by default. They control the size of the zoomed image only.

This pairing is the answer to "I want lots of choices *and* I want shoppers to see the detail": keep the swatches small so the list stays compact, and let the tooltip do the zooming.

{% hint style="warning" %}
Hover does not exist on touch devices the way it does with a mouse. Do not rely on a tooltip to carry information a mobile shopper needs — put that in the value's own help text instead. See [Working with option values](../../option-sets/option-values.md).
{% endhint %}

Whether swatch tooltips appear at all is also controlled store-wide by **Show tooltip when hovering over options** in **Settings > Settings > General**. See [Widget behavior](../../storefront/widget-behavior.md).

## Color preview

Adds a live preview of the colour the shopper has chosen or entered.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td>Off</td></tr><tr><th>Available on</th><td>Color picker, Color dropdown, Color swatch</td></tr></thead></table>

Turning it on reveals **Select text box**, where you choose which of the option set's other text options the preview applies to.

That combination is what makes "see your text in the colour you picked" work: the shopper picks a colour, and the text they typed elsewhere in the form is previewed in it. Use it for engraved or printed text where the ink colour is a separate choice.

For drawing the customer's text onto the product photo itself, use the [Personalizer](../../personalizer/README.md) rather than this setting.

## Font preview

Renders each font in the list in that font, so the shopper can see it before choosing.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td>Off</td></tr><tr><th>Available on</th><td>Font picker</td></tr></thead></table>

Turn it on for any font picker. A list of font names in a single typeface asks the shopper to imagine the result; a list where each name is drawn in its own font does not.

The trade-off is that the browser loads each font in the list, so a picker with thirty fonts is slower to render. Keep the list to the fonts you can actually produce.

See [Font picker](../selection-types/font-picker.md).

<!-- SCREENSHOT: type-shared-swatch-style | App admin → builder → option Checkbox | Swatch style ở Basic Settings với 3 lựa chọn Default / Color / Image | Khoanh field Swatch style -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The Swatch style setting on a Checkbox option offering Default, Color, and Image"><figcaption><p>Swatch style changes both the storefront appearance and the values table.</p></figcaption></figure>

<!-- SCREENSHOT: type-shared-tooltip-zoom | Storefront → trang sản phẩm | Hover 1 image swatch, tooltip Text & image hiện ảnh phóng to | Khoanh tooltip -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An image swatch hovered on the storefront showing a zoomed tooltip image"><figcaption><p>Text &#x26; image tooltips let small swatches carry large detail.</p></figcaption></figure>
