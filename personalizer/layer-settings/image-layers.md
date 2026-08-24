---
description: Draw an uploaded photo or a chosen design onto the product, masked into a shape and fitted the way you want.
icon: images
---

# Image layers

An image layer draws a picture onto the product photograph — either a file the customer uploaded, or an image attached to the value they chose.

**Applies to:** [File upload](../../option-types/input-types/file-upload.md), and eight selection types: [Dropdown](../../option-types/selection-types/dropdown.md), [Color dropdown](../../option-types/selection-types/color-dropdown.md), [Image dropdown](../../option-types/selection-types/image-dropdown.md), [Radio button](../../option-types/selection-types/radio-button.md), [Checkbox](../../option-types/selection-types/checkbox.md), [Button](../../option-types/selection-types/button.md), [Color swatch](../../option-types/selection-types/color-swatch.md), [Image swatch](../../option-types/selection-types/image-swatch.md).

## Where the image comes from

<table><thead><tr><th width="290">Option type</th><th>The layer draws</th></tr></thead><tbody><tr><td>File upload</td><td>The file the customer uploaded</td></tr><tr><td>The eight selection types</td><td>The image attached to the option value they selected</td></tr></tbody></table>

For selection types that means each value needs its own image in the values table. See [Working with option values](../../option-sets/option-values.md).

## The two settings unique to image layers

<table><thead><tr><th width="230">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Image shape</strong></td><td>A supplied shape</td><td>The shape the image is masked into. Choose a preset, or upload your own</td></tr><tr><td><strong>Background mode</strong></td><td><strong>Cover</strong></td><td>How the image fits inside that shape</td></tr></tbody></table>

Everything else — position, width, height, opacity, rotation, [clip area](clip-area.md), [customer controls](customer-controls.md) — is shared with text layers. See [Position, size, and rotation](position-size-rotation.md).

<!-- SCREENSHOT: pp-image-layer | App admin → builder → option File upload → Personalizer Settings | Image shape picker và Background mode với 5 lựa chọn | Khoanh 2 setting -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The image shape picker and background mode setting on an image layer"><figcaption><p>Shape decides the window; background mode decides how the image fills it.</p></figcaption></figure>

## Image shape

The image is masked into a shape, so it appears as part of the product rather than as a rectangle floating on top.

You can choose from the supplied shapes, or upload your own. A custom shape is the way to match an unusual window — a locket, a heart-shaped frame, a phone camera cut-out.

<table><thead><tr><th width="290">Product</th><th>Shape</th></tr></thead><tbody><tr><td>A rectangular photo frame</td><td>A rectangle matching the aperture's proportions</td></tr><tr><td>A round locket or badge</td><td>A circle</td></tr><tr><td>A phone case with a camera cut-out</td><td>A custom shape you upload</td></tr><tr><td>A printed t-shirt panel</td><td>A rectangle matching the print area</td></tr><tr><td>A heart-shaped pendant</td><td>A custom shape</td></tr></tbody></table>

Match the shape's proportions to your real aperture. A square mask on a portrait frame crops customers' photos in a way they will not expect.

## Background mode

Five ways for the image to fit the shape. This is the setting that decides whether customers' photos look right.

<table><thead><tr><th width="200">Mode</th><th width="290">Behaviour</th><th>Trade-off</th></tr></thead><tbody><tr><td><strong>Stretch</strong></td><td>Forces the image to fill the shape exactly</td><td><strong>Distorts</strong> anything whose proportions differ from the shape</td></tr><tr><td><strong>Cover</strong></td><td>Scales until the shape is filled, keeping proportions</td><td>Crops the edges. The default, and usually right</td></tr><tr><td><strong>Contain</strong></td><td>Scales until the whole image fits inside</td><td>Leaves empty space at two edges</td></tr><tr><td><strong>Full width</strong></td><td>Fills the shape's width</td><td>May overflow or fall short vertically</td></tr><tr><td><strong>Full height</strong></td><td>Fills the shape's height</td><td>May overflow or fall short horizontally</td></tr></tbody></table>

### Choosing one

