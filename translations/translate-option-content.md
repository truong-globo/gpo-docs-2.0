---
description: Translate your labels, option values, help text, and placeholders for each storefront language.
icon: pen-to-square
---

# Translate option content

Option content is the words you wrote: labels, option values, help text, placeholders, and static content like paragraphs and size charts. Each of them can be translated per storefront language.

## Before you start

* Your storefront needs more than one language, configured in Shopify. The app reads the list from there.
* Translating option content is plan-gated. If the language switcher is unavailable, see [Compare plans](../plans/compare-plans.md).
* Do the [widget text](translate-widget-text.md) once for the store first. It is quicker, and it covers the messages that appear in every option set.

## Steps

{% stepper %}
{% step %}
### Open the option set in the builder

Translation happens in place, per option set.
{% endstep %}

{% step %}
### Switch language with the control in the builder header

It lists your storefront languages, with your primary language marked.
{% endstep %}

{% step %}
### Edit the text fields

They now hold the translation for the selected language rather than the original. Type the translated version.

The preview panel renders in the selected language too, so you can see the result immediately.
{% endstep %}

{% step %}
### Work through every option

Labels, option values, help text, placeholders, and the content of any static options.
{% endstep %}

{% step %}
### Switch back to your primary language and confirm nothing was overwritten

A quick sanity check that you were editing the translation and not the original.
{% endstep %}

{% step %}
### Save, then test on each storefront

Switch language on your storefront and work through the product page in each one.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: trans-builder-switcher | App admin → builder | Language switcher ở header đang mở với danh sách ngôn ngữ storefront | Khoanh language switcher -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The language switcher in the builder header listing the storefront languages"><figcaption><p>Switch language, then edit the text in place.</p></figcaption></figure>

## What can be translated

<table><thead><tr><th width="290">Translatable</th><th>Not translatable</th></tr></thead><tbody><tr><td>Option <strong>Label</strong></td><td>Option <strong>Name</strong> — deliberately, so orders stay consistent</td></tr><tr><td>Option values</td><td>Prefix and suffix text</td></tr><tr><td><strong>Help text</strong>, at option and value level</td><td>Option set names</td></tr><tr><td><strong>Placeholder</strong></td><td>Add-on product titles — translate those in Shopify</td></tr><tr><td>Static content: Heading, Paragraph, Pop-up modal, HTML, Size chart, Tabs</td><td>The <code>globo-product-options</code> tag and other internal values</td></tr><tr><td>Conditional logic values for <strong>Shopify variant</strong> conditions</td><td></td></tr></tbody></table>

## The two that catch people out

### Option Name stays in one language

The **Name** is what appears on the cart, the order, and your packing slips. It is not translatable on purpose: your production team should read `Engraving text` whatever language the shopper bought in.

If a customer asks why their cart shows English, that is why. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).

### Variant conditions need translating too

If you use [conditions based on Shopify variants](../conditional-logic/conditions-on-shopify-variants.md), the variant name you typed is stored **per language** — because variant names themselves are translated.

So a rule that works on your English storefront will not fire on your French one until you switch language in the builder and enter the French variant name as well. The value field shows the current language as a suffix to remind you.

This is the single most common multi-language bug in the app.

## Keeping translations in step

<table><thead><tr><th width="290">When you</th><th>Remember to</th></tr></thead><tbody><tr><td>Add an option</td><td>Translate it in every language before going live</td></tr><tr><td>Add an option value</td><td>Same — an untranslated value shows in your primary language</td></tr><tr><td>Rename an option value</td><td>Update the translation, and check any conditional rule that referenced it</td></tr><tr><td>Change help text</td><td>Update every language, or the languages drift apart</td></tr><tr><td>Add a storefront language in Shopify</td><td>Go through every option set for the new language</td></tr></tbody></table>

A practical habit: finish an option set completely in your primary language, then do all the translations in one pass. Translating as you build means redoing work every time you change your mind.

## Notes

* Untranslated text falls back to your primary language rather than showing blank, so a partially translated store still works.
* The builder preview renders in the selected language, which is the quickest way to check a translation reads well in context.
* Option values keep their character rules in every language — no `,` `:` `"` `'` `|`. See [Working with option values](../option-sets/option-values.md).
* CSV export includes translations, so a translated option set can be moved between stores. See [Import and export](../option-sets/import-and-export.md).
