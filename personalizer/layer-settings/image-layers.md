---
description: Draw an uploaded photo or a chosen design onto the product, masked into a shape and fitted the way you want.
icon: images
---

# Image layers

An image layer draws a picture onto the product photo. The image is either a file the customer uploaded, or an image attached to the value they selected.

**Applies to:** [File upload](../../option-types/input-types/file-upload.md), and eight selection types: [Dropdown](../../option-types/selection-types/dropdown.md), [Color dropdown](../../option-types/selection-types/color-dropdown.md), [Image dropdown](../../option-types/selection-types/image-dropdown.md), [Radio button](../../option-types/selection-types/radio-button.md), [Checkbox](../../option-types/selection-types/checkbox.md), [Button](../../option-types/selection-types/button.md), [Color swatch](../../option-types/selection-types/color-swatch.md), [Image swatch](../../option-types/selection-types/image-swatch.md).

## Where the image comes from

<table><thead><tr><th width="290">Option type</th><th>The layer draws</th></tr></thead><tbody><tr><td>File upload</td><td>The file the customer uploaded</td></tr><tr><td>The eight selection types</td><td>The image attached to the option value they selected</td></tr></tbody></table>

For selection types, each value needs its own image in the values table. See [Working with option values](../../option-sets/option-values.md).

## Settings specific to image layers

<table><thead><tr><th width="230">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Image shape</strong></td><td>A supplied shape</td><td>The shape the image is masked into. Choose a preset, or upload your own</td></tr><tr><td><strong>Background mode</strong></td><td><strong>Cover</strong></td><td>How the image fits inside that shape</td></tr></tbody></table>

The remaining settings are shared with text layers: position, width, height, opacity, rotation, [clip area](clip-area.md), and [customer controls](customer-controls.md). See [Position, size, and rotation](position-size-rotation.md).

<!-- SCREENSHOT: pp-image-layer | App admin → builder → option File upload → Personalizer Settings | Image shape picker và Background mode với 5 lựa chọn | Khoanh 2 setting -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The image shape picker and background mode setting on an image layer"><figcaption><p>Shape decides the window; background mode decides how the image fills it.</p></figcaption></figure>

## Image shape

The image is masked into a shape, so it appears as part of the product rather than as a rectangle on top of it.

Select one of the supplied shapes, or upload your own. Use a custom shape to match an unusual aperture, such as a locket, a heart-shaped frame, or a phone camera cut-out.

<table><thead><tr><th width="290">Product</th><th>Shape</th></tr></thead><tbody><tr><td>A rectangular photo frame</td><td>A rectangle matching the aperture's proportions</td></tr><tr><td>A round locket or badge</td><td>A circle</td></tr><tr><td>A phone case with a camera cut-out</td><td>A custom shape you upload</td></tr><tr><td>A printed t-shirt panel</td><td>A rectangle matching the print area</td></tr><tr><td>A heart-shaped pendant</td><td>A custom shape</td></tr></tbody></table>

Match the shape's proportions to your real aperture. A square mask on a portrait frame crops the customer's photo unexpectedly.

## Background mode

Five options for how the image fits the shape.

<table><thead><tr><th width="200">Mode</th><th width="290">Behavior</th><th>Trade-off</th></tr></thead><tbody><tr><td><strong>Stretch</strong></td><td>Forces the image to fill the shape exactly</td><td><strong>Distorts</strong> anything whose proportions differ from the shape</td></tr><tr><td><strong>Cover</strong></td><td>Scales until the shape is filled, keeping proportions</td><td>Crops the edges. The default, and usually right</td></tr><tr><td><strong>Contain</strong></td><td>Scales until the whole image fits inside</td><td>Leaves empty space at two edges</td></tr><tr><td><strong>Full width</strong></td><td>Fills the shape's width</td><td>May overflow or fall short vertically</td></tr><tr><td><strong>Full height</strong></td><td>Fills the shape's height</td><td>May overflow or fall short horizontally</td></tr></tbody></table>

### Which value to use

<table><thead><tr><th width="290">Situation</th><th>Mode</th></tr></thead><tbody><tr><td>Customers upload their own photos, any shape</td><td><strong>Cover</strong> — always fills the window, never distorts</td></tr><tr><td>The whole image must be visible, cropping unacceptable</td><td><strong>Contain</strong>, and say in help text that empty space may show</td></tr><tr><td>Your own value images, all cropped consistently</td><td><strong>Cover</strong> or <strong>Stretch</strong> — with matching proportions they behave the same</td></tr><tr><td>A panoramic or banner-shaped area</td><td><strong>Full width</strong></td></tr><tr><td>A tall narrow area</td><td><strong>Full height</strong></td></tr></tbody></table>

{% hint style="warning" %}
Do not use **Stretch** for customer uploads. A portrait photo in a landscape aperture is distorted. **Cover** crops the image instead, which produces a better result.

Use **Cover** together with the [image editor](../../option-types/input-types/file-upload.md) on the upload option, so customers crop their photo to the correct shape before it reaches the preview.
{% endhint %}

## Example configuration

For an option that lets the customer upload a photo and see it in a frame:

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Option type</td><td>File upload, required</td></tr><tr><td>Allowed extensions</td><td><code>jpg</code>, <code>jpeg</code>, <code>png</code></td></tr><tr><td>Enable image editor</td><td>On, so customers crop before uploading</td></tr><tr><td>Help text</td><td><code>JPG or PNG, at least 1500 × 1500 pixels</code></td></tr><tr><td>Image shape</td><td>Matching your frame aperture</td></tr><tr><td>Background mode</td><td><strong>Cover</strong></td></tr><tr><td>Width and height</td><td>Sized to the aperture in the photo</td></tr><tr><td>Clip area</td><td>On, matching the aperture</td></tr><tr><td>Allow customers to</td><td><strong>Change position</strong> and <strong>Resize</strong>, so they can frame their photo</td></tr></tbody></table>

## Selection types as image layers

To let the customer select a design instead of uploading one:

{% stepper %}
{% step %}
### Add a selection option with an image per value

Use an [Image swatch](../../option-types/selection-types/image-swatch.md) for a visible grid, or an [Image dropdown](../../option-types/selection-types/image-dropdown.md) for a long list.
{% endstep %}

{% step %}
### Upload a design image on each value

Add the image in the values table. Use consistent proportions across all values.
{% endstep %}

{% step %}
### Turn on Personalizer Settings

Then set the image shape and background mode.
{% endstep %}

{% step %}
### Position and size the layer

Set where the design appears on the product.
{% endstep %}

{% step %}
### Leave customer controls off

You have already positioned the design, so the customer does not need to move it.
{% endstep %}
{% endstepper %}

A multi-select option can produce several image layers at the same time, and they overlap. Either limit the option to one selection, or position the layers to allow for the overlap.

## Notes

* An image layer draws nothing until a file is uploaded or a value with an image is selected. Unlike text layers, it has no default value.
* Uploaded images can be large. Use **Cover** and a clip area to keep the preview within the area you defined.
* Uploads are drawn at the resolution supplied, so a small file appears blurred when enlarged. State a minimum size in help text.
* A custom shape is uploaded to your store's files and can be reused across options.
