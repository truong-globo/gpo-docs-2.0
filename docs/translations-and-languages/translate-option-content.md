---
description: >-
  Translate your labels, option values, help text, and placeholders for each
  storefront language, by hand or with Auto-translate.
icon: pen-to-square
---

# Translate option content

Option content is the text you wrote: labels, option values, help text, placeholders, and static content such as paragraphs and size charts. Each of these can be translated for each storefront language.

## Before you start

* Your storefront needs more than one language, configured in Shopify. The app reads the list from there.
* Translating option content may not be available on all plans. If the **Translations** tab is unavailable, see [Compare plans](../plans-and-billing/compare-plans.md).
* Translate the [widget text](translate-widget-text.md) for the store first. It is quicker, and it covers the messages that appear in every option set.

## Steps

Translation is done per option set, on its own **Translations** tab beside **Basic**, **Advanced**, and **Personalizer**.

{% stepper %}
{% step %}
### Open the option set and select the **Translations** tab

The **Languages** screen lists every language your store sells in.

<figure><img src="../.gitbook/assets/tran 1.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Read the status of each language

Each row shows a status: **Default** for your source language, **Translated** when nothing is left, or **Not translated**. A partly finished language shows how many fields are left, such as `4 fields left`.

<figure><img src="../.gitbook/assets/tran 5.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Select a language to translate

The editor opens on **Translating** . Each row shows the **Source text** beside the field you fill in, so you are never translating blind.

<figure><img src="../.gitbook/assets/tran 6.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Work through the fields

Fields are grouped under **Option elements** and **Section titles**, and labelled by position — `Option 1`, `Section 2`, `Tab 3`, `Condition 1`.

Use **Search fields** to jump to one, or set **Translation status** to **Untranslated fields** to see only what is left.

<figure><img src="../.gitbook/assets/tran 7.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Check it with **Preview**

**Preview** is available from the languages list and from inside the editor.

<figure><img src="../.gitbook/assets/tran 8.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Select **Back to languages** and repeat

The status on the list updates as you finish each language.
{% endstep %}

{% step %}
### Save, then test on each storefront

Switch language on your storefront and work through the product page in each one.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
Fields you leave empty fall back to the source text, so a partly translated language still works on your storefront.
{% endhint %}

## Auto-translate

**Auto-translate** fills in the untranslated fields of the language you are working on, so you review and correct rather than type everything. It is on the same screen as the fields themselves.

<figure><img src="../.gitbook/assets/tran 3.png" alt=""><figcaption></figcaption></figure>

{% stepper %}
{% step %}
### Open the language you want to translate

Auto-translate works on one language at a time, and only on fields that are still empty. It never overwrites a translation you have already written.
{% endstep %}

{% step %}
### Check the estimate

The credit line reads, for example, `Monthly AI credits: 12K / 300K · This run will use about 4K credits.` The button is unavailable when there is nothing left to translate.
{% endstep %}

{% step %}
### Select **Auto-translate**

Progress is shown as it runs — `Translated 18 of 42 fields` — and a **Stop** button appears beside it.
{% endstep %}

{% step %}
### Read the result and correct it

When it finishes you get a confirmation such as `Auto-translate finished. 42 fields translated.` Machine output still needs a read-through, particularly for product names, materials, and anything you have a house term for.
{% endstep %}
{% endstepper %}

### What it skips

<table><thead><tr><th width="330">Skipped</th><th>Why, and what to do</th></tr></thead><tbody><tr><td>Fields you have already translated</td><td>Auto-translate only fills empty fields</td></tr><tr><td>Fields that are too long</td><td>Reported as <code>:count fields were skipped because they are too long to translate automatically.</code> Translate those by hand</td></tr><tr><td>Condition values</td><td>Reported as <code>:count condition values are left for you to translate by hand.</code> These have to match your Shopify variant names exactly, so they are never guessed. See <a href="translate-option-content.md#variant-conditions-need-translating-too">Variant conditions need translating too</a></td></tr></tbody></table>

### Monthly AI credits

Auto-translate runs on a monthly credit allowance that comes with your plan.

<table><thead><tr><th width="290">What you see</th><th>What it means</th></tr></thead><tbody><tr><td><code>Monthly AI credits: 12K / 300K</code></td><td>How much of this month's allowance you have used</td></tr><tr><td><code>This run will use about 4K credits</code></td><td>An estimate for the language you are about to translate, shown before you start</td></tr><tr><td><code>Monthly AI credits used up</code></td><td>The allowance is spent. <strong>Auto-translate</strong> is unavailable until it resets at the start of next month. Translating by hand still works</td></tr></tbody></table>

