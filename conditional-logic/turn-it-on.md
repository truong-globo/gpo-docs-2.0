---
description: >-
  Where the conditional logic switch lives, and what the Show, Hide, All, and Any
  choices actually do.
icon: toggle-on
---

# Turn on conditional logic

## Before you start

* An option set is open in the builder with at least two options in it — one to react, one to react *to*.
* The option you want to react to must sit **above** the option you are configuring. If it does not, drag it up first. See [Build your options](../option-sets/build-options.md).
* Conditional logic is plan-gated. If the switch is greyed out, see [Compare plans](../plans/compare-plans.md).

## Steps

{% stepper %}
{% step %}
### Select the option that should appear or disappear

This is the important thing to get right. The rule goes on the option whose **visibility** is being controlled, not on the option that triggers it.

If you want a gift message box to appear when gift wrap is ticked, the rule goes on the **gift message** option.
{% endstep %}

{% step %}
### Turn on Conditional logic

On **Basic Settings**, find the **Conditional logic** switch and turn it on.

A rule builder appears directly underneath.
{% endstep %}

{% step %}
### Choose the action

The first dropdown is **Show** or **Hide**.
{% endstep %}

{% step %}
### Choose the matching mode

The second dropdown is **All** or **Any**. It only matters once you have more than one condition.
{% endstep %}

{% step %}
### Build the condition

One row: a source, an operator, and a value. See [Build a condition](build-a-condition.md).
{% endstep %}

{% step %}
### Test it in the preview

The builder's live preview runs your rules. Change the trigger option and watch the dependent option appear and disappear.

The one thing the preview cannot test is a variant-based condition, because it has no variant selected. See [Live preview and inspector](../option-sets/live-preview-and-inspector.md).
{% endstep %}

{% step %}
### Save

Then test on your storefront with **View in Store**, checking both branches.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: clo-switch-on | App admin → builder → 1 option | Switch Conditional logic vừa bật, rule builder xuất hiện bên dưới | Khoanh switch -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The conditional logic switch turned on with the rule builder revealed underneath"><figcaption><p>The rule goes on the option being shown or hidden, not on the trigger.</p></figcaption></figure>

## Show or Hide

Both do the same job from opposite directions. The rule is evaluated, and then:

<table><thead><tr><th width="180">Action</th><th width="230">Conditions met</th><th>Conditions not met</th></tr></thead><tbody><tr><td><strong>Show</strong></td><td>The option is visible</td><td>The option is hidden</td></tr><tr><td><strong>Hide</strong></td><td>The option is hidden</td><td>The option is visible</td></tr></tbody></table>

### Which to choose

They are logically interchangeable, but one is almost always clearer to read later.

<table><thead><tr><th width="330">What you want</th><th>Use</th></tr></thead><tbody><tr><td>An option that is normally irrelevant, and becomes relevant</td><td><strong>Show</strong> — the default state is hidden, which is what you want</td></tr><tr><td>An option that is normally relevant, with one exception</td><td><strong>Hide</strong> — the default state is visible</td></tr><tr><td>An option revealed by a single yes-or-no choice</td><td><strong>Show</strong> when the switch is enabled</td></tr><tr><td>An option that must disappear for one specific variant</td><td><strong>Hide</strong> when the variant matches</td></tr></tbody></table>

{% hint style="info" %}
Prefer **Show** as your default habit. An option that starts hidden and appears when needed keeps the initial page short, which is the main reason to use conditional logic at all.
{% endhint %}

## All or Any

<table><thead><tr><th width="180">Mode</th><th>Fires when</th><th>Effect</th></tr></thead><tbody><tr><td><strong>All</strong></td><td>Every condition is true</td><td>Narrows. Each condition you add makes the rule fire less often.</td></tr><tr><td><strong>Any</strong></td><td>At least one condition is true</td><td>Widens. Each condition you add makes the rule fire more often.</td></tr></tbody></table>

With one condition the setting makes no difference.

### Worked comparison

Two conditions: `Gift wrap` **contains** `Yes` and `Delivery` **is equal to** `Express`.

<table><thead><tr><th width="230">Mode and action</th><th>The option appears when</th></tr></thead><tbody><tr><td><strong>Show</strong> + <strong>All</strong></td><td>Gift wrap is ticked <strong>and</strong> delivery is Express</td></tr><tr><td><strong>Show</strong> + <strong>Any</strong></td><td>Gift wrap is ticked <strong>or</strong> delivery is Express</td></tr><tr><td><strong>Hide</strong> + <strong>All</strong></td><td>Everything except when both are true</td></tr><tr><td><strong>Hide</strong> + <strong>Any</strong></td><td>Only when neither is true</td></tr></tbody></table>

The last two are the ones that catch people out. **Hide** plus **Any** means "hide it if any one of these is true", so the option is only visible when none of them are.

## Adding and removing conditions

* **Add another condition** appends a row.
* Each row has a delete action.
* All rows in one rule share the same **All** or **Any** mode — you cannot mix `A and (B or C)` in a single rule.

### When you need mixed logic

If you genuinely need "A and (B or C)", split the work:

* Put part of the logic on a [Section](../option-types/static-types/section.md) and the rest on the option inside it. Both must pass for the option to show, which gives you an implicit **and** between two rules.
* Or add two copies of the option, each with its own simpler rule, and make sure their conditions cannot both be true.

## Rules on a Section

**Section** supports conditional logic like any other type, and a rule there controls everything inside it.

Use it whenever more than two options share the same condition. One rule on the section beats six identical rules on six options — and when the condition later changes, you edit it once.

See [Section](../option-types/static-types/section.md).

## Limits and notes

* A hidden option is **not validated**, so a required option currently hidden cannot block add to cart.
* A hidden option with an add-on price is **not charged**. Hiding removes the charge.
* Rules are evaluated live in the shopper's browser as they make choices — there is no page reload.
* Rules are evaluated on the storefront and in the builder preview, but customer and country rules are not — those decide whether the whole option set renders.

## Troubleshooting

<details>
<summary>The switch is greyed out</summary>

Conditional logic is not in your plan. See [Compare plans](../plans/compare-plans.md).
</details>

<details>
<summary>The rule builder is empty, or the source dropdown has nothing in it</summary>

There is no eligible option above this one. Move the trigger option higher in the form, and check its type can be a trigger — twelve types cannot. See [Build a condition](build-a-condition.md#what-can-be-a-trigger).
</details>

<details>
<summary>The option is always visible</summary>

Either the conditions are always true, or you have **Hide** where you meant **Show**. Read the rule out loud as a sentence.
</details>

<details>
<summary>Two conditions and it never fires</summary>

You are on **All** and the two conditions contradict each other. Switch to **Any**, or fix the conditions.
</details>

<details>
<summary>A required option is being skipped</summary>

It is hidden by the rule, and hidden options are not validated. Either make it visible in that branch, or accept that it is optional there.
</details>
