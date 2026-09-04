---
description: >-
  Every conditional logic operator, grouped by the type of the source option, with
  what each one matches.
icon: code-compare
---

# Operators reference

The operators available depend on the type of the **source** option. There are seven sets of operators, listed on this page.

## Quick index

<table><thead><tr><th width="330">If your source is…</th><th>Jump to</th></tr></thead><tbody><tr><td>Text, Textarea, Email, Phone, Color picker, or <strong>Shopify variant</strong></td><td><a href="#text-sources">Text sources</a> — 10 operators</td></tr><tr><td>Number or Range slider</td><td><a href="#numeric-sources">Numeric sources</a> — 4 operators</td></tr><tr><td>Date and time picker</td><td><a href="#date-sources">Date sources</a> — 2 operators</td></tr><tr><td>File upload</td><td><a href="#file-upload-sources">File upload sources</a> — 6 operators</td></tr><tr><td>Radio button or Font picker</td><td><a href="#single-choice-sources">Single-choice sources</a> — 2 operators</td></tr><tr><td>Select, Dropdown, Color dropdown, Image dropdown, Checkbox, Button, Color swatch, Image swatch</td><td><a href="#multi-choice-sources">Multi-choice sources</a> — 8 operators</td></tr><tr><td>Switch</td><td><a href="#switch-sources">Switch sources</a> — 2 operators</td></tr></tbody></table>

## Text sources

**Applies to:** Text, Textarea, Email, Phone, Color picker, and **Shopify variant**.

<table><thead><tr><th width="330">Operator</th><th width="120">Value field</th><th>Matches when the entry…</th></tr></thead><tbody><tr><td><strong>is equal to</strong></td><td>Text</td><td>is exactly your value, character for character</td></tr><tr><td><strong>is not equal to</strong></td><td>Text</td><td>is anything other than your value</td></tr><tr><td><strong>starts with</strong></td><td>Text</td><td>begins with your value</td></tr><tr><td><strong>ends with</strong></td><td>Text</td><td>finishes with your value</td></tr><tr><td><strong>contains</strong></td><td>Text</td><td>has your value somewhere inside it</td></tr><tr><td><strong>does not contain</strong></td><td>Text</td><td>does not have your value anywhere inside it</td></tr><tr><td><strong>number of characters is equal to</strong></td><td>Number</td><td>is exactly that many characters long</td></tr><tr><td><strong>number of characters is not equal to</strong></td><td>Number</td><td>is any other length</td></tr><tr><td><strong>number of characters is greater than</strong></td><td>Number</td><td>is longer than that</td></tr><tr><td><strong>number of characters is less than</strong></td><td>Number</td><td>is shorter than that</td></tr></tbody></table>

**Worked examples**

<table><thead><tr><th width="330">Condition</th><th>Fires when the customer</th></tr></thead><tbody><tr><td>Engraving text — <strong>number of characters is greater than</strong> — <code>0</code></td><td>has typed anything at all. The standard way to say "they want engraving"</td></tr><tr><td>Engraving text — <strong>number of characters is greater than</strong> — <code>12</code></td><td>has typed a long message — use it to reveal a "this may not fit" warning</td></tr><tr><td>Email — <strong>contains</strong> — <code>@ourcompany.com</code></td><td>is a colleague, for internal-only options</td></tr></tbody></table>

{% hint style="info" %}
Use **number of characters is greater than 0** to detect that the customer has entered something, without checking the value itself.
{% endhint %}

## Numeric sources

**Applies to:** Number, Range slider.

<table><thead><tr><th width="330">Operator</th><th width="120">Value field</th><th>Matches when the number…</th></tr></thead><tbody><tr><td><strong>is equal to</strong></td><td>Number</td><td>is exactly that</td></tr><tr><td><strong>is not equal to</strong></td><td>Number</td><td>is anything else</td></tr><tr><td><strong>is greater than</strong></td><td>Number</td><td>is above that</td></tr><tr><td><strong>is less than</strong></td><td>Number</td><td>is below that</td></tr></tbody></table>

