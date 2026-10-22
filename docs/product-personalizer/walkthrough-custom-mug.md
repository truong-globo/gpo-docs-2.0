---
description: >-
  One personalized product built from an empty option set to a live storefront:
  a mug with a curved name and an uploaded photo.
icon: mug-hot
---

# Walkthrough: custom printed mug

A complete setup, in the order you would build it. The product is a printed mug with a curved name and a customer photo.

Replace the product and wording with your own. The same method works for a tumbler, a plate, or a pendant.

## Before you start

* A mug product with a **flat, front-facing photo** first in its gallery. This matters more than any setting.
* The Personalizer available on your plan. See [Compare plans](../plans-and-billing/compare-plans.md).
* The [app embed](../getting-started/enable-the-app-embed.md) turned on in your live theme.

## Steps

{% stepper %}
{% step %}
### Create the option set

Go to **Option Sets** > **Create option set** > **Create from scratch**. Name it `Printed mug`, and rename the starting section to `Personalize your mug`.
{% endstep %}

{% step %}
### Add the name field

Add a [Text](../option-types/input-types/text.md) option and set on the **Basic** tab:

<table><thead><tr><th width="230">Field</th><th width="180">Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Name on product page</strong> / <strong>Name on cart page</strong></td><td><code>Name on mug</code></td><td>Clear for the customer and on the order</td></tr><tr><td><strong>Max character</strong></td><td><code>12</code></td><td>What fits on the printable band</td></tr><tr><td><strong>Character counter</strong></td><td><strong>Show</strong></td><td>Customers see the limit approaching</td></tr><tr><td><strong>Default value</strong></td><td><code>Your name</code></td><td>So the design is never empty</td></tr><tr><td><strong>Text transform</strong></td><td><strong>Capitalized</strong></td><td>Every mug looks consistent</td></tr><tr><td><strong>Help text</strong></td><td><code>Up to 12 characters. Printed items cannot be returned.</code></td><td>No surprises</td></tr></tbody></table>
{% endstep %}

{% step %}
### Turn on the Personalizer and set the background

Open the option's **Personalizer** tab and turn on the **Personalizer** switch. The Personalizer editor appears.

Select **Change background** and choose:

* **Background**: **Product image**
* **Apply to**: **First product image only**
* Your mug product, to work against

