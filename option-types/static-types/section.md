---
description: >-
  The container that groups options under a heading, optionally collapsible — and
  the one static type you should use on every long form.
icon: layer-group
---

# Section

A container. Options live inside it, and it gives them a shared heading and, if you want, a single collapsible panel.

Every new option set starts with one empty Section, because options have to live somewhere.

## What customers see

A heading with your options beneath it. With a collapsible style, the heading becomes a control that opens and closes the group.

<!-- SCREENSHOT: type-section-storefront | Storefront → trang sản phẩm | 2 Section: 1 style Default mở, 1 style Collapse đang đóng | Khoanh 2 tiêu đề section -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Two sections on a storefront product page, one open and one collapsed"><figcaption><p>Sections turn a long list of fields into a short list of groups.</p></figcaption></figure>

## Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a></td><td>The heading shoppers read above the group. Required.</td></tr><tr><td><strong>Style</strong></td><td><strong>Default</strong>, <strong>Expand</strong>, or <strong>Collapse</strong>. See below.</td></tr><tr><td><strong>Prefix icon</strong></td><td>An icon beside the heading, from the app's icon picker.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a></td><td>A CSS class for your own styling.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide the whole section, and everything inside it.</td></tr></tbody></table>

Section has no **Name**, no **Column width**, and no add-on or Personalizer settings. It is a container.

### Style

<table><thead><tr><th width="180">Style</th><th>Behaviour</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>Always open, no toggle</td><td>The options inside are needed by most shoppers</td></tr><tr><td><strong>Expand</strong></td><td>Collapsible, starts open</td><td>Most shoppers want it, but you are happy for them to fold it away</td></tr><tr><td><strong>Collapse</strong></td><td>Collapsible, starts closed</td><td>An optional or advanced group most shoppers skip</td></tr></tbody></table>

{% hint style="warning" %}
Do not put **required** options inside a **Collapse** section. Shoppers do not open groups they cannot see the point of, and then they hit a validation error about a field they never saw. Keep required options in a **Default** or **Expand** section.
{% endhint %}

## The most useful thing about sections

**Conditional logic on a section applies to everything inside it.**

If you have six options that should only appear when the customer chooses "Personalise this item", you have two choices:

* put the same rule on all six options — six rules to write and six to maintain
* put one rule on the section around them — one rule

The second is always better. It is faster to build, easier to read, and impossible to get half-right.

See [Conditional logic](../../conditional-logic/README.md).

## Structuring a long form

A form with fifteen options is hard to read. The same fifteen in four sections is not:

```
▸ Personalise your bracelet          (Expand)
    Engraving text
    Engraving font
    Engraving position

▸ Gift options                       (Collapse)
    Gift wrap
    Gift message
    Send directly to recipient

▸ Delivery                           (Default)
    Delivery date
    Delivery notes

▸ Size guide                         (Collapse)
    Size chart
```

The shopper sees four decisions rather than fifteen fields, and opens only what they need.

## Working with sections in the builder

<table><thead><tr><th width="270">Action</th><th>How</th></tr></thead><tbody><tr><td>Add a section</td><td><strong>Add section</strong> in the add picker.</td></tr><tr><td>Move options into it</td><td>Drag them in. Options can be dragged between sections freely.</td></tr><tr><td>Move a whole section</td><td>Drag the section — everything inside comes with it.</td></tr><tr><td>Duplicate a section</td><td>Use the section's actions menu. Everything inside is copied, with names renumbered to stay unique.</td></tr><tr><td>Delete a section</td><td>Removes the section and everything inside it. You are asked to confirm.</td></tr></tbody></table>

{% hint style="danger" %}
Deleting a section deletes the options inside it. If you only want to remove the grouping, drag the options out first.
{% endhint %}

See [Build your options](../../option-sets/build-options.md).

## Examples

**Optional personalisation, hidden until asked for**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label</td><td><code>Personalise your bracelet</code></td></tr><tr><td>Style</td><td><strong>Collapse</strong></td></tr><tr><td>Prefix icon</td><td>A paintbrush</td></tr><tr><td>Conditional logic</td><td>Show when <strong>Add personalisation</strong> is enabled</td></tr><tr><td>Contains</td><td>Engraving text, font, position — none required</td></tr></tbody></table>

**A required group, always open**

Label `Choose your size`, **Style** **Default**, containing a required size button row.

**A reference group at the bottom**

Label `Size guide and care`, **Style** **Collapse**, containing a size chart and a paragraph.

## Limits and notes

* Available on the Advanced plan.
* Works in Shopify POS.
* Sections cannot be nested inside each other.
* Every option lives inside a section — there is no "loose" option outside one.
* An option set with sections but no options inside them cannot be saved.
* Sections collect nothing, so they never appear on the cart or the order.

## Troubleshooting

<details>
<summary>An option set will not save, even though I added sections</summary>

Sections are containers. You need at least one actual option inside one. See [Create an option set](../../option-sets/create-an-option-set.md).
</details>

<details>
<summary>Shoppers are missing a required field</summary>

It is inside a **Collapse** section they never opened. Move it, or change the style to **Expand**.
</details>

<details>
<summary>I deleted a section and lost my options</summary>

Deleting a section deletes its contents. Drag options out first next time.
</details>

<details>
<summary>I cannot nest a section inside another</summary>

Not supported. Use one level of sections, and [conditional logic](../../conditional-logic/README.md) for finer control.
</details>

<details>
<summary>Section is greyed out</summary>

It is on the Advanced plan. See [Compare plans](../../plans/compare-plans.md).
</details>

<details>
<summary>The heading does not match my theme</summary>

Its colours are store-wide: **Group label**, **Group icon**, and **Group chevron** in **Settings > Design**. See [Colors](../../storefront/colors.md).
</details>

## Next steps

* [Heading](heading.md) — a heading without a container.
* [Conditional logic](../../conditional-logic/README.md) — one rule for a whole group.
* [Build your options](../../option-sets/build-options.md)
