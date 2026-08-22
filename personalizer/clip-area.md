---
description: Define a region a layer cannot leave — the setting that makes customer freedom safe.
icon: crop-simple
---

# Clip area

A clip area is a rectangle you define on the image. Anything of the layer outside it is not drawn.

It is what lets you hand shoppers control of a layer without risking a preview — and an order — showing personalisation somewhere you cannot produce it.

**Applies to:** all twelve Personalizer-capable option types, text and image alike.

## The settings

<table><thead><tr><th width="230">Setting</th><th width="150">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Enable clip area</strong></td><td>Off</td><td>Turns it on and reveals the rest</td></tr><tr><td><strong>Clip area X position</strong></td><td><code>50</code>%</td><td>Horizontal position of the region</td></tr><tr><td><strong>Clip area Y position</strong></td><td><code>50</code>%</td><td>Vertical position of the region</td></tr><tr><td><strong>Clip area width</strong></td><td><code>50</code>%</td><td>How wide the region is</td></tr><tr><td><strong>Clip area height</strong></td><td><code>50</code>%</td><td>How tall the region is</td></tr><tr><td><strong>Clip area rotation</strong></td><td><code>0</code>°</td><td>Rotates the region, from -180 to 180</td></tr><tr><td><strong>Hide clip area</strong></td><td>Off</td><td>Hides the region's outline from the shopper</td></tr></tbody></table>

All values are percentages of the image, like [layer positions](position-size-rotation.md).

<!-- SCREENSHOT: pp-clip-area | App admin → builder → option có personalizer | Nhóm setting clip area + preview hiện vùng clip có viền | Khoanh vùng clip trong preview -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The clip area settings with the region outlined on the product preview"><figcaption><p>The clip area is visible while you position it, and can be hidden from shoppers.</p></figcaption></figure>

## What it is for

<table><thead><tr><th width="290">Situation</th><th>Why a clip area helps</th></tr></thead><tbody><tr><td>You let customers drag a layer</td><td>They cannot drag it off the printable area</td></tr><tr><td>You let customers resize a layer</td><td>An oversized layer is cropped instead of covering the whole product</td></tr><tr><td>An uploaded photo goes into a fixed window</td><td>The photo fills the window and nothing spills outside it</td></tr><tr><td>Your printable area is not the whole product</td><td>The preview shows the real boundary</td></tr><tr><td>Text must stay inside an engraved panel</td><td>Long entries are cut at the panel edge rather than running over the product</td></tr></tbody></table>

{% hint style="info" %}
If you turn on any of the [customer controls](customer-controls.md) — move, resize, rotate — set a clip area as well. Without one, a shopper can place their design anywhere on the image, including places you cannot print.
{% endhint %}

## How to set one up

{% stepper %}
{% step %}
### Turn on Enable clip area

The region appears in the preview with a visible outline.
{% endstep %}

{% step %}
### Size it to your real printable area

Set **Clip area width** and **Clip area height** to match the area you can actually produce on.
{% endstep %}

{% step %}
### Move it into place

**Clip area X position** and **Clip area Y position**. Line the outline up with the printable area in your photograph.
{% endstep %}

{% step %}
### Rotate it if the surface is not square

**Clip area rotation** matches the region to an angled panel.
{% endstep %}

{% step %}
### Position the layer inside it

The layer's own position is separate. Put it where you want the design to start.
{% endstep %}

{% step %}
### Test the boundary

Type a long entry, or drag the layer if you allowed that, and confirm it is cut at the edge of the region rather than spilling out.
{% endstep %}

{% step %}
### Decide whether shoppers see the outline

**Hide clip area** removes it from the shopper's view. See below.
{% endstep %}
{% endstepper %}

## Hide clip area

<table><thead><tr><th width="230">Setting</th><th>Effect on the shopper</th><th>Use when</th></tr></thead><tbody><tr><td>Off</td><td>They see the region's outline</td><td>You want them to understand where they can place things — useful when they can drag</td></tr><tr><td>On</td><td>The outline is invisible; the cropping still happens</td><td>The boundary is obvious from the product itself, and an outline would look like a flaw</td></tr></tbody></table>

If you let shoppers move a layer, leaving the outline **visible** is usually kinder. It tells them where the limits are instead of letting them discover it by having their design cut off.

## Clip area or auto-fit?

Both stop text escaping, differently.

<table><thead><tr><th width="230"></th><th width="290">Clip area</th><th>Auto-fit max width</th></tr></thead><tbody><tr><td>What it does</td><td>Cuts off whatever is outside the region</td><td>Shrinks the text so it fits</td></tr><tr><td>Applies to</td><td>Text and image layers</td><td><a href="../option-types/input-types/text.md">Text</a> and <a href="../option-types/input-types/number.md">Number</a> only</td></tr><tr><td>Result with a long entry</td><td>Truncated in the preview</td><td>Smaller but complete</td></tr><tr><td>Best for</td><td>Enforcing a boundary, especially with customer controls</td><td>Keeping the whole entry visible</td></tr></tbody></table>

For engraving text, [auto-fit](curve-and-auto-fit.md#auto-fit-max-width) is usually the better first choice — shrinking is friendlier than cutting. Use a clip area as well when customers can move things, or when the boundary is a hard production limit.

## Notes

* One clip area per layer. Several layers can each have their own.
* The clip area does not move with the layer. It is a fixed window; the layer moves inside it.
* It affects the preview only, not what is produced. But since it should describe your real printable area, matching them is the point.
* Rotating the region and rotating the layer are separate settings.

## Troubleshooting

<details>
<summary>The clip settings are not visible</summary>

Turn on **Enable clip area** first.
</details>

<details>
<summary>My layer has disappeared</summary>

It is outside the clip area entirely. Move the layer into the region, or enlarge the region.
</details>

<details>
<summary>Text is being cut off</summary>

That is the clip area working. If you would rather it shrank, turn on [Auto-fit max width](curve-and-auto-fit.md#auto-fit-max-width) instead, or enlarge the region.
</details>

<details>
<summary>Customers complain their design gets cut</summary>

Leave the outline visible by turning **Hide clip area** off, so they can see the boundary while they position it.
</details>

<details>
<summary>An uploaded photo does not fill the window</summary>

That is the **Background mode**, not the clip area. Try **Cover**. See [Image layers](image-layers.md).
</details>

<details>
<summary>The region does not line up with an angled panel</summary>

Use **Clip area rotation**.
</details>

## Next steps

* [Customer controls](customer-controls.md) — the reason clip areas exist.
* [Image layers](image-layers.md)
* [Curve and auto-fit width](curve-and-auto-fit.md)
