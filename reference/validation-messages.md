---
description: >-
  Every message the app can show — to your customers on the storefront, and to you
  in the builder — with what triggers each one.
icon: triangle-exclamation
---

# Validation messages

Two separate sets of messages, with two different jobs.

<table><thead><tr><th width="290">Set</th><th width="200">Seen by</th><th>Changeable</th></tr></thead><tbody><tr><td><strong>Storefront messages</strong></td><td>Your customers</td><td>Yes — reword every one of them in <strong>Translations</strong></td></tr><tr><td><strong>Builder messages</strong></td><td>You, while configuring</td><td>No — they tell you something needs fixing before you can save</td></tr></tbody></table>

## Storefront messages

These appear beside a field when the customer's entry does not pass a rule you set. Every one can be reworded per language — see [Translate widget text](../translations/translate-widget-text.md).

### Something is missing or malformed

<table><thead><tr><th width="330">Default text</th><th>Shown when</th></tr></thead><tbody><tr><td><code>This field is required</code></td><td>A <a href="../option-types/shared-settings/required-and-default-value.md">Required field</a> was left empty</td></tr><tr><td><code>Invalid</code></td><td>An entry does not fit the field's format</td></tr><tr><td><code>Invalid email</code></td><td>An <a href="../option-types/input-types/email.md">Email</a> entry is not a valid address</td></tr><tr><td><code>Invalid phone number</code></td><td>A <a href="../option-types/input-types/phone.md">Phone</a> entry fails validation</td></tr><tr><td><code>Invalid number</code></td><td>A <a href="../option-types/input-types/number.md">Number</a> entry is not a number</td></tr><tr><td><code>File not allowed</code></td><td>An upload the option cannot accept — normally the wrong file type. See <a href="../option-types/input-types/file-upload.md">File upload</a></td></tr></tbody></table>

### Character limits

