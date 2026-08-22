---
description: Placing a layer on the product photo — axes, width and height, opacity, and rotation.
icon: arrows-up-down-left-right
---

# Position, size, and rotation

Every layer, text or image, is positioned with the same handful of controls. Getting them right is what separates a convincing preview from an obviously fake one.

## The settings

<table><thead><tr><th width="200">Setting</th><th width="150">Range</th><th width="130">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>X-Axis</strong></td><td>0 – 100%</td><td><code>50</code></td><td>Horizontal position. 0 is the left edge, 100 the right</td></tr><tr><td><strong>Y-Axis</strong></td><td>0 – 100%</td><td><code>50</code></td><td>Vertical position. 0 is the top, 100 the bottom</td></tr><tr><td><strong>Width</strong></td><td>0 – 100%</td><td><code>25</code></td><td>The layer's width as a share of the image. Image layers and Textarea only</td></tr><tr><td><strong>Height</strong></td><td>0 – 100%</td><td><code>25</code></td><td>The layer's height. Image layers and Textarea only</td></tr><tr><td><strong>Opacity</strong></td><td>0 – 100%</td><td><code>100</code></td><td>Transparency. 100 is solid</td></tr><tr><td><strong>Rotation</strong></td><td>-180 – 180°</td><td><code>0</code></td><td>Rotation in degrees. Negative is anticlockwise</td></tr></tbody></table>

All the position values are **percentages of the image**, not pixels. That is what keeps a layer in the right place whether the image is shown on a phone or a large monitor.

<!-- SCREENSHOT: pp-position-settings | App admin → builder → option có personalizer | Nhóm X-Axis, Y-Axis, Opacity, Rotation dạng slider | Khoanh nhóm này -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The position, opacity, and rotation sliders on the Personalizer Settings tab"><figcaption><p>Positions are percentages of the image, so they hold at any display size.</p></figcaption></figure>

## Which types get width and height

<table><thead><tr><th width="290">Type</th><th>Width and height</th><th>Instead they get</th></tr></thead><tbody><tr><td>Image layers — File upload and the eight selection types</td><td><strong>Yes</strong></td><td></td></tr><tr><td>Textarea</td><td><strong>Yes</strong> — it is a block of text</td><td></td></tr><tr><td>Text and Number</td><td>No</td><td><a href="curve-and-auto-fit.md">Curve and Auto-fit max width</a></td></tr></tbody></table>

Text and Number are single lines, so they size themselves from the font size and grow as the customer types. That is why they have auto-fit rather than a fixed width.

## How to position a layer

{% stepper %}
{% step %}
### Start from the middle

Both axes default to 50, which puts the layer in the centre. Move outwards from there.
{% endstep %}

{% step %}
### Set the vertical position first

**Y-Axis** is usually the more obvious of the two — the engraving plate is a third of the way down, the print area is in the middle.
{% endstep %}

{% step %}
### Then the horizontal position

**X-Axis** at 50 is centred, which is right for most personalisation.
{% endstep %}

{% step %}
### Size it

Image layers: set **Width** and **Height**. Text layers: adjust **Font size** on the [text layer settings](text-layers.md).
{% endstep %}

{% step %}
### Rotate only if the product needs it

A rotated layer on a straight product looks like a mistake. Rotate to match a slanted surface or a deliberate design.
{% endstep %}

{% step %}
### Test with the extremes

A one-character entry and a maximum-length one. A tall uploaded image and a wide one. This is where positioning problems show up.
{% endstep %}

{% step %}
### Check it on mobile

Percentages hold, but a layer that is legible on a desktop preview can be too small to read on a phone.
{% endstep %}
{% endstepper %}

## Opacity

<table><thead><tr><th width="230">Value</th><th>Use for</th></tr></thead><tbody><tr><td><code>100</code></td><td>Almost everything. Printing and engraving are opaque</td></tr><tr><td><code>60</code>–<code>90</code></td><td>Etched glass, watermarks, subtle tone-on-tone printing</td></tr><tr><td>Below <code>50</code></td><td>Rarely. The customer may think their text has not registered</td></tr></tbody></table>

Reducing opacity to make a layer "sit better" in a photo is usually a sign the colour is wrong rather than the opacity.

## Rotation

<table><thead><tr><th width="230">Value</th><th>Use for</th></tr></thead><tbody><tr><td><code>0</code></td><td>Almost everything</td></tr><tr><td>A few degrees either way</td><td>Matching a product photographed slightly off-square</td></tr><tr><td><code>90</code> or <code>-90</code></td><td>Text running up the side of a product — a spine, a pen barrel</td></tr><tr><td><code>180</code></td><td>Rarely useful outside deliberate design</td></tr></tbody></table>

For text following a curved surface — around a mug or a ring — use [Curve](curve-and-auto-fit.md) rather than rotation. Rotation turns the whole line; curve bends it.

## Several layers on one image

<table><thead><tr><th width="290">Goal</th><th>How</th></tr></thead><tbody><tr><td>A name above a date</td><td>Same <strong>X-Axis</strong>, different <strong>Y-Axis</strong> — for example 40 and 55</td></tr><tr><td>Two layers side by side</td><td>Same <strong>Y-Axis</strong>, different <strong>X-Axis</strong> — for example 30 and 70</td></tr><tr><td>Text over an uploaded photo</td><td>Position the text within the photo layer's area, and give it a <a href="effects.md#stroke">stroke</a> for contrast</td></tr><tr><td>Layers that must never overlap the product edge</td><td>Give each a <a href="clip-area.md">clip area</a></td></tr></tbody></table>

## Notes

* Percentages are relative to the background image, so consistent product photography is what keeps positions accurate across products. See [Set the preview background](set-the-background.md).
* If you let customers move a layer, your position is their starting point. See [Customer controls](customer-controls.md).
* A [clip area](clip-area.md) constrains where a layer can appear, which is what makes customer freedom safe.
* Changing the background afterwards will move everything. Set the background first.

## Troubleshooting

<details>
<summary>The layer is off the image</summary>

An axis is at or near 0 or 100, or the layer is large. Bring the values towards the middle and reduce the size.
</details>

<details>
<summary>I cannot find Width and Height</summary>

Text and Number layers do not have them — they size from the font. See [Curve and auto-fit width](curve-and-auto-fit.md).
</details>

<details>
<summary>Long text overflows the product</summary>

Turn on [Auto-fit max width](curve-and-auto-fit.md#auto-fit-max-width), and set a **Max character** limit.
</details>

<details>
<summary>The layer sits in a different place on different products</summary>

Their photographs are framed differently. Standardise them, or split the products into separate option sets.
</details>

<details>
<summary>It looks right on desktop but wrong on mobile</summary>

Check the mobile width in the builder preview. Percentages hold, but legibility does not — increase the font size.
</details>

<details>
<summary>The uploaded image is stretched</summary>

That is the **Background mode**, not the size. See [Image layers](image-layers.md).
</details>

## Next steps

* [Curve and auto-fit width](curve-and-auto-fit.md) — for single-line text.
* [Clip area](clip-area.md)
* [Customer controls](customer-controls.md)
