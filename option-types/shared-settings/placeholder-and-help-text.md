---
description: >-
  Placeholder, Help text, and the four places help text can appear — the settings
  that tell shoppers what to enter.
icon: comment-dots
---

# Placeholder and help text

Between them these three settings do most of the work of preventing bad input. A clear placeholder and one line of help text will save you more support emails than any validation rule.

## Placeholder

Grey example text shown inside an empty field. It disappears as soon as the customer types.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Empty, except on <strong>Select</strong>, <strong>Dropdown</strong>, <strong>Color dropdown</strong>, <strong>Image dropdown</strong>, and <strong>Product links</strong>, which start with <code>-- Please select --</code>, and <strong>Font picker</strong>, which starts with <code>-- Select a font --</code></td></tr><tr><th>Available on</th><td>13 types: Text, Textarea, Number, Phone, Email, Color picker, Date and time picker, Select, Dropdown, Color dropdown, Image dropdown, Font picker, Product links</td></tr></thead></table>

**How it behaves**

* On text-style fields it is example text inside the box.
* On dropdown-style fields it is the first, unselected entry — the prompt the shopper sees before choosing.
* It is never submitted. If the customer types nothing, the field is empty, not filled with the placeholder.
* Translatable per storefront language.

**Use it for the format, not the instruction**

<table><thead><tr><th width="220">Field</th><th width="240">Good placeholder</th><th>Why</th></tr></thead><tbody><tr><td>Engraving text</td><td><code>e.g. Forever yours</code></td><td>Shows the kind of thing expected</td></tr><tr><td>Phone</td><td><code>+44 7700 900000</code></td><td>Shows the format without a rule</td></tr><tr><td>Date</td><td><code>DD/MM/YYYY</code></td><td>Removes all doubt about order</td></tr><tr><td>Dimensions</td><td><code>30</code></td><td>Implies a plain number, no units</td></tr><tr><td>Dropdown</td><td><code>Choose a frame colour</code></td><td>Prompts the action</td></tr></tbody></table>

{% hint style="warning" %}
Do not put required information only in the placeholder. It vanishes the moment the shopper starts typing, and screen readers treat it inconsistently. Anything the customer needs while typing belongs in **Help text**.
{% endhint %}

## Help text

A short line of explanation attached to the option. Unlike a placeholder it stays visible.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Empty</td></tr><tr><th>Available on</th><td>22 types — every input and selection type except <strong>Hidden field</strong></td></tr></thead></table>

**How it behaves**

* Always visible, wherever you position it — except in the tooltip position, where it appears on hover.
* Translatable per storefront language.
* Individual **option values** can have their own help text too, shown next to that one choice. Set it from the values table's **Action** column. **Select**, **Product links**, and **Tabs** support option-level help text only.

**What to write**

<table><thead><tr><th width="300">Situation</th><th>Help text</th></tr></thead><tbody><tr><td>A character limit exists</td><td><code>Up to 20 characters</code></td></tr><tr><td>A choice adds production time</td><td><code>Adds 3 working days to dispatch</code></td></tr><tr><td>A file must be a certain quality</td><td><code>PNG or JPG, at least 1000 × 1000 pixels</code></td></tr><tr><td>The choice is irreversible</td><td><code>Engraved items cannot be returned</code></td></tr><tr><td>The field is optional but useful</td><td><code>Optional — leave blank for no message</code></td></tr></tbody></table>

One line is usually enough. Anything longer belongs in a [Pop-up modal](../static-types/pop-up-modal.md), which shoppers can open if they want the detail.

## Help text position

Where the help text sits relative to the option.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Below option element</strong></td></tr><tr><th>Available on</th><td>The same 22 types that have Help text</td></tr></thead></table>

<table><thead><tr><th width="250">Position</th><th>Where the text appears</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Below option label</strong></td><td>Between the label and the field</td><td>The shopper needs to read it <em>before</em> deciding — a constraint or a warning.</td></tr><tr><td><strong>Below option element</strong></td><td>Under the field. This is the default.</td><td>General guidance. Matches what most themes do.</td></tr><tr><td><strong>Above option element</strong></td><td>Above the field but not tied to the label</td><td>Longer guidance that should read as its own line.</td></tr><tr><td><strong>Tooltip</strong></td><td>Hidden behind a small icon next to the label, shown on hover</td><td>Detail that most shoppers do not need, and you want the page kept short.</td></tr></tbody></table>

{% hint style="warning" %}
The **Tooltip** position hides the text until someone hovers, and hovering does not exist on touch devices in the same way. Do not put anything essential — a restriction, a warning, a returns policy — behind a tooltip. Use **Below option label** for that.
{% endhint %}

<!-- SCREENSHOT: type-shared-helptext-positions | Storefront → trang sản phẩm | 4 option giống nhau minh hoạ 4 vị trí help text khác nhau | Khoanh từng vùng help text -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Four options on a storefront page each showing help text in a different position"><figcaption><p>The same help text in each of its four positions.</p></figcaption></figure>

## Placeholder, help text, or label?

<table><thead><tr><th width="200">Put it in</th><th>When it is</th><th>Example</th></tr></thead><tbody><tr><td><strong>Label</strong></td><td>What the field is</td><td><code>Engraving text</code></td></tr><tr><td><strong>Placeholder</strong></td><td>An example of the format</td><td><code>e.g. Forever yours</code></td></tr><tr><td><strong>Help text</strong></td><td>A rule or consequence they must know</td><td><code>Up to 20 characters. Engraved items cannot be returned.</code></td></tr><tr><td>A <a href="../static-types/pop-up-modal.md">Pop-up modal</a></td><td>More than two sentences</td><td>Your full personalisation policy</td></tr></tbody></table>

## Notes

* Help text is not a substitute for validation. It tells shoppers the rule; the [limit settings](limits.md) enforce it. Use both.
* Error messages are separate from help text, and are worded store-wide in **Settings > Translations**. See [Translate widget text](../../translations/translate-widget-text.md).
* Help text does not appear on the cart or the order. Only the Name and the value the customer entered travel with the order.

## Troubleshooting

<details>
<summary>My help text is not visible on the storefront</summary>

Check **Help text position** — if it is set to **Tooltip**, the text only appears when hovering the icon next to the label. Also confirm the option's label is not hidden, since the tooltip icon sits next to it.
</details>

<details>
<summary>The placeholder is being submitted as the answer</summary>

It is not. If the order shows placeholder-looking text, the shopper typed it, or you set it as the **Default value** rather than the placeholder. See [Required field and default value](required-and-default-value.md#default-value).
</details>

<details>
<summary>My dropdown has no prompt entry</summary>

Its **Placeholder** is empty. Set it to something like `Choose a size` and the unselected prompt reappears.
</details>

<details>
<summary>I set help text on a value but nothing shows</summary>

**Select**, **Product links**, and **Tabs** support help text only at the option level. Use a type that supports per-value help text — Dropdown, Radio, Checkbox, Button, or a swatch type.
</details>

## Next steps

* [Required field and default value](required-and-default-value.md)
* [Limits](limits.md) — enforce what the help text promises.
* [Translate widget text](../../translations/translate-widget-text.md) — for the error messages.
