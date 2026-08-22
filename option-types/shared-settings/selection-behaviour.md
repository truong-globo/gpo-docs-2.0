---
description: >-
  Allow multiple, Not allow deselect, and Search suggestion — how selection
  options behave when the shopper interacts with them.
icon: hand-pointer
---

# Selection behaviour

Three settings that change how a selection option responds to clicks. **Allow multiple** is the important one — it unlocks other settings and changes how add-on pricing works.

## Allow multiple

Lets the shopper choose more than one value.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Off</td></tr><tr><th>Available on</th><td>Select, Dropdown, Color dropdown, Image dropdown, Button, Color swatch, Image swatch. Also on <strong>File upload</strong>, where it means multiple files rather than multiple values</td></tr></thead></table>

{% hint style="info" %}
**Checkbox** is multi-select by nature and has no switch. **Radio button** is single-select by nature and has none either. The switch exists on the types that can work both ways.
{% endhint %}

**What turning it on changes**

<table><thead><tr><th width="290">Effect</th><th>Detail</th></tr></thead><tbody><tr><td>The shopper can select several values</td><td>Selecting a second value no longer clears the first.</td></tr><tr><td><a href="limits.md#min-and-max-selections">Min selections</a> and <a href="limits.md#min-and-max-selections">Max selections</a> appear</td><td>They are meaningless on a single-select option, so they stay hidden until now.</td></tr><tr><td><a href="#not-allow-deselect">Not allow deselect</a> disappears</td><td>It only applies to single-select options.</td></tr><tr><td><strong>Default value</strong> accepts several values</td><td>You can preselect more than one.</td></tr><tr><td>Add-on pricing adds up</td><td>Every selected value with a price contributes. A shopper picking three paid extras pays for three.</td></tr><tr><td><strong>Mixed quantity</strong> becomes available</td><td>An advanced add-on mode that gives each value its own quantity box. See <a href="../../add-on-pricing/advanced-add-on-modes.md">Advanced add-on modes</a>.</td></tr></tbody></table>

**On File upload**

The setting is labelled to say so, and allows up to 20 files. Turning it on reveals **Min number of files** and **Max number of files**. See [File upload](../input-types/file-upload.md).

**Choosing between multi-select types**

<table><thead><tr><th width="260">You want</th><th>Use</th></tr></thead><tbody><tr><td>A plain list of extras to tick</td><td><strong>Checkbox</strong></td></tr><tr><td>Several choices without a long list on the page</td><td><strong>Dropdown</strong> with Allow multiple</td></tr><tr><td>Several colours or finishes, shown visually</td><td><strong>Color swatch</strong> or <strong>Image swatch</strong> with Allow multiple</td></tr><tr><td>Several choices as prominent buttons</td><td><strong>Button</strong> with Allow multiple</td></tr></tbody></table>

## Not allow deselect

Once the shopper has chosen something, they cannot unchoose it — they can only switch to another value.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td>Off</td></tr><tr><th>Available on</th><td>Dropdown, Color dropdown, Image dropdown, Button, Color swatch, Image swatch — and only while <strong>Allow multiple</strong> is off</td></tr></thead></table>

**Why it exists**

On these types, clicking the value you already have selected normally clears it, leaving nothing selected. That is right for an optional extra, and wrong for a mandatory choice — a shopper who accidentally clears their size selection has to notice and fix it.

Turning this on means the option always has exactly one value once the shopper has begun.

**When to use it**

* A mandatory choice such as size, finish, or material.
* Any option where "nothing selected" is not a valid answer.
* Together with a **Default value**, to guarantee the option is never empty.

**When not to use it**

* Optional paid extras. If a shopper picks a $20 upgrade and then changes their mind, they must be able to remove it. Locking that in produces complaints and refunds.

{% hint style="info" %}
This is not the same as **Required field**. Required blocks add-to-cart when nothing is selected; this prevents the shopper getting back to nothing in the first place. They work well together on a mandatory choice.
{% endhint %}

## Search suggestion

Adds a search box to the top of a dropdown so the shopper can type to filter.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td>Off</td></tr><tr><th>Available on</th><td>Dropdown, Color dropdown, Image dropdown, Font picker</td></tr></thead></table>

**How it behaves**

* The dropdown gains a search field; typing narrows the list.
* The search prompt wording is store-wide and editable — `Search...` in **Settings > Translations**. See [Translate widget text](../../translations/translate-widget-text.md).
* It filters the values you defined. It does not search your product catalogue.

**When to use it**

Once a list passes roughly fifteen values, scrolling becomes the slowest part of the purchase. Turn it on for:

* long colour or finish lists
* country, region, or city lists
* font lists — the **Font picker** benefits most, since shoppers often arrive knowing the font name
* long lists of compatible models or sizes

For shorter lists it adds a control shoppers do not need. Consider instead whether a [collapsible layout or slider](collapsible-layouts-and-sliders.md) suits the list better.

<!-- SCREENSHOT: type-shared-selection-behaviour | App admin → builder → option Dropdown | Allow multiple ở Basic Settings; Search suggestion và Not allow deselect ở Advanced Settings | Khoanh Allow multiple và nhóm Search suggestion / Not allow deselect -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Allow multiple on Basic Settings, with Search suggestion and Not allow deselect on Advanced Settings"><figcaption><p>Allow multiple is a Basic setting; the other two are Advanced.</p></figcaption></figure>

## Troubleshooting

<details>
<summary>I cannot find Min selections or Max selections</summary>

Turn on **Allow multiple** first. They are hidden on single-select options.
</details>

<details>
<summary>Not allow deselect has disappeared</summary>

You turned on **Allow multiple**. The setting only applies to single-select options.
</details>

<details>
<summary>Shoppers are being charged for several options at once</summary>

That is what **Allow multiple** does — every selected value with a price is charged. If you meant only one paid choice, turn it off, or set **Max selections** to `1`.
</details>

<details>
<summary>Shoppers cannot remove a paid extra</summary>

**Not allow deselect** is on. Turn it off for optional paid options.
</details>

<details>
<summary>The search box does not appear in my dropdown</summary>

**Search suggestion** is only available on Dropdown, Color dropdown, Image dropdown, and Font picker. A plain **Select** uses the browser's own dropdown and cannot have one.
</details>

<details>
<summary>Search finds nothing even though the value exists</summary>

Search matches the value text as displayed, including any translation for the current language. Check the value in the language you are browsing in.
</details>
