---
description: Personalizer problems by symptom, in the order to check them.
icon: wrench
---

# Troubleshooting personalizer

Most Personalizer problems come from one of four causes: no background, nothing to draw, an element placed for a different image, or a plan limit. Work through the checklist first, then find the symptom that matches.

## Start here

<table><thead><tr><th width="60">#</th><th width="290">Check</th><th>Where</th></tr></thead><tbody><tr><td>1</td><td>Is the <strong>Personalizer</strong> switch on for the option?</td><td>The option's <strong>Personalizer</strong> tab</td></tr><tr><td>2</td><td>Is a background set?</td><td><strong>Change background</strong>, above the Personalizer canvas</td></tr><tr><td>3</td><td>Is there anything to draw: a default value, an upload, or a value with an image?</td><td>The option's <strong>Basic</strong> tab, and the <strong>Preview</strong></td></tr><tr><td>4</td><td>Is the Personalizer included in your plan?</td><td><a href="../plans-and-billing/compare-plans.md">Compare plans</a></td></tr></tbody></table>

## In the editor

<details>

<summary>I cannot find the Personalizer editor</summary>

It appears once at least one option has the **Personalizer** switch on. On a wide screen it sits between the settings panel and the **Preview**. On a smaller screen, or in desktop view, it is the **Personalizer** tab at the top of the preview.

If you see a narrow strip labeled **Personalizer**, the editor is collapsed. Select the strip to open it. See [The Personalizer editor](editor.md).

</details>

<details>

<summary>There is no Personalizer tab on my option</summary>

