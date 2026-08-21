---
description: >-
  The Conditional logic switch, the Price field, Advanced settings, and Set
  quantity — the four fields that lead into the app's two biggest features.
icon: link
---

# Conditional logic and add-on fields

Four settings appear on nearly every option and each opens a door to a larger feature. This page explains what the field is, where it sits, and where to read the rest.

## Conditional logic

Turns on rules that show or hide this option depending on what the shopper has already chosen.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Off</td></tr><tr><th>Available on</th><td>All 32 option types, including <strong>Section</strong> and the visual statics</td></tr></thead></table>

**What happens when you turn it on**

A rule builder appears directly underneath, with three parts:

<table><thead><tr><th width="200">Part</th><th>Choices</th></tr></thead><tbody><tr><td>Action</td><td><strong>Show</strong> or <strong>Hide</strong> this option when the conditions are met</td></tr><tr><td>Match</td><td><strong>all conditions</strong> or <strong>any condition</strong></td></tr><tr><td>Conditions</td><td>One or more rows: a source, an operator, and a value</td></tr></tbody></table>

The source of a condition can be another option in the same option set, **or the Shopify variant the customer selected** — which is how you show an option only for the Large size, for example.

**Two things worth knowing before you start**

* The available operators depend on the type of the source option. A text source offers `contains` and character-count comparisons; a checkbox source offers selection-count comparisons; a switch source offers only `is enabled` and `is disabled`.
* A hidden option is **not validated**. A required option currently hidden by a rule cannot block **Add to cart**. That is deliberate, but it means "required" only holds while the option is visible.

**Putting the rule on a Section instead**

**Section** supports conditional logic too, and a rule on a section shows or hides everything inside it at once. If you find yourself writing the same rule on six options, put it on the section around them instead.

Full detail: [Conditional logic](../../conditional-logic/README.md), the [operators reference](../../conditional-logic/operators-reference.md), and [conditions based on Shopify variants](../../conditional-logic/conditions-on-shopify-variants.md).

<!-- SCREENSHOT: type-shared-clo-field | App admin → builder → 1 option | Switch Conditional logic đã bật, rule builder hiện bên dưới | Khoanh switch và rule builder -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The conditional logic switch turned on with its rule builder underneath"><figcaption><p>Turning the switch on reveals the rule builder in place.</p></figcaption></figure>

## Price

Attaches an extra charge to the option.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings, under <strong>Add-on Settings</strong></td></tr><tr><th>Default</th><td>No add-on</td></tr><tr><th>Available on</th><td>At <strong>option</strong> level: Text, Textarea, Number, Switch, Color picker. At <strong>option value</strong> level, in the values table's <strong>Price</strong> column: all nine selection types with values. <strong>Dimension</strong> has its own price and formula fields</td></tr></thead></table>

{% hint style="info" %}
Where the price lives follows the shape of the option. An input option has one answer, so one price. A selection option has several choices that usually cost different amounts, so the price belongs to each value. See [Where you can set add-ons](../../add-on-pricing/where-you-can-set-add-ons.md).
{% endhint %}

Selecting the field opens a dialog with three tabs — three genuinely different ways to charge:

<table><thead><tr><th width="290">Tab</th><th>What it does</th><th>Stock tracked?</th></tr></thead><tbody><tr><td><strong>Use existing product</strong></td><td>Links a product and variant you already sell. The price comes from that variant.</td><td>Yes</td></tr><tr><td><strong>Automatically generate product</strong></td><td>The app creates a product at the price you type.</td><td>Yes</td></tr><tr><td><strong>Add price</strong></td><td>Adds money to the order with no product behind it.</td><td>No</td></tr></tbody></table>

**Add price** is not supported on Shopify POS. If you sell in person, use one of the product-backed modes. See [POS limitations](../../pos/limitations.md).

Once a value is linked to a product, a **Product** column appears in the values table with a link to open that product in Shopify admin.

Full detail: [Add-on pricing](../../add-on-pricing/README.md).

## Advanced settings

How the add-on charge scales with the main product's quantity.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Default</strong></td></tr><tr><th>Available on</th><td>Every type that can carry an add-on</td></tr></thead></table>

{% hint style="warning" %}
This dropdown only does something when the option actually has a charge. On an option with no add-on it changes nothing.
{% endhint %}

