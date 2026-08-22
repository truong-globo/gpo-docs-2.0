---
description: Bend a single line of text along an arc, and shrink it automatically when it gets too long.
icon: bezier-curve
---

# Curve and auto-fit width

Two settings that exist only on single-line text layers, because they are the answers to the two problems single lines have: curved surfaces, and text that gets longer than the space.

**Applies to:** [Text](../option-types/input-types/text.md) and [Number](../option-types/input-types/number.md) only. [Textarea](../option-types/input-types/textarea.md) has **Width** and **Height** instead — see [Position, size, and rotation](position-size-rotation.md).

## Curve

Bends the line of text along an arc.

<table><thead><tr><th width="180">Range</th><th width="150">Default</th><th>Behaviour</th></tr></thead><tbody><tr><td>-100 to 100</td><td><code>0</code></td><td><code>0</code> is a straight line. Positive values curve one way, negative the other</td></tr></tbody></table>

**What it is for**

Text on anything round. A mug, a plate rim, a ring band, a bangle, a badge, a bottle label. On these products a straight line of text looks pasted on; a curved one looks printed.

**Getting it right**

<table><thead><tr><th width="230">Try</th><th>For</th></tr></thead><tbody><tr><td>A small value, 10 to 30</td><td>A gentle bend, matching a large-diameter surface such as a plate rim</td></tr><tr><td>A larger value</td><td>A tighter curve, for a ring band or a small bangle</td></tr><tr><td>A negative value</td><td>The curve bending the other way — text below the centre of a circle rather than above it</td></tr></tbody></table>

Set it by eye against your real product photograph. The correct value is entirely a function of the curvature in your image, so there is no universal number.

<!-- SCREENSHOT: pp-curve | App admin → builder → option Text → Personalizer Settings | Slider Curve và preview text đang uốn theo cung trên ảnh sản phẩm | Khoanh slider Curve và text uốn trong preview -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Curve slider with the preview text bent along an arc on the product photo"><figcaption><p>Curve is what makes text on a mug or a ring look printed rather than pasted on.</p></figcaption></figure>

## Auto-fit max width

Shrinks the font automatically when the text gets wider than a limit you set.

<table><thead><tr><th width="230">Setting</th><th width="150">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Auto-fit max width</strong></td><td>Off</td><td>Turns the behaviour on, and reveals the setting below</td></tr><tr><td><strong>Max width</strong></td><td><code>50</code>%</td><td>The widest the text may become, as a share of the image</td></tr></tbody></table>

**Why you want it**

Without it, a text layer grows as the customer types. A short name sits neatly on the engraving plate; a long one runs off the edge of the product, and the preview looks broken exactly when the customer is deciding whether to buy.

With it on, long entries shrink to fit instead. The result stays inside the area you allowed, whatever they type.

{% stepper %}
{% step %}
### Turn on Auto-fit max width

On the text layer's **Personalizer Settings**.
{% endstep %}

{% step %}
### Set Max width to the real printable width

As a percentage of the image. If the engraving plate occupies about a third of the photo's width, start at `33`.
{% endstep %}

{% step %}
### Test with your longest allowed entry

Type the maximum your **Max character** limit permits. The text should shrink and stay inside the area.
{% endstep %}

{% step %}
### Check it is still legible at that size

If a maximum-length entry becomes too small to read, your **Max character** limit is too generous for the space. Lower it.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Turn this on for any engraving or embroidery field. It is the single most effective setting for making a personalisation preview robust, because you cannot predict what customers will type.
{% endhint %}

## Using both together

They interact, and the interaction is deliberate: **with Curve enabled, the Max width is treated as the diameter of the curve.**

So on a curved product the two settings work as a pair — the max width defines how big the arc is, and the curve defines how much the text bends around it.

<table><thead><tr><th width="290">Product</th><th>Setup</th></tr></thead><tbody><tr><td>A mug with text around the side</td><td>Curve set to match the mug's curvature, auto-fit on with a max width matching the printable band</td></tr><tr><td>A ring band</td><td>A stronger curve, a small max width, and a tight <strong>Max character</strong> limit</td></tr><tr><td>A flat engraved plate</td><td>Curve at <code>0</code>, auto-fit on</td></tr><tr><td>A jersey number</td><td>Curve at <code>0</code>, auto-fit off — one or two characters cannot overflow</td></tr></tbody></table>

## Pair them with a character limit

These settings make long entries *fit*; they do not make long entries *sensible*. A twelve-character plate with a forty-character entry will shrink the text to something unreadable and unproducible.

Always set a [Max character](../option-types/shared-settings/limits.md#min-and-max-character) limit that matches what you can physically produce, and turn on the [Character counter](../option-types/shared-settings/limits.md#character-counter) so the customer can see it.

## Notes

* Both settings are on Text and Number only.
* Curve has no effect on Textarea — a multi-line block cannot follow a single arc.
* Auto-fit only shrinks. It never enlarges short text to fill the space.
* Neither changes what is produced. They shape the preview so it matches what you will produce.

## Troubleshooting

<details>
<summary>I cannot find Curve or Auto-fit</summary>

They exist on Text and Number only. On Textarea, use **Width** and **Height**.
</details>

<details>
<summary>Max width is not visible</summary>

Turn on **Auto-fit max width** first.
</details>

<details>
<summary>Long text still overflows</summary>

Auto-fit is off, or the max width is larger than the area you meant. Also check that a **Max character** limit is set.
</details>

<details>
<summary>Long text shrinks to something unreadable</summary>

Your character limit is too generous for the space. Lower **Max character** to what genuinely fits.
</details>

<details>
<summary>The curve looks wrong on the product</summary>

Adjust by eye, and try the negative equivalent — the arc may need to bend the other way. If the photograph is at an angle, no curve value will look right; use a flat-on photograph.
</details>

<details>
<summary>Curve and auto-fit together behave unexpectedly</summary>

With curve on, max width is the curve's diameter rather than a plain width limit. Adjust the two together rather than independently.
</details>
