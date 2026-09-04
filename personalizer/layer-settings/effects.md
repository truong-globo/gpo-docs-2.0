---
description: Five text effects — stroke, two neon styles, and emboss — with the settings each one reveals.
icon: sparkles
---

# Text effects

**Custom Effect** applies a visual treatment to a text layer. Select an effect that matches the product you produce.

**Applies to:** [Text](../../option-types/input-types/text.md), [Textarea](../../option-types/input-types/textarea.md), [Number](../../option-types/input-types/number.md).

## The five effects

<table><thead><tr><th width="200">Effect</th><th width="290">Appearance</th><th>Reveals</th></tr></thead><tbody><tr><td><strong>No effect</strong></td><td>Plain text. The default</td><td>Nothing</td></tr><tr><td><strong>Stroke</strong></td><td>An outline around each letter</td><td><strong>Stroke Color</strong>, <strong>Effect width</strong></td></tr><tr><td><strong>Neon Light 1</strong></td><td>A glowing outline</td><td>Nothing</td></tr><tr><td><strong>Neon Light 2</strong></td><td>A second glow treatment</td><td>Nothing</td></tr><tr><td><strong>Emboss</strong></td><td>A raised or pressed look, using a shadow</td><td><strong>Shadow X-Axis</strong>, <strong>Shadow Y-Axis</strong></td></tr></tbody></table>

<!-- SCREENSHOT: pp-effects | App admin → builder → option Text → Personalizer Settings | Custom Effect với 5 lựa chọn dạng image button | Khoanh nhóm Custom Effect -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The Custom Effect setting showing the five available text effects"><figcaption><p>Each effect is previewed as you select it, so choose by eye.</p></figcaption></figure>

## Stroke

An outline in a color you select.

<table><thead><tr><th width="230">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Stroke Color</strong></td><td>A pink</td><td>The outline color</td></tr><tr><td><strong>Effect width</strong></td><td><code>1</code> px</td><td>How thick the outline is. Adjustable in tenths</td></tr></tbody></table>

**When to use it**

A stroke can be decorative, but its main use is **legibility over a photograph**. Light text with a thin dark stroke remains readable over an uploaded photo of any brightness.

If customers upload their own images and you draw text over them, use a stroke. You cannot predict whether their photo will be light or dark.

Keep **Effect width** low. Above about `2`, the outline starts to obscure the letters.

## Neon Light 1 and Neon Light 2

Two glow treatments. Neither has additional settings.

Use them for products that emit light, such as LED signs, acrylic light panels, and neon-style displays. They are not suitable for engraved products.

The two effects differ in the appearance of the glow. Compare them against your own background image.

## Emboss

A raised or pressed appearance, created with a shadow you position.

<table><thead><tr><th width="230">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Shadow X-Axis</strong></td><td><code>1</code> px</td><td>Horizontal shadow offset, from -100 to 100</td></tr><tr><td><strong>Shadow Y-Axis</strong></td><td><code>1</code> px</td><td>Vertical shadow offset, from -100 to 100</td></tr></tbody></table>

**How to position the shadow**

The shadow offset sets the lighting direction. Small values produce a physical impression. Large values produce a drop shadow instead.

<table><thead><tr><th width="290">Effect wanted</th><th>Try</th></tr></thead><tbody><tr><td>Pressed into the surface — debossed</td><td>Small positive values, around <code>1</code> to <code>2</code></td></tr><tr><td>Raised off the surface — embossed</td><td>Small negative values</td></tr><tr><td>Matching your photograph's lighting</td><td>Offset in the same direction as the shadows already in the image</td></tr></tbody></table>

Match the direction to your product photo. If the light in the photo comes from the top left, set the shadow to fall to the bottom right.

## Choosing an effect

<table><thead><tr><th width="290">Product</th><th>Effect</th></tr></thead><tbody><tr><td>Engraved metal or wood</td><td><strong>Emboss</strong> with small offsets, or <strong>No effect</strong></td></tr><tr><td>Printed text on fabric or paper</td><td><strong>No effect</strong></td></tr><tr><td>Text over a customer's uploaded photo</td><td><strong>Stroke</strong>, thin, in a contrasting color</td></tr><tr><td>LED or acrylic light products</td><td><strong>Neon Light 1</strong> or <strong>Neon Light 2</strong></td></tr><tr><td>Vinyl or sticker lettering</td><td><strong>Stroke</strong> matching your cut outline</td></tr><tr><td>Embroidery</td><td><strong>No effect</strong>, with a font that suits stitching</td></tr></tbody></table>

{% hint style="info" %}
Select the effect that most closely matches what you produce. If a customer sees a glowing preview and receives flat engraving, the order is correct but the preview was misleading.
{% endhint %}

## Notes

* One effect per layer.
* Effects apply to the whole layer, not to part of the text.
* Effects are drawn on top of the layer's [Text color](text-layers.md#text-color), so check the two settings together.
* Effects apply to the preview only. They do not affect production.
* Thick strokes and large shadows on a long entry take longer to render, which is noticeable on older devices.
