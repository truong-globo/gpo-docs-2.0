---
description: >-
  Label, Name, and Hidden label — the three settings that control what an option
  is called and whether shoppers see that name.
icon: tag
---

# Labels and visibility

Every option that collects something from the customer has a **Label** and a **Name**, and most also offer **Hidden label**. These three decide what an option is called on the product page and on the order.

For the conceptual difference between Label and Name, and the reasoning behind it, see [Label vs Name](../../concepts/label-vs-name.md). This page is the settings reference.

## Label

The text shown above the option field on your product page.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>The option type's name — for example a new Text option starts with the label <code>Text</code></td></tr><tr><th>Available on</th><td>All types except the purely visual statics, which use their own content fields instead: Divider, Spacing, Heading, Paragraph, HTML, Pop-up modal, Size chart, Tabs</td></tr></thead></table>

**How it behaves**

* Required. An option cannot be saved with an empty Label.
* No character restrictions. Punctuation, apostrophes, emoji, and non-Latin scripts are all fine.
* Not required to be unique. Two options may legitimately share a Label — for example a `Colour` dropdown in a "Front" section and another in a "Back" section.
* Translatable per storefront language. See [Translate option content](../../translations/translate-option-content.md).
* On a **Section**, the Label is the group heading rather than a field label.

**Writing good labels**

<table><thead><tr><th width="270">Instead of</th><th>Write</th></tr></thead><tbody><tr><td><code>Text</code></td><td><code>Engraving text</code></td></tr><tr><td><code>Options</code></td><td><code>Choose your frame colour</code></td></tr><tr><td><code>Upload</code></td><td><code>Upload your photo</code></td></tr><tr><td><code>Date</code></td><td><code>Delivery date</code></td></tr></tbody></table>

Say what you want, not what the field is. Put the constraint in [Help text](placeholder-and-help-text.md#help-text) rather than the Label — `Engraving text` with help text `Up to 20 characters` reads better than `Engraving text (max 20 characters)`.

## Name

The internal name of the option. It appears on the cart page, at checkout, on the order in your Shopify admin, and in order emails, invoices, and packing slips.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>The option type's internal identifier — <code>text</code>, <code>checkbox</code>, <code>select</code>, and so on</td></tr><tr><th>Available on</th><td>All types that collect input. Not on <strong>Section</strong> or the visual statics, which never reach the order</td></tr></thead></table>

{% hint style="warning" %}
Name has three rules:

* it cannot be empty
* it must be **unique within the option set** — the check ignores capitalisation and surrounding spaces
* it cannot contain `.` `:` `"` `'` `\` `|`
{% endhint %}

**How it behaves**

* Not translatable, deliberately. Your team sees one consistent name whatever language the shopper used.
* Renamed automatically when you duplicate an option or import options whose names clash — the copy gets the type plus a number, such as `text-2`. Conditional logic rules pointing at a renamed option are repointed for you.
* Used by other features to identify the option: the dynamic order-tag workflow, order note templates, and the `option_name` column in CSV export.

**Practical advice**

Change it from the default before you go live. An order line reading `text: Forever yours` is accurate and useless; `Engraving text: Forever yours` is obvious to whoever is packing the box.

The simplest approach is to make Name the same as Label, and only diverge when Label contains a blocked character or when two options share a Label.

## Hidden label

Hides the option's Label on the product page. The option still works, and its Name still reaches the order.

<table><thead><tr><th width="180">Tab</th><td>Basic Settings</td></tr><tr><th>Default</th><td>Off</td></tr><tr><th>Available on</th><td>22 types — every input and selection type except <strong>Hidden field</strong>, which has no visible label anyway</td></tr></thead></table>

**When to use it**

* The option is self-explanatory from its placeholder — a single `Search…` box, for example.
* A [Section](../static-types/section.md) heading or a [Heading](../static-types/heading.md) element already says what the group is, and the individual label would just repeat it.
* You are building a compact row of options and the labels waste vertical space.
* You are using an [image swatch](../selection-types/image-swatch.md) row where the images speak for themselves.

**When not to use it**

* On required fields. A shopper who cannot see what a field is for will not know they have to fill it in, and your error message will be the first explanation they get.
* On anything with a price attached. Shoppers should be able to see what they are paying for.
* As a way to fix a layout problem. If labels are crowding your page, use [Column width](direction-width-and-css.md#column-width) or a collapsible [Section](../static-types/section.md) instead.

{% hint style="info" %}
Hiding the label does not hide the option. To take an option off the storefront while keeping it configured, use the **Hide** action on the option instead — see [Build your options](../../option-sets/build-options.md).
{% endhint %}

<!-- SCREENSHOT: type-shared-label-name | App admin → builder → 1 option Text | Basic Settings: Label, Name, Required field, Hidden label | Khoanh 4 field -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An option's Basic Settings showing Label, Name, Required field, and Hidden label"><figcaption><p>Label, Name, and Hidden label sit together at the top of Basic Settings.</p></figcaption></figure>

## Troubleshooting

<details>
<summary>"Name must be unique. Please enter a different value."</summary>

Another option in this option set uses the same Name once capitalisation and spaces are ignored. Duplicated options are the usual cause — rename the copy.
</details>

<details>
<summary>"Name cannot contain any of the following characters . : " ' \ |"</summary>

Remove the character. Apostrophes are the most frequent offender: use `Customers note` as the Name and put `Customer's note` in the Label.
</details>

<details>
<summary>My cart shows "text" instead of a proper name</summary>

The Name is still at its default. Set it to something readable and save. Orders already placed keep the old name.
</details>

<details>
<summary>I hid the label and now shoppers do not fill the field in</summary>

Expected — turn **Hidden label** back off, or add a [Heading](../static-types/heading.md) above the option so there is still an instruction on the page.
</details>

<details>
<summary>I translated the Label but the cart is still in English</summary>

The cart shows the **Name**, which is not translatable by design. See [Translate option content](../../translations/translate-option-content.md).
</details>

## Next steps

* [Placeholder and help text](placeholder-and-help-text.md) — the other text a shopper reads.
* [Required field and default value](required-and-default-value.md)
* [Label vs Name](../../concepts/label-vs-name.md) — the concept page.
