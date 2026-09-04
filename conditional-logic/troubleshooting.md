---
description: >-
  A rule that fires at the wrong time, or never — worked through by symptom, in
  the order worth checking.
icon: wrench
---

# Troubleshooting conditional logic

Most conditional logic problems have one of five causes. Work through this page from the top.

## Start here: the five usual causes

<table><thead><tr><th width="60">#</th><th width="290">Cause</th><th>Check</th></tr></thead><tbody><tr><td>1</td><td>The value does not match exactly</td><td>Copy the value from the source option's values table rather than retyping it</td></tr><tr><td>2</td><td><strong>is equal to</strong> used on a multi-select option</td><td>Use <strong>contains</strong> instead</td></tr><tr><td>3</td><td>The trigger sits below the option carrying the rule</td><td>Move the trigger up in the builder</td></tr><tr><td>4</td><td>A variant condition being tested in the builder preview</td><td>Test on a real product page with <strong>View in Store</strong></td></tr><tr><td>5</td><td><strong>Hide</strong> where <strong>Show</strong> was meant, or <strong>All</strong> where <strong>Any</strong> was meant</td><td>Read the rule out loud as a sentence</td></tr></tbody></table>

## By symptom

<details>

<summary>The option never appears</summary>

In order:

1. **Read the rule as a sentence.** For example, "Show this field if All of the following match: Gift wrap contains Yes." Check that this describes what you want. A **Hide** rule with matching conditions hides the option, which is correct behavior but often misread.
2. **Check the value exactly.** Open the source option's values table and compare. A trailing space or a difference in capitalization prevents a match.
3. **On a multi-select source, use contains.** With **is equal to**, a customer who selects two values matches nothing.
4. **With two or more conditions on All**, check that they can be true at the same time. `Size is equal to S` and `Size is equal to L` never can.
5. **Check the source still exists.** If you deleted the trigger option, the condition resets to an empty row.

</details>

<details>

<summary>The option is always visible</summary>

1. The conditions are always true; for example **number of characters is greater than** `-1`, or a value that is also the default.
2. You have **Show** with **Any** and one condition that is always satisfied.
3. Conditional logic is not actually on. Check the switch, and check that the option set was saved.
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

This is almost always a variant condition for the reason described above. It is expected behavior.

</details>

<details>

<summary>The option I want is not in the source dropdown</summary>

Two reasons:

1. **It appears below the option you are configuring.** Conditions can only reference options that appear earlier in the form. Move it above the current option.
2. **Its type cannot be a trigger.** The following types cannot: Hidden field, Heading, Divider, Spacing, Paragraph, HTML, Pop-up modal, Tabs, Product links, Size chart, Section, and Dimension. See [Build a condition](build-a-condition.md#what-can-be-a-trigger).

</details>

<details>

<summary>A required option is being skipped</summary>

This is by design: **a hidden option is not validated**. If the rule is hiding it, it cannot block **Add to cart**.

If the option must always be completed, it cannot be conditional. If it is required only in one branch, this behavior is correct. Test both branches so you know what customers can submit.

</details>

<details>

<summary>An add-on charge is missing</summary>

This has the same cause: **a hidden option is not charged**. Hiding an option removes its price from the total. If the charge must always apply, apply it to an option that is always visible.

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

Duplicated and imported options are renamed to keep their names unique, and rules referencing them are updated automatically, so the rules usually still work. The copies are harder to tell apart, so rename them and check that each rule references the correct option.

</details>

<details>

<summary>A variant condition never matches</summary>

Five things to check:&#x20;

* The variant name is typed exactly as in Shopify admin;&#x20;
* On a multi-dimension product it is the full name `Size / Colour`, not one part;
* Your plan includes advanced conditional logic;&#x20;
* The value is entered in the storefront language you are testing;&#x20;
* You are testing on a real product page, because variant conditions cannot evaluate in the builder preview. If all five are correct, the cause is theme integration. See [Conditions based on Shopify variants](conditions-on-shopify-variants.md).

</details>

<details>

<summary>I need "A and (B or C)"</summary>

This is not possible in a single rule because all conditions share one matching mode. There are two alternatives:

* Apply part of the logic to a [Section](../option-types/static-types/section.md) and the rest to the option inside it. Both rules must match, which creates an **AND** between them.
* Add two copies of the option with simpler rules, and make sure their conditions cannot both be true.

</details>

<details>

<summary>A divider or heading is left stranded</summary>

The options around it are hidden, but the divider or heading is not. Apply the same rule to it, or move the whole group into a [Section](../option-types/static-types/section.md) with one rule on the section.

</details>

<details>

<summary>The form flickers or jumps as the customer types</summary>

A rule using a character-count operator shows and hides an option each time the entry crosses the threshold. Use a threshold that is not close to the typical entry length. A value of `0` is safest, because the rule then changes state only once.

</details>

## How to test a rule properly

{% stepper %}
{% step %}
### Test both branches in the preview

Set the trigger so the rule matches versus does not match, and check both results.
{% endstep %}

{% step %}
### Check what happens with nothing selected

A customer arriving at the page has made no selections. Check that the form is usable in that state.
{% endstep %}

{% step %}
### Check the required options in every branch

A required option is not enforced while it is hidden. Make sure each branch of your rules still collects all the information you need.
{% endstep %}

{% step %}
### Check the price in every branch

Hidden options are not charged. Confirm the total is right in each branch.
{% endstep %}

{% step %}
### Test on a real product page

Use **View in Store**. This is required for variant conditions, and recommended for all other rules, because customers see your theme rather than the preview.
{% endstep %}

{% step %}
### Test on a phone

Conditional logic changes the height of the page as options are displayed. Check that the result is clear on a small screen.
{% endstep %}
{% endstepper %}

## Still stuck?

When [contacting support](../help/contact-support.md), include the option set name, the option the rule is applied to, the exact rule as it appears in the app, and what you expected to happen versus what actually happened. If the rule uses a variant condition, also include the product and variant names.
