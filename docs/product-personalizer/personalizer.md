---
description: >-
  Print the customer's text or photo onto the product image, live, so they see
  the finished product before they buy.
icon: wand-magic-sparkles
---

# Overview

The **Product Personalizer** draws what customers enter onto the product image as they fill in the form. They type a line of text and see it printed on the product. They upload a photo and see it inside the print area. They pick a font or a color and the design changes straight away.

You build the design in the app's Personalizer editor: turn the Personalizer on for an option, then drag it into place on the product image.

<figure><img src="../.gitbook/assets/screenshot-personalizer-storefront-tee.png" alt="A storefront product page for a t-shirt with the customer&#x27;s uploaded photo and the text Golden hour drawn on the product image"><figcaption><p>On the product page, the customer's photo, text, font, and color appear on the product image as they choose them.</p></figcaption></figure>

**Watch it done (3:48).** Building a live preview from scratch, so customers see their own text on the product image as they type.

{% embed url="https://www.youtube.com/watch?v=Q8EwrbBIs98" %}

## What it can print

Each option with the Personalizer turned on becomes one **element** on the product image.

<table><thead><tr><th width="200">Element</th><th width="290">Comes from</th><th>What you control</th></tr></thead><tbody><tr><td><strong>Text</strong></td><td><a href="../option-types/input-types/text.md">Text</a>, <a href="../option-types/input-types/textarea.md">Textarea</a>, <a href="../option-types/input-types/number.md">Number</a></td><td>Color, font size, font, effects, curve, auto-fit, and which font and color customers can pick</td></tr><tr><td><strong>Image</strong></td><td><a href="../option-types/input-types/file-upload.md">File upload</a> and eight selection types</td><td>Shape, and how the image fills it</td></tr></tbody></table>

Both kinds share position, size, rotation, opacity, a print area, and the choice of what customers can move, resize, or rotate.

## The twelve supported option types

<table><thead><tr><th width="290">Text elements</th><th>Image elements</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/text.md">Text</a></td><td><a href="../option-types/input-types/file-upload.md">File upload</a></td></tr><tr><td><a href="../option-types/input-types/textarea.md">Textarea</a></td><td><a href="../option-types/selection-types/dropdown.md">Dropdown</a></td></tr><tr><td><a href="../option-types/input-types/number.md">Number</a></td><td><a href="../option-types/selection-types/color-dropdown.md">Color dropdown</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/image-dropdown.md">Image dropdown</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/radio-button.md">Radio button</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/checkbox.md">Checkbox</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/button.md">Button</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/color-swatch.md">Color swatch</a></td></tr><tr><td></td><td><a href="../option-types/selection-types/image-swatch.md">Image swatch</a></td></tr></tbody></table>

Other option types, such as dates, phone numbers, switches, and sliders, have no **Personalizer** tab because they have nothing to print. A [Font picker](../option-types/selection-types/font-picker.md) or [Color picker](../option-types/input-types/color-picker.md) is not printed itself, but it can choose the font or color of a text element. See [Let customers pick font and color](layer-settings/font-and-color.md).

## Where to go next

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Set up the Personalizer</strong></td><td>From turning it on to seeing the design on your storefront. Start here.</td><td><a href="setup.md">setup.md</a></td></tr><tr><td><strong>The Personalizer editor</strong></td><td>The canvas, its toolbar, and how to drag, resize, and zoom.</td><td><a href="editor.md">editor.md</a></td></tr><tr><td><strong>Test like a customer</strong></td><td>Fill in the preview form, upload a test photo, and check the result before you publish.</td><td><a href="test-like-a-customer.md">test-like-a-customer.md</a></td></tr><tr><td><strong>Element settings</strong></td><td>Every card on the Personalizer tab: text style, fonts, effects, shape, position, print area, and what customers can change.</td><td><a href="layer-settings/">layer-settings</a></td></tr><tr><td><strong>Designs in cart and orders</strong></td><td>What the customer and your team see after Add to cart.</td><td><a href="cart-and-orders.md">cart-and-orders.md</a></td></tr><tr><td><strong>Walkthrough: personalized t-shirt</strong></td><td>One real product, from an empty option set to a finished design on the storefront.</td><td><a href="walkthrough-personalized-tee.md">walkthrough-personalized-tee.md</a></td></tr><tr><td><strong>Walkthrough: custom printed mug</strong></td><td>A curved name and a customer photo on a mug.</td><td><a href="walkthrough-custom-mug.md">walkthrough-custom-mug.md</a></td></tr><tr><td><strong>Troubleshooting</strong></td><td>Find the problem by what you see on the page.</td><td><a href="troubleshooting.md">troubleshooting.md</a></td></tr></tbody></table>

## Before you start

* **Check your plan.** The Personalizer is available on certain plans. A star badge next to **Personalizer** means your plan does not include it. See [Compare plans](../plans-and-billing/compare-plans.md).
* **Use a good product photo.** The design is only as convincing as the image it sits on. See [Choosing the background](setup.md#choosing-the-background).
* **Start from a template if you can.** A [personalized template](../templates/personalized-templates.md) comes with the options and the design already in place.
