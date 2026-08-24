---
description: >-
  A rule that fires at the wrong time, or never — worked through by symptom, in
  the order worth checking.
icon: wrench
---

# Troubleshooting conditional logic

Nearly every conditional logic problem is one of five things. Work through this page top to bottom and you will find it.

## Start here: the five usual causes

<table><thead><tr><th width="60">#</th><th width="290">Cause</th><th>Check</th></tr></thead><tbody><tr><td>1</td><td>The value does not match exactly</td><td>Copy the value from the source option's values table rather than retyping it</td></tr><tr><td>2</td><td><strong>is equal to</strong> used on a multi-select option</td><td>Use <strong>contains</strong> instead</td></tr><tr><td>3</td><td>The trigger sits below the option carrying the rule</td><td>Move the trigger up in the builder</td></tr><tr><td>4</td><td>A variant condition being tested in the builder preview</td><td>Test on a real product page with <strong>View in Store</strong></td></tr><tr><td>5</td><td><strong>Hide</strong> where <strong>Show</strong> was meant, or <strong>All</strong> where <strong>Any</strong> was meant</td><td>Read the rule out loud as a sentence</td></tr></tbody></table>

## By symptom

<details>
<summary>The option never appears</summary>

In order:

1. **Read the rule as a sentence.** "Show this field if All of the following match: Gift wrap contains Yes." Does that describe what you want? A **Hide** rule with true conditions hides the option — which is correct behaviour and a common mix-up.
2. **Check the value character for character.** Open the source option's values table and compare. A trailing space or different capitalisation is enough to break it.
3. **On a multi-select source, use contains.** With **is equal to**, a shopper who selects two values matches nothing.
4. **With two or more conditions on All**, check they can be true simultaneously. `Size is equal to S` and `Size is equal to L` never can.
5. **Check the source still exists.** If you deleted the trigger option, the condition resets to an empty row.

</details>

<details>
<summary>The option is always visible</summary>

1. The conditions are always true — for example **number of characters is greater than** `-1`, or a value that is also the default.
2. You have **Show** with **Any** and one condition that is always satisfied.
3. Conditional logic is not actually on. Check the switch, and check the option set was saved.
4. Your plan may not include conditional logic, in which case rules are stored but not applied. See [Locked features](../plans/compare-plans.md).

</details>

<details>
<summary>It works in the builder preview but not on the storefront</summary>

Three possibilities:

1. **A variant condition.** The preview has no variant selected, so those conditions do not evaluate there. They can only be tested on a real product page. See [Conditions based on Shopify variants](conditions-on-shopify-variants.md).
2. **The option set was not saved** after you edited the rule.
3. **Your storefront is in a different language** from the one you configured the value in. Variant condition values are stored per language.

</details>

<details>
<summary>It works on the storefront but not in the preview</summary>

Almost always a variant condition, for the same reason as above. This is expected, not a fault.

</details>

<details>
<summary>The option I want is not in the source dropdown</summary>

Two reasons:

1. **It sits below the option you are configuring.** Conditions can only read options that appear earlier in the form. Drag it above and it appears.
2. **Its type cannot be a trigger.** Twelve types cannot: Hidden field, Heading, Divider, Spacing, Paragraph, HTML, Pop-up modal, Tabs, Product links, Size chart, Section, and Dimension. See [Build a condition](build-a-condition.md#what-can-be-a-trigger).

</details>

<details>
<summary>A required option is being skipped</summary>

This is by design: **a hidden option is not validated**. If the rule is hiding it, it cannot block **Add to cart**.

If the option must always be filled in, it cannot be conditional. If it is only required in one branch, that is exactly what this behaviour gives you — but test both branches so you know what shoppers can get away with.

</details>

<details>
<summary>An add-on charge is missing</summary>

Same cause: **a hidden option is not charged**. Hiding an option removes its price from the total. If the charge should always apply, the option cannot be conditional — or the charge belongs on an option that is always visible.

</details>

<details>
<summary>The rule broke after I edited an option value</summary>

Renaming a value breaks any condition pointing at the old text. Reopen the rule and reselect the value from the dropdown.

Deleting a value has the same effect. Deleting the whole source option invalidates the condition, which resets to an empty row.

</details>

<details>
<summary>The rule broke after I changed an option's type</summary>

Operator sets are per type, so an operator that was valid for a text source may not exist for a dropdown source. Reopen every rule that reads this option and reselect the operator, then the value.

See [Operators reference](operators-reference.md).

</details>

<details>
<summary>The rule broke after duplicating or importing</summary>

Duplicates and imports get renumbered names to stay unique, and rules pointing at them are repointed automatically — so the rules usually survive. What does not survive is your ability to tell the copies apart. Rename them, then check each rule points at the option you meant.

</details>

<details>
<summary>A variant condition never matches</summary>

Five things to check: the variant name is typed exactly as in Shopify admin; on a multi-dimension product it is the full name `Size / Colour`, not one part; your plan includes advanced conditional logic; the value is entered in the storefront language you are testing; and you are testing on a real product page, because variant conditions cannot evaluate in the builder preview. If all five are right, it is theme integration — see [Conditions based on Shopify variants](conditions-on-shopify-variants.md).

</details>

<details>
<summary>I need "A and (B or C)"</summary>

Not possible in a single rule — all conditions share one matching mode. Two ways round it:

* Put part of the logic on a [Section](../option-types/static-types/section.md) and the rest on the option inside it. Both must pass, giving you an implicit **and** between two rules.
* Add two copies of the option with different simpler rules, making sure their conditions cannot both be true.

</details>

<details>
<summary>A divider or heading is left stranded</summary>

The options around it are hidden but it is not. Put the same rule on it, or better, move the whole group into a [Section](../option-types/static-types/section.md) with one rule on the section.

</details>

<details>
<summary>The form flickers or jumps as the customer types</summary>

A rule using a character-count operator is toggling an option on and off as the length crosses your threshold. Choose a threshold that is not near the typical entry length — `0` is safest, since it only fires once.

</details>

## How to test a rule properly

{% stepper %}
{% step %}
### Test both branches in the preview

Not just the interesting one. Set the trigger so the rule fires, then so it does not, and check both results.
{% endstep %}

{% step %}
### Check what happens with nothing selected

A shopper arriving at the page has made no choices. Is the form sensible in that state?
{% endstep %}

{% step %}
### Check the required options in every branch

A required option that is hidden is not enforced. Make sure each branch still collects what you need.
{% endstep %}

{% step %}
### Check the price in every branch

Hidden options are not charged. Confirm the total is right in each branch.
{% endstep %}

{% step %}
### Test on a real product page

With **View in Store**. Essential for variant conditions, and worth it for everything else — your theme, not the preview, is what shoppers see.
{% endstep %}

{% step %}
### Test on a phone

Conditional logic changes the page height as options appear. Check the result is not confusing on a small screen.
{% endstep %}
{% endstepper %}

## Still stuck?

Include these when you [contact support](../help/contact-support.md): the option set name, the option carrying the rule, the exact rule as it reads in the app, and what you expected against what happened. If it is a variant condition, add the product and variant names.
