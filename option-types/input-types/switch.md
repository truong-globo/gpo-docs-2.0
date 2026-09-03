---
description: A single on-or-off toggle with its own label, for offering one paid extra.
icon: toggle-on
---

# Switch

A toggle the customer turns on or off. It provides a single yes-or-no choice.

Use it for one optional extra, such as gift wrapping, express production, insurance, or an extended warranty.

## What customers see

A toggle with your label above it and a short label beside the toggle. The switch label is `Yes` by default.

<figure><img src="../../.gitbook/assets/2026-09-03_10-27-49.png" alt="A switch option turned on, on a storefront product page, with its add-on price shown"><figcaption><p>A switch reads as a single decision, which suits one paid extra.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart unless the switch is <strong>on</strong>. Rarely what you want — see the note below.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label above the switch. The switch label stays.</td></tr><tr><td><strong>Selected by default</strong></td><td>The switch starts in the on position. Off by default.</td></tr><tr><td><strong>Switch label</strong></td><td>The short text beside the toggle. Starts as <code>Yes</code>. Required.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#price">Price</a></td><td>The add-on charge when the switch is on.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

{% hint style="warning" %}
**Required field** on a Switch means the customer cannot add the product to the cart without turning it on. Use it only for mandatory confirmations, such as “I confirm the spelling is correct.” For optional extras, leave it off. Otherwise, every customer will have to accept and pay for the extra.
{% endhint %}

{% hint style="danger" %}
**Selected by default** combined with a price adds the charge as soon as the page loads, before the customer makes a choice. This can work for an upgrade that most customers choose, but it can also cause customers to wonder why the product costs more than the listed price.
{% endhint %}

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#advanced-settings">Advanced settings</a> / <a href="../shared-settings/conditional-logic-and-add-on-fields.md#set-quantity">Set quantity</a></td><td>How the add-on scales with quantity.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

## Add-on pricing

The price applies to the whole option and is charged when the switch is on. All three modes are available:

<table><thead><tr><th width="290">Mode</th><th>Use for</th></tr></thead><tbody><tr><td><strong>Use existing product</strong></td><td>Something you already sell and stock, such as a gift box.</td></tr><tr><td><strong>Automatically generate product</strong></td><td>Something physical you want to count and stock without building a product by hand.</td></tr><tr><td><strong>Add price</strong></td><td>A service with nothing to stock, such as express production. Not supported on POS.</td></tr></tbody></table>

The **Advanced settings** mode is especially important on a Switch:

<table><thead><tr><th width="290">Mode</th><th>On an order of three products, with $5.00</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>$15.00 — one per product</td></tr><tr><td><strong>One time charge</strong></td><td>$5.00 — one for the whole order</td></tr><tr><td><strong>Fixed quantity</strong> with <strong>Set quantity</strong> 2</td><td>$10.00 — always two</td></tr></tbody></table>

Use **One-time charge** for anything charged once per order rather than per item, such as gift wrapping a parcel or a delivery upgrade. See [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md).

## Personalizer Settings

Not supported.&#x20;

## Switch or Checkbox?

<table><thead><tr><th width="230"></th><th width="250">Switch</th><th>Checkbox</th></tr></thead><tbody><tr><td>Number of choices</td><td>Exactly one</td><td>A list of any length</td></tr><tr><td>Price lives on</td><td>The option</td><td>Each value</td></tr><tr><td>Multiple selection</td><td>Not applicable</td><td>Built in</td></tr><tr><td>Swatch style</td><td>No</td><td>Yes</td></tr><tr><td>Reads as</td><td>A single yes-or-no decision</td><td>A menu of extras</td></tr></tbody></table>

Use a Switch for a single option. Use a [Checkbox](../selection-types/checkbox.md) when there are two or more.

## Examples

**Gift wrap, charged once per order**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Gift wrap</code></td></tr><tr><td>Switch label</td><td><code>Yes, wrap it</code></td></tr><tr><td>Selected by default</td><td>Off</td></tr><tr><td>Price</td><td><strong>Automatically generate product</strong> $3.00</td></tr><tr><td>Advanced settings</td><td><strong>One time charge</strong></td></tr></tbody></table>

**Express production**

Switch label `Yes, prioritize my order`, **Add price** $10.00, **One time charge**, help text `Made and dispatched within 24 hours.`

**A confirmation the customer must give**

Label `Spelling check`, switch label `I confirm the spelling above is correct`, **Required field** on, no price. Use this together with an engraving field.

**An upgrade most people take**

Label `Premium gift box`, **Selected by default** on, a price attached, and help text stating the price clearly.

## Notes

* Available on all plans.
* Works in Shopify POS, provided the add-on is product-backed rather than **Add price**.
* No Personalizer support.
* When the switch is on, the **Switch label** text is stored in the order. Use a switch label that reads clearly on an order line. `Yes, wrap it` is clearer than `Yes`.
* Conditional logic on a Switch offers two operators: **is enabled** and **is disabled**. See [Operators reference](../../conditional-logic/operators-reference.md).
