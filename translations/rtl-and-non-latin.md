---
description: Right-to-left layout for Arabic and Hebrew storefronts, and what to watch with non-Latin scripts.
icon: align-right
---

# Right-to-left and non-Latin text

The widget supports right-to-left layout and non-Latin scripts, but a few settings need attention that a Latin-script store never thinks about.

## Right-to-left layout

The widget's alignment setting includes a right-to-left option.

**Settings** > **Settings** > **General** > **Widget Settings** > **Alignment** > **Right to left**

That lays the widget out for right-to-left reading: labels, fields, help text, and swatch rows all flow the other way.

<table><thead><tr><th width="230">Alignment</th><th>Use for</th></tr></thead><tbody><tr><td><strong>Left</strong></td><td>Left-to-right languages. The default</td></tr><tr><td><strong>Center</strong></td><td>A centred design, in either direction</td></tr><tr><td><strong>Right</strong></td><td>Right-aligned text without changing reading direction</td></tr><tr><td><strong>Right to left</strong></td><td>Arabic, Hebrew, and other right-to-left storefronts</td></tr></tbody></table>

{% hint style="warning" %}
Alignment is **store-wide**. If you sell in both a left-to-right and a right-to-left language you cannot set it per language here — you would need to control it with [custom CSS](../storefront/custom-css.md) keyed on your theme's own language markers.
{% endhint %}

See [Widget behavior](../storefront/widget-behavior.md).

## Fonts and scripts

The widget's typography is set store-wide in **Settings** > **Design** > **Typography**, and this is where non-Latin stores need care.

<table><thead><tr><th width="290">Check</th><th>Why</th></tr></thead><tbody><tr><td>The chosen font includes your script</td><td>Many otherwise excellent fonts have no Arabic, Hebrew, Thai, or CJK glyphs. Missing glyphs fall back to a system font, which looks inconsistent</td></tr><tr><td>Font size suits the script</td><td>CJK and Arabic often need a slightly larger size than Latin at the same nominal value to be equally legible</td></tr><tr><td>Bold and italic exist</td><td>Many non-Latin fonts have no italic at all, and a faked slant looks wrong</td></tr></tbody></table>

See [Borders and typography](../storefront/borders-and-typography.md).

## The Personalizer

This is where non-Latin scripts need the most attention, because the preview draws text itself.

<table><thead><tr><th width="290">Setting</th><th>What to watch</th></tr></thead><tbody><tr><td><a href="../personalizer/fonts.md">Font family</a></td><td>The font must contain your script. Test with real customer names, not placeholder text</td></tr><tr><td><a href="../personalizer/curve-and-auto-fit.md">Curve</a></td><td>Connected scripts such as Arabic do not bend the way separated letterforms do. Check the result carefully before using curve with Arabic</td></tr><tr><td><a href="../personalizer/curve-and-auto-fit.md#auto-fit-max-width">Auto-fit max width</a></td><td>Worth turning on. Character widths vary far more across scripts than within Latin</td></tr><tr><td><a href="../option-types/shared-settings/limits.md#min-and-max-character">Max character</a></td><td>A character limit means different physical widths in different scripts. Set it for the script your customers use, or use auto-fit as the real constraint</td></tr><tr><td><a href="../personalizer/text-layers.md#font-size">Font size</a></td><td>Check by eye per script rather than reusing a value that worked for Latin</td></tr></tbody></table>

If you offer personalisation in several scripts, the most reliable arrangement is a separate option set per language group, targeted with [country rules](../option-sets/assign-to-countries.md), each with its own font and limits.

## Input rules

<table><thead><tr><th width="290">Setting</th><th>Behaviour with non-Latin text</th></tr></thead><tbody><tr><td><a href="../option-types/shared-settings/text-input-rules.md#allowed-value">Allowed value</a></td><td><strong>Letters</strong> means letters, not Latin letters. It does not restrict a shopper to the Latin alphabet</td></tr><tr><td><a href="../option-types/shared-settings/text-input-rules.md#text-transform">Text transform</a></td><td>Case has no meaning in scripts without upper and lower case, so these settings do nothing there</td></tr><tr><td><a href="../option-types/shared-settings/limits.md#min-and-max-character">Character limits</a></td><td>Count characters, so one CJK character counts as one — even though it occupies more width than a Latin one</td></tr></tbody></table>

## The date picker

The calendar has its own language setting, separate from everything else on this page. It offers more than fifty languages including Arabic, Hebrew, Thai, and several CJK options.

**Other language** and **Localization** on the option's **Advanced Settings**. See [Date and time picker](../option-types/input-types/date-and-time-picker.md).

## A checklist for a right-to-left store

{% stepper %}
{% step %}
### Set Alignment to Right to left

**Settings** > **Settings** > **General**.
{% endstep %}

{% step %}
### Choose a font that includes your script

**Settings** > **Design** > **Typography**. Upload one as a custom font if the built-in choices do not cover it.
{% endstep %}

{% step %}
### Translate the widget text

**Settings** > **Translations**. See [Translate widget text](translate-widget-text.md).
{% endstep %}

{% step %}
### Translate your option content

In the builder, per option set. See [Translate option content](translate-option-content.md).
{% endstep %}

{% step %}
### Set the calendar language on any date option

Per option, on its Advanced Settings.
{% endstep %}

{% step %}
### Test a full product page on your storefront

Including a validation error, a swatch row, and any personalisation preview.
{% endstep %}
{% endstepper %}

## Troubleshooting

<details>
<summary>The widget still reads left to right</summary>

Set **Alignment** to **Right to left** in **Settings > Settings > General**, and save.
</details>

<details>
<summary>Some characters show as boxes or in the wrong font</summary>

The chosen font has no glyphs for them. Choose a font that covers your script, or upload one as a custom font.
</details>

<details>
<summary>Personalizer text renders incorrectly in Arabic</summary>

Check the font first. If the font is right and the problem is with **Curve**, turn curve off — connected scripts do not always bend cleanly.
</details>

<details>
<summary>Text transform does nothing</summary>

Expected in scripts without letter case.
</details>

<details>
<summary>I need left-to-right and right-to-left on the same store</summary>

Alignment is store-wide. Use [custom CSS](../storefront/custom-css.md) keyed on your theme's language markers, and [contact support](../help/contact-support.md) if you need help with the selectors.
</details>

<details>
<summary>The calendar is in the wrong language</summary>

Set it per date option with **Other language** and **Localization**.
</details>