**Worked examples**

<table><thead><tr><th width="330">Condition</th><th>Use for</th></tr></thead><tbody><tr><td>Quantity of names — <strong>is greater than</strong> — <code>4</code></td><td>Revealing a bulk-order note or a longer lead time</td></tr><tr><td>Width — <strong>is greater than</strong> — <code>180</code></td><td>Revealing an oversized-delivery surcharge option</td></tr><tr><td>Number of guests — <strong>is less than</strong> — <code>4</code></td><td>Hiding a group discount option</td></tr></tbody></table>

There is no "greater than or equal to" operator. To match 4 or more, use **is greater than** `3`.

## Date sources

**Applies to:** Date and time picker.

<table><thead><tr><th width="330">Operator</th><th width="120">Value field</th><th>Matches when the date…</th></tr></thead><tbody><tr><td><strong>is equal to</strong></td><td>Text</td><td>is exactly that date</td></tr><tr><td><strong>is not equal to</strong></td><td>Text</td><td>is any other date</td></tr></tbody></table>

Only two operators are available, so date conditions match specific dates rather than ranges. Enter the value in the same format the option is configured to use. See [Date and time picker](../option-types/input-types/date-and-time-picker.md).

To control which dates the customer can select, use the option's **Limit date picker** settings instead of conditional logic.

## File upload sources

**Applies to:** File upload.

<table><thead><tr><th width="330">Operator</th><th width="120">Value field</th><th>Matches when</th></tr></thead><tbody><tr><td><strong>has file</strong></td><td><em>None</em></td><td>at least one file is attached</td></tr><tr><td><strong>no file</strong></td><td><em>None</em></td><td>nothing is attached</td></tr><tr><td><strong>number of files is equal to</strong></td><td>Number</td><td>exactly that many are attached</td></tr><tr><td><strong>number of files is not equal to</strong></td><td>Number</td><td>any other number are attached</td></tr><tr><td><strong>number of files is greater than</strong></td><td>Number</td><td>more than that are attached</td></tr><tr><td><strong>number of files is less than</strong></td><td>Number</td><td>fewer than that are attached</td></tr></tbody></table>

**has file** and **no file** do not take a value. The operator is the complete condition.

**Worked examples**

<table><thead><tr><th width="330">Condition</th><th>Use for</th></tr></thead><tbody><tr><td>Your photo — <strong>has file</strong></td><td>Revealing cropping instructions or a placement choice once they have uploaded</td></tr><tr><td>Your photo — <strong>no file</strong></td><td>Showing a "we can design one for you" paid option</td></tr><tr><td>Photos — <strong>number of files is greater than</strong> — <code>4</code></td><td>Revealing a collage layout choice</td></tr></tbody></table>

## Single-choice sources

**Applies to:** Radio button, Font picker.

<table><thead><tr><th width="330">Operator</th><th width="180">Value field</th><th>Matches when</th></tr></thead><tbody><tr><td><strong>is equal to</strong></td><td>Dropdown of that option's values</td><td>that value is selected</td></tr><tr><td><strong>is not equal to</strong></td><td>Dropdown of that option's values</td><td>anything else is selected</td></tr></tbody></table>

Only one value can be selected on these types, so count and containment operators do not apply.

The value is selected from a dropdown listing the source option's own values, so there is no risk of a typing error.

## Multi-choice sources

**Applies to:** Select, Dropdown, Color dropdown, Image dropdown, Checkbox, Button, Color swatch, Image swatch.

