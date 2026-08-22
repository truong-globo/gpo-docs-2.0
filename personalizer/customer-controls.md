---
description: Let shoppers move, resize, and rotate a layer themselves — and how to do it without breaking your production.
icon: hand
---

# Customer controls

**Allow customers to** decides which adjustments the shopper can make to a layer directly on the product image.

It is the difference between a preview they look at and a design they make. It is also the setting most capable of producing orders you cannot fulfil, so it comes with a companion setting you should always use alongside it.

**Applies to:** all twelve Personalizer-capable option types.

## The three permissions

<table><thead><tr><th width="230">Permission</th><th>What the shopper can do</th></tr></thead><tbody><tr><td><strong>Change position</strong></td><td>Drag the layer around the image</td></tr><tr><td><strong>Resize</strong></td><td>Make the layer larger or smaller</td></tr><tr><td><strong>Rotate</strong></td><td>Turn the layer</td></tr></tbody></table>

All three are off by default, and you can enable any combination. With none on, the layer sits exactly where you placed it and the shopper only changes its content.

<!-- SCREENSHOT: pp-customer-controls | App admin → builder → option có personalizer | Nhóm "Allow customers to" với 3 checkbox | Khoanh nhóm này -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Allow customers to setting with change position, resize, and rotate"><figcaption><p>Three permissions, all off by default.</p></figcaption></figure>

## Always pair them with a clip area

{% hint style="warning" %}
If you enable any of these, set a [clip area](clip-area.md) as well.

Without one, a shopper can drag their photo onto the handle of the mug, resize their text to cover the whole product, or rotate a design to an angle you cannot print. The preview will show it, they will order it, and you will have to explain why you cannot make it.

A clip area confines their freedom to the area you can actually produce on.
{% endhint %}

Leave the clip area's outline **visible** — do not turn on **Hide clip area** — when customers can drag. It shows them where they can work, instead of letting them find out by having their design cut off.

## When to enable them

<table><thead><tr><th width="290">Situation</th><th>Enable</th><th>Why</th></tr></thead><tbody><tr><td>A customer photo in a frame</td><td><strong>Change position</strong>, <strong>Resize</strong></td><td>Only they know which part of their photo matters</td></tr><tr><td>A logo on a garment</td><td><strong>Change position</strong>, <strong>Resize</strong></td><td>Placement is part of what they are buying</td></tr><tr><td>An engraved name on a plate</td><td>Nothing</td><td>You know where the plate is. Let them type, not position</td></tr><tr><td>A design chosen from your own list</td><td>Nothing</td><td>You positioned it correctly already</td></tr><tr><td>A free-form collage or sticker layout</td><td>All three</td><td>The arrangement is the product</td></tr><tr><td>Text on a curved surface</td><td>Nothing</td><td><a href="curve-and-auto-fit.md">Curve</a> handles it better than a shopper can</td></tr></tbody></table>

The pattern: enable them where **placement is the customer's creative decision**, and leave them off where placement is **your production constraint**.

## Rotation deserves particular care

Rotation is the permission most likely to cause problems. A rotated engraving is often simply not producible, and a slightly rotated photo in a frame looks like an accident rather than a choice.

Enable it only where an angled result is genuinely a valid product — a free-form collage, a scattered sticker layout, a hand-arranged design.

## What the customer sees

With any permission on, selecting the layer on the product image gives them handles to work with. The app also provides short on-screen guidance — telling them to drag to move, and to use the handles to resize or rotate.

That wording is part of the widget text and can be reworded per language in **Settings > Translations**. See [Translate widget text](../translations/translate-widget-text.md).

## Where their adjustments go

Their final arrangement is part of the design that reaches the order, so you can produce what they set up rather than what you configured.

Your own position, size, and rotation settings become the **starting point** they adjust from — so it is still worth setting them sensibly. A layer that starts in the right place needs less adjusting, and a shopper who does not need to adjust anything is a shopper who does not get it wrong.

See [Designs in cart and orders](cart-and-orders.md).

## A worked configuration

A photo frame where the customer positions their own photo:

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Option</td><td>File upload, required, image editor on</td></tr><tr><td>Image shape</td><td>Matching the frame aperture</td></tr><tr><td>Background mode</td><td><strong>Cover</strong></td></tr><tr><td>Position and size</td><td>Filling the aperture — a sensible starting point</td></tr><tr><td>Clip area</td><td>On, matching the aperture, outline visible</td></tr><tr><td>Allow customers to</td><td><strong>Change position</strong>, <strong>Resize</strong></td></tr><tr><td>Rotate</td><td>Off</td></tr><tr><td>Help text</td><td><code>Drag your photo to position it. Anything outside the frame will not be printed.</code></td></tr></tbody></table>

## Notes

* Permissions are per layer, so one layer can be adjustable while another is fixed.
* They affect the preview and the recorded design, not what other layers do.
* Touch and mouse both work, but a small target on a phone is fiddly — do not rely on precise dragging on mobile.
* Say in help text what happens to anything outside the printable area. It prevents most disputes.

## Troubleshooting

<details>
<summary>Customers cannot move the layer</summary>

Turn on **Change position**. If it is on, check they are selecting the layer first.
</details>

<details>
<summary>Customers are placing designs where I cannot print</summary>

Add a [clip area](clip-area.md) and leave its outline visible.
</details>

<details>
<summary>Designs arrive rotated and unproducible</summary>

Turn **Rotate** off. Very few products genuinely need it.
</details>

<details>
<summary>Customers resize text until it is unreadable</summary>

Turn **Resize** off for text layers. [Auto-fit max width](curve-and-auto-fit.md#auto-fit-max-width) handles sizing better than a shopper can.
</details>

<details>
<summary>It is fiddly on mobile</summary>

Make the starting position and size close to what most customers want, so adjusting is optional rather than necessary.
</details>

<details>
<summary>The on-screen instructions do not suit my store</summary>

Reword them in **Settings > Translations**. See [Translate widget text](../translations/translate-widget-text.md).
</details>
