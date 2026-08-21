---
description: >-
  Every option has both a Label and a Name. They look alike, they do different
  jobs, and only one of them has rules.
icon: tag
---

# Label vs Name

These two fields sit next to each other on every option's **Basic Settings**, and they are the single most common source of confusion in the app. This page settles it.

## The difference in one table

<table><thead><tr><th width="150"></th><th width="290">Label</th><th>Name</th></tr></thead><tbody><tr><td>Who reads it</td><td>The shopper, on the product page</td><td>You and your team — and the shopper, once the item is in their cart</td></tr><tr><td>Where it appears</td><td>Above the option field in the widget</td><td>Cart page, checkout, order details in Shopify admin, order confirmation emails, invoices, packing slips</td></tr><tr><td>Typical value</td><td><code>Engraving text</code></td><td><code>Engraving text</code></td></tr><tr><td>Required</td><td>Yes</td><td>Yes</td></tr><tr><td>Must be unique</td><td>No</td><td><strong>Yes</strong>, within the option set</td></tr><tr><td>Restricted characters</td><td>No</td><td><strong>Yes</strong> — see below</td></tr><tr><td>Can be hidden</td><td>Yes, with <strong>Hidden label</strong></td><td>No. It always travels with the order.</td></tr><tr><td>Translatable per language</td><td>Yes</td><td>No</td></tr></tbody></table>

<!-- SCREENSHOT: concept-label-name-fields | App admin → builder → 1 option bất kỳ | 2 field Label và Name cạnh nhau trong Basic Settings, có icon tooltip | Khoanh cả 2 field -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Label and Name fields side by side in an option's Basic Settings"><figcaption><p>Label and Name sit side by side, but they end up in different places.</p></figcaption></figure>

## Label

The text shown above the option field on your product page. Write it for shoppers: short, plain, and in their language.

* Use anything you like — punctuation, emoji, non-Latin characters, any length. There are no restrictions.
* Two options may share the same Label. That is legitimate: two dropdowns both labelled `Colour`, one in a "Front" section and one in a "Back" section, read perfectly well on the page.
* Hide it with **Hidden label** when the option is self-explanatory or when the section heading already says it. See [Hidden label](../option-types/shared-settings/labels-and-visibility.md#hidden-label).
* Translate it per storefront language — see [Translate option content](../translations/translate-option-content.md).

## Name

The internal name of the option. It is what identifies the option everywhere outside the product page.

Because it becomes part of the order record, it has three rules.

{% hint style="warning" %}
**Name must be filled in.** It cannot be left blank.

**Name must be unique within the option set.** The check ignores capitalisation and surrounding spaces, so `Gift wrap` and `gift wrap ` count as the same name.

**Name cannot contain any of these characters:** `.` `:` `"` `'` `\` `|`
{% endhint %}

If you break one of those rules, the field turns red with the reason and the option set will not save until you fix it.

### Write Names your team can read

The value you put in **Name** is what your fulfilment team sees on the order. Compare:

<table><thead><tr><th width="240">Name</th><th>How the order line reads</th></tr></thead><tbody><tr><td><code>text</code></td><td>text: Forever yours — accurate but useless in a packing list</td></tr><tr><td><code>Engraving text</code></td><td>Engraving text: Forever yours — obvious to whoever is packing the box</td></tr></tbody></table>

The app fills **Name** in with the option type as a starting value (`text`, `checkbox`, `select`, and so on) so that a new option always has a valid name. Change it to something meaningful before you go live.

### Names are used by other features

* **Order tags automation** — the dynamic tag mode tags orders using a specific option, identified by its Name. Renaming the option later means revisiting the workflow. See [Update order tags](../automations/update-order-tags.md).
* **Order notes and email templates** — the option lists these produce use Names.
* **CSV import and export** — the `option_name` column is this field. Names must still be unique after an import. See [Import and export](../option-sets/import-and-export.md).

## When the app renames things for you

The app will change a **Name** by itself in two situations, both to protect uniqueness:

* **You duplicate an option.** The copy gets a new Name so it does not clash with the original — typically the option type plus a number, such as `text-2`.
* **You paste in or import options whose Names already exist.** Clashing Names are renumbered the same way, and any conditional logic rule that pointed at the renamed option is repointed automatically so your rules keep working.

Check the Names after duplicating or importing and give them readable values.

{% hint style="info" %}
Changing an option's **type** keeps the option in place but resets type-specific settings. Review both Label and Name afterwards — see [Build your options](../option-sets/build-options.md).
{% endhint %}

## Should Label and Name be the same?

Usually yes, and that is the simplest thing to do. Keep them different when:

* The Label is long or decorated for the storefront (`Add an engraving ✨ (optional)`) but you want a clean order line (`Engraving text`).
* The Label uses characters that Name does not allow, such as an apostrophe or a colon.
* Two options share a Label on the page but must be told apart on the order — for example `Colour` in two sections, named `Front colour` and `Back colour`.
* Your storefront is translated. The Label gets translated per language; the Name stays in one language so your team always reads the same thing.

## Troubleshooting

<details>
<summary>"Name must be unique. Please enter a different value."</summary>

Another option in the same option set already uses that Name. The check ignores capitalisation and trailing spaces. Scan the option list for a duplicate — duplicated options are the usual cause.
</details>

<details>
<summary>"Name cannot contain any of the following characters . : " ' \ |"</summary>

Remove the character. Apostrophes are the most common offender: use `Customers note` rather than `Customer's note`, and put the friendly wording in **Label** instead.
</details>

<details>
<summary>My order line shows "text" or "checkbox" instead of a proper name</summary>

The Name was left at its default. Open the option, set **Name** to something readable, and save. Existing orders keep the old name — only new orders pick up the change.
</details>

<details>
<summary>I renamed an option and an automation stopped working</summary>

Workflows that target a specific option identify it by Name. Open **Automations**, edit the workflow, and select the option again. See [Update order tags](../automations/update-order-tags.md).
</details>

<details>
<summary>I translated the Label but the cart still shows English</summary>

The cart shows **Name**, which is not translatable. This is by design so your team sees one consistent name whatever language the shopper used. See [Translate option content](../translations/translate-option-content.md).
</details>

## Next steps

* [Working with option values](option-values.md) — values have their own set of rules.
* [Label](../option-types/shared-settings/labels-and-visibility.md#label) and [Name](../option-types/shared-settings/labels-and-visibility.md#name) — the settings reference pages.
* [Show options on orders](../storefront/show-options-on-orders.md) — where Names end up.
