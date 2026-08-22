---
description: Upload your own font files and use them in the widget and in the live preview.
icon: font
---

# Custom fonts

Upload a font file once, and it becomes available anywhere the app lets you choose a font: the widget's typography, the Personalizer's text layers, and the Font picker option type.

The reason to bother is accuracy. If your engraving machine uses a particular typeface, uploading that typeface means the preview a customer sees is genuinely what they will receive.

## Where it is

**Settings** > **Settings** > **General** > **Custom fonts**.

## Steps

{% stepper %}
{% step %}
### Get the font file

You need the actual file, and the right to use it commercially. Font licensing applies to a website as much as to a printing press.
{% endstep %}

{% step %}
### Upload it

The upload area accepts **.woff2**, **.woff**, **.ttf**, and **.otf**. Anything else is rejected with a message saying so.
{% endstep %}

{% step %}
### Give it a name

The **Font name** you enter is how it appears in every font picker in the app. Use something you will recognise — the real font name, not `font1`.
{% endstep %}

{% step %}
### Select Upload font
{% endstep %}

{% step %}
### Use it

It now appears wherever fonts are chosen:

* **Settings** > **Design** > **Typography** — switch a text style to a custom font
* An option's **Personalizer Settings** — set **Font family** to **Custom**, then pick it
* A [Font picker](../option-types/selection-types/font-picker.md) option's **Custom fonts** list, to offer it to customers
{% endstep %}

{% step %}
### Test the characters you need

Upload-and-test is the only reliable check. Try accented letters, apostrophes, and digits — display and script fonts often omit some.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: settings-custom-fonts | App admin → Settings → General → Custom fonts | Khu vực upload font với Font name và Font file, danh sách font đã upload | Khoanh khu vực upload -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The custom fonts area with the font name field and upload zone"><figcaption><p>One upload, then the font is available everywhere fonts are chosen.</p></figcaption></figure>

## Accepted formats

<table><thead><tr><th width="180">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.woff2</strong></td><td>The best choice where you have it. Smallest, so pages load faster</td></tr><tr><td><strong>.woff</strong></td><td>Also web-optimised</td></tr><tr><td><strong>.ttf</strong></td><td>Common desktop format. Works, but larger than the web formats</td></tr><tr><td><strong>.otf</strong></td><td>The same</td></tr></tbody></table>

If you have a choice, upload `.woff2`. If you only have a desktop `.ttf` or `.otf`, that is fine — it just weighs more.

## Where custom fonts are worth it

<table><thead><tr><th width="290">Use</th><th>Why</th></tr></thead><tbody><tr><td>The Personalizer, matching your production font</td><td>The customer's preview is then genuinely accurate. This is the strongest reason to use custom fonts at all</td></tr><tr><td>A <a href="../option-types/selection-types/font-picker.md">Font picker</a> offering your real engraving fonts</td><td>Customers choose from what you can actually cut</td></tr><tr><td>Widget typography matching a brand font</td><td>Where your theme uses a font the app's list does not have</td></tr></tbody></table>

## Practical advice

<table><thead><tr><th width="290">Do</th><th>Avoid</th></tr></thead><tbody><tr><td>Upload only the fonts you use</td><td>A library of twenty fonts, most of them unused. Each one in a Font picker is loaded when previewing</td></tr><tr><td>Upload the specific weight you need</td><td>Relying on the bold or italic setting. Many fonts have no real bold or italic cut, and the result looks distorted</td></tr><tr><td>Name them recognisably</td><td>Names like <code>final-2</code> that mean nothing in six months</td></tr><tr><td>Check licensing for web use</td><td>Assuming a desktop licence covers your storefront</td></tr><tr><td>Test with real customer names</td><td>Testing with the word "test", which uses four very ordinary characters</td></tr></tbody></table>

## Notes

* Custom fonts are plan-gated. See [Compare plans](../plans/compare-plans.md).
* Uploaded fonts are stored with your store's files.
* A custom font used in the Personalizer is loaded when the product page renders, so keep the file as small as the format allows.
* The date picker's calendar language is unrelated to fonts. See [Date and time picker](../option-types/input-types/date-and-time-picker.md).

## Troubleshooting

<details>
<summary>"File type must be .woff2, .woff, .ttf or .otf"</summary>

The file is a different format. Convert it, or ask your font supplier for a web format.
</details>

<details>
<summary>My uploaded font is not in the picker</summary>

Reload the page. If it is still missing, check the upload completed and that custom fonts are included in your plan.
</details>

<details>
<summary>Some characters render in a different font</summary>

The font has no glyphs for them, so a fallback is used. Test with the characters your customers actually type — accents in particular.
</details>

<details>
<summary>Bold or italic looks artificial</summary>

The font has no real bold or italic cut. Upload the proper weight as a separate custom font.
</details>

<details>
<summary>The font looks different in production than in the preview</summary>

The uploaded file and your production font are not the same file. Upload the production one.
</details>

<details>
<summary>Custom fonts is greyed out</summary>

Not included in your plan. See [Compare plans](../plans/compare-plans.md).
</details>

## Next steps

* [Fonts](../personalizer/fonts.md) — using them in the live preview.
* [Font picker](../option-types/selection-types/font-picker.md) — offering them to customers.
* [Borders and typography](../storefront/borders-and-typography.md) — using them in the widget.
