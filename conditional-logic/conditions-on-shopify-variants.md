---
description: >-
  Show or hide options based on the Shopify variant the customer selected — how to
  set it up, and what to check when it does not work.
icon: shuffle
---

# Conditions based on Shopify variants

Conditional logic normally reads the app's own options. It can also read the **Shopify variant** the customer selected on the product page, such as the size, color, or material defined on the product itself.

For example:

* Show engraving options only on the metal version of a product.
* Show shoe width options only for wide-fit sizes.
* Show a warning only on the extra-large frame.

## What this is for

Product variants and app options are two separate systems. Variants belong to Shopify and have their own prices and inventory. Options are added by the app on top of the product.

A variant condition connects the two.

<table><thead><tr><th width="330">You want</th><th>Because</th></tr></thead><tbody><tr><td>Engraving only on the metal version</td><td>You cannot engrave the fabric one</td></tr><tr><td>A shoe width choice only on wide-fit sizes</td><td>It is meaningless on the others</td></tr><tr><td>A longer lead-time note only on the largest size</td><td>Only that one is made to order</td></tr><tr><td>A different set of colours per material</td><td>Your palettes differ by material</td></tr><tr><td>A warning only on one variant</td><td>It has a limitation the others do not</td></tr></tbody></table>

## Before you start

* This requires the **advanced** level of conditional logic. On other plans you can select **Shopify variant** as a source, but the operator and value fields are locked. See [Compare plans](../plans/compare-plans.md).
* Know the exact variant name as it appears on your product in Shopify admin.
* You have a product page to test on. The builder's preview cannot evaluate variant conditions, because no variant is selected there.

## Steps

{% stepper %}
{% step %}
### Find the exact variant name in Shopify

Open the product in Shopify admin and note the variant name **exactly**, including capitalization, spacing, and punctuation. When a product has one variant dimension, the name is that value, for example `Silver`, `Large`, or `Oak`.
{% endstep %}

{% step %}
### On the option you want to show or hide, turn on Conditional logic and pick Shopify variant

The rule goes on the option whose visibility you are controlling. **Shopify variant** is the first entry in the source dropdown, above your own options.
{% endstep %}

{% step %}
### Choose an operator and type the variant name

Variant conditions use the text operators: **is equal to**, **is not equal to**, **starts with**, **ends with**, **contains**, **does not contain**, plus the character-count ones. Use **is equal to** for one specific variant, **contains** when the name has several parts and you only care about one.

The value is a text field rather than a dropdown, because the app cannot know which products the option set will be applied to.

{% hint style="warning" %}
Type it exactly as Shopify shows it. `Large` and `large` are different, and `Silver ` with a trailing space will not match.
{% endhint %}

The field displays your current storefront language as a suffix. This matters if your store is translated. See [Translated variant names](#translated-variant-names) below.
{% endstep %}

{% step %}
### Test on a real product page

Select **View in Store**, then switch between variants and check that the option is displayed and hidden as expected.

**This step is required.** The builder preview cannot test variant conditions, because no variant is selected there.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: clo-variant-condition | App admin → builder → rule builder | Điều kiện với source "Shopify variant", operator "is equal to", value "Silver", ô value có suffix hiển thị locale | Khoanh dòng điều kiện, mũi tên nhỏ vào suffix locale -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A condition using Shopify variant as its source with a typed variant name"><figcaption><p>The variant name is typed, not picked — and the field shows which language you are typing it in.</p></figcaption></figure>

## Products with several variant dimensions

A product with both Size and Color has variant names that combine both values, usually in the form `Large / Silver`.

<table><thead><tr><th width="290">You want</th><th>Condition</th></tr></thead><tbody><tr><td>Only the Large Silver variant</td><td><strong>is equal to</strong> — <code>Large / Silver</code></td></tr><tr><td>Every Silver variant, whatever the size</td><td><strong>contains</strong> — <code>Silver</code></td></tr><tr><td>Every Large variant, whatever the color</td><td><strong>contains</strong> — <code>Large</code></td></tr><tr><td>Everything except Silver</td><td><strong>does not contain</strong> — <code>Silver</code></td></tr><tr><td>Variants whose name begins with Large</td><td><strong>starts with</strong> — <code>Large</code></td></tr></tbody></table>

{% hint style="info" %}
Use **contains** on a product with several variant dimensions. It avoids writing one condition per combination, and it continues to work when you add a new size.

Check for values that appear inside other values. **contains** `Large` also matches `Extra Large`. Use **is equal to** or a more specific value in that case.
{% endhint %}

## Translated variant names

Variant names are text, so they are translated. A customer on your French storefront sees the French variant name, and the condition needs the French text to match it. This is why the value field displays your current storefront language as a suffix.

The condition stores **one value per language**, so:

1. Type the variant name in your primary storefront language.
2. Switch language with the control in the builder header, and re-enter the same variant name in that language.
3. Repeat for every storefront language, then test on each storefront.

See [Translate option content](../translations/translate-option-content.md).

<details>
<summary>Why this depends on your theme</summary>

Reading the selected variant requires the app to read your theme's variant picker, and themes build these differently. The app supports a wide range of themes.

On a theme the app cannot read, the condition never matches. The option is then always displayed or never displayed, depending on the action you selected.

{% hint style="info" %}
When you add a variant condition and your plan does not include advanced conditional logic, the app displays a link to contact support about integrating the feature with your theme. If a variant condition does not work on your theme, use that link. See [Contact support](../help/contact-support.md).
{% endhint %}

</details>

## Variant condition or a separate option set?

In some cases a separate option set is a better solution than a condition.

<table><thead><tr><th width="290">Situation</th><th>Better approach</th></tr></thead><tbody><tr><td>One or two options differ by variant</td><td>Variant conditions</td></tr><tr><td>Almost the whole form differs by variant</td><td>Two option sets, targeted at different products by tag — see <a href="../option-sets/assign-to-products.md">Assign to products</a></td></tr><tr><td>The variant is really a product option, not a variant</td><td>Move it into the app as a real option, and free up the Shopify variant</td></tr><tr><td>You are past Shopify's variant limit</td><td>That is what this app is for — replace variants with options</td></tr></tbody></table>

## Notes
* Requires the advanced level of conditional logic.
* The value is typed, not selected. The app cannot list the variants of a product the option set has not been applied to yet.
* Matching is exact and language-specific.
* The builder preview cannot evaluate variant conditions. Always test with **View in Store**.
* If you rename a variant in Shopify, every condition referencing it stops matching. Check your option sets after renaming a variant.
* One condition reads one variant name. For several variants, add several conditions with **Any** matching, or use **contains** with a part of the name they share.
