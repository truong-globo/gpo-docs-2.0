---
description: >-
  The browser's own dropdown — the plainest, most dependable way to offer a list
  of choices.
icon: caret-down
---

# Select

A native dropdown, drawn by the shopper's own browser or phone.

That is its strength and its limitation. It looks and behaves exactly as the device expects, which mobile shoppers find familiar, but it cannot be styled and it cannot show colours or pictures.

For anything richer, use [Dropdown](dropdown.md) — see the comparison below.

## What customers see

A closed field showing the placeholder or the current choice. Selecting it opens the device's own picker — a list on a desktop, a wheel or sheet on a phone.

<!-- SCREENSHOT: type-select-storefront | Storefront → trang sản phẩm | 1 native Select đang đóng và 1 đang mở | Khoanh riêng field Select -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A native select dropdown on a storefront product page"><figcaption><p>A Select uses the device's own picker, which is why it looks different on every platform.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until something is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><strong>Option values</strong></td><td>The list of choices, each with an optional price. See <a href="../../option-sets/option-values.md">Working with option values</a>.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#allow-multiple">Allow multiple</a></td><td>Lets the shopper choose several.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>The unselected prompt. Starts as <code>-- Please select --</code>.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Preselects one of the values.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How the add-on scales with quantity.</td></tr><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-icon">Prefix icon</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix-text">Prefix text</a></td><td>An icon or text at the start of the field.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

## What Select does not have

<table><thead><tr><th width="290">Missing</th><th>Because</th></tr></thead><tbody><tr><td><strong>Swatch style</strong></td><td>A native dropdown cannot draw colours or images inside itself.</td></tr><tr><td><strong>Search suggestion</strong></td><td>The device's picker has its own behaviour; the app cannot add a search box to it.</td></tr><tr><td><strong>Min and max selections</strong></td><td>Not offered on this type, even with <strong>Allow multiple</strong> on.</td></tr><tr><td><strong>Out of stock options</strong></td><td>Out-of-stock values cannot be blurred or struck through in a native picker.</td></tr><tr><td><strong>Not allow deselect</strong></td><td>Deselection is handled by the device.</td></tr><tr><td>Personalizer Settings</td><td>Not supported on this type.</td></tr></tbody></table>

If you need any of those, use [Dropdown](dropdown.md).

## Select or Dropdown?

<table><thead><tr><th width="230"></th><th width="230">Select</th><th>Dropdown</th></tr></thead><tbody><tr><td>Rendered by</td><td>The shopper's device</td><td>The app</td></tr><tr><td>Matches your design settings</td><td>No</td><td>Yes</td></tr><tr><td>Colours or images per entry</td><td>No</td><td>Yes</td></tr><tr><td>Search</td><td>No</td><td>Yes</td></tr><tr><td>Min and max selections</td><td>No</td><td>Yes</td></tr><tr><td>Out-of-stock display</td><td>No</td><td>Yes</td></tr><tr><td>Personalizer</td><td>No</td><td>Yes</td></tr><tr><td>Feels native on mobile</td><td><strong>Yes</strong></td><td>Less so</td></tr></tbody></table>

Use Select when the list is short, plain, and you would rather it look like the rest of the device than like your brand. Use Dropdown for everything else.

## Add-on pricing

Prices belong to each option value, set in the values table's **Price** column. All three modes are available per value, and the option-level **Advanced settings** dropdown controls how the charge scales.

Because Select cannot show out-of-stock states, avoid it for values linked to limited stock — a shopper can pick a sold-out value with no visual warning. Use [Dropdown](dropdown.md) there.

See [Add-on pricing](../../add-on-pricing/README.md).

## Examples

**A short, plain list**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Card style</code></td></tr><tr><td>Option values</td><td><code>Plain</code>, <code>Ribbon</code>, <code>Foiled</code></td></tr><tr><td>Placeholder</td><td><code>Choose a card style</code></td></tr><tr><td>Required field</td><td>On</td></tr></tbody></table>

**A country or region list**

Long, plain, no prices. A Select is fine — although a [Dropdown](dropdown.md) with search would be kinder past about thirty entries.

**A quantity band**

Values `1-10`, `11-50`, `51+`, no prices, used to route the enquiry rather than to charge.

## Limits and notes

* Available on all plans.
* Works in Shopify POS.
* No Personalizer support.
* Values follow the order of the values table.
* The chosen value reaches the order as its text.
* Very long lists work, but the device's picker is the whole navigation experience — there is no search to help.

## Troubleshooting

<details>
<summary>The dropdown does not match my theme</summary>

Expected — it is drawn by the browser, not the app, so the design settings do not reach it. Use [Dropdown](dropdown.md) if appearance matters.
</details>

<details>
<summary>I cannot find Swatch style, search, or out-of-stock settings</summary>

Select does not have them. Switch the option's type to Dropdown, which keeps your values and labels.
</details>

<details>
<summary>Shoppers pick sold-out values</summary>

Select cannot show stock state. Use Dropdown with **Out of stock options** set to **Hide** or **Blur**.
</details>

<details>
<summary>There is no prompt entry at the top</summary>

Its **Placeholder** is empty. Set one.
</details>
