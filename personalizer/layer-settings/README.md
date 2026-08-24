---
description: >-
  Every setting on a layer's Personalizer Settings tab, explained once — styling,
  placement, boundaries, and what the shopper may change.
icon: layer-group
---

# Layer settings

Once the Personalizer is on for an option, everything else you configure belongs to its **layer** — the thing drawn on the product photo.

These pages document those settings. [Set up the Personalizer](../setup.md) is the procedure; these are the details.

## How to find a setting

<table><thead><tr><th width="330">Setting</th><th>Page</th></tr></thead><tbody><tr><td><strong>Color</strong>, <strong>Font size</strong>, <strong>Font style</strong>, <strong>Text alignment</strong></td><td><a href="text-layers.md">Text layers</a></td></tr><tr><td><strong>Font</strong>, Google fonts, custom fonts</td><td><a href="fonts.md">Fonts</a></td></tr><tr><td><strong>Effect</strong>, <strong>Stroke color</strong>, <strong>Effect width</strong>, <strong>Shadow X-Axis</strong>, <strong>Shadow Y-Axis</strong></td><td><a href="effects.md">Text effects</a></td></tr><tr><td><strong>X-Axis</strong>, <strong>Y-Axis</strong>, <strong>Width</strong>, <strong>Height</strong>, <strong>Opacity</strong>, <strong>Rotation</strong></td><td><a href="position-size-rotation.md">Position, size, and rotation</a></td></tr><tr><td><strong>Curve</strong> (<strong>Arc</strong>), <strong>Auto-fit max width</strong></td><td><a href="curve-and-auto-fit.md">Curve and auto-fit width</a></td></tr><tr><td><strong>Enable clip area</strong>, clip width, height, position, rotation, and hiding</td><td><a href="clip-area.md">Clip area</a></td></tr><tr><td><strong>Image shape</strong>, <strong>Background mode</strong></td><td><a href="image-layers.md">Image layers</a></td></tr><tr><td><strong>Allow customers to</strong> — drag, resize, rotate</td><td><a href="customer-controls.md">Customer controls</a></td></tr></tbody></table>

## Which settings a layer has

A layer is either **text** or an **image**, and that decides most of what you see. The full grid is in [Set up the Personalizer](../setup.md#what-you-get-by-option-type); the short version:

<table><thead><tr><th width="230">Layer</th><th width="250">Comes from</th><th>Gets</th></tr></thead><tbody><tr><td><strong>Text</strong></td><td><a href="../../option-types/input-types/text.md">Text</a>, <a href="../../option-types/input-types/textarea.md">Textarea</a>, <a href="../../option-types/input-types/number.md">Number</a></td><td>Colour, size, style, font, effects. Curve and auto-fit on Text and Number; alignment, width, and height on Textarea</td></tr><tr><td><strong>Image</strong></td><td><a href="../../option-types/input-types/file-upload.md">File upload</a> and eight selection types</td><td>Shape and fit mode, width and height</td></tr></tbody></table>

Both kinds share position, opacity, rotation, a clip area, and customer controls.

{% hint style="warning" %}
Two settings are worth reading before the others, because they are what stops a design arriving unproducible:

* [Auto-fit max width](curve-and-auto-fit.md#auto-fit-max-width), so long text shrinks instead of running off the product.
* [Clip area](clip-area.md), so a layer the shopper can move cannot be moved somewhere you cannot print. Any [customer control](customer-controls.md) needs one.
{% endhint %}

## Settings are per option

The same option type can be configured completely differently in two places — a `Name` text layer in cursive across the front, a `Date` text layer small and straight underneath. Nothing here is store-wide.

The background, by contrast, is shared by every layer in the option set. See [Choosing the background](../setup.md#choosing-the-background).
