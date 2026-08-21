---
description: >-
  A phone number field with optional international validation, country flags, and
  a default country.
icon: phone
---

# Phone

A field for a telephone number. On its own it is a plain text field; turn on validation and it becomes a country-aware input with a flag selector and dialling code.

Use it for delivery contact numbers, appointment bookings, and anything where you will actually call the customer.

## What customers see

A phone field with your label above it. With validation on, a country flag and dialling code appear at the start of the field, and the shopper can change the country.

<!-- SCREENSHOT: type-phone-storefront | Storefront → trang sản phẩm | Field Phone có validate bật: cờ quốc gia + mã vùng ở đầu ô | Khoanh vùng cờ và mã vùng -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A phone field on a storefront product page with a country flag and dialling code"><figcaption><p>With validation on, the field shows a country flag and dialling code.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until a number is entered.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>An example number — worth setting, since formats differ by country.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Pre-fills the field.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="290">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Validate international phone numbers</strong></td><td>Turns the field into a country-aware phone input. Off by default. Reveals the two settings below.</td></tr><tr><td><strong>Only used to display country flags and codes</strong></td><td>Shows the flag and dialling code but does <strong>not</strong> reject numbers that look invalid. Use it when you want the visual help without turning away entries.</td></tr><tr><td><strong>Select default country</strong></td><td>Which country the field starts on. Choose from the full country list.</td></tr><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-icon">Prefix icon</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-text">Prefix text</a></td><td>An icon or text at the start of the field.</td></tr><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#suffix">Suffix</a></td><td>Fixed text after the field.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

{% hint style="info" %}
The three validation settings interact:

* **Validation off** — a plain text field. Anything can be typed.
* **Validation on** — flag, dialling code, and rejection of numbers that are not valid for the selected country.
* **Validation on** plus **Only used to display country flags and codes** — flag and dialling code, but nothing is rejected.

The middle option is the strictest and the third is the friendliest. If you get complaints about valid numbers being refused, the third is the fix.
{% endhint %}

## Add-on pricing

Phone cannot carry an add-on price. It is a contact detail, not a paid choice.

If you need to charge for something related — a phone consultation, say — put the charge on a [Switch](switch.md) beside it and use [conditional logic](../../conditional-logic/README.md) to reveal the phone field when the switch is on.

## Personalizer Settings

Not supported. Phone numbers are not printed on products.

## Examples

**Delivery contact for a courier**

<table><thead><tr><th width="270">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Delivery contact number</code></td></tr><tr><td>Required field</td><td>On</td></tr><tr><td>Validate international phone numbers</td><td>On</td></tr><tr><td>Select default country</td><td>Your main market</td></tr><tr><td>Help text</td><td><code>Our courier will text you before delivery.</code></td></tr></tbody></table>

**A number for an optional callback**

Validation on with **Only used to display country flags and codes** on, not required, shown by a conditional rule when the shopper asks to be called.

**A local-only number**

Validation on, default country set to your own, help text explaining you only deliver domestically.

## Limits and notes

* Available on paid plans. International validation is separately plan-gated — see [Compare plans](../../plans/compare-plans.md).
* Works in Shopify POS.
* Cannot carry an add-on price.
* No Personalizer support.
* The number reaches the order as the shopper entered it, including the dialling code when validation is on.
* Asking for a phone number reduces conversion. Only ask when you will use it, and say why in help text.

## Troubleshooting

<details>
<summary>Valid numbers are being rejected</summary>

The number is being checked against the selected country. Either the shopper needs to switch the country flag, or you should turn on **Only used to display country flags and codes** so nothing is rejected.
</details>

<details>
<summary>No flag or dialling code appears</summary>

**Validate international phone numbers** is off, or the feature is not in your plan.
</details>

<details>
<summary>The field starts on the wrong country</summary>

Set **Select default country**. Shoppers can still change it themselves.
</details>

<details>
<summary>I cannot find a Price field</summary>

Phone has none by design. Put the charge on a Switch or Checkbox beside it.
</details>

<details>
<summary>Orders arrive with numbers in inconsistent formats</summary>

Turn validation fully on, which normalises entries by country, and set a **Placeholder** showing the format you expect.
</details>

## Next steps

* [Email](email.md) — the other contact field.
* [Switch](switch.md) — where to put a related charge.
* [Conditional logic](../../conditional-logic/README.md) — ask for a number only when it is needed.
