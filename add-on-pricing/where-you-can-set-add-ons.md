---
description: >-
  Option level or option value level — where the Price field lives on each type,
  and which types cannot carry a price at all.
icon: location-dot
---

# Where you can set add-ons

The price field is in a different place depending on the shape of the option. Getting this straight first saves hunting for a field that is not there.

## Two levels

<table><thead><tr><th width="230">Level</th><th width="290">Where the field is</th><th>Because</th></tr></thead><tbody><tr><td><strong>Option level</strong></td><td><strong>Basic Settings</strong>, under <strong>Add-on Settings</strong>, labelled <strong>Price</strong></td><td>The option has one answer, so one price</td></tr><tr><td><strong>Option value level</strong></td><td>The <strong>Price</strong> column in the option values table</td><td>Different choices usually cost different amounts</td></tr></tbody></table>

<!-- SCREENSHOT: addon-two-levels | App admin → builder | Bên trái: option Text với field Price ở Add-on Settings. Bên phải: option Checkbox với cột Price trong bảng option values | Khoanh 2 chỗ đặt giá -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="An option-level Price field beside an option values table with a Price column"><figcaption><p>Input types take one price; selection types take a price per choice.</p></figcaption></figure>

## By option type

### Option level

These five have a single **Price** field for the whole option:

<table><thead><tr><th width="230">Type</th><th>Typical use</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/text.md">Text</a></td><td>An engraving fee, flat or per character</td></tr><tr><td><a href="../option-types/input-types/textarea.md">Textarea</a></td><td>A message printing fee</td></tr><tr><td><a href="../option-types/input-types/number.md">Number</a></td><td>A per-unit charge driven by the number entered</td></tr><tr><td><a href="../option-types/input-types/switch.md">Switch</a></td><td>One paid extra, on or off</td></tr><tr><td><a href="../option-types/input-types/color-picker.md">Color picker</a></td><td>A custom-colour surcharge</td></tr></tbody></table>

### Option value level

These nine take a price per value, in the values table:

<table><thead><tr><th width="230">Type</th><th>Typical use</th></tr></thead><tbody><tr><td><a href="../option-types/selection-types/select.md">Select</a>, <a href="../option-types/selection-types/dropdown.md">Dropdown</a></td><td>Tiers or grades at different prices</td></tr><tr><td><a href="../option-types/selection-types/color-dropdown.md">Color dropdown</a>, <a href="../option-types/selection-types/image-dropdown.md">Image dropdown</a></td><td>Premium colours or designs</td></tr><tr><td><a href="../option-types/selection-types/radio-button.md">Radio button</a></td><td>Service tiers</td></tr><tr><td><a href="../option-types/selection-types/checkbox.md">Checkbox</a></td><td>A menu of extras, each priced</td></tr><tr><td><a href="../option-types/selection-types/button.md">Button</a></td><td>Sizes or pack sizes at different prices</td></tr><tr><td><a href="../option-types/selection-types/color-swatch.md">Color swatch</a>, <a href="../option-types/selection-types/image-swatch.md">Image swatch</a></td><td>Standard colours free, premium ones charged</td></tr></tbody></table>

Values with no price are free. Mixing is normal and expected: three free colours and two paid ones in the same option.

Each value can also use a **different mode** — one linked to an existing product, another generated, a third with a plain price. The choice is per value, not per option.

### Its own arrangement

<table><thead><tr><th width="230">Type</th><th>How pricing works</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/dimension.md">Dimension</a></td><td>An <strong>Add-on price</strong> field plus a <strong>Formula</strong>, so the price is calculated from the measurements. See <a href="dimension-formula.md">Dimension add-on formula</a>.</td></tr></tbody></table>

### Cannot carry a price

<table><thead><tr><th width="290">Type</th><th>Why</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/phone.md">Phone</a>, <a href="../option-types/input-types/email.md">Email</a></td><td>Contact details, not paid choices</td></tr><tr><td><a href="../option-types/input-types/hidden-field.md">Hidden field</a></td><td>The customer makes no choice</td></tr><tr><td><a href="../option-types/input-types/date-and-time-picker.md">Date and time picker</a></td><td>A date is not a stocked item</td></tr><tr><td><a href="../option-types/input-types/file-upload.md">File upload</a></td><td>An upload is not a purchase</td></tr><tr><td><a href="../option-types/input-types/range-slider.md">Range slider</a></td><td>Use <a href="../option-types/input-types/number.md">Number</a> if the value should drive a charge</td></tr><tr><td><a href="../option-types/selection-types/font-picker.md">Font picker</a></td><td>A presentation choice</td></tr><tr><td><a href="../option-types/selection-types/product-links.md">Product links</a></td><td>It navigates away rather than adding anything</td></tr><tr><td>All nine <a href="../option-types/static-types/README.md">static types</a></td><td>They collect nothing</td></tr></tbody></table>

## Charging for an option that cannot be priced

This comes up constantly — a fee for express delivery on a date picker, a setup fee for an artwork upload. The pattern is always the same:

{% stepper %}
{% step %}
### Add a Switch or Checkbox next to it

Give it the price. A [Switch](../option-types/input-types/switch.md) for one option, a [Checkbox](../option-types/selection-types/checkbox.md) for several.
{% endstep %}

{% step %}
### Word it as the thing being paid for

`Express production (+$10.00)` or `Artwork setup fee`. The shopper should understand what the charge buys.
{% endstep %}

{% step %}
### Reveal the unpriced option conditionally

Put the priced Switch **above**, and use [conditional logic](../conditional-logic/README.md) so the date picker or upload field appears once the switch is on.
{% endstep %}

{% step %}
### Or the other way round

Reveal the priced switch once they have used the unpriced option — for example show a "rush order" switch only after they pick a date within the next three days.
{% endstep %}
{% endstepper %}

## Worked examples

**A file upload with a setup fee**

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Price</th></tr></thead><tbody><tr><td><code>Artwork setup</code></td><td>Switch</td><td>$15.00, <strong>One time charge</strong></td></tr><tr><td><code>Your artwork</code></td><td>File upload</td><td>None. Shown when the switch is on</td></tr></tbody></table>

**Colours, mostly free**

An [Image swatch](../option-types/selection-types/image-swatch.md) with eight values: five free, three priced through **Automatically generate product** so each premium finish has its own stock.

**Engraving priced by length**

A [Text](../option-types/input-types/text.md) option with **Price** $0.50 and **Advanced settings** set to **Per character**, plus a **Max character** as a ceiling.

## Notes

* The **Advanced settings** dropdown that controls how a charge scales is always at **option** level, even when the prices are on the values. It applies to all values in that option.
* **Mixed quantity** is the exception that gives each value its own quantity box — multi-select options only. See [Advanced add-on modes](advanced-add-on-modes.md).
* Once a value is linked to a product, a **Product** column appears in the values table with a link to open it in Shopify admin.
