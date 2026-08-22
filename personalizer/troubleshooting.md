---
description: Personalizer problems by symptom, in the order worth checking.
icon: wrench
---

# Troubleshooting personalizer

Most Personalizer problems are one of four things: no background, no content to draw, a layer positioned against a different image, or a plan limit. Start with the checklist, then find your symptom.

## Start here

<table><thead><tr><th width="60">#</th><th width="290">Check</th><th>Where</th></tr></thead><tbody><tr><td>1</td><td>Is a background configured for the option set?</td><td><strong>Change background</strong> in the preview panel</td></tr><tr><td>2</td><td>Is <strong>Enable personalize</strong> on for the option?</td><td>The option's <strong>Personalizer Settings</strong> tab</td></tr><tr><td>3</td><td>Is there anything to draw — a default value, or an uploaded file?</td><td><strong>Basic Settings</strong></td></tr><tr><td>4</td><td>Is the Personalizer included in your plan?</td><td><a href="../plans/compare-plans.md">Compare plans</a></td></tr></tbody></table>

## Nothing appears on the product photo

<details>
<summary>The preview is blank or shows only the product</summary>

In order:

1. **No background.** Open **Change background** and select one. See [Set the preview background](set-the-background.md).
2. **Enable personalize is off** on the option.
3. **Nothing to draw.** A text layer with no **Default value** draws nothing until the customer types. An image layer draws nothing until a file is uploaded or a value with an image is chosen.
4. **The layer is outside the image**, or outside its [clip area](clip-area.md). Bring the axes towards 50.
5. **Opacity is at 0.**

</details>

<details>
<summary>There is no Personalizer Settings tab on my option</summary>

That option type does not support it. Twelve types do — see the [overview](README.md#the-twelve-supported-option-types). Text, Textarea, Number, File upload, and eight selection types.

</details>

<details>
<summary>The tab is there but everything is greyed out</summary>

The Personalizer is not in your plan.

</details>

<details>
<summary>It works in the builder but not on the storefront</summary>

Save the option set, then reload the product page. Also confirm the option set is **Active** and published to **Online Store**, and that the product you are testing on is one it applies to.

</details>

## The layer is in the wrong place

<details>
<summary>The layer is positioned wrongly on some products but not others</summary>

Their photographs are framed differently. Positions are percentages of the image, so they only hold when your product photography is consistent.

Fixes, in order of preference: standardise your photographs; use **First product image only** with a consistent front-on shot; or split the products into separate option sets.

</details>

<details>
<summary>Personalisation appears on close-up and lifestyle photos</summary>

**Apply to** is set to **All product images**. Choose a single image instead.

</details>

<details>
<summary>The layer moved after I changed the background</summary>

Expected — positions are relative to the background. Reposition every layer after changing it, which is why the background comes first.

</details>

<details>
<summary>Two layers overlap</summary>

They share a position. Give them different **Y-Axis** values, or use [conditional logic](../conditional-logic/README.md) so only one is visible at a time.

</details>

## Text problems

<details>
<summary>Long text runs off the product</summary>

Turn on [Auto-fit max width](curve-and-auto-fit.md#auto-fit-max-width), and set a **Max character** limit matching what physically fits.

</details>

<details>
<summary>Long text shrinks until it is unreadable</summary>

Your character limit is too generous for the printable area. Lower **Max character**.

</details>

<details>
<summary>The text is invisible</summary>

Contrast against the background, or **Opacity** turned down. Check the colour against your real background image rather than the builder panel. Over customer photos, add a thin [stroke](effects.md#stroke).

</details>

<details>
<summary>The font is not the one I chose</summary>

Confirm it is still selected, save, and reload. For custom fonts, check the font is uploaded in **Settings > Settings > General > Custom fonts** and that custom fonts are in your plan. See [Fonts](fonts.md).

</details>

<details>
<summary>Some characters render in a different font</summary>

The font has no glyph for them. Choose one with a fuller character set, and test with accented names.

</details>

<details>
<summary>The curve looks wrong</summary>

Adjust by eye, and try the negative value — the arc may need to bend the other way. If your product photograph is at an angle, no curve value will look right; use a flat-on photograph.

</details>

<details>
<summary>Bold or italic looks distorted</summary>

The font has no true bold or italic cut. Upload the proper weight as a custom font.

</details>

## Image problems

<details>
<summary>The uploaded image is squashed</summary>

**Background mode** is on **Stretch**. Switch to **Cover**.

</details>

<details>
<summary>Customers' photos are cropped and they complain</summary>

**Cover** crops to fill. Either switch to **Contain** and accept empty space, or turn on the upload option's image editor so they crop it themselves. See [File upload](../option-types/input-types/file-upload.md).

</details>

<details>
<summary>The image looks soft</summary>

The uploaded file is smaller than the size it is drawn at. Ask for a minimum resolution in help text.

</details>

<details>
<summary>Selection values draw no image</summary>

Each value needs its own image in the values table. Check every value, not just the first.

</details>

<details>
<summary>Several images stack on top of each other</summary>

A multi-select option contributes one layer per selection. Limit it to one selection, or position for the overlap.

</details>

## Customer control problems

<details>
<summary>Customers cannot move the layer</summary>

Turn on **Change position** under **Allow customers to**.

</details>

<details>
<summary>Customers place designs where I cannot print</summary>

Add a [clip area](clip-area.md) and leave its outline visible so they can see the boundary.

</details>

<details>
<summary>Designs arrive rotated or resized unusably</summary>

Turn off **Rotate**, and **Resize** for text layers. Very few products need either.

</details>

<details>
<summary>It is fiddly on a phone</summary>

Set the starting position and size close to what most customers want, so adjusting becomes optional.

</details>

## Cart and order problems

<details>
<summary>There is no design preview in the cart</summary>

Check **Personalize preview mode** in **Settings > Settings > General > Cart page**, and that it is available on your plan.

</details>

<details>
<summary>The design downloads instead of opening in the cart</summary>

**Personalize preview mode** is set to **Download file**.

</details>

<details>
<summary>My order line is unreadable</summary>

The option's **Name** is still at its default. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).

</details>

<details>
<summary>Customers cannot correct a typo after adding to cart</summary>

Turn on **Show "Edit Options" button in cart**. See [Cart page](../storefront/cart-page.md).

</details>

## Performance

<details>
<summary>The product page feels slow</summary>

Reduce the number of layers, use a smaller background image, and avoid very thick strokes or large shadows on long text. Many layers on a large image is slow on older phones.

</details>

<details>
<summary>The builder preview stopped rendering</summary>

Very large option sets disable the in-app preview. Test with **View in Store** instead. See [Live preview and inspector](../option-sets/live-preview-and-inspector.md).

</details>

## Still stuck?

Include these when you [contact support](../help/contact-support.md): the option set name, the option, its Personalizer settings, the product you are testing on, and a screenshot of what you see against what you expected.
