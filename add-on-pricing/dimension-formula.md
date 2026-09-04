---
description: Price a product by the measurements the customer enters, using a formula on the Dimension option type.
icon: ruler-combined
---

# Dimension add-on formula

[Dimension](../option-types/input-types/dimension.md) is the only option type that calculates its own price. Instead of a flat charge, you set a rate and a formula, and the price is calculated from the measurements the customer enters.

Use it for made-to-measure products such as blinds, canvases, worktops, glass, and cut fabric.

## The two fields

Both are on **Basic Settings**, under the axis rows.

<table><thead><tr><th width="230">Field</th><th>Holds</th></tr></thead><tbody><tr><td><strong>Add-on price</strong></td><td>A number the formula refers to as <code>{{addon}}</code>. Usually your rate per unit of area or length.</td></tr><tr><td><strong>Formula</strong></td><td>An expression using <code>x</code>, <code>y</code>, and <code>z</code> for the three axes, and <code>{{addon}}</code> for the rate.</td></tr></tbody></table>

The field's placeholder shows the expected format: `x * y * {{addon}}`.

<table><thead><tr><th width="180">Symbol</th><th>Means</th></tr></thead><tbody><tr><td><code>x</code></td><td>The first axis — usually Width</td></tr><tr><td><code>y</code></td><td>The second axis — usually Height or Drop</td></tr><tr><td><code>z</code></td><td>The third axis — usually Depth, if you kept it</td></tr><tr><td><code>{{addon}}</code></td><td>Whatever you put in <strong>Add-on price</strong></td></tr></tbody></table>

{% hint style="warning" %}
**A formula cannot contain subtraction.** A `-` is rejected with the message "Formula cannot contain subtraction." Use multiplication, addition, and division instead.
{% endhint %}

## Common formulas

<table><thead><tr><th width="270">Formula</th><th width="180">Prices by</th><th>Use for</th></tr></thead><tbody><tr><td><code>x * y * {{addon}}</code></td><td>Area</td><td>Blinds, canvases, glass, printed panels</td></tr><tr><td><code>x * {{addon}}</code></td><td>Length</td><td>Cut fabric, trim, cable, worktop edging</td></tr><tr><td><code>(x + y) * 2 * {{addon}}</code></td><td>Perimeter</td><td>Frames, mouldings, edge banding</td></tr><tr><td><code>x * y * z * {{addon}}</code></td><td>Volume</td><td>Boxes, packing, foam inserts</td></tr><tr><td><code>x * y * {{addon}} / 10000</code></td><td>Area in square metres, from centimeters</td><td>When your rate is per m² and the customer enters cm</td></tr></tbody></table>

## Working out your rate

The rate depends on the units the customer enters, so calculate it from a size you already price.

{% stepper %}
{% step %}
### Pick a size you already know the price of

For example, a 60 × 90 cm canvas that you sell for $54.00.
{% endstep %}

{% step %}
### Divide the price by the formula's result without the rate

For an area formula: 60 × 90 = 5400. Then 54 ÷ 5400 = **0.01**.
{% endstep %}

{% step %}
### Put that number in Add-on price

`0.01`, with the formula `x * y * {{addon}}`.
{% endstep %}

{% step %}
### Check a second size

120 × 180 = 21600, and 21600 × 0.01 = $216.00. If that price is not acceptable, your pricing is not linear. See [When pricing is not linear](#when-pricing-is-not-linear) below.
{% endstep %}

{% step %}
### Check your smallest and largest allowed sizes

Enter the minimum and maximum you allow on each axis, and check that both resulting prices are acceptable. A very small size can produce a price close to zero.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
A rate such as `0.0001` is normal. It is a price per square centimeter. Set **Min** and **Max** on each axis so a customer cannot enter a size that produces an incorrect price.
{% endhint %}

## When pricing is not linear

A formula multiplies, so it assumes that double the size costs double the price. Real pricing often differs, because small items have a minimum cost and large items cost less per unit.

There are two alternatives:

<table><thead><tr><th width="290">Approach</th><th>How</th></tr></thead><tbody><tr><td>A minimum charge</td><td>Add a separate <a href="../option-types/input-types/switch.md">Switch</a> or <a href="../option-types/selection-types/radio-button.md">Radio button</a> priced as a base fee, always applied, with the formula covering only the variable part</td></tr><tr><td>Size bands</td><td>Skip Dimension. Use a <a href="../option-types/selection-types/radio-button.md">Radio button</a> or <a href="../option-types/selection-types/button.md">Button</a> with one value per size band, each individually priced, and a <a href="../option-types/input-types/number.md">Number</a> field for the exact measurement you need for production</td></tr></tbody></table>

Size bands are usually the better option. The customer sees a clear price for their band, and you set every price.

## Worked examples

**A made-to-measure blind**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>X-Axis</td><td>Label <code>Width</code>, unit <code>cm</code>, min <code>30</code>, max <code>240</code></td></tr><tr><td>Y-Axis</td><td>Label <code>Drop</code>, unit <code>cm</code>, min <code>30</code>, max <code>250</code></td></tr><tr><td>Z-Axis</td><td>Deleted</td></tr><tr><td>Add-on price</td><td><code>0.012</code></td></tr><tr><td>Formula</td><td><code>x * y * {{addon}}</code></td></tr></tbody></table>

For a 100 × 150 blind: 100 × 150 × 0.012 = **$180.00**.

**A frame priced by perimeter**

Width and height in cm, rate `0.15`, formula `(x + y) * 2 * {{addon}}`.

For a 40 × 50 frame: (40 + 50) × 2 × 0.15 = **$27.00**.

**Cut-to-length fabric**

One axis only, with the label `Length`, the unit `m`, a rate of `12`, and the formula `x * {{addon}}`.

For For 3.5 meters: 3.5 × 12 = **$42.00**.

## Notes

* The formula is set per Dimension option. For two sets of priced measurements, use two Dimension options.
* Each axis has its own **Unit**, but the formula uses the numbers only and does not convert between units. If one axis uses centimeters and another uses meters, convert the value in the formula.
* **Dimension is not supported in Shopify POS.** For in-person orders, collect measurements with [Number](../option-types/input-types/number.md) fields and apply the price another way. See [POS limitations](../pos/limitations.md).
* Each measurement is stored in the order as its own value with the axis label, for example `Width: 100` and `Drop: 150`.
