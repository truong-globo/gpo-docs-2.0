---
description: Five text effects — stroke, two neon styles, and emboss — with the settings each one reveals.
icon: sparkles
---

# Text effects

**Custom Effect** applies a visual treatment to a text layer. Used well it makes a preview look like a real engraved or printed product; used carelessly it makes it look like a word-processor.

**Applies to:** [Text](../../option-types/input-types/text.md), [Textarea](../../option-types/input-types/textarea.md), [Number](../../option-types/input-types/number.md).

## The five effects

<table><thead><tr><th width="200">Effect</th><th width="290">Appearance</th><th>Reveals</th></tr></thead><tbody><tr><td><strong>No effect</strong></td><td>Plain text. The default</td><td>Nothing</td></tr><tr><td><strong>Stroke</strong></td><td>An outline around each letter</td><td><strong>Stroke Color</strong>, <strong>Effect width</strong></td></tr><tr><td><strong>Neon Light 1</strong></td><td>A glowing outline</td><td>Nothing</td></tr><tr><td><strong>Neon Light 2</strong></td><td>A second glow treatment</td><td>Nothing</td></tr><tr><td><strong>Emboss</strong></td><td>A raised or pressed look, using a shadow</td><td><strong>Shadow X-Axis</strong>, <strong>Shadow Y-Axis</strong></td></tr></tbody></table>

<!-- SCREENSHOT: pp-effects | App admin → builder → option Text → Personalizer Settings | Custom Effect với 5 lựa chọn dạng image button | Khoanh nhóm Custom Effect -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The Custom Effect setting showing the five available text effects"><figcaption><p>Each effect is previewed as you select it, so choose by eye.</p></figcaption></figure>

## Stroke

An outline in a colour of your choosing.

<table><thead><tr><th width="230">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Stroke Color</strong></td><td>A pink</td><td>The outline colour</td></tr><tr><td><strong>Effect width</strong></td><td><code>1</code> px</td><td>How thick the outline is. Adjustable in tenths</td></tr></tbody></table>

**What it is actually good for**

The obvious use is a decorative outline. The much more useful one is **legibility over a photograph**: light text with a thin dark stroke stays readable over an uploaded photo of any brightness.

If you let customers upload their own images and draw text over them, a stroke is close to essential — you cannot know whether their photo will be light or dark.

Keep **Effect width** low. Above about `2` on typical text the outline starts to dominate the letterforms.

## Neon Light 1 and Neon Light 2

Two glow treatments, with no further settings — what you see in the preview is what you get.

They suit products that genuinely glow: LED signs, acrylic light panels, neon-style displays. On an engraved metal bracelet a glow looks like a mistake.

Choose between them by eye against your own background. They differ in the character of the glow.

## Emboss

A raised or pressed appearance, produced with a shadow you position.

<table><thead><tr><th width="230">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Shadow X-Axis</strong></td><td><code>1</code> px</td><td>Horizontal shadow offset, from -100 to 100</td></tr><tr><td><strong>Shadow Y-Axis</strong></td><td><code>1</code> px</td><td>Vertical shadow offset, from -100 to 100</td></tr></tbody></table>

**Getting it convincing**

The shadow offset is a lighting direction. Small values look like a physical impression; large values look like a drop shadow, which is a different and less convincing effect.

<table><thead><tr><th width="290">Effect wanted</th><th>Try</th></tr></thead><tbody><tr><td>Pressed into the surface — debossed</td><td>Small positive values, around <code>1</code> to <code>2</code></td></tr><tr><td>Raised off the surface — embossed</td><td>Small negative values</td></tr><tr><td>Matching your photograph's lighting</td><td>Offset in the same direction as the shadows already in the image</td></tr></tbody></table>

Match the direction to your product photograph. If the light in your photo comes from the top left, the shadow should fall to the bottom right.

## Choosing an effect

<table><thead><tr><th width="290">Product</th><th>Effect</th></tr></thead><tbody><tr><td>Engraved metal or wood</td><td><strong>Emboss</strong> with small offsets, or <strong>No effect</strong></td></tr><tr><td>Printed text on fabric or paper</td><td><strong>No effect</strong></td></tr><tr><td>Text over a customer's uploaded photo</td><td><strong>Stroke</strong>, thin, in a contrasting colour</td></tr><tr><td>LED or acrylic light products</td><td><strong>Neon Light 1</strong> or <strong>Neon Light 2</strong></td></tr><tr><td>Vinyl or sticker lettering</td><td><strong>Stroke</strong> matching your cut outline</td></tr><tr><td>Embroidery</td><td><strong>No effect</strong>, with a font that suits stitching</td></tr></tbody></table>

{% hint style="info" %}
The best effect is usually the one that most closely matches what you produce, not the one that looks most impressive in the builder. A shopper who sees a glowing preview and receives flat engraving is disappointed, even though the engraving is exactly what they ordered.
{% endhint %}

## Notes

* One effect per layer.
* Effects apply to the whole layer, not to part of the text.
* Effects are drawn on top of the layer's [Text color](text-layers.md#text-color), so the two interact — check them together.
* Effects have no bearing on production. They change the preview only.
* Very thick strokes and large shadows on a long entry cost more to render, which is noticeable on older phones.

## Troubleshooting

<details>
<summary>The stroke settings are not there</summary>

They appear only when **Custom Effect** is set to **Stroke**.
</details>

<details>
<summary>The shadow settings are not there</summary>

They appear only when **Custom Effect** is set to **Emboss**.
</details>

<details>
<summary>The stroke swamps the text</summary>

Reduce **Effect width**. Below `1` is possible, in tenths.
</details>

<details>
<summary>Emboss looks like a drop shadow</summary>

The offsets are too large. Bring them close to `1`.
</details>

<details>
<summary>The effect makes the text unreadable</summary>

Check the effect colour against the text colour and the background together. A stroke close in colour to the text makes it look blurred.
</details>

<details>
<summary>The preview looks different on the storefront</summary>

Compare on the same background. If it genuinely differs, check the option set was saved.
</details>
