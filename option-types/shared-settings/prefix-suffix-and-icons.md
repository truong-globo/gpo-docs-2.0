---
description: >-
  Add an icon or fixed text inside a field, add a unit after a field, and add an
  icon to a Section or Size chart.
icon: icons
---

# Prefix, suffix, and icons

These settings add fixed text or an icon to a field. They do not change the value the customer submits. All of them are available under **Advanced Settings**.

## Prefix

Adds an icon or fixed text at the start of the field.

<table><thead><tr><th width="230">Value</th><th>Description</th></tr></thead><tbody><tr><td><strong>Icon</strong> (default)</td><td>Displays the <strong>Prefix icon</strong> setting, where you select an icon from the app's icon picker.</td></tr><tr><td><strong>Text</strong></td><td>Displays the <strong>Prefix text</strong> setting, where you enter text.</td></tr></tbody></table>

Nothing is displayed on the storefront until you select an icon or enter text.

Use an icon when it is widely understood, such as an envelope for an email field or a calendar for a date field. Use text for a symbol or unit, such as `$` or `#`. Keep prefix text to one or two characters, because it reduces the space available for the customer's input.

On the Range slider option type, **Prefix** and **Suffix** are plain text fields without the icon option.

## Suffix

Adds fixed text at the end of the field. Empty by default.

A suffix is normally a unit, such as `cm`, `kg`, or `%`.

Adding the unit as a suffix keeps the submitted value clean. The customer enters `30`, and `30` is saved to the order. This is required if you calculate the price from the value. See [Dimension add-on formula](../../add-on-pricing/dimension-formula.md).

A suffix is always displayed and is not part of the value. A [placeholder](placeholder-and-help-text.md#placeholder) is displayed only while the field is empty. Use the suffix for a unit and the placeholder for an example of the format.

## Element icons

The Section and Size chart option types have their own icon setting, which is separate from field prefixes. Section uses **Prefix icon** on Basic Settings, displayed beside the section heading. Size chart uses **Chart icon** on Advanced Settings, displayed beside the link that opens the chart.

## Notes

* Prefix and suffix text cannot be translated per language. If units differ by market, use separate option sets with [country rules](../../option-sets/assign-to-countries.md).
* Prefix and suffix text is not saved to the order. If your production team needs the unit, add it to the option's **Name**, for example `Width (cm)`.
* Prefix and suffix do not validate input. Use [Limits](limits.md) and [Text input rules](text-input-rules.md) to control what customers can enter.

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Prefix and Suffix settings on a Number option"><figcaption><p>Prefix, Prefix icon, and Suffix under Advanced Settings.</p></figcaption></figure>
