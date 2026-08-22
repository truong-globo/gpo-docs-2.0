---
description: >-
  Show or hide options based on the Shopify variant the customer selected — how to
  set it up, and what to check when it does not work.
icon: shuffle
---

# Conditions based on Shopify variants

Conditional logic normally reacts to the app's own options. It can also react to the **Shopify variant** the customer selected on the product page — the size, colour, or material that is part of the product itself rather than part of your option set.

That makes it possible to say things like: offer engraving only on the metal version, ask for a shoe width only for wide-fit sizes, show a warning only on the extra-large frame.

## What this is for

Your product's variants and your app options are two different systems. Variants are Shopify's, with their own prices and inventory; options are the app's, layered on top.

A variant condition is the bridge between them.

<table><thead><tr><th width="330">You want</th><th>Because</th></tr></thead><tbody><tr><td>Engraving only on the metal version</td><td>You cannot engrave the fabric one</td></tr><tr><td>A shoe width choice only on wide-fit sizes</td><td>It is meaningless on the others</td></tr><tr><td>A longer lead-time note only on the largest size</td><td>Only that one is made to order</td></tr><tr><td>A different set of colours per material</td><td>Your palettes differ by material</td></tr><tr><td>A warning only on one variant</td><td>It has a limitation the others do not</td></tr></tbody></table>

## Before you start

* This requires the **Advanced** level of conditional logic. On other plans you can select **Shopify variant** as a source but the operator and value fields are locked with an upgrade prompt. See [Compare plans](../plans/compare-plans.md).
* Know the exact variant name as it appears on your product in Shopify admin.
* Have a real product page to test on. The builder's preview cannot evaluate variant conditions, because no variant is selected there.

## Steps

{% stepper %}
{% step %}
### Find the exact variant name in Shopify

Open the product in Shopify admin and look at its variants. Note the name **exactly** — capitalisation, spacing, and punctuation all matter.

For a product with one variant dimension, the name is that value: `Silver`, `Large`, `Oak`.
{% endstep %}

{% step %}
### Select the option that should appear or disappear

The rule goes on the option whose visibility you are controlling.
{% endstep %}

{% step %}
### Turn on Conditional logic and choose Shopify variant

**Shopify variant** is the first entry in the source dropdown, above your own options.
{% endstep %}

{% step %}
### Choose an operator

Variant conditions use the text operator set: **is equal to**, **is not equal to**, **starts with**, **ends with**, **contains**, **does not contain**, plus the character-count operators.

**is equal to** for one specific variant. **contains** when the variant name has several parts and you only care about one of them.
{% endstep %}

{% step %}
### Type the variant name

The value is a text field, not a dropdown — the app cannot know which product the option set will be applied to, so it cannot offer a list.

{% hint style="warning" %}
Type it exactly as it appears in Shopify. `Large` and `large` are different; `Silver ` with a trailing space will not match.
{% endhint %}

