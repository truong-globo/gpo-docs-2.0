---
description: >-
  Min and max characters, values, selections, and files — plus the character
  counter that shows shoppers where they stand.
icon: ruler-horizontal
---

# Limits

There are four pairs of min/max settings, each used by a different group of option types, plus a character counter. The rules are the same for all of them: leave one limit empty to make that end unlimited; enter a limit to have the app validate it before **Add to cart**.

<table><thead><tr><th width="290">Setting pair</th><th>Measures</th><th>On</th></tr></thead><tbody><tr><td><a href="limits.md#min-and-max-character">Min character</a> / <a href="limits.md#min-and-max-character">Max character</a></td><td>How much text was typed</td><td>Text, Textarea</td></tr><tr><td><a href="limits.md#min-and-max-value">Min value</a> / <a href="limits.md#min-and-max-value">Max value</a></td><td>The number entered or chosen</td><td>Number, Range slider</td></tr><tr><td><a href="limits.md#min-and-max-selections">Min selections</a> / <a href="limits.md#min-and-max-selections">Max selections</a></td><td>How many choices were made</td><td>Checkbox, and any multi-select selection type</td></tr><tr><td><a href="limits.md#min-and-max-number-of-files">Min number of files</a> / <a href="limits.md#min-and-max-number-of-files">Max number of files</a></td><td>How many files were attached</td><td>File upload</td></tr></tbody></table>

{% hint style="info" %}
All limit settings are restricted by plan in some way. If a limit field is greyed out, see [Compare plans](../../plans/compare-plans.md).
{% endhint %}

## Min and max character

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Both empty — no limit at either end</td></tr><tr><td>Available on</td><td>Text, Textarea</td></tr></tbody></table>

**How it behaves**

