---
description: Default, Google, and your own uploaded fonts in the live preview — and how to let the customer choose.
icon: font-awesome
---

# Fonts

The **Font family** setting controls which typeface the text layer is drawn in. Use a font that matches what you produce, so the preview is accurate.

**Applies to:** [Text](../../option-types/input-types/text.md), [Textarea](../../option-types/input-types/textarea.md), [Number](../../option-types/input-types/number.md).

## The three choices

<table><thead><tr><th width="200">Choice</th><th width="290">What it uses</th><th>Reveals</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>The app's standard typeface</td><td>Nothing further</td></tr><tr><td><strong>Google</strong></td><td>A font from Google's library</td><td><strong>Select Google font</strong></td></tr><tr><td><strong>Custom</strong></td><td>A font file you uploaded to the app</td><td><strong>Select Custom font</strong></td></tr></tbody></table>

<!-- SCREENSHOT: pp-font-family | App admin → builder → option Text → Personalizer Settings | Font family với 3 lựa chọn Default/Google/Custom và picker font đang mở | Khoanh Font family và picker -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The font family setting with Google selected and the font picker open"><figcaption><p>Choosing Google or Custom reveals a picker for the font itself.</p></figcaption></figure>

## Default

The app's own typeface. Use it while building, or when the font is not part of the product.

It is not suitable for engraving or embroidery, because the preview font will not match the font you produce.

## Google

Choose one font from Google's library.

<table><thead><tr><th width="290">Good for</th><th>Watch out for</th></tr></thead><tbody><tr><td>Finding a close match to your production font quickly</td><td>Close is not the same. Check the letterforms your customers will actually use</td></tr><tr><td>Scripts and display faces you do not own</td><td>Very ornate faces read badly at small sizes</td></tr><tr><td>Consistency with your storefront if it already uses a Google font</td><td>Fonts with limited character sets — check accents and non-Latin characters if your customers use them</td></tr></tbody></table>

Test the font with real names, including accented characters, before you publish.

## Custom

Your own font file, uploaded to the app once and then selectable here.

Use this when the font is part of the product. If your engraving machine uses a specific typeface, upload that typeface so the preview matches the result.

{% stepper %}
{% step %}
### Upload the font

**Settings** > **Settings** > **General** > **Custom fonts**. See [Custom fonts](../../settings/custom-fonts.md).
{% endstep %}

{% step %}
### Set Font family to Custom

On the text layer's **Personalizer Settings**.
{% endstep %}

{% step %}
### Select the font

From **Select Custom font**.
{% endstep %}

{% step %}
### Check the characters you need

Upload the font and test it. Check accented letters, punctuation, and digits, because some display fonts do not include them.
{% endstep %}
{% endstepper %}

Custom fonts may not be available on all plans. See [Compare plans](../../plans/compare-plans.md).

## Letting the customer choose the font

The layer's font is fixed. To let customers select the font, add a [Font picker](../../option-types/selection-types/font-picker.md) option.

{% stepper %}
{% step %}
### Add the text option with its Personalizer layer

Set its **Font family** to your most commonly selected font. This becomes the starting font.
{% endstep %}

{% step %}
### Add a Font picker option

List only the fonts you can produce. You can add up to 30 Google fonts, plus your custom fonts.
{% endstep %}

{% step %}
### Turn on Font preview on the picker

This draws each font name in its own typeface.
{% endstep %}

{% step %}
### Point Select text box at the text option

This displays the customer's own text in the selected font, rather than only the font name.
{% endstep %}

{% step %}
### Test on a real product page

Change the font and check that the preview updates.
{% endstep %}
{% endstepper %}

## Choosing fonts you can produce

Offer fonts based on what you can produce, not only on their appearance.

<table><thead><tr><th width="290">Ask</th><th>Because</th></tr></thead><tbody><tr><td>Can our machine or supplier actually use this font?</td><td>Otherwise every order needs renegotiating</td></tr><tr><td>Does it include every character our customers type?</td><td>Accents, apostrophes, digits</td></tr><tr><td>Is it legible at the size we engrave?</td><td>Fine hairlines disappear when cut small</td></tr><tr><td>Are we licensed to use it commercially?</td><td>Font licensing applies to your production as well as your website</td></tr></tbody></table>

A short list of fonts you can produce is more useful than a long list you cannot.

## Notes

* One font per layer. For two fonts on one product, use two options.
* [Font style](text-layers.md#font-style), which controls bold and italic, is a separate setting. It requires the font to include those versions.
* Google fonts load from Google when the page renders; custom fonts load from your store's files.
* Every font in a Font picker list is loaded for the preview, so a long list takes longer to display.