Text and Textarea only. See [Limits](../option-types/shared-settings/limits.md#min-and-max-character).

<table><thead><tr><th width="330">Default text</th><th>Shown when</th></tr></thead><tbody><tr><td><code>Please enter more than or equal to {{min_character}} characters</code></td><td>The entry is shorter than <strong>Min character</strong></td></tr><tr><td><code>Please enter less than or equal to {{character_limit}} characters</code></td><td>The entry is longer than <strong>Max character</strong></td></tr><tr><td><code>Please enter exactly {{exactly_character}} characters</code></td><td>Min and max are the same number</td></tr><tr><td><code>{{character_count}}/{{character_limit}} characters</code></td><td>Not an error — the running <a href="../option-types/shared-settings/limits.md#character-counter">character counter</a></td></tr></tbody></table>

### Value limits

Number and Range slider. See [Limits](../option-types/shared-settings/limits.md#min-and-max-value).

<table><thead><tr><th width="330">Default text</th><th>Shown when</th></tr></thead><tbody><tr><td><code>Please enter a value greater than or equal to {{min_value}}</code></td><td>Below <strong>Min value</strong></td></tr><tr><td><code>Please enter a value less than or equal to {{max_value}}</code></td><td>Above <strong>Max value</strong></td></tr><tr><td><code>Please enter a value equal to {{exactly_value}}</code></td><td>Min and max are the same number</td></tr></tbody></table>

### Selection limits

Multi-select options. See [Limits](../option-types/shared-settings/limits.md#min-and-max-selections).

<table><thead><tr><th width="330">Default text</th><th>Shown when</th></tr></thead><tbody><tr><td><code>Please select at least {{min_selection}} options</code></td><td>Fewer than <strong>Min selections</strong> chosen</td></tr><tr><td><code>Please select at maximum {{max_selection}} options</code></td><td>More than <strong>Max selections</strong> chosen</td></tr><tr><td><code>Please select exactly {{exactly_selection}} options</code></td><td>Min and max are the same number</td></tr></tbody></table>

### File count limits

File upload only. See [Limits](../option-types/shared-settings/limits.md#min-and-max-number-of-files).

<table><thead><tr><th width="330">Default text</th><th>Shown when</th></tr></thead><tbody><tr><td><code>Please add more than or equal to {{min_files}} files</code></td><td>Fewer than <strong>Min files</strong> uploaded</td></tr><tr><td><code>Please add less than or equal to {{max_files}} files</code></td><td>More than <strong>Max files</strong> uploaded</td></tr><tr><td><code>Please add exactly {{exactly_files}} files</code></td><td>Min and max are the same number</td></tr></tbody></table>

### Add to cart

<table><thead><tr><th width="330">Default text</th><th>Shown when</th></tr></thead><tbody><tr><td><code>Some items are no longer available. Please try again later.</code></td><td>Something in the cart — usually an add-on product — is no longer purchasable. Most often stock, or a product that was unpublished. See <a href="../add-on-pricing/stock-and-inventory.md">Stock and inventory</a></td></tr><tr><td><code>This product cannot be purchased using this checkout method. Please add the item to cart, then proceed to checkout from the cart.</code></td><td>The customer tried an accelerated payment button on a product with options. Those buttons skip the cart, which would skip the options</td></tr><tr><td><code>All {{inventory_quantity}} {{product_title}} are in your cart.</code></td><td>The customer tried to add more than you have in stock. This one is not in the <strong>Translations</strong> page, so it cannot be reworded there</td></tr></tbody></table>

## The variables

`{{ }}` placeholders are filled in from your option settings. Keep them when rewording, or the message loses its number.

<table><thead><tr><th width="290">Variable</th><th>Filled with</th></tr></thead><tbody><tr><td><code>{{min_character}}</code>, <code>{{character_limit}}</code>, <code>{{exactly_character}}</code></td><td>Your character limits</td></tr><tr><td><code>{{character_count}}</code></td><td>How many characters have been typed so far</td></tr><tr><td><code>{{min_value}}</code>, <code>{{max_value}}</code>, <code>{{exactly_value}}</code></td><td>Your value limits</td></tr><tr><td><code>{{min_selection}}</code>, <code>{{max_selection}}</code>, <code>{{exactly_selection}}</code></td><td>Your selection limits</td></tr><tr><td><code>{{min_files}}</code>, <code>{{max_files}}</code>, <code>{{exactly_files}}</code></td><td>Your file count limits</td></tr><tr><td><code>{{addon}}</code></td><td>The add-on amount, in the widget's add-on message</td></tr></tbody></table>

## Two behaviours worth knowing

{% hint style="info" %}
**Hidden options are never validated.** An option hidden by a [conditional rule](../conditional-logic/README.md) is skipped, even when it is required — otherwise a hidden required field would make the product impossible to buy.

**A blocked add to cart looks like a broken button** unless the shopper is taken to the error. **Auto-scroll to first error message** in **Settings** > **Settings** > **General** does that, and is on by default. If it has been turned off, shoppers get no feedback at all.
{% endhint %}

## Builder messages

These appear while you are configuring, and stop you saving something that would not work. `:field` is replaced with the name of the setting.

### On an option

<table><thead><tr><th width="330">Message</th><th>Cause and fix</th></tr></thead><tbody><tr><td><code>:field is required.</code></td><td>A setting that cannot be left empty is empty — usually <strong>Label</strong> or <strong>Name</strong></td></tr><tr><td><code>:field must be unique. Please enter a different value.</code></td><td>Two options share a <strong>Name</strong>. Names identify the answer on the order, so they cannot repeat. See <a href="../concepts/label-vs-name.md">Label vs Name</a></td></tr><tr><td><code>:field cannot contain any of the following characters . : " ' \ |</code></td><td>Remove those characters. They would break how the answer is stored on the order</td></tr><tr><td><code>:field cannot be negative.</code></td><td>A price or number below zero. Add-on prices cannot be negative — there is no discount mode</td></tr><tr><td><code>Switch label is required.</code></td><td>A <a href="../option-types/input-types/switch.md">Switch</a> needs its on and off labels filled in</td></tr><tr><td><code>Value must be unique</code></td><td>Two <a href="../concepts/option-values.md">option values</a> share the same value</td></tr></tbody></table>

### On limits

<table><thead><tr><th width="330">Message</th><th>Cause and fix</th></tr></thead><tbody><tr><td><code>The value must be greater than min.</code> / <code>The value must be less than max.</code></td><td>Min and max are the wrong way round</td></tr><tr><td><code>The value must be between min and max.</code></td><td>A value — usually the default — sits outside the range you set</td></tr><tr><td><code>The value must be greater than default value.</code> / <code>The value must be less than default value.</code></td><td>Your min or max would exclude your own default. Change one of them</td></tr><tr><td><code>The value must be between 1 (or min) and the number of option values.</code></td><td>A selection limit is higher than the number of values available. You cannot require five choices from four values</td></tr><tr><td><code>The value must be between 1 and the number of option values (or max).</code></td><td>The same problem from the other side</td></tr><tr><td><code>The value must be between 1 (or min) and 20.</code> / <code>The value must be between 1 and 20 (or max).</code></td><td>A layout setting — such as swatches per row — outside its allowed range</td></tr></tbody></table>

### On add-ons and formulas

<table><thead><tr><th width="330">Message</th><th>Cause and fix</th></tr></thead><tbody><tr><td><code>:field cannot contain subtraction.</code></td><td>A <a href="../add-on-pricing/dimension-formula.md">dimension formula</a> contains <code>-</code>. Use multiplication, addition, and division</td></tr><tr><td><code>Connect this option value to an existing product or variant in your store.</code></td><td>The <strong>Use existing product</strong> tab was left without a product selected. See <a href="../add-on-pricing/use-an-existing-product.md">Use an existing product</a></td></tr><tr><td><code>This variant does not exist on your store anymore. Please select another.</code></td><td>The linked variant was deleted in Shopify. Reopen the price dialog and pick a current one</td></tr></tbody></table>

### On rules and other screens

<table><thead><tr><th width="330">Message</th><th>Cause and fix</th></tr></thead><tbody><tr><td><code>Please select product to apply this option set.</code></td><td>The product rule is set to specific products or collections with nothing chosen. See <a href="../option-sets/assign-to-products.md">Assign to products</a></td></tr><tr><td><code>Please select customer to apply this option set.</code></td><td>The same for the customer rule. See <a href="../option-sets/assign-to-customers.md">Assign to customers</a></td></tr><tr><td><code>This element has reached the maximum number of font options (30).</code></td><td>A <a href="../option-types/selection-types/font-picker.md">Font picker</a> is full. Remove one before adding another</td></tr><tr><td><code>File type must be .woff2, .woff, .ttf or .otf</code></td><td>A custom font upload in the wrong format. See <a href="../settings/custom-fonts.md">Custom fonts</a></td></tr><tr><td><code>Upgrade required</code></td><td>The feature is not in your plan. See <a href="../concepts/plans-and-feature-gating.md">Plans and locked features</a></td></tr><tr><td><code>Export failed</code></td><td>The CSV export did not complete. Try again; if it repeats, tell us which option set</td></tr><tr><td><code>Something went wrong. Please try again.</code></td><td>A general failure. If it repeats on the same action, that is worth reporting with what you were doing</td></tr></tbody></table>

## Notes

* Builder messages are not translatable — they are part of the admin, which follows the admin's own language setting.
* A save is blocked while any message is showing. The builder highlights which option needs attention.
* Storefront messages are per language. A locale with no translation falls back to the default set.
* Two things prevent errors rather than reporting them: the file picker is filtered to the types your option accepts, and a character limit stops the customer typing past it. Shoppers often never see the matching message.
* Almost every storefront message is in the **Translations** page. The stock message above is the exception.

## Next steps

* [Translate widget text](../translations/translate-widget-text.md) — where to reword the storefront messages.
* [Limits](../option-types/shared-settings/limits.md) — the settings these messages come from.
* [Cart and checkout problems](../help/troubleshooting-cart-checkout.md)