* Counts all characters, including spaces and punctuation.
* Leaving **Min character** empty means any length is allowed, including a single character.
* Leaving **Max character** empty means there is no upper limit.
* Validation runs when the shopper selects **Add to cart**, not while they are typing. Add a [Character counter](limits.md#character-counter) if you want live feedback.
* Setting **Max character** below **Min character** is rejected while editing, with the message `The value must be greater than min.`

**Typical uses**

<table><thead><tr><th width="270">Situation</th><th>Min</th><th>Max</th></tr></thead><tbody><tr><td>Engraving on a ring band</td><td>—</td><td><code>15</code></td></tr><tr><td>Two initials for a monogram</td><td><code>2</code></td><td><code>3</code></td></tr><tr><td>Gift message on a card</td><td>—</td><td><code>200</code></td></tr><tr><td>Special instructions, guarding against nonsense</td><td><code>10</code></td><td><code>500</code></td></tr></tbody></table>

{% hint style="warning" %}
Set the maximum to what physically fits, rather than choosing a convenient round number. A 20-character limit on a pendant that only fits 12 characters simply moves the problem to your workshop. Repeat the limit in **Help text** so shoppers know it before they start typing.
{% endhint %}

Related: **Per character** add-on pricing charges based on how much the customer types, making it a natural fit for a maximum character limit. See [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md).

## Character counter

Shows a live count as the shopper types.

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>Hide</strong></td></tr><tr><td>Available on</td><td>Text, Textarea</td></tr></tbody></table>

Set it to **Show** to display a running character count. The wording is store-wide and editable in **Settings > Translations**: `{{character_count}}/{{character_limit}} characters`. See [Translate widget text](../../translations/translate-widget-text.md).

Turn it on whenever you set a **Max character**. It gives shoppers feedback while they type instead of waiting until **Add to cart** to discover that their input is too long. This lets them adjust their text before submitting the form.

## Min and max value

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Both empty on <strong>Number</strong>. On <strong>Range slider</strong>, <code>0</code> and <code>100</code></td></tr><tr><td>Available on</td><td>Number, Range slider</td></tr></tbody></table>

**How it behaves**

* On **Number**, the limits define what values the shopper can enter. Leave one limit empty to make that end unbounded.
* On **Range slider**, the limits define the two ends of the slider track, so shoppers cannot select a value outside the range. The slider also has a **Step** setting that controls the increment — see [Range slider](../input-types/range-slider.md).
* A **Default value** outside the range is rejected while editing, with the message `The value must be between min and max.`

**Typical uses**

<table><thead><tr><th width="290">Situation</th><th>Min</th><th>Max</th></tr></thead><tbody><tr><td>Number of embroidered names</td><td><code>1</code></td><td><code>6</code></td></tr><tr><td>Width in centimetres you can cut</td><td><code>10</code></td><td><code>240</code></td></tr><tr><td>Guest count for a catering order</td><td><code>4</code></td><td><code>100</code></td></tr><tr><td>Discount-free donation amount</td><td><code>1</code></td><td>—</td></tr></tbody></table>

When a number is used to calculate a price, these limits also protect against zero or negative values. See [Dimension add-on formula](../../add-on-pricing/dimension-formula.md) for size-based pricing.

## Min and max selections

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Both empty</td></tr><tr><td>Available on</td><td><strong>Checkbox</strong> always; and on <strong>Dropdown</strong>, <strong>Color dropdown</strong>, <strong>Image dropdown</strong>, <strong>Button</strong>, <strong>Color swatch</strong>, and <strong>Image swatch</strong> once <a href="selection-behaviour.md#allow-multiple">Allow multiple</a> is turned on</td></tr></tbody></table>

**How it behaves**

* Counts the number of values the shopper selects.
* On multi-select types, these settings appear only after **Allow multiple** is enabled. A single-select option can have only one selection.
* Setting **Min selections** and **Max selections** to the same number means “exactly this many.” The app uses a specific validation message: `Please select exactly {{exactly_selection}} options`.
* **Required field** and **Min selections** overlap: **Required field** means at least one selection, which is the same as **Min selections = 1**. Use **Required field** for the simple case and **Min selections** when you need to require more than one selection.

**Typical uses**

<table><thead><tr><th width="290">Situation</th><th>Min</th><th>Max</th></tr></thead><tbody><tr><td>Pick any three toppings</td><td><code>3</code></td><td><code>3</code></td></tr><tr><td>Up to two free extras</td><td>—</td><td><code>2</code></td></tr><tr><td>At least one flavour in a box of six</td><td><code>1</code></td><td><code>6</code></td></tr><tr><td>Choose two to four colours</td><td><code>2</code></td><td><code>4</code></td></tr></tbody></table>

{% hint style="info" %}
The app also checks your limits against the number of values available in the option. For example, you cannot require five selections when the option has only four values. The app rejects this with the message: `The value must be between 1 and the number of option values.`
{% endhint %}

## Min and max number of files

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Both empty</td></tr><tr><td>Available on</td><td>File upload, once <strong>Allow multiple</strong> is on</td></tr></tbody></table>

**How it behaves**

* Both settings accept a value between 1 and 20. The app rejects anything outside this range with the message: `The value must be between 1 and 20 (or max).`
* The fields appear only after **Allow multiple** is enabled for the option.
* The maximum number of files a customer can upload at once, as well as the maximum file size, is also limited by your plan. The option-level limit cannot exceed the plan limit.
* Setting **Min files** and **Max files** to the same number requires exactly that many files.

**Typical uses**

<table><thead><tr><th width="290">Situation</th><th>Min</th><th>Max</th></tr></thead><tbody><tr><td>One photo to print</td><td>Leave <strong>Allow multiple</strong> off</td><td></td></tr><tr><td>A photo collage of exactly four images</td><td><code>4</code></td><td><code>4</code></td></tr><tr><td>Up to ten reference images</td><td>—</td><td><code>10</code></td></tr><tr><td>At least two angles of a garment for repair</td><td><code>2</code></td><td><code>6</code></td></tr></tbody></table>

See [File upload](../input-types/file-upload.md) for the allowed file extensions and the rest of the settings.

## Limits and validation together

<table><thead><tr><th width="270">Limit</th><th>Default message</th></tr></thead><tbody><tr><td>Min character</td><td>Please enter more than or equal to {{min_character}} characters</td></tr><tr><td>Max character</td><td>Please enter less than or equal to {{character_limit}} characters</td></tr><tr><td>Exact character count</td><td>Please enter exactly {{exactly_character}} characters</td></tr><tr><td>Min value</td><td>Please enter a value greater than or equal to {{min_value}}</td></tr><tr><td>Max value</td><td>Please enter a value less than or equal to {{max_value}}</td></tr><tr><td>Exact value</td><td>Please enter a value equal to {{exactly_value}}</td></tr><tr><td>Min selections</td><td>Please select at least {{min_selection}} options</td></tr><tr><td>Max selections</td><td>Please select at maximum {{max_selection}} options</td></tr><tr><td>Exact selections</td><td>Please select exactly {{exactly_selection}} options</td></tr><tr><td>Min files</td><td>Please add more than or equal to {{min_files}} files</td></tr><tr><td>Max files</td><td>Please add less than or equal to {{max_files}} files</td></tr><tr><td>Exact files</td><td>Please add exactly {{exactly_files}} files</td></tr></tbody></table>

Every message is editable per storefront language, and the `{{ }}` placeholders fill themselves in from your settings. See [Translate widget text](../../translations/translate-widget-text.md) and [Validation messages](../../translations/translate-widget-text.md).

<figure><img src="../../.gitbook/assets/2026-08-31_10-21-10 (1).png" alt="Min character, Max character, and the character counter on a Text option"><figcaption><p>Limits sit next to each other on Basic Settings, with the counter beside them.</p></figcaption></figure>