Every position from here on is measured against that photo, so set it now. See [Choosing the background](setup.md#choosing-the-background).
{% endstep %}

{% step %}
### Style the name

In **Text style**:

<table><thead><tr><th width="230">Setting</th><th width="180">Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Color</strong></td><td>Your print color</td><td>Realistic rather than decorative</td></tr><tr><td><strong>Font size</strong></td><td><code>7</code>, adjusted by eye</td><td>Set it against your real photo</td></tr><tr><td><strong>Font family</strong></td><td><strong>Custom</strong>, your print font</td><td>The design then matches production. See <a href="layer-settings/fonts.md">Fonts</a></td></tr><tr><td><strong>Effect</strong></td><td><strong>No effect</strong></td><td>Printing is flat</td></tr></tbody></table>
{% endstep %}

{% step %}
### Curve the name to the mug

Still in **Text style**:

* **Curve**: raise it until the text follows the curve of the mug in your photo. The right value depends on your image.
* **Auto-fit max width**: on, with **Max width** set to the printable band.

Then drag the name on the canvas to the printable band, or set **X position** `50` and **Y position** around `45` in **Position and size**.

In the **Preview**, type a one-character name and a twelve-character name. The long name should shrink rather than run past the band. See [Curve and auto-fit width](layer-settings/curve-and-auto-fit.md).
{% endstep %}

{% step %}
### Add the photo upload

Add a [File upload](../option-types/input-types/file-upload.md) option:

<table><thead><tr><th width="230">Field</th><th width="180">Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Name on product page</strong> / <strong>Name on cart page</strong></td><td><code>Photo on mug</code></td><td></td></tr><tr><td><strong>Required field</strong></td><td>Off</td><td>Some customers want the name only</td></tr><tr><td><strong>Allowed extensions</strong></td><td><code>jpg</code>, <code>jpeg</code>, <code>png</code></td><td>Files you can print from</td></tr><tr><td><strong>Enable image editor</strong></td><td>On</td><td>Customers crop their own photo, so you get a usable file</td></tr><tr><td><strong>Help text</strong></td><td><code>JPG or PNG, at least 1200 × 1200 pixels.</code></td><td>Sets the quality you need</td></tr></tbody></table>
{% endstep %}

{% step %}
### Print the photo

Select **Add element** in the editor toolbar and pick `Photo on mug`. Then, on its **Personalizer** tab:

<table><thead><tr><th width="230">Card</th><th width="180">Setting</th><th>Value</th></tr></thead><tbody><tr><td><strong>Shape and fill</strong></td><td><strong>Image shape</strong></td><td>A rectangle matching your print panel</td></tr><tr><td></td><td><strong>Background mode</strong></td><td><strong>Cover</strong>, so any photo fills the panel</td></tr><tr><td><strong>Position and size</strong></td><td><strong>Width</strong>, <strong>Height</strong>, position</td><td>On the panel, below the name, so the two do not overlap</td></tr><tr><td><strong>Print area</strong></td><td><strong>Crop area</strong></td><td>On, matching the print panel, outline visible</td></tr><tr><td><strong>What customers can change</strong></td><td><strong>Change position</strong>, <strong>Resize</strong></td><td>On. Only customers know which part of their photo matters</td></tr><tr><td></td><td><strong>Rotate</strong></td><td>Off. A turned photo on a mug looks like a mistake</td></tr></tbody></table>

See [Shape and fill](layer-settings/image-layers.md), [Print area](layer-settings/clip-area.md), and [What customers can change](layer-settings/customer-controls.md).
{% endstep %}

{% step %}
### Price the personalization

Put the charge on the name field, because every personalized mug has one. On its **Basic** tab, open **Price**, select **New product**, and enter your fee. Set **Add-on quantity** to **Default**, because each mug is printed individually. See [New product](../add-on-pricing/auto-generate-a-product.md).
{% endstep %}

{% step %}
### Charge for the photo only when it is used

Add a [Switch](../option-types/input-types/switch.md) labeled `Photo printing`, priced as a one-time charge, **above** the upload option. Give the upload option a conditional rule: Show · All · `Photo printing` · **is enabled**.

The upload now appears only after the customer turns on photo printing. A hidden option prints nothing, so the design shows the name only. See [Conditional logic](../conditional-logic/conditional-logic.md).
{% endstep %}

{% step %}
### Assign, save, activate

On **Setup flow** > **Assign products**, use **Automatic Rules** with `Product tag · is equal to · printed-mug`, so new mugs use the option set automatically.

Select **Save**. Set the status to **Active** and confirm **Online Store** is ticked.
{% endstep %}

{% step %}
### Test on a real product page

Select **View in Store**, then check as a customer would:

1. A short name follows the curve.
2. A twelve-character name shrinks and stays on the band.
3. Turning on photo printing shows the upload option.
4. A portrait photo and a landscape photo both fill the panel with **Cover**.
5. Dragging the photo to the edge cuts it at the crop area.
6. The price is right after each step.
7. All of the above works on a phone.
{% endstep %}

{% step %}
### Place a test order

Add the mug to the cart, check that **Preview Your Design** shows the right design, and place the order. The order should list `Name on mug`, `Photo printing`, and a link to the uploaded file. Fix any unclear option names now. See [Designs in cart and orders](cart-and-orders.md).
{% endstep %}
{% endstepper %}

## What to change for other products

<table><thead><tr><th width="290">Product</th><th>Differences</th></tr></thead><tbody><tr><td>A photo frame</td><td>No curve. One image element, a crop area matching the window, <strong>Change position</strong> and <strong>Resize</strong> on</td></tr><tr><td>An engraved pen</td><td>Curve for the barrel, a very tight character limit, no image element</td></tr><tr><td>A t-shirt</td><td>No curve, a larger print area, a photo upload plus optional text. See <a href="walkthrough-personalized-tee.md">Walkthrough: personalized t-shirt</a></td></tr><tr><td>A ring band</td><td>A strong curve, a five-character limit, auto-fit essential</td></tr><tr><td>A jersey</td><td>A <a href="../option-types/input-types/number.md">Number</a> element for the number and a Text element for the name, placed separately</td></tr></tbody></table>
