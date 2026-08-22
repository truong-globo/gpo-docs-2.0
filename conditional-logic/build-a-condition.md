---
description: >-
  Choosing a source, an operator, and a value — plus which option types can be a
  trigger and which cannot.
icon: diagram-project
---

# Build a condition

A condition is three dropdowns, filled left to right. Each one changes what the next one offers, so the order matters.

## The three parts

<table><thead><tr><th width="180">Part</th><th>What you choose</th></tr></thead><tbody><tr><td>Source</td><td>What the condition looks at: <strong>Shopify variant</strong>, or one of the options above this one.</td></tr><tr><td>Operator</td><td>How to compare. The choices depend entirely on the source's type.</td></tr><tr><td>Value</td><td>What to compare against. The field changes shape depending on the operator — and sometimes disappears.</td></tr></tbody></table>

{% hint style="info" %}
Always work left to right. Changing the source resets the operator and clears the value, because a new source offers a different set of operators.
{% endhint %}

<!-- SCREENSHOT: clo-three-dropdowns | App admin → builder → rule builder | 1 dòng điều kiện với 3 ô: source, operator, value | Khoanh 3 ô, đánh số 1-2-3 -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="One condition row showing the source, operator, and value fields"><figcaption><p>Fill the three fields left to right — each one changes what the next offers.</p></figcaption></figure>

## Choosing the source

The source dropdown lists:

1. **Shopify variant** — the variant the customer selected on the product page. See [Conditions based on Shopify variants](conditions-on-shopify-variants.md).
2. **Every eligible option above this one** in the same option set.

### Only options above

This is the constraint that surprises people. A condition can only read an option that appears **earlier** in the form than the option carrying the rule.

That is deliberate: the customer fills a form top to bottom, so an option can only sensibly react to something they have already reached.

If the option you want is missing from the dropdown, drag it above this one in the builder and it appears. See [Build your options](../option-sets/build-options.md).

### What can be a trigger

Twelve types cannot be used as a source, because they collect nothing usable:

<table><thead><tr><th width="290">Cannot be a trigger</th><th>Why</th></tr></thead><tbody><tr><td>Hidden field</td><td>Its value never changes, so a condition on it is always the same</td></tr><tr><td>Heading, Divider, Spacing, Paragraph, HTML, Pop-up modal, Tabs, Size chart, Section</td><td>They collect nothing</td></tr><tr><td>Product links</td><td>It navigates away rather than recording a choice</td></tr><tr><td>Dimension</td><td>It holds several measurements rather than one value</td></tr></tbody></table>

Everything else can be a trigger: Text, Textarea, Number, Phone, Email, Date and time picker, File upload, Color picker, Switch, Range slider, and all nine selection types with values.

{% hint style="info" %}
**Section** cannot be a *source*, but it can carry a *rule*. A section is a container — nothing to read, plenty to hide.
{% endhint %}

## Choosing the operator

The operator list is decided by the source's type. There are seven distinct sets — the full tables are in [Operators reference](operators-reference.md).

<table><thead><tr><th width="330">Source type</th><th>Operator set</th></tr></thead><tbody><tr><td>Text, Textarea, Email, Phone, Color picker, Shopify variant</td><td>Text: 10 operators, including character counts</td></tr><tr><td>Number, Range slider</td><td>Numeric: 4 operators</td></tr><tr><td>Date and time picker</td><td>2 operators</td></tr><tr><td>File upload</td><td>6 operators, including file counts</td></tr><tr><td>Radio button, Font picker</td><td>2 operators</td></tr><tr><td>Select, Dropdown, Color dropdown, Image dropdown, Checkbox, Button, Color swatch, Image swatch</td><td>8 operators, including selection counts</td></tr><tr><td>Switch</td><td>2 operators: <strong>is enabled</strong>, <strong>is disabled</strong></td></tr></tbody></table>

When you pick a source, the app sets a sensible starting operator: **has file** for a File upload, **is enabled** for a Switch, and **is equal to** for everything else.

## Filling in the value

