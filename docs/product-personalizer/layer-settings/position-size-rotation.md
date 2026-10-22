---
description: >-
  Place an element on the product image by dragging it or typing exact
  values for position, width, height, rotation, and opacity.
icon: arrows-up-down-left-right
---

# Position and size

The **Position and size** card places an element on the product image. Its own help text sums it up: **Drag the element on the preview, or set exact values.** Dragging on the canvas and typing here change the same settings.

<figure><img src="../../.gitbook/assets/screenshot-personalizer-position-and-size.png" alt="The Position and size card with X position, Y position, Rotation, and Opacity fields for a text element selected on a tote bag"><figcaption><p>Every value in Position and size updates as you drag the element on the canvas.</p></figcaption></figure>

## The settings

<table><thead><tr><th width="200">Setting</th><th width="150">Range</th><th width="130">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Width</strong></td><td>0 to 100%</td><td><code>25</code></td><td>The element's width as a share of the image. Image elements and Textarea only</td></tr><tr><td><strong>Height</strong></td><td>0 to 100%</td><td><code>25</code></td><td>The element's height. Image elements and Textarea only</td></tr><tr><td><strong>X position</strong></td><td>0 to 100%</td><td><code>50</code></td><td>The horizontal center of the element. 0 is the left edge, 100 the right</td></tr><tr><td><strong>Y position</strong></td><td>0 to 100%</td><td><code>50</code></td><td>The vertical center. 0 is the top, 100 the bottom</td></tr><tr><td><strong>Rotation</strong></td><td>-180 to 180°</td><td><code>0</code></td><td>Turns the element. Negative values turn it counterclockwise</td></tr><tr><td><strong>Opacity</strong></td><td>0 to 100%</td><td><code>100</code></td><td>Transparency. 100 is solid</td></tr></tbody></table>

All values are **percentages of the image**, not pixels, so the element stays in the same place on a phone and on a large screen.

Text and Number have no width or height. Their size comes from **Font size**, and they grow as the customer types. Use [Auto-fit max width](curve-and-auto-fit.md#auto-fit-max-width) to limit them.

## How to place an element

{% stepper %}
{% step %}
### Drag it roughly into place

Select the element on the canvas and drag it to the print area. It snaps to the center lines of the image when you get close.
{% endstep %}

{% step %}
### Size it

For an image, drag a corner handle or type **Width** and **Height**. For text, set **Font size** in [Text style](text-layers.md#font-size).
{% endstep %}

{% step %}
### Fine-tune the values

Type exact **X position** and **Y position** values, or press the arrow keys on the canvas to nudge it 1% at a time. Hold Shift to move 5%.
{% endstep %}

{% step %}
### Rotate only if the product needs it

Rotate to match a slanted surface or an intended design. On a straight product, rotation looks like a mistake.
{% endstep %}

{% step %}
### Test the extremes

In the **Preview**, try a one-character entry, the longest allowed entry, a tall photo, and a wide photo. Placement problems show up at the extremes.
{% endstep %}
{% endstepper %}

## Opacity

<table><thead><tr><th width="230">Value</th><th>Use for</th></tr></thead><tbody><tr><td><code>100</code></td><td>Almost everything. Print and engraving are solid</td></tr><tr><td><code>60</code> to <code>90</code></td><td>Etched glass, watermarks, tone-on-tone printing</td></tr><tr><td>Below <code>50</code></td><td>Rarely. Customers may think their entry did not register</td></tr></tbody></table>

If an element does not sit well on the photo, adjust its color before lowering opacity.

## Several elements on one image

<table><thead><tr><th width="290">Goal</th><th>How</th></tr></thead><tbody><tr><td>A name above a date</td><td>Same <strong>X position</strong>, different <strong>Y position</strong>, for example 40 and 55</td></tr><tr><td>Two elements side by side</td><td>Same <strong>Y position</strong>, different <strong>X position</strong>, for example 30 and 70</td></tr><tr><td>Text over an uploaded photo</td><td>Place the text inside the photo's area and give it a <a href="effects.md#stroke">stroke</a></td></tr><tr><td>Reaching an element under another one</td><td>Use <strong>Elements</strong> in the editor toolbar. See <a href="../editor.md#elements">Elements</a></td></tr></tbody></table>

## Notes

* Positions are relative to the background, so they only line up across products whose photos are framed the same way. See [Choosing the background](../setup.md#choosing-the-background).
* If customers can move the element, your position is their starting point. See [What customers can change](customer-controls.md).
* A [print area](clip-area.md) limits where the element can appear. Use one whenever customers can move it.
* For text on a round surface, use [Curve](curve-and-auto-fit.md#curve) instead of rotation.