Credits are counted per run, not per language, so translating a short option set costs far less than a long one. The allowance is shared across your whole store, and the exact number depends on your plan — see [Compare plans](../plans-and-billing/compare-plans.md).

{% hint style="warning" %}
Credits are spent as the work is done. If you **Stop** a run part-way, the fields already translated are kept, and so is the cost of translating them.
{% endhint %}

### If it stops early

<table><thead><tr><th width="330">Message</th><th>What to do</th></tr></thead><tbody><tr><td>A translation is already running for this option set</td><td>Wait for the other run to finish. Only one run per option set at a time, even across browser tabs</td></tr><tr><td>Too many translation requests. Try again in <code>:count</code> seconds</td><td>Wait the number of seconds shown, then select <strong>Try again</strong></td></tr><tr><td>Translation timed out</td><td>The fields already translated were kept. Select <strong>Try again</strong> to continue with the rest</td></tr><tr><td>Auto-translate is temporarily unavailable</td><td>A problem on the translation service. Try again later</td></tr><tr><td>Auto-translate failed</td><td>Select <strong>Try again</strong>. If it keeps happening, see <a href="../help/contact-support.md">Contact support</a></td></tr></tbody></table>

A run that stops part-way keeps everything it had already translated, and **Try again** picks up from what is still empty.

{% hint style="info" %}
Auto-translate may not be available on all plans. See [Compare plans](../plans-and-billing/compare-plans.md).
{% endhint %}

## What can be translated

<table><thead><tr><th width="290">Translatable</th><th>Not translatable</th></tr></thead><tbody><tr><td>Option <strong>Label</strong></td><td>Option <strong>Name</strong> — deliberately, so orders stay consistent</td></tr><tr><td>Option values</td><td>Prefix and suffix text</td></tr><tr><td><strong>Help text</strong>, at option and value level</td><td>Option set names</td></tr><tr><td><strong>Placeholder</strong></td><td>Add-on product titles — translate those in Shopify</td></tr><tr><td>Static content: Heading, Paragraph, Pop-up modal, HTML, Size chart, Tabs</td><td>The <code>globo-product-options</code> tag and other internal values</td></tr><tr><td>Conditional logic values for <strong>Shopify variant</strong> conditions</td><td>Conditions that test your own option values — they compare the source value</td></tr><tr><td>Section titles</td><td></td></tr></tbody></table>

## Two things to be aware of

### Option Name stays in one language

The **Name** appears on the cart, the order, and your packing slips. It is intentionally not translatable, so your production team reads `Engraving text` regardless of the language the customer ordered in.

This is why a customer's cart can show English text on a translated storefront. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).

### Variant conditions need translating too

If you use [conditions based on Shopify variants](../conditional-logic/conditions-on-shopify-variants.md), the variant name you entered is stored **for each language**, because variant names are translated as well.

A rule that works on your English storefront does not run on your French storefront until the French variant name is entered too. These values appear in the **Translations** tab like any other field, labelled `Condition 1`, `Condition 2`, and so on, so they are listed with everything else rather than hidden inside the rule builder.

This is the most common cause of conditional logic not working on a translated storefront.

Conditions that test one of **your own** option values are not translated. They compare against the source value, so they keep working in every language.

## Keeping translations in step

<table><thead><tr><th width="290">When you</th><th>Remember to</th></tr></thead><tbody><tr><td>Add an option</td><td>Translate it in every language before going live</td></tr><tr><td>Add an option value</td><td>Same — an untranslated value shows in your primary language</td></tr><tr><td>Rename an option value</td><td>Update the translation, and check any conditional rule that referenced it</td></tr><tr><td>Change help text</td><td>Update every language, or the languages drift apart</td></tr><tr><td>Add a storefront language in Shopify</td><td>Go through every option set for the new language</td></tr></tbody></table>

Finish an option set completely in your primary language, then translate it in one pass. Translating while you build means repeating the work every time you change something.

## Notes

* Untranslated fields fall back to the source text rather than displaying blank, so a partially translated store still works.
* **Preview** displays the option set in the selected language, which is the quickest way to check a translation in context.
* Option values keep their character rules in every language. The characters `,` `:` `"` `'` `|` are not allowed. See [Working with option values](../option-sets/option-values.md).
* CSV export includes translations, so you can move a translated option set between stores. See [Import and export](../option-sets/import-and-export.md).
