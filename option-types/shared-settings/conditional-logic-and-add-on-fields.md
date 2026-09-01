---
description: >-
  The Conditional logic switch, Price field, Advanced settings, and Set quantity
  — four settings that unlock the app’s two most powerful features.
icon: link
---

# Conditional logic and add-on fields

Four settings appear on nearly every option, and each unlocks a larger feature. This page explains what each setting does, where to find it, and where to learn more.

## Conditional logic

Turns on rules that show or hide the option based on what the shopper has already selected.

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Off</td></tr><tr><td>Available on</td><td>All 32 option types, including <strong>Section</strong> and the visual statics</td></tr></tbody></table>

**What happens when you turn it on**

A rule builder appears directly underneath, with three parts:

<table><thead><tr><th width="200">Part</th><th>Choices</th></tr></thead><tbody><tr><td>Action</td><td><strong>Show</strong> or <strong>Hide</strong> this option when the conditions are met</td></tr><tr><td>Match</td><td><strong>all conditions</strong> or <strong>any condition</strong></td></tr><tr><td>Conditions</td><td>One or more rows: a source, an operator, and a value</td></tr></tbody></table>

The source of a condition can be another option in the same option set **or the Shopify variant the customer selected** — which lets you show an option only for the Large size, for example.

#### Two things worth knowing before you start

* The available operators depend on the type of the source option. A text source offers `contains` and character-count comparisons; a checkbox source offers selection-count comparisons; a switch source offers only `is enabled` and `is disabled`.
* A hidden option is **not validated**. A required option that is currently hidden by a rule cannot block **Add to cart**.

#### Putting the rule on a Section

**Section** supports conditional logic too. A rule on a section shows or hides everything inside it at once. If you find yourself applying the same rule to six options, put it on the section that contains them instead.

Full detail: [Conditional logic](../../conditional-logic/), the [operators reference](../../conditional-logic/operators-reference.md), and [conditions based on Shopify variants](../../conditional-logic/conditions-on-shopify-variants.md).

## Price

Attaching an extra charge to the option.

| Tab          | Basic Settings, under **Add-on Settings**                                                                                                                                                                                      |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Default      | No add-on                                                                                                                                                                                                                      |
| Available on | At **option** level: Text, Textarea, Number, Switch, Color picker. At **option value** level, in the values table's **Price** column: all nine selection types with values. **Dimension** has its own price and formula fields |

{% hint style="info" %}
Where the price lives depends on the shape of the option. An input option has one answer, so it has one price. A selection option has multiple choices that may cost different amounts, so the price is set on each value. See [Where you can set add-ons](../../add-on-pricing/where-you-can-set-add-ons.md).
{% endhint %}

Selecting the field opens a dialog with three tabs — three genuinely different ways to charge:

<table><thead><tr><th width="290">Tab</th><th>What it does</th><th>Stock tracked?</th></tr></thead><tbody><tr><td><strong>Use existing product</strong></td><td>Links a product and variant you already sell. The price comes from that variant.</td><td>Yes</td></tr><tr><td><strong>Automatically generate product</strong></td><td>The app creates a product at the price you type.</td><td>Yes</td></tr><tr><td><strong>Add price</strong></td><td>Adds money to the order with no product behind it.</td><td>No</td></tr></tbody></table>

**Add price** is not supported on Shopify POS. If you sell in person, use one of the product-backed modes. See [POS limitations](../../pos/limitations.md).

Once a value is linked to a product, a **Product** column appears in the values table with a link to open that product in Shopify admin.

Full detail: [Add-on pricing](../../add-on-pricing/).

## Advanced settings

How the add-on charge scales with the main product's quantity.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>Default</strong></td></tr><tr><td>Available on</td><td>Every type that can carry an add-on</td></tr></tbody></table>

{% hint style="warning" %}
This dropdown only does something when the option actually has a charge. On an option with no add-on, it changes nothing.
{% endhint %}

<table><thead><tr><th width="290">Mode</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>The add-on follows the main product's quantity.</td></tr><tr><td><strong>One time charge</strong></td><td>Charged once, however many of the main product are bought.</td></tr><tr><td><strong>Fixed quantity</strong></td><td>Always the quantity you set, regardless of the main product.</td></tr><tr><td><strong>Dynamic quantity</strong></td><td>The quantity you set, multiplied by the main product's quantity.</td></tr><tr><td><strong>Fixed quantity (by customer)</strong></td><td>A quantity box appears for the customer; that quantity is used as-is.</td></tr><tr><td><strong>Dynamic quantity (by customer)</strong></td><td>The customer's quantity, multiplied by the main product's quantity.</td></tr><tr><td><strong>Mixed quantity</strong></td><td>A quantity box per option value. Multi-select options only.</td></tr><tr><td><strong>Per character</strong></td><td>Charged by how many characters the customer typed. <strong>Text</strong> and <strong>Textarea</strong> only.</td></tr></tbody></table>

Each mode is explained with a worked calculation in [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md).

## Set quantity

The number used by two of the modes above.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Empty</td></tr><tr><td>Available on</td><td>Appears only when <strong>Advanced settings</strong> is <strong>Fixed quantity</strong> or <strong>Dynamic quantity</strong></td></tr></tbody></table>

* With **Fixed quantity**, this is the exact number of add-ons added, whatever the main quantity.
* With **Dynamic quantity**, this is multiplied by the main product's quantity.

## How these four interact

<table><thead><tr><th width="330">Combination</th><th>Result</th></tr></thead><tbody><tr><td>A priced option hidden by a rule</td><td>Not shown, not charged. Hiding an option removes its charge.</td></tr><tr><td>A priced option with a <strong>Default value</strong></td><td>Charged the moment the page loads, before the shopper chooses anything.</td></tr><tr><td>A multi-select option with prices</td><td>Every selected value is charged. Cap it with <a href="limits.md#min-and-max-selections">Max selections</a>.</td></tr><tr><td>A required option hidden by a rule</td><td>Not enforced while hidden.</td></tr><tr><td>A priced option on POS with <strong>Add price</strong></td><td>Not supported. Use a product-backed mode.</td></tr></tbody></table>
