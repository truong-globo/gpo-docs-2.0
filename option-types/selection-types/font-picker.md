---
description: >-
  Let customers choose the lettering — a list of Google fonts and your own
  uploaded fonts, each drawn in its own typeface.
icon: font-awesome
---

# Font picker

A list of fonts. The customer picks one, and with **Font preview** on, each name is drawn in its own typeface so they can see what they are choosing.

Use it wherever the customer's text is produced in a font they select: engraving, embroidery, printed names, signage.

## What customers see

A dropdown or a row of buttons listing your fonts. With **Font preview** on, each entry is rendered in that font.

<!-- SCREENSHOT: type-fontpicker-storefront | Storefront → trang sản phẩm | Font picker đang mở, mỗi tên font được vẽ bằng chính font đó | Khoanh vùng danh sách font -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An open font picker on a storefront product page with each font name drawn in its own typeface"><figcaption><p>With Font preview on, shoppers see the lettering rather than imagining it.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until a font is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><strong>Google fonts</strong></td><td>The Google fonts offered. Starts with Roboto, Open Sans, Montserrat, Poppins, and Oswald. Up to 30 fonts.</td></tr><tr><td><strong>Custom fonts</strong></td><td>Fonts you uploaded yourself, in <strong>Settings &gt; Settings &gt; General &gt; Custom fonts</strong>. Several can be offered.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>The unselected prompt. Starts as <code>-- Select a font --</code>.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Preselects a font.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

### Google fonts and Custom fonts

The two lists are separate and combine into one list for the shopper.

<table><thead><tr><th width="230">List</th><th>Where the fonts come from</th></tr></thead><tbody><tr><td><strong>Google fonts</strong></td><td>A searchable picker of Google's font library. Add up to 30. The picker tells you when you have reached the limit.</td></tr><tr><td><strong>Custom fonts</strong></td><td>Font files you uploaded to the app. Upload them once in <strong>Settings</strong>, then select them here. See <a href="../../settings/custom-fonts.md">Custom fonts</a>.</td></tr></tbody></table>

{% hint style="warning" %}
Only offer fonts you can actually produce. A shopper who picks a font your engraving machine does not have creates an order you have to renegotiate. Keep the list to your real capabilities — five well-chosen fonts beat thirty.
{% endhint %}

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Style</strong></td><td><strong>Dropdown</strong> or <strong>Button</strong>. Dropdown is a list; Button shows the fonts as a row of tappable buttons.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#search-suggestion">Search suggestion</a></td><td>Adds a search box. Worth turning on for a long list.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#font-preview">Font preview</a></td><td>Draws each font name in that font.</td></tr><tr><td><strong>Select text box</strong></td><td>Which text option the font preview applies to. Appears once <strong>Font preview</strong> is on.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-icon">Prefix icon</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-text">Prefix text</a></td><td>An icon or text at the start of the field.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

### Font preview and Select text box

Turn on **Font preview** and point **Select text box** at your text option, and the shopper's own words are shown in the font they hover or select — far more persuasive than a list of font names.

Pair it with the [Personalizer](../../personalizer/README.md) on the text option and the words appear on the product photo in that font too.

## Add-on pricing

Font picker cannot carry a price. Fonts are a presentation choice, not a stocked item.

If a particular font costs you more — a licensed script, a font that needs hand-finishing — put the charge on a separate [Switch](../input-types/switch.md) or [Radio button](radio-button.md) and use [conditional logic](../../conditional-logic/README.md) to reveal it when that font is chosen.

## Personalizer Settings

Not on the picker itself. The Personalizer belongs to the **text** option — the font choice feeds into it.

To let customers choose a font and see their text in it on the product photo:

{% stepper %}
{% step %}
### Add a text option and turn on its Personalizer

Set it up as a text layer. See [Text layers](../../personalizer/layer-settings/text-layers.md).
{% endstep %}

{% step %}
### Set its Font family

Choose **Google** or **Custom** and pick the font, which becomes the starting font. See [Fonts](../../personalizer/layer-settings/fonts.md).
{% endstep %}

{% step %}
### Add a Font picker for the customer's choice

With **Font preview** on and **Select text box** pointing at the text option.
{% endstep %}
{% endstepper %}

## Examples

**Five engraving fonts**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Engraving font</code></td></tr><tr><td>Google fonts</td><td>Five fonts your machine can cut</td></tr><tr><td>Style</td><td><strong>Button</strong></td></tr><tr><td>Font preview</td><td>On, pointing at <code>Engraving text</code></td></tr><tr><td>Default value</td><td>Your most popular font</td></tr><tr><td>Required field</td><td>On</td></tr></tbody></table>

**A long list, searchable**

Thirty Google fonts, **Style** **Dropdown**, **Search suggestion** on, **Font preview** on.

**Your own brand fonts**

Uploaded custom fonts only, no Google fonts, **Style** **Button** so the three options are always visible.

## Notes
* Available on the Advanced plan. Custom fonts are separately plan-gated.
* Works in Shopify POS.
* Up to 30 Google fonts per option.
* Cannot carry an add-on price.
* No **Out of stock options** — fonts do not have stock.
* Each font in the list is loaded by the browser when previewing, so a very long list is slower to render. Another reason to keep it short.
* The chosen font's name reaches the order, so your team knows which to use.
