---
description: >-
  Let the customer choose any colour at all, with an optional live preview of
  their text in that colour.
icon: eye-dropper
---

# Color picker

A field that opens a colour picker, letting the customer choose any colour rather than one of yours.

Use it only when you genuinely can produce any colour — custom paint, custom thread, printed ink. If your range is fixed, use [Color swatch](../selection-types/color-swatch.md) instead: a picker invites requests you cannot fulfil.

## What customers see

A field showing the currently chosen colour. Selecting it opens a picker where they choose a colour visually or enter a value.

<!-- SCREENSHOT: type-colorpicker-storefront | Storefront → trang sản phẩm | Field Color picker đang mở bảng chọn màu | Khoanh vùng picker -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A colour picker open on a storefront product page"><figcaption><p>The picker gives the shopper the whole spectrum — use it only when you can match it.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until a colour is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#price">Price</a></td><td>The add-on charge for choosing a custom colour.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>Text in the field before a colour is chosen.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>A starting colour.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How the add-on scales with quantity.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#color-preview">Color preview</a></td><td>Shows a live preview of the chosen colour applied to text.</td></tr><tr><td><strong>Select text box</strong></td><td>Which text option in this option set the colour preview applies to. Only appears once <strong>Color preview</strong> is on.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

### Color preview and Select text box

These two together produce the "see your text in the colour you picked" effect, without needing the full Personalizer.

{% stepper %}
{% step %}
### Add a text option first

The colour has to be applied to something. Add a [Text](text.md) or [Textarea](textarea.md) option for the words.
{% endstep %}

{% step %}
### Turn on Color preview

On the Color picker's **Advanced Settings**.
{% endstep %}

{% step %}
### Point Select text box at the text option

Choose the text option you just added.
{% endstep %}

{% step %}
### Test it

Type into the text field and change the colour — the preview follows.
{% endstep %}
{% endstepper %}

For drawing the text onto the **product photo** rather than previewing it beside the field, use the [Personalizer](../../personalizer/README.md) on the text option instead. Colour picker itself has no Personalizer settings.

## Add-on pricing

The price belongs to the option, so it is a charge for choosing a custom colour at all — a common and reasonable fee, since a bespoke colour costs you more than a stock one.

All three modes are available. Typically:

* **Add price** for a flat "custom colour" surcharge with nothing to stock.
* **Automatically generate product** if you want to count how many custom-colour orders you take.

See [Add-on pricing](../../add-on-pricing/README.md).

## Examples

**Custom paint colour with a surcharge**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Custom paint colour</code></td></tr><tr><td>Price</td><td><strong>Add price</strong> $15.00, mode <strong>One time charge</strong></td></tr><tr><td>Help text</td><td><code>We match to the nearest available paint. Allow 5 extra days.</code></td></tr><tr><td>Conditional logic</td><td>Show when <strong>Finish</strong> is <code>Custom colour</code></td></tr></tbody></table>

That pattern — a swatch list of stock colours, plus a picker revealed only when they choose "custom" — is the right way to offer both.

**Thread colour for embroidery, previewed**

Color picker with **Color preview** on, **Select text box** pointing at the `Embroidered name` text option.

**Ink colour on a printed card**

Default value set to your most common ink colour, not required, so most shoppers accept the default.

## Limits and notes

* Available on paid plans.
* Works in Shopify POS.
* No Personalizer settings on this type — apply the Personalizer to the text option instead.
* The chosen colour reaches the order as a colour value. Your team will need to interpret it against your own colour system.
* There is no way to restrict the picker to a subset of colours. If you need that, use [Color swatch](../selection-types/color-swatch.md).

{% hint style="warning" %}
Screens differ. A colour the customer chose on their phone will not match your product exactly. Say so in help text — "we match to the nearest available shade" saves disputes.
{% endhint %}

## Troubleshooting

<details>
<summary>Color preview does nothing</summary>

Set **Select text box** as well — the preview needs to know which text it is colouring, and that text option must exist in the same option set.
</details>

<details>
<summary>Customers choose colours I cannot produce</summary>

Switch to a [Color swatch](../selection-types/color-swatch.md) with your real palette, and offer the picker only behind a conditional rule for genuine bespoke work.
</details>

<details>
<summary>The colour on the order does not match what they saw</summary>

Expected — screens are not calibrated. Explain your matching policy in help text.
</details>

<details>
<summary>I want the chosen colour drawn on the product photo</summary>

That is the Personalizer, applied to the text or image option, not to the picker. See [Product Personalizer](../../personalizer/README.md).
</details>

## Next steps

* [Color swatch](../selection-types/color-swatch.md) — a fixed palette instead.
* [Swatch style and previews](../shared-settings/swatch-style-and-previews.md#color-preview)
* [Conditional logic](../../conditional-logic/README.md) — offer the picker only to those who want bespoke.