The value field changes shape depending on what you chose. This is worth knowing, because a missing value field is usually the app telling you the condition is already complete.

<table><thead><tr><th width="290">Source and operator</th><th>Value field</th></tr></thead><tbody><tr><td>A selection type, with a normal operator</td><td>A <strong>dropdown of that option's own values</strong>. You pick, you do not type — so there is no risk of a typo.</td></tr><tr><td>A selection type, with a count operator</td><td>A number field — how many selections.</td></tr><tr><td>Text-like, with a normal operator</td><td>A text field. What you type must match what the customer types.</td></tr><tr><td>Text-like, with a character-count operator</td><td>A number field.</td></tr><tr><td>Number or Range slider</td><td>A number field.</td></tr><tr><td>File upload, with <strong>has file</strong> or <strong>no file</strong></td><td><strong>None.</strong> The operator is the whole condition.</td></tr><tr><td>File upload, with a file-count operator</td><td>A number field.</td></tr><tr><td>Switch</td><td><strong>None.</strong> <strong>is enabled</strong> and <strong>is disabled</strong> need nothing else.</td></tr><tr><td>Shopify variant</td><td>A text field, showing the current storefront language as a suffix. See <a href="conditions-on-shopify-variants.md">Conditions based on Shopify variants</a>.</td></tr></tbody></table>

{% hint style="warning" %}
When the value is a **text field**, the comparison is exact on characters. `Yes, wrap it` and `Yes, wrap it.` are different values, and so are `Large` and `large ` with a trailing space.

Whenever the source is a selection type, use the value dropdown rather than a count operator with a typed number — picking from the list removes the whole class of typo problems.
{% endhint %}

## Adding more conditions

**Add another condition** appends a row. All rows share the rule's **All** or **Any** mode.

Some practical advice:

* Two conditions is usually plenty. Three or more is a sign that the option set wants restructuring — often into a [Section](../option-types/static-types/section.md) with a rule of its own.
* With **All**, check your conditions can be true at the same time. `Size is equal to S` and `Size is equal to L` can never both be true.
* With **Any**, check they are not so broad that the rule always fires.

## What happens if the source option changes later

<table><thead><tr><th width="290">You do this</th><th>What happens to the rule</th></tr></thead><tbody><tr><td>Rename an option value</td><td>Conditions pointing at the old value stop matching. Reopen the rule and reselect the value.</td></tr><tr><td>Delete the source option</td><td>The condition is no longer valid and resets to an empty row. Rebuild it.</td></tr><tr><td>Change the source option's type</td><td>The operator set changes, so the existing operator may no longer be valid. Reopen the rule and reselect.</td></tr><tr><td>Move the source option below this one</td><td>It is no longer eligible as a source. Move it back, or rebuild the rule.</td></tr><tr><td>Duplicate or import options</td><td>Names are renumbered to stay unique, and rules pointing at them are repointed automatically.</td></tr></tbody></table>

Get into the habit of testing your rules in the preview after editing option values.

## Limits and notes

* Conditions can only read options in the **same option set**. A rule cannot look at an option in a different set that happens to apply to the same product.
* A hidden option is not validated and not charged.
* All conditions in one rule share the same matching mode — no mixed `and`/`or` in a single rule.
* Variant conditions require the Advanced level of conditional logic.

## Troubleshooting

<details>
<summary>The option I want is not in the source dropdown</summary>

Either it sits below this option — move it up — or its type cannot be a trigger. See the list above.
</details>

<details>
<summary>The value field disappeared</summary>

Expected for **has file**, **no file**, **is enabled**, and **is disabled**. Those operators need no value.
</details>

<details>
<summary>My typed value never matches</summary>

The comparison is exact. Copy the value from the source option's values table rather than retyping it, or use the value dropdown, which is available whenever the source is a selection type.
</details>

<details>
<summary>My condition reset itself to empty</summary>

The source option was deleted, so the condition became invalid. Rebuild it against an option that still exists.
</details>

<details>
<summary>The operator list changed after I edited the source option</summary>

You changed its type, which changes the operator set. Reselect the operator.
</details>