<table><thead><tr><th width="330">Operator</th><th width="180">Value field</th><th>Matches when</th></tr></thead><tbody><tr><td><strong>is equal to</strong></td><td>Dropdown of values</td><td>that value is the selection</td></tr><tr><td><strong>is not equal to</strong></td><td>Dropdown of values</td><td>the selection is something else</td></tr><tr><td><strong>contains</strong></td><td>Dropdown of values</td><td>that value is among the selections</td></tr><tr><td><strong>does not contain</strong></td><td>Dropdown of values</td><td>that value is not among the selections</td></tr><tr><td><strong>number of selections is equal to</strong></td><td>Number</td><td>exactly that many are selected</td></tr><tr><td><strong>number of selections is not equal to</strong></td><td>Number</td><td>any other number are selected</td></tr><tr><td><strong>number of selections is greater than</strong></td><td>Number</td><td>more than that are selected</td></tr><tr><td><strong>number of selections is less than</strong></td><td>Number</td><td>fewer than that are selected</td></tr></tbody></table>

### is equal to versus contains

This is the most important distinction on this page.

<table><thead><tr><th width="230">Operator</th><th>Behavior</th><th>Use when</th></tr></thead><tbody><tr><td><strong>is equal to</strong></td><td>Matches only when that value is <em>the</em> selection</td><td>The option is single-select, or you specifically mean "only this one"</td></tr><tr><td><strong>contains</strong></td><td>Matches when that value is <em>among</em> the selections</td><td>The option allows multiple, and you mean "they picked this, possibly with others"</td></tr></tbody></table>

{% hint style="warning" %}
On a **Checkbox**, or any option with **Allow multiple** enabled, use **contains** instead of **is equal to**. If a customer selects `Gift wrap` and `Gift bag`, the selection is not equal to `Gift wrap`, so an **is equal to** rule does not match. This is the most common mistake when building conditions.
{% endhint %}

**Worked examples**

<table><thead><tr><th width="330">Condition</th><th>Use for</th></tr></thead><tbody><tr><td>Gift wrap — <strong>contains</strong> — <code>Yes, wrap it as a gift</code></td><td>Revealing a gift message box</td></tr><tr><td>Extras — <strong>number of selections is greater than</strong> — <code>2</code></td><td>Revealing a bulk note, or a longer lead time warning</td></tr><tr><td>Size — <strong>is equal to</strong> — <code>XL</code></td><td>Revealing an option only for one size</td></tr><tr><td>Finish — <strong>does not contain</strong> — <code>Standard</code></td><td>Revealing a premium-finish care note</td></tr></tbody></table>

## Switch sources

**Applies to:** Switch.

<table><thead><tr><th width="330">Operator</th><th width="120">Value field</th><th>Matches when</th></tr></thead><tbody><tr><td><strong>is enabled</strong></td><td><em>None</em></td><td>the switch is on</td></tr><tr><td><strong>is disabled</strong></td><td><em>None</em></td><td>the switch is off</td></tr></tbody></table>

Neither operator takes a value. A Switch has two states and no typed value, which makes it a reliable trigger.

If you need a complex rule on a text field to detect whether the customer wants an option, add a Switch above it and use that as the trigger instead.

## Choosing the right operator

<table><thead><tr><th width="330">You want to detect</th><th>Use</th></tr></thead><tbody><tr><td>They filled in a text field at all</td><td><strong>number of characters is greater than</strong> <code>0</code></td></tr><tr><td>They picked a specific value, single-select</td><td><strong>is equal to</strong></td></tr><tr><td>They picked a specific value, multi-select</td><td><strong>contains</strong></td></tr><tr><td>They picked several things</td><td><strong>number of selections is greater than</strong></td></tr><tr><td>They uploaded something</td><td><strong>has file</strong></td></tr><tr><td>They said yes to one thing</td><td>A Switch with <strong>is enabled</strong></td></tr><tr><td>Their number is above a threshold</td><td><strong>is greater than</strong></td></tr><tr><td>They chose a particular Shopify variant</td><td><strong>Shopify variant</strong> with <strong>is equal to</strong> — see <a href="conditions-on-shopify-variants.md">Conditions based on Shopify variants</a></td></tr></tbody></table>
