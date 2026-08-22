---
description: The moving parts of the live preview — background, layers, and what the customer can change.
icon: diagram-project
---

# How the live preview works

Three things make up a personalised product page. Understanding them separately makes the rest of this section straightforward.

## The three parts

<table><thead><tr><th width="180">Part</th><th width="230">What it is</th><th>Where you set it</th></tr></thead><tbody><tr><td><strong>The background</strong></td><td>The image the layers are drawn on — a product photo or an image you upload</td><td>Once per option set, from the preview panel</td></tr><tr><td><strong>The layers</strong></td><td>One per option with the Personalizer turned on. Text or image</td><td>Per option, on its <strong>Personalizer Settings</strong> tab</td></tr><tr><td><strong>Customer controls</strong></td><td>Which layers the shopper may move, resize, or rotate themselves</td><td>Per option, per layer</td></tr></tbody></table>

## What happens on the storefront

{% stepper %}
{% step %}
### The page loads with the background

Your chosen image is shown. Depending on your settings it replaces the product photo immediately, or waits until the customer starts personalising.
{% endstep %}

{% step %}
### Layers are drawn in their configured positions

Each personalised option contributes a layer, positioned where you placed it, in its font, colour, and effect.

Text layers with a **Default value** show that text straight away, so the preview is never empty. Image layers wait for a choice or an upload.
{% endstep %}

{% step %}
### The customer changes something and the layer redraws

They type, and the text on the product changes as they type. They pick a design, and the image appears. There is no reload and no button to press.
{% endstep %}

{% step %}
### They adjust it themselves, if you allow it

Where you enabled it, they can drag a layer, resize it, or rotate it. See [Customer controls](customer-controls.md).
{% endstep %}

{% step %}
### The design travels with the order

Their choices — and the resulting design — reach the cart and the order, so you can produce what they saw. See [Designs in cart and orders](cart-and-orders.md).
{% endstep %}
{% endstepper %}

## One background, many layers

The background belongs to the **option set**, not to an option. Every personalised option in that set draws onto the same background.

That is why the order of work matters: choose the background first, then position the layers against it. Changing the background afterwards means repositioning everything.

## Layers stack

Several personalised options mean several layers on one image. They are drawn together, and they can overlap.

<table><thead><tr><th width="290">Situation</th><th>What to do</th></tr></thead><tbody><tr><td>A name and a date, both on the same product</td><td>Give them different <strong>Y-Axis</strong> positions so they sit on separate lines</td></tr><tr><td>An uploaded photo and text over it</td><td>Position the text within the photo's area, and check contrast</td></tr><tr><td>Two options that are alternatives, never both</td><td>Use <a href="../conditional-logic/README.md">conditional logic</a> so only one is ever visible</td></tr><tr><td>Layers that must not stray outside a printable area</td><td>Give each a <a href="clip-area.md">clip area</a></td></tr></tbody></table>

A hidden option contributes no layer. That makes conditional logic a clean way to switch between alternative designs.

## What the preview is, and is not

<table><thead><tr><th width="290">It is</th><th>It is not</th></tr></thead><tbody><tr><td>A representation of the finished product, good enough to sell from</td><td>A print-ready proof</td></tr><tr><td>Live, updating as the customer types</td><td>Colour-accurate — screens are not calibrated</td></tr><tr><td>A record of what the customer intended</td><td>A guarantee that your production will match it exactly</td></tr></tbody></table>

Say so where it matters. A line of [help text](../option-types/shared-settings/placeholder-and-help-text.md#help-text) — "the preview is a guide; final placement may vary slightly" — prevents disputes about millimetres.

## Building order

Do it in this order and you will not redo work:

{% stepper %}
{% step %}
### Set the background

[Set the preview background](set-the-background.md). Everything else is positioned against it.
{% endstep %}

{% step %}
### Add and configure the options themselves

Labels, limits, prices. Do the ordinary option work before the personalisation work.
{% endstep %}

{% step %}
### Turn on the Personalizer per option

[Enable personalizer on an option](enable-on-an-option.md).
{% endstep %}

{% step %}
### Style each layer

Fonts, colours, effects for text; shapes and fit modes for images.
{% endstep %}

{% step %}
### Position each layer

Then check with a long entry and a short one, and on mobile.
{% endstep %}

{% step %}
### Decide what the customer may adjust

[Customer controls](customer-controls.md). Add a [clip area](clip-area.md) if you are giving them freedom.
{% endstep %}

{% step %}
### Test on a real product page

With **View in Store**, using a realistic entry rather than "test".
{% endstep %}
{% endstepper %}

## Notes

* The Personalizer is plan-gated.
* The builder's preview panel shows the personalised result as you configure it, so most of the work can be done without leaving the app.
* Positions are percentages, not pixels, so a layer stays in the same relative place whatever size the image is displayed at.
* Performance is worth watching: many layers on a large image on an old phone is slower than one layer.
