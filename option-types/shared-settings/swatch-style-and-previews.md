---
description: >-
  Display option values as colors or images, set swatch and tooltip sizes, and
  preview colors and fonts before the customer selects them.
icon: palette
---

# Swatch style and previews

These settings control how option values are displayed, and how much detail a customer can see before selecting one.

Set **Swatch style** first. It changes which columns appear in the option values table.

## Swatch style

**Swatch style** displays option values as text, colors, or images.

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Depends on the option type</td></tr><tr><td>Available on</td><td>Checkbox, Radio button, Button, Dropdown, Color dropdown, Color swatch</td></tr></tbody></table>

The available styles depend on the option type.

<table><thead><tr><th width="230">Option type</th><th>Available styles</th><th>Default</th></tr></thead><tbody><tr><td>Checkbox, Radio button</td><td>Default, Color, Image</td><td><strong>Default</strong></td></tr><tr><td>Button, Dropdown</td><td>Default, Image</td><td><strong>Default</strong></td></tr><tr><td>Color dropdown, Color swatch</td><td>Color, Image</td><td><strong>Color</strong></td></tr><tr><td>Image dropdown, Image swatch</td><td>Always images</td><td>Not applicable</td></tr></tbody></table>

**Default**

The option values are displayed as text, using the option type's standard appearance.

No extra column is added to the option values table.

**Color**

Each option value displays a color chip.

A **Color** column is added to the option values table. For each value, you can set one color, or two colors to create a split swatch.

**Image**

Each option value displays an image.

An **Image** column is added to the option values table. For each value, you can upload an image or select one of the product's existing images.

{% hint style="warning" %}
Changing **Swatch style** changes the columns in the option values table. Select the style before you enter your option values.
{% endhint %}

The option type still controls the selection behavior. A Checkbox set to **Color** displays color swatches and allows multiple selections. A Radio button set to **Color** allows one selection.

If you want a swatch layout from the start, use the [Color swatch](../selection-types/color-swatch.md) or [Image swatch](../selection-types/image-swatch.md) option type. These types also include the sizing and slider settings described below.

## Swatch image width and height

Sets the display size of each swatch image.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><code>60</code> pixels each</td></tr><tr><td>Available on</td><td>Image swatch</td></tr></tbody></table>

Both values are in pixels and affect the display size only. The uploaded image file is not changed.

**Swatch image width** and **Swatch image height** are set separately, so you can display rectangular swatches for products such as fabric strips or nameplates.

Larger swatches are easier to see on mobile, but they increase the height of the option.

<table><thead><tr><th width="290">Type of value</th><th>Suggested size</th></tr></thead><tbody><tr><td>Color or material chips</td><td><code>40</code>–<code>60</code></td></tr><tr><td>Patterns or prints with fine detail</td><td><code>80</code>–<code>120</code></td></tr><tr><td>Product photos used as values</td><td><code>120</code> or more</td></tr><tr><td>Long lists with many values</td><td>Smaller sizes, with a tooltip</td></tr></tbody></table>

If you need large swatches and many values, use a [slider or collapsible layout](collapsible-layouts-and-sliders.md).

## Tooltip style

Sets what is displayed when a customer hovers over a swatch.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>Text</strong></td></tr><tr><td>Available on</td><td>Image swatch</td></tr></tbody></table>

<table><thead><tr><th width="290">Value</th><th>Displays on hover</th></tr></thead><tbody><tr><td><strong>Text</strong></td><td>The option value name</td></tr><tr><td><strong>Text &#x26; image</strong></td><td>The option value name and a larger version of the image</td></tr></tbody></table>

**Text**

Displays the option value name only.

**Text & image**

Displays the option value name and an enlarged version of the swatch image.

Selecting **Text & image** displays two additional settings, **Tooltip image width** and **Tooltip image height**. Both are `150` pixels by default and control the size of the enlarged image only.

Use this when an option has many values and customers still need to see detail. Keep the swatches small to reduce the height of the option, and use the tooltip to display the larger image.

{% hint style="warning" %}
Tooltips are displayed on hover, which is not available on touch devices. Do not use tooltips for information that mobile customers need. Add that information to the option value's help text instead.
{% endhint %}

Tooltips are also controlled store-wide by **Show tooltip when hovering over options** under **Settings > Settings > General**. See [Widget behavior](../../storefront/widget-behavior.md).

## Color preview

Displays a preview of the color the customer selected or entered.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Off</td></tr><tr><td>Available on</td><td>Color picker, Color dropdown, Color swatch</td></tr></tbody></table>

When enabled, the **Select text box** setting is displayed. Use it to select one of the text options in the same option set. The text the customer enters in that option is then previewed in the selected color.

Use this for engraved or printed text where the color is a separate option.

To draw the customer's text onto the product image, use the [Personalizer](../../personalizer/README.md) instead.

## Font preview

Displays each font in the list using that font.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Off</td></tr><tr><td>Available on</td><td>Font picker</td></tr></tbody></table>

When enabled, each font name is rendered in its own font, so customers can see the font before selecting it.

The browser loads every font in the list, so a list with many fonts takes longer to display. Include only the fonts you can produce.

For more information, see:

* [Font picker](../selection-types/font-picker.md)
* [Working with option values](../../option-sets/option-values.md)
* [Collapsible layouts and sliders](collapsible-layouts-and-sliders.md)

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Swatch style setting on a Checkbox option"><figcaption><p>Swatch style options for a Checkbox option.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Image swatch tooltip displaying an enlarged image"><figcaption><p>A Text &#x26; image tooltip displaying an enlarged swatch image.</p></figcaption></figure>
