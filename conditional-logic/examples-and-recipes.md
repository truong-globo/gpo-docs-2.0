---
description: >-
  Eight complete conditional logic setups you can copy, from a simple reveal to a
  branching form.
icon: book-open
---

# Examples and recipes

Each example lists the options involved, where to apply the rule, and the exact condition. Replace the labels and values with your own.

Two rules apply to every example: the trigger option must appear **above** the option the rule is applied to, and a hidden option is **not validated**.

## 1. Reveal a gift message when gift wrap is chosen

This is the most common use of conditional logic.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Gift wrap</code></td><td>Checkbox</td><td>One value: <code>Yes, wrap it as a gift</code>, priced</td></tr><tr><td><code>Gift message</code></td><td>Textarea</td><td>Max character 200. <strong>The rule goes here</strong></td></tr></tbody></table>

**Rule on `Gift message`:** Show · All · `Gift wrap` — **contains** — `Yes, wrap it as a gift`

{% hint style="info" %}
Use **contains** rather than **is equal to**, because Checkbox allows multiple selections. If you later add a second value such as `Gift bag`, an **is equal to** rule stops matching.
{% endhint %}

## 2. Reveal font and position once they have typed an engraving

This detects that the customer wants engraving, without checking what they entered.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Engraving text</code></td><td>Text</td><td>Max character 15, priced</td></tr><tr><td><code>Engraving details</code></td><td>Section</td><td><strong>The rule goes here</strong>, containing the two options below</td></tr><tr><td><code>Engraving font</code></td><td>Font picker</td><td>Five fonts</td></tr><tr><td><code>Engraving position</code></td><td>Radio button</td><td><code>Front</code>, <code>Back</code></td></tr></tbody></table>

**Rule on the `Engraving details` section:** Show · All · `Engraving text` — **number of characters is greater than** — `0`

One rule on the section controls both options inside it. If you add a third engraving option later, no extra rule is needed.

## 3. Warn when the engraving is too long to look good

This displays a warning without blocking the purchase.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Engraving text</code></td><td>Text</td><td>Max character 20</td></tr><tr><td>Warning</td><td>Paragraph</td><td><strong>The rule goes here.</strong> "Messages over 12 characters are engraved smaller."</td></tr></tbody></table>

**Rule on the paragraph:** Show · All · `Engraving text` — **number of characters is greater than** — `12`

Static types support conditional logic, so you can display a warning based on the customer's input.

## 4. Offer a design service to customers who have no artwork

This offers a service when the customer has no file to upload.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Your artwork</code></td><td>File upload</td><td>Not required</td></tr><tr><td><code>Design service</code></td><td>Switch</td><td><strong>The rule goes here.</strong> Priced, One time charge</td></tr></tbody></table>

**Rule on `Design service`:** Show · All · `Your artwork` — **no file**

The option is displayed only while no file has been uploaded, and is hidden as soon as the customer attaches one.

## 5. Ask for placement once they have uploaded a photo

This is the reverse of the previous example.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Your photo</code></td><td>File upload</td><td>Required, image editor on</td></tr><tr><td><code>Photo placement</code></td><td>Image swatch</td><td><strong>The rule goes here.</strong> Three layout options</td></tr></tbody></table>

**Rule on `Photo placement`:** Show · All · `Your photo` — **has file**

## 6. Engraving only on the metal version

This uses a variant condition, which requires the advanced level of conditional logic. See [Conditions based on Shopify variants](conditions-on-shopify-variants.md).

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Engraving</code></td><td>Section</td><td><strong>The rule goes here</strong></td></tr></tbody></table>

**Rule on the section:** Show · All · **Shopify variant** — **contains** — `Silver`

Use **contains** rather than **is equal to**, so the rule matches both `Small / Silver` and `Large / Silver`.

Test this on a real product page. The builder preview cannot evaluate variant conditions.

## 7. A tiered upsell that reveals its own extras

Each service level displays only the options that belong to it.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Service level</code></td><td>Radio button</td><td><code>Standard</code>, <code>Plus</code>, <code>Premium</code>, each priced and with its own help text</td></tr><tr><td><code>Premium extras</code></td><td>Section</td><td><strong>Rule A</strong>, containing the premium-only options</td></tr><tr><td><code>Standard notice</code></td><td>Paragraph</td><td><strong>Rule B.</strong> "Standard does not include insurance."</td></tr></tbody></table>

**Rule A on `Premium extras`:** Show · All · `Service level` — **is equal to** — `Premium`

**Rule B on `Standard notice`:** Show · All · `Service level` — **is equal to** — `Standard`

Use **is equal to** here, because Radio button allows only one selection.

## 8. Reveal a bulk-order note when they order a lot of extras

This reacts to the number of selections rather than to a specific value.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Add-ons</code></td><td>Checkbox</td><td>Eight values, each priced, Max selections 8</td></tr><tr><td><code>Bulk note</code></td><td>Paragraph</td><td><strong>The rule goes here.</strong> "Orders with more than three extras take an extra 2 days."</td></tr></tbody></table>

**Rule on `Bulk note`:** Show · All · `Add-ons` — **number of selections is greater than** — `3`

## Two conditions at once

The examples above use one condition each. The following examples combine two or more.

**A gift message only for gift-wrapped express orders**

Rule on `Gift message`: Show · **All** ·

* `Gift wrap` — **contains** — `Yes, wrap it as a gift`
* `Delivery` — **is equal to** — `Express`

**A lead-time warning for anything personalized**

Rule on the warning paragraph: Show · **Any** ·

* `Engraving text` — **number of characters is greater than** — `0`
* `Your photo` — **has file**
* `Custom color` — **is enabled**

Use **Any** here, because one personalized element is enough to display the warning.

## Patterns to reuse

<table><thead><tr><th width="290">Pattern</th><th>Why it works</th></tr></thead><tbody><tr><td>A <strong>Switch</strong> at the top of a form, with a <strong>Section</strong> below it carrying one rule</td><td>The cleanest possible "do you want to personalise this?" flow. Two objects, one rule.</td></tr><tr><td><strong>number of characters is greater than 0</strong> as a "did they fill this in" test</td><td>Works whatever they typed, and needs no maintenance when your wording changes.</td></tr><tr><td>Rules on <strong>Paragraph</strong> options for contextual warnings</td><td>Says the right thing at the right moment, instead of a wall of caveats nobody reads.</td></tr><tr><td>One rule on a <strong>Section</strong> instead of the same rule on six options</td><td>Faster to build, and impossible to get half-right.</td></tr><tr><td>Two option sets rather than one heavily branched set</td><td>When almost everything differs, targeting by product tag is clearer than logic.</td></tr></tbody></table>
