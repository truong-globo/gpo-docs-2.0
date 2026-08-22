---
description: Colour, size, style, and alignment for text drawn on the product photo.
icon: font
---

# Text layers

A text layer draws what the customer typed onto the product image. These are the settings that decide how it looks.

**Applies to:** [Text](../option-types/input-types/text.md), [Textarea](../option-types/input-types/textarea.md), [Number](../option-types/input-types/number.md).

## The settings

<table><thead><tr><th width="230">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Text color</strong></td><td>Black</td><td>The colour the text is drawn in.</td></tr><tr><td><strong>Font size</strong></td><td><code>6</code></td><td>The size, on a scale from 0 to 50 relative to the image.</td></tr><tr><td><strong>Text alignment</strong></td><td><strong>Center</strong></td><td><strong>Left</strong>, <strong>Center</strong>, or <strong>Right</strong>. <strong>Textarea only.</strong></td></tr><tr><td><strong>Font style</strong></td><td><strong>Normal</strong></td><td><strong>Normal</strong>, <strong>Italic</strong>, or <strong>Bold</strong>.</td></tr><tr><td><strong>Font family</strong></td><td><strong>Default</strong></td><td><strong>Default</strong>, <strong>Google</strong>, or <strong>Custom</strong>. See <a href="fonts.md">Fonts</a>.</td></tr></tbody></table>

Everything else about a text layer lives on its own page: [effects](effects.md), [position, size and rotation](position-size-rotation.md), [curve and auto-fit](curve-and-auto-fit.md), [clip area](clip-area.md), and [customer controls](customer-controls.md).

<!-- SCREENSHOT: pp-text-layer-settings | App admin → builder → option Text → Personalizer Settings | Nhóm setting Text color, Font size, Font style, Font family | Khoanh nhóm này -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The text layer settings for colour, font size, font style, and font family"><figcaption><p>The first group on the Personalizer tab styles the text itself.</p></figcaption></figure>

## Font size

The scale runs 0 to 50 and is relative to the background image, not in points. That is deliberate — it means a layer keeps its proportions whatever size the image is displayed at, from a phone to a large monitor.

The default of `6` is a starting point, not a recommendation. What you actually need depends on how much of the image the personalisation should occupy.

<table><thead><tr><th width="230">Roughly</th><th>Suits</th></tr></thead><tbody><tr><td><code>3</code>–<code>5</code></td><td>Small discreet engraving — the inside of a ring, a subtle monogram</td></tr><tr><td><code>6</code>–<code>10</code></td><td>Typical engraving or printed name</td></tr><tr><td><code>12</code>–<code>20</code></td><td>A bold statement — a jersey number, a large printed word</td></tr><tr><td><code>25</code>+</td><td>Text as the main design element</td></tr></tbody></table>

Set it by eye against your real background rather than by number, and check with the longest entry your **Max character** allows.

## Text color

Two things worth thinking about:

**Contrast.** Dark text on a dark product disappears. Check your colour against the actual background you configured, not against the white builder panel.

**Realism.** The colour should be one you can actually produce. If you engrave in silver, a preview in black is closer to the truth than a preview in bright blue.

If the customer chooses the colour, pair this layer with a [Color picker](../option-types/input-types/color-picker.md) or [Color swatch](../option-types/selection-types/color-swatch.md) — but note that the layer's colour here is fixed. To let the shopper's chosen colour drive the preview text, use the **Color preview** and **Select text box** settings on the colour option. See [Swatch style and previews](../option-types/shared-settings/swatch-style-and-previews.md#color-preview).

## Text alignment

**Textarea only**, because it is the only text type that produces more than one line.

<table><thead><tr><th width="200">Alignment</th><th>Use for</th></tr></thead><tbody><tr><td><strong>Left</strong></td><td>Addresses, lists, anything read as a block</td></tr><tr><td><strong>Center</strong></td><td>Messages, verses, greetings. The default and usually right</td></tr><tr><td><strong>Right</strong></td><td>Rarely — a signature, or a deliberately asymmetric design</td></tr></tbody></table>

Alignment works inside the layer's **Width**, which Textarea also has. A centred layer with no width to centre inside does nothing visible.

## Font style

**Normal**, **Italic**, or **Bold** — applied to the whole layer, not to part of it. There is no way to bold one word.

Bear in mind that not every font has a true italic or bold cut. If your custom font does not, the result may look artificially slanted or thickened. Test it.

## A worked example

An engraved bracelet:

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Option type</td><td>Text, <strong>Max character</strong> 15</td></tr><tr><td>Default value</td><td><code>Your name</code></td></tr><tr><td>Text color</td><td>A light grey, matching engraved silver</td></tr><tr><td>Font size</td><td><code>5</code></td></tr><tr><td>Font style</td><td><strong>Normal</strong></td></tr><tr><td>Font family</td><td><strong>Google</strong>, a clean script</td></tr><tr><td>Position</td><td>Centred on the bracelet plate</td></tr><tr><td>Auto-fit max width</td><td>On, so long names shrink rather than overflow</td></tr></tbody></table>

## Notes

* Set a **Default value** on **Basic Settings** so the preview is never empty.
* [Text transform](../option-types/shared-settings/text-input-rules.md#text-transform) applies before the text is drawn, so a layer shows the transformed version — which is what you will produce.
* The layer draws the current entry, so a **Max character** limit is also a limit on how much can overflow.
* Number layers behave exactly like Text layers, which is what makes jersey numbers and years straightforward.

## Troubleshooting

<details>
<summary>The text is invisible</summary>

Contrast against the background, or **Opacity** turned down, or a **Text color** matching the product. Check against your real background image.
</details>

<details>
<summary>Long entries run off the product</summary>

Turn on [Auto-fit max width](curve-and-auto-fit.md#auto-fit-max-width), reduce **Font size**, and set a **Max character** that matches what fits.
</details>

<details>
<summary>The preview is empty until the customer types</summary>

Set a **Default value** on **Basic Settings**.
</details>

<details>
<summary>Text alignment does nothing</summary>

It exists on Textarea only, and it aligns within the layer's **Width** — so give the layer a width.
</details>

<details>
<summary>Bold or italic looks distorted</summary>

The font has no real bold or italic cut. Choose a different font, or upload the proper weight as a custom font. See [Fonts](fonts.md).
</details>

<details>
<summary>I want part of the text styled differently</summary>

Not possible — settings apply to the whole layer. Use two options, each its own layer.
</details>
