---
description: One personalised product built from an empty option set to a live storefront — a mug with a curved name and an uploaded photo.
icon: mug-hot
---

# Walkthrough: custom printed mug

A complete build, in the order you would actually do it. The product is a printed mug that takes a curved name and a customer photo.

Substitute your own product and wording as you go. Everything here applies just as well to a frame, a t-shirt, or a pendant.

## Before you start

* A mug product in Shopify with a **flat, front-on photograph** — this matters more than any setting on this page.
* The Personalizer on your plan. See [Compare plans](../plans/compare-plans.md).
* The [app embed](../getting-started/enable-the-app-embed.md) enabled on your live theme.

## Steps

{% stepper %}
{% step %}
### Create the option set and set the background

**Option Sets** > **Create option set** > **Create from scratch**. Name it `Printed mug`.

Rename the starting section to `Personalise your mug`.

Then, before anything else, open **Change background** in the preview panel:

* **Background**: **Product image**
* **Apply to**: **First product image only**
* Select your mug product to preview against

Everything you position from here is measured against that photograph, which is why this comes first. See [Set the preview background](set-the-background.md).
{% endstep %}

{% step %}
### Add the name field

Add a [Text](../option-types/input-types/text.md) option and set, on **Basic Settings**:

<table><thead><tr><th width="230">Field</th><th width="180">Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Label</strong> / <strong>Name</strong></td><td><code>Name on mug</code></td><td>Readable on the order</td></tr><tr><td><strong>Max character</strong></td><td><code>12</code></td><td>What actually fits on the printable band</td></tr><tr><td><strong>Character counter</strong></td><td><strong>Show</strong></td><td>They see the limit approaching</td></tr><tr><td><strong>Default value</strong></td><td><code>Your name</code></td><td>So the preview is never empty</td></tr><tr><td><strong>Text transform</strong></td><td><strong>Capitalized</strong></td><td>Every mug looks consistent</td></tr><tr><td><strong>Help text</strong></td><td><code>Up to 12 characters. Printed items cannot be returned.</code></td><td>No surprises</td></tr></tbody></table>
{% endstep %}

{% step %}
### Turn on the Personalizer for the name

Open **Personalizer Settings** and turn on **Enable personalize**. Then style it:

<table><thead><tr><th width="230">Setting</th><th width="180">Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Text color</strong></td><td>Your print colour</td><td>Realistic rather than decorative</td></tr><tr><td><strong>Font size</strong></td><td><code>7</code>, adjusted by eye</td><td>Set it against your real photo</td></tr><tr><td><strong>Font family</strong></td><td><strong>Custom</strong>, your print font</td><td>The preview then matches production. See <a href="fonts.md">Fonts</a></td></tr><tr><td><strong>Custom Effect</strong></td><td><strong>No effect</strong></td><td>Printing is flat</td></tr></tbody></table>
{% endstep %}

{% step %}
### Curve the name to the mug

Still on **Personalizer Settings**:

* **Curve** — increase it until the text follows the mug's curvature in your photograph. There is no correct number; set it by eye.
* **Auto-fit max width** — on, with **Max width** matching the printable band.
* **X-Axis** — `50`, centred.
* **Y-Axis** — wherever the printable band sits, often around `45`.

Then test in the preview with a one-character name and a twelve-character one. The short one should look right; the long one should shrink rather than overflow.

See [Curve and auto-fit width](curve-and-auto-fit.md).
{% endstep %}

{% step %}
### Add the photo upload

Add a [File upload](../option-types/input-types/file-upload.md) option:

<table><thead><tr><th width="230">Field</th><th width="180">Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Label</strong> / <strong>Name</strong></td><td><code>Photo on mug</code></td><td></td></tr><tr><td><strong>Required field</strong></td><td>Off</td><td>Some customers want the name only</td></tr><tr><td><strong>Allowed extensions</strong></td><td><code>jpg</code>, <code>jpeg</code>, <code>png</code></td><td>What you can print from</td></tr><tr><td><strong>Enable image editor</strong></td><td>On</td><td>They crop their own photo, so you get a usable file</td></tr><tr><td><strong>Help text</strong></td><td><code>JPG or PNG, at least 1200 × 1200 pixels.</code></td><td>Sets the quality bar</td></tr></tbody></table>
{% endstep %}

