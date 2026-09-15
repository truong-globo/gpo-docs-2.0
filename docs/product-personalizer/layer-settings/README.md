---
description: >-
  Every setting on a layer's Personalizer Settings tab, explained once — styling,
  placement, boundaries, and what the customer may change.
icon: layer-group
---

# Layer settings

When the Personalizer is enabled for an option, the remaining settings apply to its **layer**, which is the content drawn on the product photo.

These pages describe those settings. For the setup procedure, see [Set up the Personalizer](../setup.md).

## How to find a setting

<table><thead><tr><th width="330">Setting</th><th>Page</th></tr></thead><tbody><tr><td><strong>Color</strong>, <strong>Font size</strong>, <strong>Font style</strong>, <strong>Text alignment</strong></td><td><a href="text-layers.md">Text layers</a></td></tr><tr><td><strong>Font</strong>, Google fonts, custom fonts</td><td><a href="fonts.md">Fonts</a></td></tr><tr><td><strong>Effect</strong>, <strong>Stroke color</strong>, <strong>Effect width</strong>, <strong>Shadow X-Axis</strong>, <strong>Shadow Y-Axis</strong></td><td><a href="effects.md">Text effects</a></td></tr><tr><td><strong>X-Axis</strong>, <strong>Y-Axis</strong>, <strong>Width</strong>, <strong>Height</strong>, <strong>Opacity</strong>, <strong>Rotation</strong></td><td><a href="position-size-rotation.md">Position, size, and rotation</a></td></tr><tr><td><strong>Curve</strong> (<strong>Arc</strong>), <strong>Auto-fit max width</strong></td><td><a href="curve-and-auto-fit.md">Curve and auto-fit width</a></td></tr><tr><td><strong>Enable clip area</strong>, clip width, height, position, rotation, and hiding</td><td><a href="clip-area.md">Clip area</a></td></tr><tr><td><strong>Image shape</strong>, <strong>Background mode</strong></td><td><a href="image-layers.md">Image layers</a></td></tr><tr><td><strong>Allow customers to</strong> — drag, resize, rotate</td><td><a href="customer-controls.md">Customer controls</a></td></tr></tbody></table>

## Which settings a layer has

A layer is either **text** or an **image**, which determines most of the available settings. For the full table, see [Set up the Personalizer](../setup.md#what-you-get-by-option-type).

<table><thead><tr><th width="230">Layer</th><th width="250">Comes from</th><th>Gets</th></tr></thead><tbody><tr><td><strong>Text</strong></td><td><a href="../../option-types/input-types/text.md">Text</a>, <a href="../../option-types/input-types/textarea.md">Textarea</a>, <a href="../../option-types/input-types/number.md">Number</a></td><td>Color, size, style, font, effects. Curve and auto-fit on Text and Number; alignment, width, and height on Textarea</td></tr><tr><td><strong>Image</strong></td><td><a href="../../option-types/input-types/file-upload.md">File upload</a> and eight selection types</td><td>Shape and fit mode, width and height</td></tr></tbody></table>

Both types share position, opacity, rotation, a clip area, and customer controls.

{% hint style="warning" %}
Read these two settings first. They prevent a customer from submitting a design you cannot produce:

* [Auto-fit max width](curve-and-auto-fit.md#auto-fit-max-width) reduces the font size of long text instead of letting it extend past the product.
* [Clip area](clip-area.md) prevents the customer from moving a layer outside the printable area. Set one whenever you enable a [customer control](customer-controls.md).
{% endhint %}

## Settings are per option

The same option type can be configured differently in two places. For example, a `Name` text layer can use a script font across the front, while a `Date` text layer is small and straight below it. None of these settings are store-wide.

The background is shared by every layer in the option set. See [Choosing the background](../setup.md#choosing-the-background).
