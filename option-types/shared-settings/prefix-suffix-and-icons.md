---
description: >-
  Add an icon or fixed text inside a field, add a unit after a field, and add an
  icon to a Section or Size chart.
icon: icons
---

# Prefix, suffix, and icons

These settings add fixed text or an icon to a field. They do not change the value the customer submits.

## Prefix

Adds an icon or fixed text at the start of the field.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>Icon</strong>, with no icon selected</td></tr><tr><td>Available on</td><td>Text, Textarea, Number, Phone, Email, Date and time picker, Select, Dropdown, Font picker, Range slider</td></tr></tbody></table>

**Prefix** selects which type of prefix to use.

<table><thead><tr><th width="290">Value</th><th>Displays</th></tr></thead><tbody><tr><td><strong>Icon</strong></td><td>The <strong>Prefix icon</strong> setting, where you select an icon</td></tr><tr><td><strong>Text</strong></td><td>The <strong>Prefix text</strong> setting, where you enter text</td></tr></tbody></table>

Nothing is displayed on the storefront until you select an icon or enter text.

On **Range slider**, **Prefix** and **Suffix** are plain text fields. The icon option is not available.

**Prefix icon**

Select an icon from the app's icon picker. The icon is displayed inside the field, at the start.

<table><thead><tr><th width="290">Field type</th><th>Common icon</th></tr></thead><tbody><tr><td>Email</td><td>Envelope</td></tr><tr><td>Phone</td><td>Telephone</td></tr><tr><td>Date and time picker</td><td>Calendar</td></tr><tr><td>Dropdown used for search</td><td>Magnifying glass</td></tr><tr><td>Address or location</td><td>Map pin</td></tr></tbody></table>

**Prefix text**

Enter fixed text to display at the start of the field. This is normally a symbol or a unit.

<table><thead><tr><th width="290">Field purpose</th><th>Prefix text</th></tr></thead><tbody><tr><td>A donation amount</td><td><code>$</code></td></tr><tr><td>A quantity in a set</td><td><code>x</code></td></tr><tr><td>An order reference</td><td><code>#</code></td></tr><tr><td>A phone number for one country</td><td><code>+44</code></td></tr></tbody></table>

Use one or two characters. Longer text reduces the space available for the customer's input, especially on mobile.

## Suffix

Adds fixed text at the end of the field.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Empty</td></tr><tr><td>Available on</td><td>Text, Textarea, Number, Phone, Email, Date and time picker, Range slider</td></tr></tbody></table>

A suffix is normally a unit.

<table><thead><tr><th width="290">Field purpose</th><th>Suffix</th></tr></thead><tbody><tr><td>A width to cut</td><td><code>cm</code></td></tr><tr><td>A weight</td><td><code>kg</code></td></tr><tr><td>A duration</td><td><code>days</code></td></tr><tr><td>A percentage</td><td><code>%</code></td></tr><tr><td>A screen size</td><td><code>inches</code></td></tr></tbody></table>

Adding the unit as a suffix keeps the submitted value clean. The customer enters `30`, and `30` is saved to the order. This is required if you calculate the price from the value. See [Dimension add-on formula](../../add-on-pricing/dimension-formula.md).

**Suffix or placeholder**

<table><thead><tr><th width="290">Setting</th><th>Behavior</th></tr></thead><tbody><tr><td><strong>Suffix</strong></td><td>Always displayed. Not part of the submitted value</td></tr><tr><td><a href="placeholder-and-help-text.md#placeholder"><strong>Placeholder</strong></a></td><td>Displayed only while the field is empty</td></tr></tbody></table>

Use the suffix for a unit, and the placeholder for an example of the expected format. They can be used together, for example prefix `$`, placeholder `25`, suffix `USD`.

## Element icons

Two option types have their own icon setting, which is separate from field prefixes.

<table><thead><tr><th width="230">Option type</th><th>Setting</th><th>Icon position</th></tr></thead><tbody><tr><td><a href="../static-types/section.md">Section</a></td><td><strong>Prefix icon</strong>, on Basic Settings</td><td>Beside the section heading</td></tr><tr><td><a href="../static-types/size-chart.md">Size chart</a></td><td><strong>Chart icon</strong>, on Advanced Settings</td><td>Beside the link that opens the chart</td></tr></tbody></table>

Both settings use the same icon picker.

## Notes

* Prefix and suffix text cannot be translated per language. If units differ by market, for example `cm` and `in`, use separate option sets with [country rules](../../option-sets/assign-to-countries.md).
* Prefix and suffix text is not included in the value saved to the order. If your production team needs the unit, add it to the option's **Name**, for example `Width (cm)`. See [Labels and visibility](labels-and-visibility.md#name).
* Prefix and suffix do not validate input. A `cm` suffix does not prevent a customer from entering `30 inches`. Use [Limits](limits.md) and [Text input rules](text-input-rules.md) to control input.

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Prefix and Suffix settings on a Number option"><figcaption><p>Prefix, Prefix icon, and Suffix under Advanced Settings.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Number field with a prefix symbol and a unit suffix"><figcaption><p>A number field with a prefix and a suffix on the storefront.</p></figcaption></figure>