{% step %}
### Turn on the Personalizer for the photo

On its **Personalizer Settings**:

<table><thead><tr><th width="230">Setting</th><th width="180">Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Image shape</strong></td><td>A rectangle matching your print panel</td><td>The photo reads as printed, not pasted</td></tr><tr><td><strong>Background mode</strong></td><td><strong>Cover</strong></td><td>Fills the panel whatever shape they upload</td></tr><tr><td><strong>Width</strong> / <strong>Height</strong></td><td>Sized to the panel</td><td></td></tr><tr><td><strong>X-Axis</strong> / <strong>Y-Axis</strong></td><td>Positioned on the panel, below the name</td><td>So the two layers do not overlap</td></tr><tr><td><strong>Enable clip area</strong></td><td>On, matching the print panel, outline visible</td><td>Nothing can stray off the printable area</td></tr><tr><td><strong>Allow customers to</strong></td><td><strong>Change position</strong>, <strong>Resize</strong></td><td>Only they know which part of their photo matters</td></tr><tr><td><strong>Rotate</strong></td><td>Off</td><td>A rotated photo on a mug looks like a mistake</td></tr></tbody></table>

See [Image layers](image-layers.md), [Clip area](clip-area.md), and [Customer controls](customer-controls.md).
{% endstep %}

{% step %}
### Price the personalisation

Put the charge on the name field, since every personalised mug has one. On its **Basic Settings**, open **Price**, choose **Automatically generate product**, and enter your fee — so the printing is counted as a product in your reporting.

Set **Advanced settings** to **Default**, since each mug is printed individually.

See [Automatically generate a product](../add-on-pricing/auto-generate-a-product.md).
{% endstep %}

{% step %}
### Add a photo surcharge, only when a photo is used

Add a second [Switch](../option-types/input-types/switch.md) or use conditional logic on a priced option. The simplest arrangement:

* Add a Switch labelled `Photo printing`, priced, **One time charge**
* Put it **above** the upload option
* Give the upload option a conditional rule: Show · All · `Photo printing` — **is enabled**

Now the upload only appears once they have opted in and paid for it. See [Conditional logic](../conditional-logic/README.md).
{% endstep %}

{% step %}
### Assign, save, activate

On **Assign products**, use **Automatic Rules** with `Product tag — is equal to — printed-mug`, so new mugs pick the set up automatically.

Save. Set the status to **Active** and confirm **Online Store** is ticked.
{% endstep %}

{% step %}
### Test on a real product page

**View in Store**, then work through it as a customer would:

1. Type a short name. Does it sit right on the curve?
2. Type a twelve-character name. Does it shrink and stay inside the band?
3. Turn on photo printing. Does the upload appear?
4. Upload a portrait photo and a landscape one. Does **Cover** handle both?
5. Drag the photo to the edge. Is it clipped at the panel boundary?
6. Check the price after each step.
7. Repeat the whole thing on a phone.
{% endstep %}

{% step %}
### Place a test order and check what your team receives

Add it to the cart, check **Preview Your Design** shows what you expect, and place the order.

On the order in Shopify admin you should see `Name on mug`, `Photo printing`, and a link to the uploaded file. If the names read poorly, fix them now rather than after a hundred orders.

Then consider an [automation](../automations/README.md) so those details reach your production team without anybody opening Shopify admin.
{% endstep %}
{% endstepper %}

## What to change for other products

<table><thead><tr><th width="290">Product</th><th>Differences</th></tr></thead><tbody><tr><td>A photo frame</td><td>No curve. One image layer, clip area matching the aperture, both customer controls on</td></tr><tr><td>An engraved pen</td><td>Curve for the barrel, a very tight character limit, no image layer</td></tr><tr><td>A t-shirt</td><td>No curve, larger print area, artwork upload plus optional text</td></tr><tr><td>A ring band</td><td>A strong curve, a five-character limit, auto-fit essential</td></tr><tr><td>A jersey</td><td>A <a href="../option-types/input-types/number.md">Number</a> layer for the number and a Text layer for the name, positioned separately</td></tr></tbody></table>
