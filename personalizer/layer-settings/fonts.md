---
description: Default, Google, and your own uploaded fonts in the live preview — and how to let the customer choose.
icon: font-awesome
---

# Fonts

The **Font family** setting on a text layer decides which typeface the preview draws in. It matters more than it sounds: the font is most of what makes an engraving preview look real.

**Applies to:** [Text](../../option-types/input-types/text.md), [Textarea](../../option-types/input-types/textarea.md), [Number](../../option-types/input-types/number.md).

## The three choices

<table><thead><tr><th width="200">Choice</th><th width="290">What it uses</th><th>Reveals</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>The app's standard typeface</td><td>Nothing further</td></tr><tr><td><strong>Google</strong></td><td>A font from Google's library</td><td><strong>Select Google font</strong></td></tr><tr><td><strong>Custom</strong></td><td>A font file you uploaded to the app</td><td><strong>Select Custom font</strong></td></tr></tbody></table>

<!-- SCREENSHOT: pp-font-family | App admin → builder → option Text → Personalizer Settings | Font family với 3 lựa chọn Default/Google/Custom và picker font đang mở | Khoanh Font family và picker -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The font family setting with Google selected and the font picker open"><figcaption><p>Choosing Google or Custom reveals a picker for the font itself.</p></figcaption></figure>

## Default

The app's own typeface. Fine while you are building, and fine for a preview where the font is not part of the product's appeal.

It is rarely the right final choice for engraving or embroidery, because the preview font and the production font will not match.

## Google

Choose one font from Google's library.

<table><thead><tr><th width="290">Good for</th><th>Watch out for</th></tr></thead><tbody><tr><td>Finding a close match to your production font quickly</td><td>Close is not the same. Check the letterforms your customers will actually use</td></tr><tr><td>Scripts and display faces you do not own</td><td>Very ornate faces read badly at small sizes</td></tr><tr><td>Consistency with your storefront if it already uses a Google font</td><td>Fonts with limited character sets — check accents and non-Latin characters if your customers use them</td></tr></tbody></table>

Test with real names, including accented characters, before going live.

## Custom

Your own font file, uploaded to the app once and then selectable here.

This is the right choice whenever the font is part of what you sell. If your engraving machine uses a specific typeface, upload that typeface, and the preview is genuinely what the customer will get.

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

Upload-and-test is the only reliable check. Try accented letters, punctuation, and any digits — some display fonts omit them.
{% endstep %}
{% endstepper %}

Custom fonts are plan-gated. See [Compare plans](../../plans/compare-plans.md).

## Letting the customer choose the font

The layer's font is fixed. To let shoppers pick, add a [Font picker](../../option-types/selection-types/font-picker.md) option alongside.

{% stepper %}
{% step %}
### Add the text option with its Personalizer layer

Set its **Font family** to your most popular choice — that becomes the starting font.
{% endstep %}

{% step %}
### Add a Font picker option

List only the fonts you can actually produce. Up to 30 Google fonts, plus your custom fonts.
{% endstep %}

{% step %}
### Turn on Font preview on the picker

So each font name is drawn in its own typeface.
{% endstep %}

{% step %}
### Point Select text box at the text option

So the shopper sees their own words in the font, not just the font's name.
{% endstep %}

{% step %}
### Test on a real product page

Switching fonts should update the preview.
{% endstep %}
{% endstepper %}

## Choosing fonts you can produce

The most common mistake here is offering fonts for their appearance rather than their producibility.

<table><thead><tr><th width="290">Ask</th><th>Because</th></tr></thead><tbody><tr><td>Can our machine or supplier actually use this font?</td><td>Otherwise every order needs renegotiating</td></tr><tr><td>Does it include every character our customers type?</td><td>Accents, apostrophes, digits</td></tr><tr><td>Is it legible at the size we engrave?</td><td>Fine hairlines disappear when cut small</td></tr><tr><td>Are we licensed to use it commercially?</td><td>Font licensing applies to your production as well as your website</td></tr></tbody></table>

Five fonts you can produce well beat thirty you cannot.

## Notes

* One font per layer. For two fonts on one product, use two options.
* [Font style](text-layers.md#font-style) — bold and italic — is separate, and depends on the font having those cuts.
* Google fonts load from Google when the page renders; custom fonts load from your store's files.
* Each font in a Font picker list is loaded for the preview, so long lists are slower. Another reason to keep them short.
