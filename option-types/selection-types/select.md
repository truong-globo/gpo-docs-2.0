---
description: A simple, reliable way to let customers choose one value from a list.
icon: caret-down
---

# Select

**Select** uses the browser’s native dropdown, so the picker is rendered by the shopper’s browser or device. This makes it familiar and easy to use, especially on mobile.

The trade-off is that native dropdowns offer limited customization. You cannot fully style them or display colors and images inside the list.

If you need more control over the appearance or want to show richer choices, use [Dropdown](dropdown.md) instead. See the comparison below.

## What customers see

A closed field shows either the placeholder or the currently selected value. When the shopper selects it, the device opens its native picker — typically a list on desktop and a wheel or bottom sheet on mobile.

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>The customer-facing label and the name stored with the order</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Block add to cart until something is chosen.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hide the label.</td></tr><tr><td><strong>Option values</strong></td><td>The list of choices, each with an optional price. See <a href="../../option-sets/option-values.md">Working with option values</a>.</td></tr><tr><td><a href="../shared-settings/selection-behaviour.md#allow-multiple">Allow multiple</a></td><td>Let the shopper choose several.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#placeholder">Placeholder</a></td><td>The unselected prompt. Start as <code>-- Please select --</code>.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Preselect one of the values.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How the add-on scales with quantity.</td></tr><tr><td><a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix icon</a> / <a href="../shared-settings/prefix-suffix-and-icons.md#prefix">Prefix text</a></td><td>An icon or text at the start of the field.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

## What Select does not have

<table><thead><tr><th width="290">Missing</th><th>Because</th></tr></thead><tbody><tr><td><strong>Swatch style</strong></td><td>A native dropdown cannot draw colours or images inside itself.</td></tr><tr><td><strong>Search suggestion</strong></td><td>The device's picker has its own behaviour; the app cannot add a search box to it.</td></tr><tr><td><strong>Min and max selections</strong></td><td>Not offered on this type, even with <strong>Allow multiple</strong> on.</td></tr><tr><td><strong>Out of stock options</strong></td><td>Out-of-stock values cannot be blurred or struck through in a native picker.</td></tr><tr><td><strong>Not allow deselect</strong></td><td>Deselection is handled by the device.</td></tr><tr><td>Personalizer Settings</td><td>Not supported on this type.</td></tr></tbody></table>

If you need any of the features above, use [Dropdown](dropdown.md) instead.

## Select or Dropdown?

<table><thead><tr><th width="230"></th><th width="230">Select</th><th>Dropdown</th></tr></thead><tbody><tr><td>Rendered by</td><td>The shopper's device</td><td>The app</td></tr><tr><td>Matches your design settings</td><td>No</td><td>Yes</td></tr><tr><td>Colours or images per entry</td><td>No</td><td>Yes</td></tr><tr><td>Search</td><td>No</td><td>Yes</td></tr><tr><td>Min and max selections</td><td>No</td><td>Yes</td></tr><tr><td>Out-of-stock display</td><td>No</td><td>Yes</td></tr><tr><td>Personalizer</td><td>No</td><td>Yes</td></tr><tr><td>Feels native on mobile</td><td><strong>Yes</strong></td><td>Less so</td></tr></tbody></table>

Use Select when the list is short and simple, and you prefer the native look and feel of the shopper’s device. Use Dropdown when you need more styling or richer content.

## Add-on pricing

Prices are set for each option value in the values table’s **Price** column. Each value supports all three pricing modes, while the option-level **Advanced settings** dropdown controls how the charge is calculated.

Because **Select** cannot display out-of-stock states, avoid using it for values linked to limited inventory. A shopper could select a sold-out value without seeing a warning. Use [Dropdown](dropdown.md) instead.

See [Add-on pricing](../../add-on-pricing/).

## Examples

**A short, plain list**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Card style</code></td></tr><tr><td>Option values</td><td><code>Plain</code>, <code>Ribbon</code>, <code>Foiled</code></td></tr><tr><td>Placeholder</td><td><code>Choose a card style</code></td></tr><tr><td>Required field</td><td>On</td></tr></tbody></table>

**A country or region list**

For a long, simple list with no prices, **Select** is fine. For lists with more than about 30 entries, consider [Dropdown](dropdown.md) with search to make finding a value easier.

**A quantity band**

Values `1-10`, `11-50`, `51+`, no prices, used to route the enquiry rather than to charge.

## Notes

* Available on all plans.
* Works in Shopify POS.
* No Personalizer support.
* Values appear in the same order as the values table.
* The selected value is stored in the order as text.
* Very long lists are supported, but the device’s native picker is the only way to navigate them. Search is not available.
