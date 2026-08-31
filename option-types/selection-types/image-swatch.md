---
description: >-
  A grid of pictures with adjustable size, zooming tooltips, and slider layouts —
  for patterns, materials, and designs.
icon: images
---

# Image swatch

A grid of pictures, one per value. The type to use when the choice is visual and the picture is the whole decision: fabrics, patterns, print designs, materials, finishes.

It has more presentation settings than any other selection type, because a grid of images is the hardest thing to fit on a product page.

## What customers see

A grid of picture swatches at the size you set. Hovering shows the value's name, and optionally a zoomed version of the image. Long lists can be shown as a slider.

<!-- SCREENSHOT: type-imageswatch-storefront | Storefront → trang sản phẩm | Grid image swatch, 1 swatch đang chọn, hover 1 swatch hiện tooltip Text & image phóng to | Khoanh riêng grid và tooltip -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A grid of image swatches on a storefront product page with a zoomed tooltip on the hovered swatch"><figcaption><p>Small swatches plus a zooming tooltip is how you show detail without a huge grid.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until one is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><strong>Option values</strong></td><td>The choices, each with an <strong>Image</strong> column. Upload a picture or reuse one of the product's own images. See <a href="../../option-sets/option-values.md">Working with option values</a>.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#allow-multiple">Allow multiple</a></td><td>Lets the shopper choose several.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-selections">Min selections</a> / <a href="../shared-settings/limits.md#min-and-max-selections">Max selections</a></td><td>Shown once <strong>Allow multiple</strong> is on.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance for the whole option.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Preselects a value.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

There is no **Swatch style** setting — this type is always images.

## Advanced Settings

<table><thead><tr><th width="270">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How add-ons scale — including <strong>Mixed quantity</strong> when multiple is on.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#enable-custom-layout">Enable custom layout</a></td><td>Unlocks the layouts below.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#layout-type">Layout type</a></td><td><strong>Expand</strong>, <strong>Collapse</strong>, or <strong>Slider</strong>.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#scroll-type">Scroll type</a>, <strong>Scroll height</strong>, <strong>Number of option values</strong></td><td>Scroll area for the Expand and Collapse layouts.</td></tr><tr><td><a href="../shared-settings/collapsible-layouts-and-sliders.md#slider-settings">Number of rows</a>, <strong>Swatches per row</strong>, <strong>Show navigation arrows</strong>, <strong>Show indicators</strong>, <strong>Slider style</strong></td><td>Slider layout settings.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#swatch-image-width-and-height">Swatch image width</a> / <strong>Swatch image height</strong></td><td>Swatch size in pixels. Both start at <code>60</code>.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#tooltip-style">Tooltip style</a></td><td><strong>Text</strong>, or <strong>Text &amp; image</strong> for a zoomed preview on hover.</td></tr><tr><td><strong>Tooltip image width</strong> / <strong>Tooltip image height</strong></td><td>The zoomed image size. Both start at <code>150</code>. Shown once the tooltip style includes an image.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#not-allow-deselect">Not allow deselect</a></td><td>Stops the shopper clearing their choice. Single-select only.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#direction-style">Direction style</a></td><td><strong>Vertical</strong> or <strong>Horizontal</strong>.</td></tr><tr><td><a href="../shared-settings/out-of-stock-options.md">Out of stock options</a></td><td>How sold-out values look.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the option-level help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

### Size and tooltip together

The two settings that matter most on this type are the swatch size and the tooltip style, and they solve opposite problems:

<table><thead><tr><th width="290">Problem</th><th>Answer</th></tr></thead><tbody><tr><td>Detail is not visible in a small swatch</td><td><strong>Tooltip style</strong> <strong>Text &amp; image</strong> with a large tooltip image — keep swatches small, let the tooltip do the zooming</td></tr><tr><td>The grid dominates the page</td><td>Smaller swatches, or the <strong>Slider</strong> layout</td></tr><tr><td>Shoppers cannot tell two patterns apart</td><td>Larger swatches, plus the zooming tooltip</td></tr><tr><td>Non-square products look wrong</td><td>Rectangular swatches — width and height are independent</td></tr></tbody></table>

Remember that hover does not exist in the same way on touch devices. Anything essential should be in the value's own help text rather than a tooltip.

## Personalizer Settings

Supported as an **image layer**: the selected value's image is drawn onto the product photo. Settings are image shape, background mode, size, position, rotation, clip area, and customer controls.

This is one of the strongest combinations in the app — a grid of designs, and the chosen design appearing on the product immediately. See [Image layers](../../personalizer/layer-settings/image-layers.md).

## Add-on pricing

Prices belong to each value, so premium fabrics can cost more than standard ones. Linking values to add-on products gives each design its own stock.

See [Add-on pricing](../../add-on-pricing/README.md).

## Preparing your images

The presentation settings can only do so much with inconsistent source images. Before uploading:

* Crop every image to the same proportions. Mismatched crops make a grid look untidy however you size it.
* Photograph or scan at the same distance and lighting, so colours are comparable.
* Upload at a size larger than your tooltip dimensions, or the zoomed version will be soft.
* Keep file sizes reasonable — a grid of forty large images is a slow product page.

## Examples

**Twenty fabric swatches with zoom**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Fabric</code></td></tr><tr><td>Swatch image width / height</td><td><code>60</code> / <code>60</code></td></tr><tr><td>Tooltip style</td><td><strong>Text &amp; image</strong></td></tr><tr><td>Tooltip image width / height</td><td><code>240</code> / <code>240</code></td></tr><tr><td>Layout type</td><td><strong>Slider</strong>, 2 rows, 5.5 per row, arrows shown</td></tr><tr><td>Required field</td><td>On</td></tr></tbody></table>

**Six print designs, large**

Swatches at `120` × `120`, no slider, **Personalizer** on so the chosen design appears on the product photo.

**Fabric strips**

Swatches at `140` wide × `40` high, matching the shape of the material.

**Designs with different prices**

Standard designs free, licensed artwork priced through **Use existing product** so it maps to a real SKU.

## Notes
* Available on all plans. Slider layout is separately plan-gated.
* Works in Shopify POS.
* Every value needs an image; without one the swatch is blank.
* Swatch sizes are display sizes — they do not resize the uploaded file.
* Value names appear on hover only, so put anything essential in per-value help text.
