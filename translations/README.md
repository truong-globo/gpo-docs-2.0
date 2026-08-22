---
description: The three separate layers of language in the app, and which one you need.
icon: language
---

# Overview

Language in this app means three different things, and confusing them is the most common source of "I translated it but nothing changed".

## The three layers

<table><thead><tr><th width="230">Layer</th><th width="290">What it covers</th><th>Where you change it</th></tr></thead><tbody><tr><td><strong>The app's own interface</strong></td><td>The admin you are looking at — menus, buttons, setting names</td><td>The language control on the <strong>Dashboard</strong>. See <a href="app-admin-language.md">App admin language</a></td></tr><tr><td><strong>Your option content</strong></td><td>Labels, option values, help text, placeholders — the words you wrote</td><td>The language switcher in the <strong>builder</strong>. See <a href="translate-option-content.md">Translate option content</a></td></tr><tr><td><strong>The widget's fixed text</strong></td><td>Text the app supplies — <code>Choose file</code>, <code>This field is required</code>, and every other message</td><td><strong>Settings &gt; Translations</strong>. See <a href="translate-widget-text.md">Translate widget text</a></td></tr></tbody></table>

{% hint style="info" %}
Changing the **app admin language** does nothing to your storefront. It changes the language *you* work in. The two storefront layers are separate from it and from each other.
{% endhint %}

## Which one do you need?

<table><thead><tr><th width="330">You want</th><th>Go to</th></tr></thead><tbody><tr><td>To work in the app in your own language</td><td><a href="app-admin-language.md">App admin language</a></td></tr><tr><td>Your option labels and choices in your customers' languages</td><td><a href="translate-option-content.md">Translate option content</a></td></tr><tr><td>Error messages and upload prompts translated</td><td><a href="translate-widget-text.md">Translate widget text</a></td></tr><tr><td>To change the wording of an error message, in one language</td><td><a href="translate-widget-text.md">Translate widget text</a></td></tr><tr><td>Right-to-left layout, or non-Latin scripts</td><td><a href="rtl-and-non-latin.md">Right-to-left and non-Latin text</a></td></tr></tbody></table>

## A complete multi-language setup

For a storefront in more than one language, all three layers need attention:

{% stepper %}
{% step %}
### Set the app admin language to yours

So you are comfortable while you work.
{% endstep %}

{% step %}
### Translate the widget's fixed text, per storefront language

**Settings** > **Translations**. Do this once for the store — it covers every option set.
{% endstep %}

{% step %}
### Translate your option content, per option set

In the builder, using the language switcher. This is the per-option-set work.
{% endstep %}

{% step %}
### Check anything that is deliberately not translated

Option **Name** fields stay in one language by design, and so do prefix and suffix text. See below.
{% endstep %}

{% step %}
### Test each storefront

Switch language on your storefront and work through a product page in each one.
{% endstep %}
{% endstepper %}

## What is never translated

<table><thead><tr><th width="290">Not translatable</th><th>Why</th></tr></thead><tbody><tr><td>Option <strong>Name</strong></td><td>It appears on your orders. Keeping it in one language means your team reads one consistent name whatever language the shopper used. See <a href="../option-types/shared-settings/labels-and-visibility.md">Label and Name</a></td></tr><tr><td>Prefix and suffix text</td><td>Units and symbols. For units that differ by market, use separate option sets with <a href="../option-sets/assign-to-countries.md">country rules</a></td></tr><tr><td>Option set names</td><td>Internal only</td></tr><tr><td>Add-on product titles</td><td>They are Shopify products — translate them with Shopify's own tools</td></tr></tbody></table>

## Notes

* Translating option content is plan-gated. See [Compare plans](../plans/compare-plans.md).
* The languages available for translation are your **storefront** languages, as configured in Shopify.
* The date picker's calendar has its own language setting, separate from all of this. See [Date and time picker](../option-types/input-types/date-and-time-picker.md).
