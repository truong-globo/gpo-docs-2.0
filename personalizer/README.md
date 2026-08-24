---
description: Show the customer's own text and images on the product photo, live, as they type — the app's most persuasive feature.
icon: wand-magic-sparkles
---

# Overview

The Product Personalizer draws what the customer enters onto the product photograph, live. They type a name and see it engraved. They upload a photo and see it in the frame. They pick a colour and watch the product change.

It is the difference between asking somebody to imagine a personalised product and showing it to them.

<!-- SCREENSHOT: pp-storefront-hero | Storefront → trang sản phẩm có personalizer | Ảnh sản phẩm với text khách nhập được vẽ lên, cạnh là field nhập | Khoanh vùng preview trên ảnh sản phẩm -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A storefront product page with the customer's typed text drawn onto the product photo"><figcaption><p>The customer's own words, on the product, before they buy.</p></figcaption></figure>

## What it can draw

<table><thead><tr><th width="230">Layer</th><th width="290">From</th><th>Controls you get</th></tr></thead><tbody><tr><td><strong>Text</strong></td><td><a href="../option-types/input-types/text.md">Text</a>, <a href="../option-types/input-types/textarea.md">Textarea</a>, <a href="../option-types/input-types/number.md">Number</a></td><td>Colour, size, style, font, five effects, curve, auto-fit</td></tr><tr><td><strong>Images</strong></td><td><a href="../option-types/input-types/file-upload.md">File upload</a> and eight selection types</td><td>Shape masking, fit mode, size</td></tr></tbody></table>

Both kinds share position, opacity, rotation, a clip area, and the choice of what the customer may adjust themselves.

## The twelve supported option types

<table><thead><tr><th width="290">Text layers</th><th>Image layers</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/text.md">Text</a></td><td><a href="../option-types/input-types/file-upload.md">File upload</a></td></tr><tr><td><a href="../option-types/input-types/textarea.md">Textarea</a></td><td><a href="../option-types/selection-types/dropdown.md">Dropdown</a></td></tr><tr><td><a href="../option-types/input-types/number.md">Number</a></td><td><a href="../option-types/selection-types/color-dropdown.md">Color dropdown</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/image-dropdown.md">Image dropdown</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/radio-button.md">Radio button</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/checkbox.md">Checkbox</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/button.md">Button</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/color-swatch.md">Color swatch</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/image-swatch.md">Image swatch</a></td></tr></tbody></table>

Any other type — dates, phone numbers, switches, sliders — has no Personalizer tab, because there is nothing meaningful to draw.

## How to read this section

The order below is the order you would actually build in.

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Set up the Personalizer</strong></td><td>The background, the layers, and the order to build them in. Start here.</td><td><a href="setup.md">setup.md</a></td></tr><tr><td><strong>Layer settings</strong></td><td>Eight pages covering every setting on a layer: styling, fonts, effects, placement, curve and auto-fit, clip area, image fitting, and customer controls.</td><td><a href="layer-settings/README.md">layer-settings</a></td></tr><tr><td><strong>Designs in cart and orders</strong></td><td>What you and the customer see afterwards.</td><td><a href="cart-and-orders.md">cart-and-orders.md</a></td></tr><tr><td><strong>Walkthrough: custom printed mug</strong></td><td>One product, built end to end.</td><td><a href="walkthrough-custom-mug.md">walkthrough-custom-mug.md</a></td></tr><tr><td><strong>Troubleshooting</strong></td><td>By symptom.</td><td><a href="troubleshooting.md">troubleshooting.md</a></td></tr></tbody></table>

## Before you start

* The Personalizer is plan-gated. If the **Personalizer Settings** tab is unavailable, see [Compare plans](../plans/compare-plans.md).
* You need a good product photograph. The preview is only as convincing as the image it draws on — see [Choosing the background](setup.md#choosing-the-background).
* Budget time for positioning. Getting a layer to sit exactly where the engraving really goes takes a few minutes per product, and it is the difference between convincing and amateurish.

{% hint style="info" %}
The fastest way in is a [personalized template](../templates/personalized-templates.md). Twenty complete setups ship with the app, already positioned, and you can adapt one rather than starting from an empty canvas.
{% endhint %}