<table><thead><tr><th width="290">Mode</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>The add-on follows the main product's quantity.</td></tr><tr><td><strong>One time charge</strong></td><td>Charged once, however many of the main product are bought.</td></tr><tr><td><strong>Fixed quantity</strong></td><td>Always the quantity you set, regardless of the main product.</td></tr><tr><td><strong>Dynamic quantity</strong></td><td>The quantity you set, multiplied by the main product's quantity.</td></tr><tr><td><strong>Fixed quantity (by customer)</strong></td><td>A quantity box appears for the customer; that quantity is used as-is.</td></tr><tr><td><strong>Dynamic quantity (by customer)</strong></td><td>The customer's quantity, multiplied by the main product's quantity.</td></tr><tr><td><strong>Mixed quantity</strong></td><td>A quantity box per option value. Multi-select options only.</td></tr><tr><td><strong>Per character</strong></td><td>Charged by how many characters the customer typed. <strong>Text</strong> and <strong>Textarea</strong> only.</td></tr></tbody></table>

Each mode is explained with a worked calculation in [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md).

## Set quantity

The number used by two of the modes above.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td>Empty</td></tr><tr><th>Available on</th><td>Appears only when <strong>Advanced settings</strong> is <strong>Fixed quantity</strong> or <strong>Dynamic quantity</strong></td></tr></thead></table>

* With **Fixed quantity**, this is the exact number of add-ons added, whatever the main quantity.
* With **Dynamic quantity**, this is multiplied by the main product's quantity.

For example, a gift box that always includes four ribbons: **Fixed quantity**, **Set quantity** `4`. The same value with **Dynamic quantity** on an order of three boxes gives twelve ribbons.

<!-- SCREENSHOT: type-shared-addon-fields | App admin → builder → option Text | Add-on Settings với field Price và dropdown Advanced settings; nếu chọn Fixed quantity thì hiện Set quantity | Khoanh nhóm Add-on Settings -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The Add-on Settings group with the Price field and the Advanced settings dropdown"><figcaption><p>Price sets the amount; Advanced settings decides how it scales.</p></figcaption></figure>

## How these four interact

<table><thead><tr><th width="330">Combination</th><th>Result</th></tr></thead><tbody><tr><td>A priced option hidden by a rule</td><td>Not shown, not charged. Hiding an option removes its charge.</td></tr><tr><td>A priced option with a <strong>Default value</strong></td><td>Charged the moment the page loads, before the shopper chooses anything.</td></tr><tr><td>A multi-select option with prices</td><td>Every selected value is charged. Cap it with <a href="limits.md#min-and-max-selections">Max selections</a>.</td></tr><tr><td>A required option hidden by a rule</td><td>Not enforced while hidden.</td></tr><tr><td>A priced option on POS with <strong>Add price</strong></td><td>Not supported. Use a product-backed mode.</td></tr></tbody></table>

## Troubleshooting

<details>
<summary>The rule builder does not appear</summary>

Turn the **Conditional logic** switch on. If the switch itself is greyed out, conditional logic is not in your plan — see [Compare plans](../../plans/compare-plans.md).
</details>

<details>
<summary>My conditional rule works in the builder preview but not on the storefront</summary>

Most often a variant-based condition, which the preview cannot evaluate. See [Troubleshooting conditional logic](../../conditional-logic/troubleshooting.md).
</details>

<details>
<summary>I set a Price but the total does not change</summary>

Check **Settings > Settings > Add-on price**: **Show add-on for inputs** and **Show add-on for options** control whether the preview is displayed, and **Add add-on price to the product price** controls whether the shown product price updates. See [Add-on price display settings](../../add-on-pricing/price-display-settings.md).
</details>

<details>
<summary>Advanced settings makes no difference</summary>

The option has no add-on attached, so there is nothing to scale. Set the **Price** field first.
</details>

<details>
<summary>Set quantity is not visible</summary>

It only appears for **Fixed quantity** and **Dynamic quantity**. The other modes either take the quantity from the customer or do not need one.
</details>

<details>
<summary>Mixed quantity is missing from the list</summary>

It requires a multi-select option. Turn on [Allow multiple](selection-behaviour.md#allow-multiple), or use a Checkbox.
</details>

<details>
<summary>Per character is missing from the list</summary>

It exists on **Text** and **Textarea** only — the two types where there are characters to count.
</details>

## Next steps

* [Conditional logic](../../conditional-logic/README.md)
* [Add-on pricing](../../add-on-pricing/README.md)
* [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md)
