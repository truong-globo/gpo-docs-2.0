---
description: >-
  Eight complete conditional logic setups you can copy, from a simple reveal to a
  branching form.
icon: book-open
---

# Examples and recipes

Each recipe lists the options involved, where the rule goes, and the exact condition. Substitute your own labels and values.

Throughout, remember the two rules that decide whether any of this works: the trigger option must sit **above** the option carrying the rule, and a hidden option is **not validated**.

## 1. Reveal a gift message when gift wrap is chosen

The most common setup in the app.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Gift wrap</code></td><td>Checkbox</td><td>One value: <code>Yes, wrap it as a gift</code>, priced</td></tr><tr><td><code>Gift message</code></td><td>Textarea</td><td>Max character 200. <strong>The rule goes here</strong></td></tr></tbody></table>

**Rule on `Gift message`:** Show · All · `Gift wrap` — **contains** — `Yes, wrap it as a gift`

{% hint style="info" %}
**contains**, not **is equal to** — because Checkbox is multi-select. If you later add a second value like `Gift bag`, an **is equal to** rule would silently stop working.
{% endhint %}

## 2. Reveal font and position once they have typed an engraving

Detects "they want engraving" without caring what they typed.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Engraving text</code></td><td>Text</td><td>Max character 15, priced</td></tr><tr><td><code>Engraving details</code></td><td>Section</td><td><strong>The rule goes here</strong>, containing the two options below</td></tr><tr><td><code>Engraving font</code></td><td>Font picker</td><td>Five fonts</td></tr><tr><td><code>Engraving position</code></td><td>Radio button</td><td><code>Front</code>, <code>Back</code></td></tr></tbody></table>

**Rule on the `Engraving details` section:** Show · All · `Engraving text` — **number of characters is greater than** — `0`

One rule on the section handles both options inside it. Adding a third engraving option later needs no extra rule.

## 3. Warn when the engraving is too long to look good

A soft warning, without blocking the sale.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Engraving text</code></td><td>Text</td><td>Max character 20</td></tr><tr><td>Warning</td><td>Paragraph</td><td><strong>The rule goes here.</strong> "Messages over 12 characters are engraved smaller."</td></tr></tbody></table>

**Rule on the paragraph:** Show · All · `Engraving text` — **number of characters is greater than** — `12`

Static types support conditional logic, which is what makes contextual warnings possible.

## 4. Offer a design service to shoppers who have no artwork

Turns a missing upload into a sale.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Your artwork</code></td><td>File upload</td><td>Not required</td></tr><tr><td><code>Design service</code></td><td>Switch</td><td><strong>The rule goes here.</strong> Priced, One time charge</td></tr></tbody></table>

**Rule on `Design service`:** Show · All · `Your artwork` — **no file**

The option appears only while nothing has been uploaded, and disappears the moment they attach a file.

## 5. Ask for placement once they have uploaded a photo

The mirror image of the previous recipe.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Your photo</code></td><td>File upload</td><td>Required, image editor on</td></tr><tr><td><code>Photo placement</code></td><td>Image swatch</td><td><strong>The rule goes here.</strong> Three layout options</td></tr></tbody></table>

**Rule on `Photo placement`:** Show · All · `Your photo` — **has file**

## 6. Engraving only on the metal version

A variant-based rule. Requires advanced conditional logic — see [Conditions based on Shopify variants](conditions-on-shopify-variants.md).

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Engraving</code></td><td>Section</td><td><strong>The rule goes here</strong></td></tr></tbody></table>

**Rule on the section:** Show · All · **Shopify variant** — **contains** — `Silver`

**contains** rather than **is equal to**, so it matches `Small / Silver` and `Large / Silver` alike.

Test on a real product page — the builder preview cannot evaluate variant conditions.

## 7. A tiered upsell that reveals its own extras

Each tier shows only what belongs to it.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Service level</code></td><td>Radio button</td><td><code>Standard</code>, <code>Plus</code>, <code>Premium</code>, each priced and with its own help text</td></tr><tr><td><code>Premium extras</code></td><td>Section</td><td><strong>Rule A</strong>, containing the premium-only options</td></tr><tr><td><code>Standard notice</code></td><td>Paragraph</td><td><strong>Rule B.</strong> "Standard does not include insurance."</td></tr></tbody></table>

**Rule A on `Premium extras`:** Show · All · `Service level` — **is equal to** — `Premium`

**Rule B on `Standard notice`:** Show · All · `Service level` — **is equal to** — `Standard`

**is equal to** is correct here because Radio button is single-select.

## 8. Reveal a bulk-order note when they order a lot of extras

Reacting to a count rather than a value.

<table><thead><tr><th width="230">Option</th><th width="150">Type</th><th>Notes</th></tr></thead><tbody><tr><td><code>Add-ons</code></td><td>Checkbox</td><td>Eight values, each priced, Max selections 8</td></tr><tr><td><code>Bulk note</code></td><td>Paragraph</td><td><strong>The rule goes here.</strong> "Orders with more than three extras take an extra 2 days."</td></tr></tbody></table>

**Rule on `Bulk note`:** Show · All · `Add-ons` — **number of selections is greater than** — `3`

## Two conditions at once

The recipes above use one condition each. Two examples of combining them:

**A gift message only for gift-wrapped express orders**

Rule on `Gift message`: Show · **All** ·

* `Gift wrap` — **contains** — `Yes, wrap it as a gift`
* `Delivery` — **is equal to** — `Express`

**A lead-time warning for anything personalised**

Rule on the warning paragraph: Show · **Any** ·

* `Engraving text` — **number of characters is greater than** — `0`
* `Your photo` — **has file**
* `Custom colour` — **is enabled**

**Any** is right here: one personalised element is enough to justify the warning.

## Patterns worth stealing

<table><thead><tr><th width="290">Pattern</th><th>Why it works</th></tr></thead><tbody><tr><td>A <strong>Switch</strong> at the top of a form, with a <strong>Section</strong> below it carrying one rule</td><td>The cleanest possible "do you want to personalise this?" flow. Two objects, one rule.</td></tr><tr><td><strong>number of characters is greater than 0</strong> as a "did they fill this in" test</td><td>Works whatever they typed, and needs no maintenance when your wording changes.</td></tr><tr><td>Rules on <strong>Paragraph</strong> options for contextual warnings</td><td>Says the right thing at the right moment, instead of a wall of caveats nobody reads.</td></tr><tr><td>One rule on a <strong>Section</strong> instead of the same rule on six options</td><td>Faster to build, and impossible to get half-right.</td></tr><tr><td>Two option sets rather than one heavily branched set</td><td>When almost everything differs, targeting by product tag is clearer than logic.</td></tr></tbody></table>