That option type cannot be printed. Twelve types are supported: Text, Textarea, Number, File upload, and eight selection types. See the [overview](personalizer.md#the-twelve-supported-option-types).

</details>

<details>

<summary>The cards on the Personalizer tab are dimmed</summary>

The **Personalizer** switch is off. Turn it on. If the tab shows a star badge, your plan does not include the Personalizer.

</details>

<details>

<summary>The editor shows "Add a product image to see the print area."</summary>

No background is set. Select **Change background** and choose a product image or a custom image. See [Choosing the background](setup.md#choosing-the-background).

</details>

<details>

<summary>I cannot select an element that is under another one</summary>

Open **Elements** in the editor toolbar and select its name. To get the top element out of the way, select its eye icon. That only hides it in the editor. See [Elements](editor.md#elements).

</details>

<details>

<summary>Text has no resize handles on the canvas</summary>

Text is sized with **Font size** in [Text style](layer-settings/text-layers.md#font-size), not by dragging. Image elements have resize handles.

</details>

<details>

<summary>An option is missing from Add element</summary>

**Add element** only lists supported options that are not printed yet. If the option is already printed, find it in **Elements** instead.

</details>

## Nothing appears on the product image

<details>

<summary>The design is blank or shows only the product</summary>

Check in this order:

1. **No background.** See [Choosing the background](setup.md#choosing-the-background).
2. **The Personalizer switch is off** on the option.
3. **Nothing to draw.** A text element with no **Default value** draws nothing until the customer types. An image element draws nothing until a file is uploaded or a value with an image is selected.
4. **The element is hidden in the editor.** Check the eye icon in **Elements**.
5. **The element is outside the image** or outside its [crop area](layer-settings/clip-area.md). Set **X position** and **Y position** to `50`.
6. **Opacity is 0.**

</details>

<details>

<summary>It works in the builder but not on the storefront</summary>

Save the option set and reload the product page. Then check that the option set is **Active**, published to **Online Store**, and assigned to the product you are viewing, and that the [app embed](../getting-started/enable-the-app-embed.md) is on.

</details>

## The element is in the wrong place

<details>

<summary>It is right on some products but not others</summary>

The product photos are framed differently. Positions are percentages of the image, so they only line up when photos are consistent.

Fixes, best first: make your photos consistent, use **First product image only** with a front-facing photo first in every gallery, or split the products into separate option sets.

</details>

<details>

<summary>The design appears on close-ups and lifestyle photos</summary>

**Apply to** is set to **All product images**. Choose a single image instead.

</details>

<details>

<summary>Elements moved after I changed the background</summary>

Expected. Positions are relative to the background. Check every element after changing it.

</details>

<details>

<summary>Two elements overlap</summary>

They share a position. Give them different **Y position** values, or use [conditional logic](../conditional-logic/conditional-logic.md) so only one shows at a time.

</details>

## Text problems

<details>

<summary>Long text runs off the product</summary>

Turn on [Auto-fit max width](layer-settings/curve-and-auto-fit.md#auto-fit-max-width), and set a **Max character** limit that matches what fits.

</details>

<details>

<summary>Long text shrinks until it is unreadable</summary>

The character limit is too high for the print area. Lower **Max character**.

</details>

<details>

<summary>The text is hard to see</summary>

The color is too close to the product, or **Opacity** is low. Check the color on the product image, not in the settings panel. Over customer photos, add a thin [stroke](layer-settings/effects.md#stroke).

</details>

<details>

<summary>The font is not the one I chose</summary>

Check that it is still selected in **Select font**, then save and reload. For custom fonts, check the font is uploaded in **Settings > Settings > General > Custom fonts** and that your plan includes custom fonts. See [Fonts](layer-settings/fonts.md).

If **Font family** shows **Not used: “…” starts on …**, the text is linked to a Font picker with a default value, so customers start on that font. See [Let customers pick font and color](layer-settings/font-and-color.md).

</details>

<details>

<summary>Some characters show in a different font</summary>

The font does not include those characters. Choose a font with a wider character set and test names with accents.

</details>

<details>

<summary>The curve looks wrong</summary>

Adjust the value, and try a negative value if the arc bends the wrong way. If the product photo is angled, no curve value will look right. Use a flat, front-facing photo.

</details>

<details>

<summary>Bold or italic looks distorted</summary>

The font has no real bold or italic version. Upload the proper weight as a custom font.

</details>

## Font and color choices

<details>

<summary>Picking a font or color does not change the text</summary>

The text is not linked to that option. On the text option's **Personalizer** tab, check **What customers can change** > **Font and color**. The linked option's name should appear under each ticked checkbox.

</details>

<details>

<summary>The option set will not save: "Pick a Font Picker, or untick Font."</summary>

A font or color checkbox is ticked but no option is chosen. Select the option under the checkbox, or untick it. The same applies to **Pick a color option, or untick Color.**

</details>

<details>

<summary>On the storefront the text uses my own font or color, not the customer's</summary>

The linked Font picker or color option is hidden, for example by conditional logic, so the text falls back to its own **Font family** and **Color**.

</details>

## Image problems

<details>

<summary>The uploaded photo is squashed</summary>

**Background mode** is **Stretch**. Switch to **Cover**.

</details>

<details>

<summary>Customers complain their photos are cropped</summary>

**Cover** crops to fill the shape. Use **Contain**, which leaves empty space, or turn on the upload option's image editor so customers crop their own photo. See [File upload](../option-types/input-types/file-upload.md).

</details>

<details>

<summary>The photo looks blurry</summary>

The uploaded file is smaller than the size it is printed at. Ask for a minimum size in the help text.

</details>

<details>

<summary>Selecting a value draws no image</summary>

Each value needs its own image in the values table. Check every value, not just the first.

</details>

<details>

<summary>Several images stack on top of each other</summary>

An option that allows several selections prints one image per selected value. Limit it to one selection, or place the values apart.

</details>

## Customer control problems

<details>

<summary>Customers cannot move the element</summary>

Tick **Change position** in **What customers can change**.

</details>

<details>

<summary>Customers place designs where I cannot print</summary>

Turn on **Crop area** in [Print area](layer-settings/clip-area.md) and leave **Hide the outline** off, so customers see the boundary.

</details>

<details>

<summary>Designs arrive rotated or resized badly</summary>

Untick **Rotate**, and **Resize** for text. Few products need either.

</details>

<details>

<summary>Adjusting the element is hard on a phone</summary>

Set the starting position and size most customers need, so they rarely have to adjust it.

</details>

## Cart and order problems

<details>

<summary>There is no design preview in the cart</summary>

Check **Personalizer preview mode** in **Settings > Settings > General > Cart page**, and that your plan includes it. Cart drawer apps do not show **Preview Your Design**. Customers see it on the cart page.

</details>

<details>

<summary>The design downloads instead of opening in the cart</summary>

**Personalizer preview mode** is set to **Download file**.

</details>

<details>

<summary>My order line is hard to read</summary>

The option's **Name on cart page** is still the default. See [Labels and visibility](../option-types/shared-settings/labels-and-visibility.md).

</details>

<details>

<summary>Customers cannot fix a typo after adding to cart</summary>

Turn on **Show "Edit Options" button in cart**. See [Cart page](../storefront-display-and-design/cart-page.md).

</details>

## Performance

<details>

<summary>The product page feels slow</summary>

Use fewer elements and a smaller background image, and avoid thick strokes and large shadows on long text. Many elements on a large image draw slowly on older phones.

</details>

<details>

<summary>The builder preview stopped rendering</summary>

The in-app preview turns off on very large option sets. Test with **View in Store** instead. See [Live preview and inspector](../option-sets/live-preview-and-inspector.md).

</details>

## Still stuck?

When [contacting support](../help/contact-support.md), include the option set name, the option, its Personalizer settings, the product you are testing on, and a screenshot of what you see next to what you expected.
