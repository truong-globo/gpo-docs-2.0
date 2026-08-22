---
description: >-
  An email address field with built-in format validation — for digital gifts,
  proofs, and recipient notifications.
icon: envelope
---

# Email

A field that accepts an email address and checks it looks like one before the shopper can add to cart.

Use it when the email you need is **not** the buyer's own — a gift recipient, a second contact for a proof, a colleague to copy in. Shopify already collects the buyer's email at checkout, so do not ask for it twice.

## What customers see

A single-line field with your label above it. If they type something that is not a valid address, adding to cart is blocked with `Invalid email`.

<!-- SCREENSHOT: type-email-storefront | Storefront → trang sản phẩm | Field Email với help text, và trạng thái lỗi "Invalid email" | Khoanh field và thông báo lỗi -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An email field on a storefront product page showing the invalid email message"><figcaption><p>Format validation is built in — there is no setting to turn it on.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until an address is entered.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>An example address.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible — the right place to explain what you will use the address for.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Pre-fills the field.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#suffix">Suffix</a></td><td>Fixed text after the field.</td></tr><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-icon">Prefix icon</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-text">Prefix text</a></td><td>An icon or text at the start — an envelope icon is the obvious choice.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

## Validation

Format checking is built in and always on — there is no switch. An entry that is not a valid address blocks **Add to cart** with `Invalid email`, which you can reword per language in **Settings > Translations**. See [Translate widget text](../../translations/translate-widget-text.md).

The check is on the format only. It confirms the address is shaped like an email; it cannot confirm the mailbox exists.

## Add-on pricing

Email cannot carry an add-on price.

If the thing being paid for is the email delivery itself — a digital gift card sent to a recipient — put the charge on the [Switch](switch.md) or [Checkbox](../selection-types/checkbox.md) that turns the feature on, and reveal the email field with [conditional logic](../../conditional-logic/README.md).

## Personalizer Settings

Not supported.

## Examples

**Gift recipient's email for a digital gift**

<table><thead><tr><th width="270">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Recipient email</code></td></tr><tr><td>Required field</td><td>On</td></tr><tr><td>Placeholder</td><td><code>them@example.com</code></td></tr><tr><td>Help text</td><td><code>We will email the gift here on the date you choose.</code></td></tr><tr><td>Conditional logic</td><td>Show when <strong>Send as a gift</strong> is selected</td></tr></tbody></table>

**A second address for a proof**

Not required, help text `Optional — we will copy this address on the artwork proof.`

**Notify me when the custom piece ships**

Not required, prefix an envelope icon, help text explaining that Shopify already emails the buyer and this is for somebody else.

## Limits and notes

* Available on paid plans.
* Works in Shopify POS.
* Cannot carry an add-on price.
* No Personalizer support.
* Only one address per field. For several recipients, add several Email options, or use a [Textarea](textarea.md) and accept that you cannot validate the entries.

{% hint style="warning" %}
An email address is personal data. Only collect it when you have a reason, say what the reason is in help text, and make sure your privacy policy covers it. See [Permissions and data](../../reference/permissions-and-data.md).
{% endhint %}

## Troubleshooting

<details>
<summary>"Invalid email" on an address that looks fine</summary>

Check for a trailing space, a comma instead of a full stop, or two addresses in one field. Only one address per field is accepted.
</details>

<details>
<summary>I want to collect several addresses</summary>

Add one Email option per address, or use a Textarea and validate by hand.
</details>

<details>
<summary>I cannot find a Price field</summary>

Email has none. Put the charge on the option that turns the feature on.
</details>

<details>
<summary>Customers enter their own email even though I asked for the recipient's</summary>

Make the label explicit — `Recipient's email address` rather than `Email` — and explain it in help text.
</details>

<details>
<summary>Can the app email this address automatically?</summary>

Not from the option itself. Workflows email **you** when an order arrives. See [Automations](../../automations/README.md).
</details>
