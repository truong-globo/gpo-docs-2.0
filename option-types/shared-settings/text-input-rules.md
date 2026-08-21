---
description: >-
  Allowed value and Text transform — restrict which characters a shopper may
  type, and normalise the capitalisation of what they submit.
icon: keyboard
---

# Text input rules

Two settings, both on **Text** and **Textarea** only. [Limits](limits.md) control *how much* a shopper types; these control *what* they type and how it comes out.

They exist mainly for engraving, embroidery, and printing, where the production process cannot accept every character or where mixed capitalisation looks wrong.

## Allowed value

Restricts which characters the field accepts.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Default</strong> — anything is accepted</td></tr><tr><th>Available on</th><td>Text, Textarea</td></tr></thead></table>

<table><thead><tr><th width="230">Choice</th><th>Accepts</th><th>Blocks</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>Anything the shopper can type</td><td>Nothing</td></tr><tr><td><strong>Letters</strong></td><td>Letters only</td><td>Digits, punctuation, symbols</td></tr><tr><td><strong>Letters &amp; numbers</strong></td><td>Letters and digits</td><td>Punctuation and symbols</td></tr></tbody></table>

**How it behaves**

* The restriction applies as the shopper types — blocked characters simply do not appear in the field.
* Spaces are still allowed, so multi-word entries work under all three settings.
* This is about characters, not language. **Letters** does not mean "English letters only".

**When to use it**

<table><thead><tr><th width="300">Situation</th><th>Setting</th></tr></thead><tbody><tr><td>Engraving on a machine that cannot cut symbols</td><td><strong>Letters &amp; numbers</strong></td></tr><tr><td>A name to embroider</td><td><strong>Letters</strong></td></tr><tr><td>A gift message</td><td><strong>Default</strong> — people want commas and full stops</td></tr><tr><td>A reference or order code</td><td><strong>Letters &amp; numbers</strong></td></tr></tbody></table>

{% hint style="warning" %}
Say so in [Help text](placeholder-and-help-text.md#help-text). A shopper typing an apostrophe into a **Letters** field sees nothing happen, with no explanation. `Letters only — no punctuation` prevents the confusion entirely.
{% endhint %}

Be conservative with **Letters**. It blocks digits, so `Flat 3B` and `Team 2024` become impossible. If your real constraint is "no emoji and no symbols", **Letters & numbers** is almost always the right choice.

## Text transform

Normalises the capitalisation of what the shopper typed.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Default</strong> — submitted exactly as typed</td></tr><tr><th>Available on</th><td>Text, Textarea</td></tr></thead></table>

<table><thead><tr><th width="200">Choice</th><th>Input</th><th>Result</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td><code>john SMITH</code></td><td><code>john SMITH</code></td></tr><tr><td><strong>UPPERCASE</strong></td><td><code>john SMITH</code></td><td><code>JOHN SMITH</code></td></tr><tr><td><strong>lowercase</strong></td><td><code>john SMITH</code></td><td><code>john smith</code></td></tr><tr><td><strong>Sentence</strong></td><td><code>john SMITH</code></td><td><code>John smith</code></td></tr><tr><td><strong>Capitalized</strong></td><td><code>john SMITH</code></td><td><code>John Smith</code></td></tr></tbody></table>

**How it behaves**

* The transform is applied to the entry, so what reaches your order is already normalised — you do not have to tidy it up before production.
* **Sentence** capitalises the first letter and lowercases the rest, which suits a message.
* **Capitalized** capitalises the first letter of each word, which suits names.

**When to use it**

<table><thead><tr><th width="300">Situation</th><th>Setting</th></tr></thead><tbody><tr><td>Names to engrave in one consistent style</td><td><strong>Capitalized</strong></td></tr><tr><td>Initials or a monogram</td><td><strong>UPPERCASE</strong></td></tr><tr><td>A stamped label in a lowercase typeface</td><td><strong>lowercase</strong></td></tr><tr><td>A gift message in the shopper's own words</td><td><strong>Default</strong></td></tr><tr><td>Team names on a jersey, printed in caps</td><td><strong>UPPERCASE</strong></td></tr></tbody></table>

{% hint style="info" %}
**Capitalized** works on word boundaries, so genuinely unusual capitalisation is flattened: `McDonald` becomes `Mcdonald`, `iPhone` becomes `Iphone`. If your customers' entries include names like that, use **Default** and let a human check the order.
{% endhint %}

## Using both together

They are independent and combine cleanly. A typical engraving field:

<table><thead><tr><th width="240">Setting</th><th>Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Max character</strong></td><td><code>15</code></td><td>What physically fits</td></tr><tr><td><strong>Character counter</strong></td><td><strong>Show</strong></td><td>So they can see the limit closing in</td></tr><tr><td><strong>Allowed value</strong></td><td><strong>Letters &amp; numbers</strong></td><td>The machine cannot cut symbols</td></tr><tr><td><strong>Text transform</strong></td><td><strong>Capitalized</strong></td><td>Every engraving looks the same</td></tr><tr><td><strong>Help text</strong></td><td><code>Up to 15 letters and numbers. Engraved items cannot be returned.</code></td><td>No surprises</td></tr></tbody></table>

<!-- SCREENSHOT: type-shared-text-rules | App admin → builder → option Text → tab Advanced Settings | Allowed value và Text transform | Khoanh 2 field -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The Allowed value and Text transform settings on a Text option's Advanced Settings"><figcaption><p>Both live on Advanced Settings, next to each other.</p></figcaption></figure>

## Notes

* The Personalizer live preview draws the transformed text, so what the customer sees on the product photo matches what you will produce. See [Text layers](../../personalizer/text-layers.md).
* Neither setting affects the option's **Label**, **Name**, or **Help text** — only the shopper's entry.
* Neither applies to any other option type. A dropdown's values are text you control, so there is nothing to restrict or normalise.

## Troubleshooting

<details>
<summary>Shoppers say they cannot type certain characters</summary>

**Allowed value** is set to **Letters** or **Letters & numbers**. Loosen it, or explain it in help text.
</details>

<details>
<summary>Digits are being rejected in a name field</summary>

**Letters** blocks digits. Switch to **Letters & numbers**.
</details>

<details>
<summary>My orders arrive in the wrong capitalisation</summary>

Set **Text transform**. If they are already arriving transformed but wrongly — `Mcdonald` instead of `McDonald` — switch back to **Default** and check those orders by hand.
</details>

<details>
<summary>Text transform is not applying</summary>

Confirm you are looking at a Text or Textarea option, save the option set, and refresh the product page. Existing cart items keep the value they were added with.
</details>

## Next steps

* [Limits](limits.md) — how much they can type.
* [Placeholder and help text](placeholder-and-help-text.md) — explain the rules.
* [Text](../input-types/text.md) and [Textarea](../input-types/textarea.md) — the two types these apply to.
