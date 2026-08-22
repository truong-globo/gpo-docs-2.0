---
description: >-
  Make an option compulsory, and pre-fill it — the two settings that decide what
  happens when a customer does nothing.
icon: asterisk
---

# Required field and default value

These two settings answer the same question from opposite directions: what happens if the shopper ignores this option? **Required field** stops them ignoring it. **Default value** decides it for them.

## Required field

Blocks **Add to cart** until the option is filled in.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Off</td></tr><tr><th>Available on</th><td>21 types — every input and selection type except <strong>Hidden field</strong> and <strong>Product links</strong>, which never collect an answer that could be missing</td></tr></thead></table>

**How it behaves**

* On the storefront the label is marked, using the required character colour set in **Settings > Design**.
* If the shopper tries to add to cart without filling it in, the add is blocked and your validation message appears — `This field is required` by default, editable in **Settings > Translations**.
* The page can scroll to the first problem automatically. That is **Auto-scroll to first error message** in **Settings > Settings > General**, and it is on by default. See [Widget behavior](../../storefront/widget-behavior.md).
* On a **Checkbox**, required means at least one box must be ticked. For "exactly two of these five", use [Min and max selections](limits.md#min-and-max-selections) instead.
* On a **File upload**, required means at least one file must be attached.

**What counts as filled in**

<table><thead><tr><th width="240">Type</th><th>Satisfied when</th></tr></thead><tbody><tr><td>Text, Textarea, Number, Phone, Email</td><td>Any character has been entered</td></tr><tr><td>Select, Dropdown, Radio, Button, swatches</td><td>A value is selected</td></tr><tr><td>Checkbox</td><td>At least one value is ticked</td></tr><tr><td>File upload</td><td>At least one file is attached</td></tr><tr><td>Date and time picker</td><td>A date, or a time, or both, depending on the format</td></tr><tr><td>Switch</td><td>The switch is on</td></tr><tr><td>Range slider</td><td>A value has been set</td></tr><tr><td>Color picker</td><td>A colour has been chosen</td></tr><tr><td>Dimension</td><td>Every axis row has a value</td></tr></tbody></table>

{% hint style="warning" %}
Be careful combining **Required field** with [conditional logic](conditional-logic-and-add-on-fields.md#conditional-logic). A required option that is currently hidden by a rule is not enforced — that is deliberate, so a hidden field cannot block the sale. But it also means "required" only holds while the option is visible. Test both branches of your rule before going live.
{% endhint %}

**When to use it — and when not**

Use it when you genuinely cannot fulfil the order without the answer: a size, an engraving spelling, a photo to print.

Do not use it for anything optional-but-nice. A required gift message on every product turns a two-click purchase into a form to fill in, and shoppers abandon. If in doubt, leave it off and see whether people fill it in anyway.

## Default value

Pre-fills the option so a customer who changes nothing still submits something.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Empty</td></tr><tr><th>Available on</th><td>18 types. It takes four different shapes depending on the type — see below</td></tr></thead></table>

<table><thead><tr><th width="230">Shape</th><th width="240">On these types</th><th>What you enter</th></tr></thead><tbody><tr><td>Free text</td><td>Text, Textarea, Email, Phone, Hidden field, Range slider</td><td>Any text, or a number for the slider</td></tr><tr><td>Number</td><td>Number</td><td>A number, which must fall inside <strong>Min value</strong> and <strong>Max value</strong></td></tr><tr><td>Value picker</td><td>Select, Dropdown, Color dropdown, Image dropdown, Radio, Checkbox, Button, Color swatch, Image swatch, Font picker</td><td>One of the option's own values, chosen from a list. Multi-select types accept several</td></tr><tr><td>Colour</td><td>Color picker</td><td>A colour</td></tr></tbody></table>

**How it behaves**

* The option arrives pre-filled on the product page, and the value is submitted unless the customer changes it.
* **A default value with an add-on price charges immediately.** The shopper sees the higher price the moment the page loads, without having chosen anything. That may be exactly what you want for a paid upgrade you expect most people to take — but it is the most common cause of "why is my product more expensive than the listed price?".
* On a value-picker type, the default must be one of the option's current values. If you rename or delete that value, revisit the default.
* On a Number field, a default outside the min and max is rejected while you edit, with "The value must be between min and max."
* The Personalizer draws the default value in the live preview, so a text layer has something to show before the customer types. See [Text layers](../../personalizer/text-layers.md).

**Good uses**

<table><thead><tr><th width="290">Situation</th><th>Default</th></tr></thead><tbody><tr><td>Most customers pick the standard size</td><td>Preselect it — fewer decisions, faster checkout</td></tr><tr><td>Quantity-style number field</td><td><code>1</code></td></tr><tr><td>Free option among paid ones</td><td>Preselect the free one, so nobody is charged by accident</td></tr><tr><td>Personalizer text layer</td><td><code>Your name</code>, so the preview is not blank</td></tr><tr><td>Hidden field carrying fixed information</td><td>The value itself — that is the whole purpose of the type</td></tr></tbody></table>

<!-- SCREENSHOT: type-shared-required-default | App admin → builder → 1 option Select | Basic Settings với Required field bật và Default value đã chọn 1 giá trị | Khoanh Required field và Default value -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An option's Basic Settings with Required field enabled and a default value selected"><figcaption><p>Required and Default value are alternatives more often than they are partners.</p></figcaption></figure>

## Required or default?

<table><thead><tr><th width="290">You want</th><th>Use</th></tr></thead><tbody><tr><td>The shopper must actively decide</td><td><strong>Required field</strong>, no default</td></tr><tr><td>A sensible answer if they do not care</td><td><strong>Default value</strong>, not required</td></tr><tr><td>They must decide, but you want to nudge one option</td><td>Both — but make sure the default is the free or safest choice</td></tr><tr><td>Nothing at all should be submitted when they skip it</td><td>Neither</td></tr></tbody></table>

Setting both is usually pointless: a field with a default is never empty, so "required" can never fail. The exception is a value picker where the default may be removed later.

## Troubleshooting

<details>
<summary>Add to cart is blocked and I cannot see which field is at fault</summary>

Turn on **Auto-scroll to first error message** in **Settings > Settings > General**. Also check for a required option that is currently hidden by conditional logic in the other branch of a rule.
</details>

<details>
<summary>My product price is higher than the listed price as soon as the page loads</summary>

A default value has an add-on price attached. Either remove the default, or make the default the free value. See [Add-on pricing](../../add-on-pricing/README.md).
</details>

<details>
<summary>The default value is not being applied</summary>

On value-picker types the default must match one of the option's current values exactly. If you edited or deleted that value, reselect the default.
</details>

<details>
<summary>"The value must be between min and max"</summary>

The default on a Number field falls outside its limits. Change the default, or widen **Min value** and **Max value**. See [Limits](limits.md).
</details>

<details>
<summary>A required option is not being enforced</summary>

It is hidden by a conditional logic rule. Hidden options are not validated, by design. Check the rule, and whether the option should be required in both branches.
</details>

<details>
<summary>The required marker is invisible against my theme</summary>

Its colour is store-wide: **Required character** in **Settings > Design**. See [Colors](../../storefront/colors.md).
</details>
