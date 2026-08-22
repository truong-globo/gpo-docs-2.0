---
description: >-
  Show and hide options based on what the customer already chose — including
  based on the Shopify variant they picked.
icon: sitemap
---

# Overview

Conditional logic is what turns a long form into a short one. Instead of showing every option to every shopper, you show each option only when it is relevant.

Ask for a gift message only when they chose gift wrap. Ask for a shoe width only for the sizes you make it in. Offer engraving fonts only once they have typed something to engrave.

## What it can do

<table><thead><tr><th width="290">Capability</th><th>Detail</th></tr></thead><tbody><tr><td>Show or hide any option</td><td>All 32 option types support conditional logic, including the static ones.</td></tr><tr><td>Show or hide a whole group</td><td>A rule on a <a href="../option-types/static-types/section.md">Section</a> applies to everything inside it.</td></tr><tr><td>React to another option</td><td>Any earlier option in the same option set can be the trigger.</td></tr><tr><td>React to the Shopify variant</td><td>Show an option only for a specific variant the customer selected. See <a href="conditions-on-shopify-variants.md">Conditions based on Shopify variants</a>.</td></tr><tr><td>Combine several conditions</td><td>With <strong>All</strong> or <strong>Any</strong> matching.</td></tr><tr><td>Count rather than compare</td><td>Number of characters typed, number of values selected, number of files attached.</td></tr></tbody></table>

## What it cannot do

* It cannot change an option's price, label, or values — only whether it is shown.
* It cannot read the customer, the country, or the cart. Those are option-set-level rules — see [Assign to customers](../option-sets/assign-to-customers.md) and [Assign to countries](../option-sets/assign-to-countries.md).
* It cannot look at an option **below** itself. Conditions can only read options that appear earlier in the form.
* It cannot read every option type. Twelve types cannot be used as a trigger — see [Build a condition](build-a-condition.md#what-can-be-a-trigger).

## The rule in one sentence

Every rule reads as one sentence in the app:

> **Show** this field if **All** of the following match: **Gift wrap** — **contains** — `Yes, wrap it as a gift`

Four parts: an action, a matching mode, and one or more conditions made of a source, an operator, and a value.

<!-- SCREENSHOT: clo-rule-anatomy | App admin → builder → 1 option có conditional logic bật | Toàn bộ rule builder: Show/Hide, All/Any, 1 dòng điều kiện | Khoanh 4 phần: action, match, source, operator+value -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The conditional logic rule builder with its action, matching mode, and one condition"><figcaption><p>Every rule is an action, a matching mode, and a list of conditions.</p></figcaption></figure>

## Pages in this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Turn on conditional logic</strong></td><td>Where the switch is, and the Show / Hide and All / Any choices.</td><td><a href="turn-it-on.md">turn-it-on.md</a></td></tr><tr><td><strong>Build a condition</strong></td><td>Choosing a source, an operator, and a value — and what can be a trigger.</td><td><a href="build-a-condition.md">build-a-condition.md</a></td></tr><tr><td><strong>Operators reference</strong></td><td>Every operator, grouped by the type of the source option.</td><td><a href="operators-reference.md">operators-reference.md</a></td></tr><tr><td><strong>Conditions based on Shopify variants</strong></td><td>React to the variant the customer picked, and what to check if it does not work.</td><td><a href="conditions-on-shopify-variants.md">conditions-on-shopify-variants.md</a></td></tr><tr><td><strong>Examples and recipes</strong></td><td>Eight complete rules you can copy.</td><td><a href="examples-and-recipes.md">examples-and-recipes.md</a></td></tr><tr><td><strong>Troubleshooting</strong></td><td>When a rule fires at the wrong time, or never.</td><td><a href="troubleshooting.md">troubleshooting.md</a></td></tr></tbody></table>

## Two things to know before you start

{% hint style="warning" %}
**A hidden option is not validated.** If a required option is currently hidden by a rule, it does not block **Add to cart**. That is deliberate — otherwise a hidden field could make the product unbuyable — but it means "required" only holds while the option is visible. Test both branches of every rule.
{% endhint %}

{% hint style="info" %}
**Conditions can only read options above the one you are configuring.** The source dropdown lists only the options that appear earlier in the form. If the option you want to react to is not listed, move it above this one in the builder. See [Build your options](../option-sets/build-options.md).
{% endhint %}

## Plans

Conditional logic comes at two levels, and which you have depends on your plan:

<table><thead><tr><th width="230">Level</th><th>What you get</th></tr></thead><tbody><tr><td><strong>Basic</strong></td><td>Rules based on other options in the option set.</td></tr><tr><td><strong>Advanced</strong></td><td>The same, plus conditions based on the <strong>Shopify variant</strong> the customer selected.</td></tr></tbody></table>

On a Basic plan you can still select **Shopify variant** as a source, but the operator and value fields are locked with an upgrade prompt. See [Compare plans](../plans/compare-plans.md).

## Where to put the rule

If several options should appear together, put one rule on the [Section](../option-types/static-types/section.md) around them rather than the same rule on each option. One rule is faster to build, easier to read, and impossible to get half-right.

## Next steps

* [Turn on conditional logic](turn-it-on.md)
* [Examples and recipes](examples-and-recipes.md) — if you would rather start from a working rule.
* [Conditional logic and add-on fields](../option-types/shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic) — the settings reference.