Notice the field shows your current storefront language as a suffix. That matters — see [Translated variant names](#translated-variant-names) below.
{% endstep %}

{% step %}
### Test on a real product page

Use **View in Store**, then switch between variants and check the option appears and disappears as intended.

This step is not optional. The builder preview cannot test variant conditions.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: clo-variant-condition | App admin → builder → rule builder | Điều kiện với source "Shopify variant", operator "is equal to", value "Silver", ô value có suffix hiển thị locale | Khoanh dòng điều kiện, mũi tên nhỏ vào suffix locale -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A condition using Shopify variant as its source with a typed variant name"><figcaption><p>The variant name is typed, not picked — and the field shows which language you are typing it in.</p></figcaption></figure>

## Products with several variant dimensions

A product with both Size and Colour has variants whose names combine both — typically as `Large / Silver`.

<table><thead><tr><th width="290">You want</th><th>Condition</th></tr></thead><tbody><tr><td>Only the Large Silver variant</td><td><strong>is equal to</strong> — <code>Large / Silver</code></td></tr><tr><td>Every Silver variant, whatever the size</td><td><strong>contains</strong> — <code>Silver</code></td></tr><tr><td>Every Large variant, whatever the colour</td><td><strong>contains</strong> — <code>Large</code></td></tr><tr><td>Everything except Silver</td><td><strong>does not contain</strong> — <code>Silver</code></td></tr><tr><td>Variants whose name begins with Large</td><td><strong>starts with</strong> — <code>Large</code></td></tr></tbody></table>

{% hint style="info" %}
**contains** is usually the right operator on a multi-dimension product. It saves writing one condition per combination, and it keeps working when you add a new size.

Be careful with values that appear inside other values, though. **contains** `Large` also matches `Extra Large`. Use **is equal to** or a more specific value when that matters.
{% endhint %}

## Translated variant names

The value field shows your current storefront language as a suffix, because variant names are text and text gets translated.

If your storefront has more than one language, the shopper on your French storefront sees the French variant name, and your condition needs the French text to match it.

{% stepper %}
{% step %}
### Enter the value in your primary language first

Type the variant name as it appears in your main storefront language.
{% endstep %}

{% step %}
### Switch language with the builder's language switcher

Use the language control in the builder header.
{% endstep %}

{% step %}
### Re-enter the variant name in that language

The condition stores a value per language, so each one needs the matching translated variant name.
{% endstep %}

{% step %}
### Repeat for every storefront language

And test on each storefront.
{% endstep %}
{% endstepper %}

See [Translate option content](../translations/translate-option-content.md).

## Why this depends on your theme

Reading the selected variant means listening to your theme's own variant picker, and themes build those very differently. The app handles this on a wide range of themes.

On a theme it cannot read, the condition never matches — the option either always shows or never shows, depending on your action.

{% hint style="info" %}
The app knows this is theme-dependent. When you add a variant condition and your plan does not include advanced conditional logic, it offers a direct link to contact support about integrating the feature with your theme. If a variant condition does not work on your theme, that is the right route — it is usually a small piece of integration work. See [Contact support](../help/contact-support.md).
{% endhint %}

## Variant condition or a separate option set?

Sometimes the better answer is not a condition at all.

<table><thead><tr><th width="290">Situation</th><th>Better approach</th></tr></thead><tbody><tr><td>One or two options differ by variant</td><td>Variant conditions</td></tr><tr><td>Almost the whole form differs by variant</td><td>Two option sets, targeted at different products by tag — see <a href="../option-sets/assign-to-products.md">Assign to products</a></td></tr><tr><td>The variant is really a product option, not a variant</td><td>Move it into the app as a real option, and free up the Shopify variant</td></tr><tr><td>You are past Shopify's variant limit</td><td>That is what this app is for — replace variants with options</td></tr></tbody></table>

## Limits and notes

* Requires the Advanced level of conditional logic.
* The value is typed, not selected — the app has no way to list variants of a product it has not been applied to yet.
* Matching is exact on characters, and language-specific.
* The builder preview cannot evaluate variant conditions. Always test with **View in Store**.
* If you rename a variant in Shopify, every condition referring to it stops matching. Search your option sets after renaming variants.
* One condition reads one variant name. For several variants, add several conditions with **Any** matching, or use **contains** with a shared part of the name.

## Troubleshooting

<details>
<summary>The condition never matches</summary>

Work through these in order:

1. Is the variant name typed exactly as in Shopify admin, including capitalisation and spacing?
2. On a multi-dimension product, is the full name `Size / Colour` rather than just one part? Use **contains** if you only want one part.
3. Are you testing on a real product page rather than the builder preview?
4. Does your plan include advanced conditional logic?
5. Does your storefront language match the language you typed the value in?

If all five are right, it is likely theme integration — contact support.
</details>

<details>
<summary>It works in the builder but not on the storefront</summary>

It cannot have worked in the builder — the preview has no variant selected, so variant conditions do not evaluate there. Test only on a real product page.
</details>

<details>
<summary>The operator and value fields are locked</summary>

Variant conditions need advanced conditional logic. See [Compare plans](../plans/compare-plans.md).
</details>

<details>
<summary>It works on my English storefront but not the French one</summary>

The variant name is translated, and the condition stores a value per language. Switch language in the builder and enter the French variant name too.
</details>

<details>
<summary>It matches more variants than I expected</summary>

**contains** is matching a substring — `Large` also matches `Extra Large`. Use **is equal to** with the full name, or pick a more distinctive value.
</details>

<details>
<summary>It stopped working after I edited my product</summary>

A renamed variant breaks every condition referring to it. Update the conditions to the new name.
</details>
