---
description: >-
  Min and max characters, values, selections, and files — plus the character
  counter that shows shoppers where they stand.
icon: ruler-horizontal
---

# Limits

Four pairs of min and max settings, each on a different family of option types, plus a counter. They all work the same way: leave one empty and that end is unlimited; fill it in and the app validates against it before **Add to cart**.

<table><thead><tr><th width="290">Setting pair</th><th>Measures</th><th>On</th></tr></thead><tbody><tr><td><a href="#min-and-max-character">Min character</a> / <a href="#min-and-max-character">Max character</a></td><td>How much text was typed</td><td>Text, Textarea</td></tr><tr><td><a href="#min-and-max-value">Min value</a> / <a href="#min-and-max-value">Max value</a></td><td>The number entered or chosen</td><td>Number, Range slider</td></tr><tr><td><a href="#min-and-max-selections">Min selections</a> / <a href="#min-and-max-selections">Max selections</a></td><td>How many choices were made</td><td>Checkbox, and any multi-select selection type</td></tr><tr><td><a href="#min-and-max-number-of-files">Min number of files</a> / <a href="#min-and-max-number-of-files">Max number of files</a></td><td>How many files were attached</td><td>File upload</td></tr></tbody></table>

{% hint style="info" %}
All limits are plan-gated in some form. If a limit field is greyed out, see [Compare plans](../../plans/compare-plans.md).
{% endhint %}

## Min and max character

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Both empty — no limit at either end</td></tr><tr><th>Available on</th><td>Text, Textarea</td></tr></thead></table>

**How it behaves**

