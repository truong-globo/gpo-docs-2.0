---
description: >-
  Let the customer choose any color, with an optional live preview of their text in
  that color.
icon: eye-dropper
---

# Color picker

A field that opens a color picker, so the customer can choose any color instead of selecting from a list you define.

Use it only when you can produce any color, such as custom paint, custom thread, or printed ink. If you offer a fixed range of colors, use [Color swatch](../selection-types/color-swatch.md) instead. A picker allows customers to request colors you cannot supply.

## What customers see

A field showing the currently selected color. Selecting it opens a picker, where the customer chooses a color visually or enters a value.

<!-- SCREENSHOT: type-colorpicker-storefront | Storefront → trang sản phẩm | Field Color picker đang mở bảng chọn màu | Khoanh vùng picker -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A color picker open on a storefront product page"><figcaption><p>The picker gives the shopper the whole spectrum — use it only when you can match it.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until a color is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#price">Price</a></td><td>The add-on charge for choosing a custom color.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>Text in the field before a color is chosen.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>A starting color.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How the add-on scales with quantity.</td></tr><tr><td><a href="../shared-settings/swatch-style-and-previews.md#color-preview">Color preview</a></td><td>Shows a live preview of the chosen color applied to text.</td></tr><tr><td><strong>Select text box</strong></td><td>Which text option in this option set the color preview applies to. Only appears once <strong>Color preview</strong> is on.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

### Color preview and Select text box

Use these two settings together to preview the customer's text in the color they selected, without using the Personalizer.

{% stepper %}
{% step %}
### Add a text option first

The color is applied to a text option, so add a [Text](text.md) or [Textarea](textarea.md) option first.
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

Enter text in the text field and change the color. The preview updates.
{% endstep %}
{% endstepper %}

To draw the text on the product photo instead of previewing it beside the field, apply the [Personalizer](../../personalizer/README.md) to the text option. Color picker has no Personalizer settings of its own.

## Add-on pricing

The price applies to the whole option, so it is a charge for selecting a custom color. This is common when a custom color costs more to produce than a standard one.

All three modes are available. Typically:

* **Add price** for a flat custom color surcharge with no inventory to track.
* **Automatically generate product** to track how many custom color orders you receive.

See [Add-on pricing](../../add-on-pricing/README.md).

## Examples

**Custom paint color with a surcharge**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Custom paint color</code></td></tr><tr><td>Price</td><td><strong>Add price</strong> $15.00, mode <strong>One time charge</strong></td></tr><tr><td>Help text</td><td><code>We match to the nearest available paint. Allow 5 extra days.</code></td></tr><tr><td>Conditional logic</td><td>Show when <strong>Finish</strong> is <code>Custom color</code></td></tr></tbody></table>

This combines a swatch list of standard colors with a picker that is displayed only when the customer selects "custom".

**Thread color for embroidery, previewed**

Color picker with **Color preview** on, **Select text box** pointing at the `Embroidered name` text option.

**Ink color on a printed card**

**Default value** set to your most common ink color and **Required field** off, so most customers keep the default.

## Notes
* Available on paid plans.
* Works in Shopify POS.
* This type has no Personalizer settings. Apply the Personalizer to the text option instead.
* The selected color is stored in the order as a color value. Your team needs to match it to your own color system.
* The picker cannot be restricted to a subset of colors. To limit the choices, use [Color swatch](../selection-types/color-swatch.md).

{% hint style="warning" %}
Colors differ between screens, so the color a customer selects on their device will not match your product exactly. State this in help text, for example "We match to the nearest available shade."
{% endhint %}