<table><thead><tr><th width="290">Situation</th><th>Mode</th></tr></thead><tbody><tr><td>Customers upload their own photos, any shape</td><td><strong>Cover</strong> — always fills the window, never distorts</td></tr><tr><td>The whole image must be visible, cropping unacceptable</td><td><strong>Contain</strong>, and say in help text that empty space may show</td></tr><tr><td>Your own value images, all cropped consistently</td><td><strong>Cover</strong> or <strong>Stretch</strong> — with matching proportions they behave the same</td></tr><tr><td>A panoramic or banner-shaped area</td><td><strong>Full width</strong></td></tr><tr><td>A tall narrow area</td><td><strong>Full height</strong></td></tr></tbody></table>

{% hint style="warning" %}
Avoid **Stretch** for customer uploads. Someone uploading a portrait photo into a landscape window gets a squashed picture — and either buys it and complains, or does not buy. **Cover** crops instead, which is almost always the lesser evil.

Better still, combine **Cover** with the [image editor](../../option-types/input-types/file-upload.md) on the upload option, so customers crop their own photo to the right shape before it ever reaches the preview.
{% endhint %}

## The combination that works

For "upload your photo and see it in the frame":

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Option type</td><td>File upload, required</td></tr><tr><td>Allowed extensions</td><td><code>jpg</code>, <code>jpeg</code>, <code>png</code></td></tr><tr><td>Enable image editor</td><td>On, so customers crop before uploading</td></tr><tr><td>Help text</td><td><code>JPG or PNG, at least 1500 × 1500 pixels</code></td></tr><tr><td>Image shape</td><td>Matching your frame aperture</td></tr><tr><td>Background mode</td><td><strong>Cover</strong></td></tr><tr><td>Width and height</td><td>Sized to the aperture in the photo</td></tr><tr><td>Clip area</td><td>On, matching the aperture</td></tr><tr><td>Allow customers to</td><td><strong>Change position</strong> and <strong>Resize</strong>, so they can frame their photo</td></tr></tbody></table>

## Selection types as image layers

For a chooser rather than an upload — "pick a design and see it on the product":

{% stepper %}
{% step %}
### Add a selection option with an image per value

An [Image swatch](../../option-types/selection-types/image-swatch.md) for a visible grid, or an [Image dropdown](../../option-types/selection-types/image-dropdown.md) for a long list.
{% endstep %}

{% step %}
### Upload a design image on each value

In the values table. Use consistent proportions across the values.
{% endstep %}

{% step %}
### Turn on Personalizer Settings

Then set the shape and background mode.
{% endstep %}

{% step %}
### Position and size the layer

Where the design sits on the product.
{% endstep %}

{% step %}
### Leave customer controls off

You positioned the design deliberately; there is no reason for the shopper to move it.
{% endstep %}
{% endstepper %}

Note that a multi-select option can contribute several image layers at once, which will overlap. Either restrict it to one selection, or position deliberately for the overlap.

## Notes

* An image layer draws nothing until a file is uploaded or a value with an image is chosen. Unlike text layers, there is no default to fall back on.
* Uploaded images can be large; **Cover** and a sensible clip area keep the preview tidy regardless.
* Customer uploads are drawn at the resolution supplied, so a small file looks soft when enlarged. Ask for a minimum size in help text.
* A custom shape is uploaded to your store's files, and can be reused across options.

## Troubleshooting

<details>
<summary>Nothing appears on the product</summary>

No file has been uploaded, or no value with an image is selected. For selection types, check every value actually has an image.
</details>

<details>
<summary>The image is distorted</summary>

**Background mode** is on **Stretch**. Switch to **Cover**.
</details>

<details>
<summary>The image is cropped and customers complain</summary>

**Cover** crops to fill. Switch to **Contain** if the whole image must show, or turn on the upload option's image editor so they crop it themselves.
</details>

<details>
<summary>There is empty space around the image</summary>

**Contain** leaves space when proportions differ. Use **Cover**, or a shape matching your images' proportions.
</details>

<details>
<summary>The image spills outside the product</summary>

Reduce **Width** and **Height**, and add a [clip area](clip-area.md).
</details>

<details>
<summary>The uploaded photo looks soft</summary>

The file is smaller than the size it is drawn at. Ask for a minimum resolution in help text.
</details>

<details>
<summary>Several images are stacked on top of each other</summary>

A multi-select option is contributing one layer per selection. Limit it to one selection, or position for the overlap.
</details>
