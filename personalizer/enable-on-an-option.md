---
description: Turn the Personalizer on for one option, and understand what appears when you do.
icon: toggle-on
---

# Enable personalizer on an option

The background belongs to the option set; the layers belong to individual options. This is where you turn a layer on.

## Before you start

* A background is configured for the option set — see [Set the preview background](set-the-background.md).
* The option is one of the [twelve supported types](README.md#the-twelve-supported-option-types).
* The Personalizer is plan-gated. If the tab is unavailable, see [Compare plans](../plans/compare-plans.md).

## Steps

{% stepper %}
{% step %}
### Select the option

Open the option whose content should appear on the product photo.
{% endstep %}

{% step %}
### Open the Personalizer Settings tab

It sits beside **Basic Settings** and **Advanced Settings**. It only appears on supported types — if it is missing, the type does not support it.
{% endstep %}

{% step %}
### Turn on Enable personalize

Everything else on the tab appears once this is on. With it off, the tab holds nothing but the switch.
{% endstep %}

{% step %}
### Style the layer

For a text layer: colour, size, style, font, and effects. For an image layer: shape and fit mode. See [Text layers](text-layers.md) and [Image layers](image-layers.md).
{% endstep %}

{% step %}
### Position it

Set the axes, and the size where the type offers it. See [Position, size, and rotation](position-size-rotation.md).
{% endstep %}

{% step %}
### Decide what the customer may change

[Customer controls](customer-controls.md), plus a [clip area](clip-area.md) if you are giving them freedom.
{% endstep %}

{% step %}
### Test with a realistic entry

In the builder preview, type something a real customer would — a full name, not "test". Then check a very long entry and a very short one.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: pp-enable-tab | App admin → builder → option Text → tab Personalizer Settings | Switch "Enable personalize" đã bật, các nhóm setting hiện ra bên dưới | Khoanh switch -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Personalizer Settings tab with Enable personalize turned on and its settings revealed"><figcaption><p>Nothing on the tab appears until the switch is on.</p></figcaption></figure>

## What you get, by option type

The settings offered depend on whether the option produces text or an image.

<table><thead><tr><th width="290">Setting group</th><th width="230">Text, Textarea, Number</th><th>File upload and the eight selection types</th></tr></thead><tbody><tr><td>Colour, font size, font style, font family</td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Text alignment</td><td>Textarea only</td><td>No</td></tr><tr><td>Text effects</td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Curve and auto-fit max width</td><td>Text and Number only</td><td>No</td></tr><tr><td>Image shape and background mode</td><td>No</td><td><strong>Yes</strong></td></tr><tr><td>Width and height</td><td>Textarea only</td><td><strong>Yes</strong></td></tr><tr><td>X-Axis, Y-Axis, opacity, rotation</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td></tr><tr><td>Clip area</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td></tr><tr><td>Allow customers to</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td></tr></tbody></table>

The pattern: Text and Number are single lines, so they get curve and auto-fit instead of width and height. Textarea is a block, so it gets alignment, width, and height. Image types get shape and fit mode.

## Give text layers a default value

A text layer with nothing in it draws nothing, so the preview looks broken until the customer types.

Set a **Default value** on **Basic Settings** — `Your name`, `Your text` — and the preview always has something to show. It is the single most effective thing you can do to make a personalised product page look finished.

The default is also what the customer submits if they change nothing, so choose something sensible rather than `test`.

## Several personalised options on one product

Normal, and where most of the design effort goes.

<table><thead><tr><th width="290">Combination</th><th>What to watch</th></tr></thead><tbody><tr><td>A name and a date</td><td>Different <strong>Y-Axis</strong> values so they do not overlap</td></tr><tr><td>Text plus an uploaded photo</td><td>Contrast — dark text over a dark photo disappears. Consider a <a href="effects.md">stroke effect</a></td></tr><tr><td>Two alternative designs</td><td><a href="../conditional-logic/README.md">Conditional logic</a> so only one is ever visible</td></tr><tr><td>Many layers</td><td>Performance on older phones. Keep it to what the product really needs</td></tr></tbody></table>

Remember that a hidden option draws no layer, so conditional logic is the clean way to switch between alternatives.

## Notes

* Turning the Personalizer off leaves the option working normally — it just stops drawing on the photo. Nothing else is lost.
* The layer's settings are per option, so the same option type can be configured differently in two places.
* The Personalizer does not change what reaches the order in terms of the customer's text or file — that travels as an option value either way. What it adds is the visual design record. See [Designs in cart and orders](cart-and-orders.md).

## Troubleshooting

<details>
<summary>There is no Personalizer Settings tab</summary>

The option type does not support it. Twelve types do — see the [overview](README.md#the-twelve-supported-option-types).
</details>

<details>
<summary>The tab is there but greyed out</summary>

The Personalizer is not in your plan. See [Compare plans](../plans/compare-plans.md).
</details>

<details>
<summary>The tab is empty apart from a switch</summary>

Turn on **Enable personalize**.
</details>

<details>
<summary>Nothing appears on the product photo</summary>

Three things: the option set needs a background; a text layer needs either a default value or something typed; an image layer needs a choice made or a file uploaded.
</details>

<details>
<summary>Two layers are on top of each other</summary>

They share the same position. Change one layer's **Y-Axis**.
</details>
