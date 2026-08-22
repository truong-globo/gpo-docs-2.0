---
description: Price a product by the measurements the customer enters, using a formula on the Dimension option type.
icon: ruler-combined
---

# Dimension add-on formula

[Dimension](../option-types/input-types/dimension.md) is the only option type that calculates its own price. Instead of a flat charge, you give it a rate and a formula, and the price comes from the measurements the customer entered.

This is how made-to-measure products are priced: blinds, canvases, worktops, glass, cut fabric.

## The two fields

Both are on **Basic Settings**, under the axis rows.

<table><thead><tr><th width="230">Field</th><th>Holds</th></tr></thead><tbody><tr><td><strong>Add-on price</strong></td><td>A number the formula refers to as <code>{{addon}}</code>. Usually your rate per unit of area or length.</td></tr><tr><td><strong>Formula</strong></td><td>An expression using <code>x</code>, <code>y</code>, and <code>z</code> for the three axes, and <code>{{addon}}</code> for the rate.</td></tr></tbody></table>

The field's own placeholder shows the shape of it: `x * y * {{addon}}`.

<table><thead><tr><th width="180">Symbol</th><th>Means</th></tr></thead><tbody><tr><td><code>x</code></td><td>The first axis — usually Width</td></tr><tr><td><code>y</code></td><td>The second axis — usually Height or Drop</td></tr><tr><td><code>z</code></td><td>The third axis — usually Depth, if you kept it</td></tr><tr><td><code>{{addon}}</code></td><td>Whatever you put in <strong>Add-on price</strong></td></tr></tbody></table>

{% hint style="warning" %}
**A formula cannot contain subtraction.** A `-` is rejected while you edit, with "Formula cannot contain subtraction." Express what you need with multiplication, addition, and division instead.
{% endhint %}

## Common formulas

<table><thead><tr><th width="270">Formula</th><th width="180">Prices by</th><th>Use for</th></tr></thead><tbody><tr><td><code>x * y * {{addon}}</code></td><td>Area</td><td>Blinds, canvases, glass, printed panels</td></tr><tr><td><code>x * {{addon}}</code></td><td>Length</td><td>Cut fabric, trim, cable, worktop edging</td></tr><tr><td><code>(x + y) * 2 * {{addon}}</code></td><td>Perimeter</td><td>Frames, mouldings, edge banding</td></tr><tr><td><code>x * y * z * {{addon}}</code></td><td>Volume</td><td>Boxes, packing, foam inserts</td></tr><tr><td><code>x * y * {{addon}} / 10000</code></td><td>Area in square metres, from centimetres</td><td>When your rate is per m² and the customer enters cm</td></tr></tbody></table>

## Working out your rate

The rate is the number that trips people up, because it depends on the units the customer types in.

{% stepper %}
{% step %}
### Pick a size you already know the price of

Say a 60 × 90 cm canvas that you sell for $54.00.
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

120 × 180 = 21600 × 0.01 = $216.00. Is that a price you are happy to sell at? If not, your pricing is not linear and you may need a different approach — see below.
{% endstep %}

{% step %}
### Check your smallest and largest allowed sizes

Enter the minimum and maximum you allow on each axis and confirm both resulting prices are acceptable. This is where you find out that your smallest size prices at almost nothing.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
If the rate ends up as something like `0.0001`, that is normal — it is a price per square centimetre. Set **Min** and **Max** on each axis so nobody can enter a size that produces a nonsense price.
{% endhint %}

## When pricing is not linear

A formula multiplies, so it assumes double the size costs double. Real pricing often does not work that way — small items carry a minimum cost and large ones get cheaper per unit.

Two ways to handle it:

<table><thead><tr><th width="290">Approach</th><th>How</th></tr></thead><tbody><tr><td>A minimum charge</td><td>Add a separate <a href="../option-types/input-types/switch.md">Switch</a> or <a href="../option-types/selection-types/radio-button.md">Radio button</a> priced as a base fee, always applied, with the formula covering only the variable part</td></tr><tr><td>Size bands</td><td>Skip Dimension. Use a <a href="../option-types/selection-types/radio-button.md">Radio button</a> or <a href="../option-types/selection-types/button.md">Button</a> with one value per size band, each individually priced, and a <a href="../option-types/input-types/number.md">Number</a> field for the exact measurement you need for production</td></tr></tbody></table>

Size bands are often the better answer: the customer sees a clear price for their band, and you keep control of every number.

## Worked examples

**A made-to-measure blind**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>X-Axis</td><td>Label <code>Width</code>, unit <code>cm</code>, min <code>30</code>, max <code>240</code></td></tr><tr><td>Y-Axis</td><td>Label <code>Drop</code>, unit <code>cm</code>, min <code>30</code>, max <code>250</code></td></tr><tr><td>Z-Axis</td><td>Deleted</td></tr><tr><td>Add-on price</td><td><code>0.012</code></td></tr><tr><td>Formula</td><td><code>x * y * {{addon}}</code></td></tr></tbody></table>

A 100 × 150 blind: 100 × 150 × 0.012 = **$180.00**.

**A frame priced by perimeter**

Width and height in cm, rate `0.15`, formula `(x + y) * 2 * {{addon}}`.

A 40 × 50 frame: (40 + 50) × 2 × 0.15 = **$27.00**.

**Cut-to-length fabric**

One axis only, label `Length`, unit `m`, rate `12`, formula `x * {{addon}}`.

3.5 metres: 3.5 × 12 = **$42.00**.

## Notes

* The formula is per Dimension option. For two priced measurements sets, use two Dimension options.
* Each axis keeps its own **Unit**, but the formula works on the numbers — it does not convert between units. If one axis is in centimetres and another in metres, do the conversion in the formula.
* **Dimension is not supported in Shopify POS.** For in-person orders, ask for measurements with [Number](../option-types/input-types/number.md) fields and price them another way. See [POS limitations](../pos/limitations.md).
* The measurements reach the order as separate values with their axis labels, so your workshop sees `Width: 100` and `Drop: 150`.

## Troubleshooting

<details>
<summary>"Formula cannot contain subtraction"</summary>

Remove the `-`. Rewrite using multiplication, addition, and division.
</details>

<details>
<summary>The price is out by a factor of ten or a hundred</summary>

The rate is out by an order of magnitude. Work it back from a size whose price you know — see [Working out your rate](#working-out-your-rate).
</details>

<details>
<summary>Small sizes price at almost nothing</summary>

Linear pricing does that. Add a base fee on a separate option, or switch to size bands.
</details>

<details>
<summary>The price does not update as the customer types</summary>

Check the formula refers to the axes you actually kept — a formula using `z` on a two-axis option cannot resolve.
</details>

<details>
<summary>Customers order sizes I cannot make</summary>

**Min** and **Max** are empty on one of the axes. Set both on every axis.
</details>

## Next steps

* [Dimension](../option-types/input-types/dimension.md) — the option type in full.
* [Advanced add-on modes](advanced-add-on-modes.md) — quantity-based pricing instead.
* [How pricing is applied](how-pricing-is-applied.md)
