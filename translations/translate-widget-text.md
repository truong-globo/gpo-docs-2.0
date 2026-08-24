---
description: Reword every message the app itself shows shoppers — upload prompts, cart buttons, and all the validation messages.
icon: comments
---

# Translate widget text

Widget text is the text the **app** supplies rather than the text you wrote: `Choose file`, `This field is required`, `Edit Options`. It is set once for the store and applies to every option set.

Two reasons to come here: translating for another storefront language, and simply rewording something in your own language.

## Where it is

**Settings** in the app menu, then the **Translations** tab.

<!-- SCREENSHOT: trans-widget-text | App admin → Settings → Translations | 4 nhóm text với các field, nút Add language | Khoanh nút Add language -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Translations page with its four groups of widget text and the add language control"><figcaption><p>Four groups, and one set of values per language.</p></figcaption></figure>

## The four groups

<table><thead><tr><th width="290">Group</th><th>Covers</th></tr></thead><tbody><tr><td><strong>Widget</strong></td><td>File upload prompts, the add-on message, quantity and search prompts</td></tr><tr><td><strong>Cart widget</strong></td><td>The cart-page controls: <strong>Edit Options</strong>, <strong>Cancel</strong>, <strong>Save Changes</strong>, <strong>Preview Your Design</strong>, <strong>Your Design</strong></td></tr><tr><td><strong>Add to cart error messages</strong></td><td>Two messages about items becoming unavailable or a checkout method not being usable</td></tr><tr><td><strong>Validation error messages</strong></td><td>Every message a shopper sees when their entry does not pass a rule — about twenty of them</td></tr></tbody></table>

## Adding a language

{% stepper %}
{% step %}
### Select Add language

The list offers your storefront languages.
{% endstep %}

{% step %}
### Choose the language

It is added as a tab alongside **Default**.
{% endstep %}

{% step %}
### Fill in the values

Work through the four groups. Anything left blank falls back to the default.
{% endstep %}

{% step %}
### Save

Then test on the storefront in that language by triggering a validation error deliberately — leave a required field empty and try to add to cart.
{% endstep %}
{% endstepper %}

**Remove language** removes a language's set of values. The default set cannot be removed.

## Variables

Several messages contain `{{ }}` placeholders that the app fills in from your option settings. Keep them in your translation or the message loses its number.

<table><thead><tr><th width="290">Variable</th><th>Filled with</th></tr></thead><tbody><tr><td><code>{{addon}}</code></td><td>The add-on amount</td></tr><tr><td><code>{{min_character}}</code> / <code>{{character_limit}}</code></td><td>Your min and max character settings</td></tr><tr><td><code>{{character_count}}</code></td><td>How many characters the shopper has typed</td></tr><tr><td><code>{{min_value}}</code> / <code>{{max_value}}</code></td><td>Your min and max value settings</td></tr><tr><td><code>{{min_selection}}</code> / <code>{{max_selection}}</code> / <code>{{exactly_selection}}</code></td><td>Your selection limits</td></tr><tr><td><code>{{min_files}}</code> / <code>{{max_files}}</code></td><td>Your file count limits</td></tr></tbody></table>

The app has a reference of these built in, so you can check them without leaving the page.

{% hint style="warning" %}
A message with its variable removed still displays — it just says "Please enter less than or equal to characters", which is worse than the original. If you shorten a message, keep the variable.
{% endhint %}

## Worth rewording even in English

The defaults are correct but neutral. A few changes make a noticeable difference:

<table><thead><tr><th width="290">Default</th><th>Better</th></tr></thead><tbody><tr><td><code>This field is required</code></td><td><code>Please fill this in before adding to your bag</code></td></tr><tr><td><code>Please enter less than or equal to {{character_limit}} characters</code></td><td><code>That is too long — up to {{character_limit}} characters fit</code></td></tr><tr><td><code>File not allowed</code></td><td><code>We can only accept JPG and PNG files</code></td></tr><tr><td><code>Please select at least {{min_selection}} options</code></td><td><code>Choose at least {{min_selection}} to continue</code></td></tr><tr><td><code>Choose file</code></td><td><code>Upload your photo</code></td></tr></tbody></table>

Error messages are read at the moment a shopper is frustrated. Wording them like a person rather than a form is one of the cheapest improvements available.

## Notes

* These settings are store-wide. There is no per-option-set override.
* Anything blank in a language falls back to the default set, so a partial translation still works.
* This is separate from [option content](translate-option-content.md), which is your own labels and values, and from the [app admin language](app-admin-language.md), which is what you see.
* The full list of validation messages and what triggers each is in [Validation messages](translate-widget-text.md).
