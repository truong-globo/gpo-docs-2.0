---
description: >-
  Prefix, Prefix icon, Prefix text, Suffix, and the element icons — small pieces
  of fixed text and iconography inside and beside a field.
icon: icons
---

# Prefix, suffix, and icons

Small decorations that make a field self-explanatory: a currency symbol before a number, `cm` after a measurement, a calendar icon beside a date.

None of them affect what the customer submits. They are labels attached to the field, not part of the value.

## Prefix

A small icon or piece of text at the start of the field.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Icon</strong></td></tr><tr><th>Available on</th><td>9 types: Text, Textarea, Number, Phone, Email, Date and time picker, Select, Dropdown, Font picker</td></tr></thead></table>

**Prefix** itself is only the choice between two kinds:

<table><thead><tr><th width="180">Choice</th><th>Reveals</th></tr></thead><tbody><tr><td><strong>Icon</strong></td><td><strong>Prefix icon</strong> — pick an icon from the app's icon picker</td></tr><tr><td><strong>Text</strong></td><td><strong>Prefix text</strong> — type a short piece of text</td></tr></tbody></table>

Neither shows anything until you actually choose an icon or type some text. Leaving both empty means no prefix.

### Prefix icon

An icon chosen from the app's built-in picker, shown inside the field at the start.

Useful when the icon is universally understood and saves words:

<table><thead><tr><th width="240">Field</th><th>Icon</th></tr></thead><tbody><tr><td>Email</td><td>An envelope</td></tr><tr><td>Phone</td><td>A telephone</td></tr><tr><td>Date</td><td>A calendar</td></tr><tr><td>Search-style dropdown</td><td>A magnifying glass</td></tr><tr><td>Location or address</td><td>A pin</td></tr></tbody></table>

### Prefix text

Short fixed text at the start of the field. Best for units and symbols:

<table><thead><tr><th width="240">Field</th><th>Prefix text</th></tr></thead><tbody><tr><td>A donation amount</td><td><code>$</code></td></tr><tr><td>A quantity in a set</td><td><code>x</code></td></tr><tr><td>An order reference</td><td><code>#</code></td></tr><tr><td>A phone number for one country</td><td><code>+44</code></td></tr></tbody></table>

Keep it to one or two characters. Longer text eats the space the shopper types into, especially on mobile.

## Suffix

Short fixed text at the end of the field.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td>Empty</td></tr><tr><th>Available on</th><td>6 types: Text, Textarea, Number, Phone, Email, Date and time picker. <strong>Range slider</strong> has its own <strong>Prefix</strong> and <strong>Suffix</strong> text fields, without the icon-or-text choice</td></tr></thead></table>

Suffixes are almost always units:

<table><thead><tr><th width="290">Field</th><th>Suffix</th></tr></thead><tbody><tr><td>A width to cut</td><td><code>cm</code></td></tr><tr><td>A weight</td><td><code>kg</code></td></tr><tr><td>A duration</td><td><code>days</code></td></tr><tr><td>A percentage</td><td><code>%</code></td></tr><tr><td>A screen size</td><td><code>inches</code></td></tr></tbody></table>

{% hint style="info" %}
A unit as a suffix is better than a unit in the label, and much better than asking the shopper to type it. `Width [ 30 ] cm` is unambiguous, and the value that reaches your order is a clean `30` you can calculate with — which matters if you price by size. See [Dimension add-on formula](../../add-on-pricing/dimension-formula.md).
{% endhint %}

**Suffix versus placeholder**

A suffix is always visible and is not part of the value. A [placeholder](placeholder-and-help-text.md#placeholder) disappears as soon as the shopper types. For a unit, use the suffix. For an example of the format, use the placeholder. They work well together: prefix `$`, placeholder `25`, suffix `USD`.

## Element icons

Two option types have an icon of their own, unrelated to field prefixes.

<table><thead><tr><th width="230">Type</th><th width="200">Setting</th><th>Where the icon appears</th></tr></thead><tbody><tr><td><a href="../static-types/section.md">Section</a></td><td><strong>Prefix icon</strong>, on Basic Settings</td><td>Beside the section's heading</td></tr><tr><td><a href="../static-types/size-chart.md">Size chart</a></td><td><strong>Chart icon</strong>, on Advanced Settings</td><td>Beside the link that opens the chart</td></tr></tbody></table>

Both use the same icon picker. A ruler icon on a size chart, or a paintbrush on a "Personalise it" section, makes the element easier to spot in a long form.

<!-- SCREENSHOT: type-shared-prefix-suffix | App admin → builder → option Number → Advanced Settings | Prefix (Icon/Text), Prefix icon hoặc Prefix text, Suffix | Khoanh nhóm Prefix/Suffix -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The Prefix, Prefix icon, and Suffix settings on a Number option"><figcaption><p>Prefix chooses between an icon and text; the field below it holds the actual value.</p></figcaption></figure>

<!-- SCREENSHOT: type-shared-prefix-storefront | Storefront → trang sản phẩm | 1 field Number có prefix "$" và suffix "cm" hiển thị trong ô input | Khoanh vùng prefix và suffix -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A number field on the storefront with a prefix symbol and a unit suffix"><figcaption><p>Prefix and suffix sit inside the field, so the shopper types only the value.</p></figcaption></figure>

## Notes

* Prefix and suffix text is not translatable per language, unlike labels and help text. For units that differ by market — `cm` against `in` — use separate option sets with [country rules](../../option-sets/assign-to-countries.md).
* Neither is included in the value on the order. If your production team needs the unit recorded, put it in the option's **Name** — for example `Width (cm)`. See [Labels and visibility](labels-and-visibility.md#name).
* Prefixes and suffixes do not validate anything. A `cm` suffix does not stop a shopper typing `30 inches`. Use [Limits](limits.md) and [Text input rules](text-input-rules.md) for that.
