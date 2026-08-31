---
description: >-
  Display option values as colors or images, set swatch and tooltip sizes, and
  preview colors and fonts before the customer selects them.
icon: palette
---

# Swatch style and previews

These settings control how option values are displayed, and how much detail a customer can see before selecting one.

## Swatch style

Displays option values as text, colors, or images. Available under **Basic Settings**.

<table><thead><tr><th width="230">Value</th><th>Description</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>The values are displayed as text.</td></tr><tr><td><strong>Color</strong></td><td>Each value displays a color chip. Adds a <strong>Color</strong> column to the option values table.</td></tr><tr><td><strong>Image</strong></td><td>Each value displays an image. Adds an <strong>Image</strong> column to the option values table.</td></tr></tbody></table>

The available values depend on the option type. Color swatch and Color dropdown default to **Color**. Image swatch and Image dropdown always use images.

{% hint style="warning" %}
Changing **Swatch style** changes the columns in the option values table. Select the style before you enter your option values.
{% endhint %}

## Swatch image width and height

Sets the display size of each swatch image, in pixels. Both are `60` by default and are set separately, so swatches can be rectangular.

Larger swatches are easier to see on mobile, but they increase the height of the option. For many large swatches, use a [slider or collapsible layout](collapsible-layouts-and-sliders.md).

## Tooltip style

Sets what is displayed when a customer hovers over a swatch.

<table><thead><tr><th width="230">Value</th><th>Description</th></tr></thead><tbody><tr><td><strong>Text</strong> (default)</td><td>Displays the option value name.</td></tr><tr><td><strong>Text &#x26; image</strong></td><td>Displays the name and an enlarged image. Adds the <strong>Tooltip image width</strong> and <strong>Tooltip image height</strong> settings, both <code>150</code> px.</td></tr></tbody></table>

{% hint style="warning" %}
Tooltips are displayed on hover, which is not available on touch devices. Add information that mobile customers need to the option value's help text instead.
{% endhint %}

Tooltips are also controlled store-wide by **Show tooltip when hovering over options** under **Settings > Settings > General**.

## Color preview

Off by default. Displays a preview of the color the customer selected or entered.

When enabled, the **Select text box** setting appears. Use it to select a text option in the same option set. The text the customer enters there is previewed in the selected color.

To draw the customer's text onto the product image, use the [Personalizer](../../personalizer/README.md) instead.

## Font preview

Off by default. Displays each font name in its own font, so customers can see the font before selecting it.

The browser loads every font in the list, so a long list takes longer to display.

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Swatch style setting on a Checkbox option"><figcaption><p>Swatch style options for a Checkbox option.</p></figcaption></figure>
