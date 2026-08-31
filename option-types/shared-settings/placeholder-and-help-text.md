---
description: >-
  Placeholder, Help text, and the four places help text can appear — settings
  that guide shoppers on what to enter.
icon: comment-dots
---

# Placeholder and help text

Together, these settings do much of the work of helping shoppers enter the right information. A clear placeholder and a short line of help text can prevent more confusion — and support requests — than a validation rule alone.

<figure><img src="../../.gitbook/assets/2026-08-31_10-05-10 (1).png" alt=""><figcaption></figcaption></figure>

## Placeholder

Grey text shown inside an empty field. It disappears as soon as the customer starts typing.

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Empty, except on <strong>Select</strong>, <strong>Dropdown</strong>, <strong>Color dropdown</strong>, <strong>Image dropdown</strong>, and <strong>Product links</strong>, which start with <code>-- Please select --</code>, and <strong>Font picker</strong>, which starts with <code>-- Select a font --</code></td></tr><tr><td>Available on</td><td>13 types: Text, Textarea, Number, Phone, Email, Color picker, Date and time picker, Select, Dropdown, Color dropdown, Image dropdown, Font picker, Product links</td></tr></tbody></table>

#### How it behaves

* On text-style fields, it appears as example text inside the input box.
* On dropdown-style fields, it appears as the first, unselected entry — the prompt shoppers see before making a choice.
* It is never submitted with the order. If the customer enters nothing, the field remains empty rather than using the placeholder as its value.
* It can be translated separately for each storefront language.

**Use it for the format, not the instruction**

<table><thead><tr><th width="220">Field</th><th width="240">Good placeholder</th><th>Why</th></tr></thead><tbody><tr><td>Engraving text</td><td><code>e.g. Forever yours</code></td><td>Shows the kind of thing expected</td></tr><tr><td>Phone</td><td><code>+44 7700 900000</code></td><td>Shows the format without a rule</td></tr><tr><td>Date</td><td><code>DD/MM/YYYY</code></td><td>Removes all doubt about order</td></tr><tr><td>Dimensions</td><td><code>30</code></td><td>Implies a plain number, no units</td></tr><tr><td>Dropdown</td><td><code>Choose a frame colour</code></td><td>Prompts the action</td></tr></tbody></table>

{% hint style="warning" %}
Do not put required information only in the placeholder. It disappears as soon as the shopper starts typing, and screen readers may not handle it consistently. Put any information the customer needs while entering their response in **Help text** instead.
{% endhint %}

## Help text

A short line of explanation attached to the option. Unlike a placeholder, it stays visible.

<table><thead><tr><th width="180">Tab</th><th>Basic Settings</th></tr></thead><tbody><tr><td>Default</td><td>Empty</td></tr><tr><td>Available on</td><td>22 types — every input and selection type except <strong>Hidden field</strong></td></tr></tbody></table>

#### How it behaves

* Always visible wherever you place it, except in the **Tooltip** position, where it appears when shoppers hover over it.
* Translatable per storefront language.
* Individual **option values** can also have their own help text, displayed next to that specific choice. Add it from the **Action** column in the values table. **Select**, **Product links**, and **Tabs** support help text at the option level only.

**What to write**

<table><thead><tr><th width="300">Situation</th><th>Help text</th></tr></thead><tbody><tr><td>A character limit exists</td><td><code>Up to 20 characters</code></td></tr><tr><td>A choice adds production time</td><td><code>Adds 3 working days to dispatch</code></td></tr><tr><td>A file must be a certain quality</td><td><code>PNG or JPG, at least 1000 × 1000 pixels</code></td></tr><tr><td>The choice is irreversible</td><td><code>Engraved items cannot be returned</code></td></tr><tr><td>The field is optional but useful</td><td><code>Optional — leave blank for no message</code></td></tr></tbody></table>

One line is usually enough. Anything longer belongs in a [Pop-up modal](../static-types/pop-up-modal.md), which shoppers can open if they want the detail.

## Help text position

Where the help text sits relative to the option.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>Below option element</strong></td></tr><tr><td>Available on</td><td>The same 22 types that have Help text</td></tr></tbody></table>

<table><thead><tr><th width="250">Position</th><th>Where the text appears</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Below option label</strong></td><td>Between the label and the field</td><td>The shopper needs to read it <em>before</em> deciding — a constraint or a warning.</td></tr><tr><td><strong>Below option element</strong></td><td>Under the field. This is the default.</td><td>General guidance. Matches what most themes do.</td></tr><tr><td><strong>Above option element</strong></td><td>Above the field but not tied to the label</td><td>Longer guidance that should read as its own line.</td></tr><tr><td><strong>Tooltip</strong></td><td>Hidden behind a small icon next to the label, shown on hover</td><td>Detail that most shoppers do not need, and you want the page kept short.</td></tr></tbody></table>

{% hint style="warning" %}
The **Tooltip** position hides the text until a shopper hovers over it, and hover interactions work differently on touch devices. Do not put essential information — such as restrictions, warnings, or return policies — in a tooltip. Use **Below option label** instead.
{% endhint %}

## Placeholder, help text, or label?

<table><thead><tr><th width="200">Put it in</th><th>When it is</th><th>Example</th></tr></thead><tbody><tr><td><strong>Label</strong></td><td>What the field is</td><td><code>Engraving text</code></td></tr><tr><td><strong>Placeholder</strong></td><td>An example of the format</td><td><code>e.g. Forever yours</code></td></tr><tr><td><strong>Help text</strong></td><td>A rule or consequence they must know</td><td><code>Up to 20 characters. Engraved items cannot be returned.</code></td></tr><tr><td>A <a href="../static-types/pop-up-modal.md">Pop-up modal</a></td><td>More than two sentences</td><td>Your full personalisation policy</td></tr></tbody></table>

## Notes

* **Help text is not a substitute for validation.** It tells shoppers what the rule is; the [limit settings](limits.md) enforce it. Use both.
*
* **Error messages are separate from help text.** Their wording is managed store-wide in **Settings > Translations**. See [Translate widget text](../../translations/translate-widget-text.md).
* **Help text does not appear in the cart or order.** Only the option’s **Name** and the value the customer entered are carried through to the order.
