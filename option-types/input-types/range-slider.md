---
description: >-
  A number chosen by dragging, bounded by a minimum, a maximum, and a step.
icon: sliders
---

# Range slider

A track the customer drags to choose a number. Same result as a [Number](number.md) field, different feel.

Use it when the value is approximate and the range matters more than precision — a budget, a length within a comfortable span, a quantity between two sensible bounds.

## What customers see

A slider with the current value shown, bounded at both ends. It can be given a prefix and a suffix so the value reads with its unit.

<!-- SCREENSHOT: type-range-storefront | Storefront → trang sản phẩm | 1 Range slider với giá trị hiện tại, prefix/suffix | Khoanh riêng slider -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A range slider on a storefront product page showing its current value with a unit"><figcaption><p>A slider communicates the available range at a glance.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until a value is set.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-value">Min value</a></td><td>The left end of the track. Starts at <code>0</code>.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-value">Max value</a></td><td>The right end of the track. Starts at <code>100</code>.</td></tr><tr><td><strong>Step</strong></td><td>The increment the slider moves in. Starts at <code>1</code>.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>Where the handle starts.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

Unlike Number, the slider's min and max are not optional — they define the track, so both always have a value.

### Step

**Step** is the setting people forget. It decides which values are reachable at all.

<table><thead><tr><th width="180">Min / Max</th><th width="130">Step</th><th>Selectable values</th></tr></thead><tbody><tr><td>0 / 100</td><td><code>1</code></td><td>0, 1, 2, … 100</td></tr><tr><td>0 / 100</td><td><code>5</code></td><td>0, 5, 10, … 100</td></tr><tr><td>0 / 10</td><td><code>0.5</code></td><td>0, 0.5, 1, … 10</td></tr><tr><td>10 / 240</td><td><code>10</code></td><td>10, 20, 30, … 240</td></tr></tbody></table>

A wide range with a step of `1` is fiddly to hit precisely on a phone. Choose a step that matches how exactly you actually need the answer — and if you need exactness, use a [Number](number.md) field instead.

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Prefix</strong></td><td>Fixed text before the value, such as a currency symbol. A plain text field on this type — there is no icon-or-text choice.</td></tr><tr><td><strong>Suffix</strong></td><td>Fixed text after the value, such as <code>cm</code> or <code>%</code>.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

Set a suffix on anything with a unit. A slider showing `180` is ambiguous; `180 cm` is not.

## Add-on pricing and Personalizer

Neither is supported. The slider cannot carry a price and does not appear in the live preview.

That is the practical reason to prefer [Number](number.md) whenever the value should drive a charge — Number's **Fixed quantity (by customer)** and **Dynamic quantity (by customer)** modes turn the entered figure into the add-on quantity. A slider cannot.

For size-driven pricing across two or three measurements, use [Dimension](dimension.md), which has a formula.

## Design

The slider's colours are store-wide, in **Settings > Design**: **Range slider thumb**, **Range slider background**, and **Range slider active background**. See [Colors](../../storefront/colors.md).

## Examples

**Length within a comfortable span**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Chain length</code></td></tr><tr><td>Min / Max</td><td><code>40</code> / <code>60</code></td></tr><tr><td>Step</td><td><code>2</code></td></tr><tr><td>Default value</td><td><code>45</code></td></tr><tr><td>Suffix</td><td><code>cm</code></td></tr></tbody></table>

**A budget for a bespoke commission**

Min `100`, max `2000`, step `50`, prefix `$`, help text `We will come back to you with options in this range.`

**Firmness or intensity**

Min `1`, max `5`, step `1`, suffix ` / 5`, no price.

**A donation added to the order**

Better as a [Number](number.md) field, so the figure can drive an add-on quantity — a slider cannot be priced.

## Limits and notes

* Available on the Advanced plan.
* Works in Shopify POS.
* Cannot carry an add-on price; no Personalizer support.
* Both **Min value** and **Max value** are required, since they define the track.
* Poorly suited to precise entry, especially on touch devices. Use Number for exact figures.
* The chosen number reaches the order as a plain value, without the prefix or suffix.

## Troubleshooting

<details>
<summary>Shoppers cannot land on the exact value they want</summary>

**Step** is too coarse, or the range is too wide for a slider. Reduce the step, narrow the range, or switch to a [Number](number.md) field.
</details>

<details>
<summary>I cannot find a Price field</summary>

Range slider has none. Use Number if the value should drive a charge.
</details>

<details>
<summary>The value has no unit on the order</summary>

Prefix and suffix are display only. Put the unit in the option's **Name** — `Chain length (cm)`.
</details>

<details>
<summary>The slider does not match my theme's colours</summary>

Its three colours are in **Settings > Design**. See [Colors](../../storefront/colors.md).
</details>

<details>
<summary>Range slider is greyed out</summary>

It is on the Advanced plan. See [Compare plans](../../plans/compare-plans.md).
</details>