* Counts characters, including spaces and punctuation.
* Leaving **Min character** empty means any length is acceptable, including one character.
* Leaving **Max character** empty means no upper limit.
* Validation runs on **Add to cart**, not while typing. Add a [Character counter](#character-counter) if you want live feedback.
* Setting max below min is rejected while you edit, with "The value must be greater than min."

**Typical uses**

<table><thead><tr><th width="270">Situation</th><th>Min</th><th>Max</th></tr></thead><tbody><tr><td>Engraving on a ring band</td><td>—</td><td><code>15</code></td></tr><tr><td>Two initials for a monogram</td><td><code>2</code></td><td><code>3</code></td></tr><tr><td>Gift message on a card</td><td>—</td><td><code>200</code></td></tr><tr><td>Special instructions, guarding against nonsense</td><td><code>10</code></td><td><code>500</code></td></tr></tbody></table>

{% hint style="warning" %}
Set the max to what physically fits, not to a round number. A 20-character limit on a pendant that fits 12 characters just moves the problem to your workshop. Repeat the limit in [Help text](placeholder-and-help-text.md#help-text) so shoppers know before they type.
{% endhint %}

Related: **Per character** add-on pricing charges by how much the customer types, which pairs naturally with a max. See [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md).

## Character counter

Shows a live count as the shopper types.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td><strong>Hide</strong></td></tr><tr><th>Available on</th><td>Text, Textarea</td></tr></thead></table>

Set it to **Show** and the field displays a running count. The wording is store-wide and editable: `{{character_count}}/{{character_limit}} characters` in **Settings > Translations**. See [Translate widget text](../../translations/translate-widget-text.md).

Turn it on whenever you have set a **Max character**. It converts a rejection at add-to-cart into feedback while typing, which is the difference between a shopper adjusting their text and a shopper giving up.

## Min and max value

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Both empty on <strong>Number</strong>. On <strong>Range slider</strong>, <code>0</code> and <code>100</code></td></tr><tr><th>Available on</th><td>Number, Range slider</td></tr></thead></table>

**How it behaves**

* On **Number**, they bound what the shopper may enter. Empty means unbounded at that end.
* On **Range slider**, they are the two ends of the track, so the shopper can never leave the range. The slider also has a **Step**, which sets the increment — see [Range slider](../input-types/range-slider.md).
* A **Default value** outside the range is rejected while you edit: "The value must be between min and max."

**Typical uses**

<table><thead><tr><th width="290">Situation</th><th>Min</th><th>Max</th></tr></thead><tbody><tr><td>Number of embroidered names</td><td><code>1</code></td><td><code>6</code></td></tr><tr><td>Width in centimetres you can cut</td><td><code>10</code></td><td><code>240</code></td></tr><tr><td>Guest count for a catering order</td><td><code>4</code></td><td><code>100</code></td></tr><tr><td>Discount-free donation amount</td><td><code>1</code></td><td>—</td></tr></tbody></table>

Where the number drives a price, this is also your protection against a zero or a negative. See [Dimension add-on formula](../../add-on-pricing/dimension-formula.md) for size-driven pricing.

## Min and max selections

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Both empty</td></tr><tr><th>Available on</th><td><strong>Checkbox</strong> always; and on <strong>Dropdown</strong>, <strong>Color dropdown</strong>, <strong>Image dropdown</strong>, <strong>Button</strong>, <strong>Color swatch</strong>, and <strong>Image swatch</strong> once <a href="selection-behaviour.md#allow-multiple">Allow multiple</a> is turned on</td></tr></thead></table>

**How it behaves**

* Counts how many values the shopper selected.
* On the multi-select types the fields only appear after **Allow multiple** is on — a single-select option can only ever have one selection.
* Setting min and max to the same number means "exactly this many", and the app uses a distinct message for it: `Please select exactly {{exactly_selection}} options`.
* **Required field** and **Min selections** overlap: required means at least one, `Min selections = 1` means the same thing. Use required for the simple case and min for anything above one.

**Typical uses**

<table><thead><tr><th width="290">Situation</th><th>Min</th><th>Max</th></tr></thead><tbody><tr><td>Pick any three toppings</td><td><code>3</code></td><td><code>3</code></td></tr><tr><td>Up to two free extras</td><td>—</td><td><code>2</code></td></tr><tr><td>At least one flavour in a box of six</td><td><code>1</code></td><td><code>6</code></td></tr><tr><td>Choose two to four colours</td><td><code>2</code></td><td><code>4</code></td></tr></tbody></table>

{% hint style="info" %}
When the option has add-on prices and the mode is **Default** or **One time charge**, the app also checks your min and max against the number of values the option actually has, and warns if the limit is impossible — "The value must be between 1 and the number of option values."
{% endhint %}

## Min and max number of files

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Both empty</td></tr><tr><th>Available on</th><td>File upload, once <strong>Allow multiple</strong> is on</td></tr></thead></table>

**How it behaves**

* Both accept a value between 1 and 20. The app rejects anything outside that: "The value must be between 1 and 20 (or max)."
* The fields only appear after **Allow multiple** is turned on for the option.
* How many files a customer may upload at once, and the size limit per file, are also capped by your plan — the option's own limit cannot exceed the plan's.
* Setting both to the same number means exactly that many files.

**Typical uses**

<table><thead><tr><th width="290">Situation</th><th>Min</th><th>Max</th></tr></thead><tbody><tr><td>One photo to print</td><td colspan="2">Leave <strong>Allow multiple</strong> off</td></tr><tr><td>A photo collage of exactly four images</td><td><code>4</code></td><td><code>4</code></td></tr><tr><td>Up to ten reference images</td><td>—</td><td><code>10</code></td></tr><tr><td>At least two angles of a garment for repair</td><td><code>2</code></td><td><code>6</code></td></tr></tbody></table>

See [File upload](../input-types/file-upload.md) for the allowed file extensions and the rest of the settings.

## Limits and validation together

<table><thead><tr><th width="270">Limit</th><th>Default message</th></tr></thead><tbody><tr><td>Min character</td><td>Please enter more than or equal to {{min_character}} characters</td></tr><tr><td>Max character</td><td>Please enter less than or equal to {{character_limit}} characters</td></tr><tr><td>Exact character count</td><td>Please enter exactly {{exactly_character}} characters</td></tr><tr><td>Min value</td><td>Please enter a value greater than or equal to {{min_value}}</td></tr><tr><td>Max value</td><td>Please enter a value less than or equal to {{max_value}}</td></tr><tr><td>Exact value</td><td>Please enter a value equal to {{exactly_value}}</td></tr><tr><td>Min selections</td><td>Please select at least {{min_selection}} options</td></tr><tr><td>Max selections</td><td>Please select at maximum {{max_selection}} options</td></tr><tr><td>Exact selections</td><td>Please select exactly {{exactly_selection}} options</td></tr><tr><td>Min files</td><td>Please add more than or equal to {{min_files}} files</td></tr><tr><td>Max files</td><td>Please add less than or equal to {{max_files}} files</td></tr><tr><td>Exact files</td><td>Please add exactly {{exactly_files}} files</td></tr></tbody></table>

Every message is editable per storefront language, and the `{{ }}` placeholders fill themselves in from your settings. See [Translate widget text](../../translations/translate-widget-text.md) and [Validation messages](../../reference/validation-messages.md).

<!-- SCREENSHOT: type-shared-limits | App admin → builder → option Text | Basic Settings với Min character, Max character, Character counter = Show | Khoanh nhóm min/max và character counter -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Min character, Max character, and the character counter on a Text option"><figcaption><p>Limits sit next to each other on Basic Settings, with the counter beside them.</p></figcaption></figure>

## Troubleshooting

<details>
<summary>"The value must be greater than min" / "less than max"</summary>

Min and max are the wrong way round. Fix whichever is wrong.
</details>

<details>
<summary>"The value must be between 1 and 20 (or max)"</summary>

A file count outside the permitted 1 to 20 range. Choose a number inside it.
</details>

<details>
<summary>"The value must be between 1 and the number of option values"</summary>

Your min or max selections is higher than the number of values the option has. Add more values, or lower the limit.
</details>

<details>
<summary>I cannot see Min selections or Min number of files</summary>

Turn on **Allow multiple** first. Those limits are meaningless on a single-select option or a single-file upload.
</details>

<details>
<summary>The limit is not being enforced on the storefront</summary>

Three things to check: the option set is saved; the option is not hidden by a conditional rule, since hidden options are not validated; and the limit is not greyed out on your plan.
</details>

<details>
<summary>My character counter is not showing</summary>

Set **Character counter** to **Show**. If it shows but the wording looks wrong, check the `char_counter` message in **Settings > Translations**.
</details>
