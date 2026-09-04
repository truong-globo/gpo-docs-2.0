---
description: The six store-wide settings that decide how add-on prices are shown to customers on the product page.
icon: eye
---

# Add-on price display settings

The price you set determines what the customer pays. These settings control what the customer **sees** while making selections.

All of them are under **Settings** > **Settings** > **Add-on price**. They are store-wide and apply to every option set.

<!-- SCREENSHOT: addon-price-settings | App admin → Settings → Add-on price | Toàn bộ các setting của tab | Không khoanh -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The add-on price settings tab with all its options"><figcaption><p>All the add-on display settings in one place, applied store-wide.</p></figcaption></figure>

## The settings

<table><thead><tr><th width="290">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Add-on money format</strong></td><td><strong>Without currency</strong></td><td>Whether the amount includes your currency code. <strong>Without currency</strong> gives <code>$5.00</code>; <strong>With currency</strong> gives <code>$5.00 USD</code>.</td></tr><tr><td><strong>Add-on label format</strong></td><td><code>(+ {{addon}})</code></td><td>The wrapper around the amount. <code>{{addon}}</code> is replaced by the price.</td></tr><tr><td><strong>Show add-on for inputs</strong></td><td>On</td><td>Whether input-type options show their add-on — Text, Textarea, Number.</td></tr><tr><td><strong>Show add-on for options</strong></td><td>On</td><td>Whether selection-type options show theirs — Select, Radio, Checkbox, Button, Color swatch, Image swatch.</td></tr><tr><td><strong>Show add-on message</strong></td><td>On</td><td>Whether a summary message appears telling the customer the selections will add to the price.</td></tr><tr><td><strong>Add add-on price to the product price</strong></td><td><strong>On</strong> for new stores</td><td>Whether the product price shown on the page increases as they choose, or the add-on is shown separately.</td></tr><tr><td><strong>Merge Main product &amp; Add-on products</strong></td><td><strong>On</strong> for new stores</td><td>Cart presentation. See <a href="merge-as-bundle.md">Merge main product and add-ons</a>.</td></tr></tbody></table>

## Add-on label format

The format string surrounds the amount. `{{addon}}` is replaced by the price.

<table><thead><tr><th width="290">Format</th><th>Customer sees</th></tr></thead><tbody><tr><td><code>(+ {{addon}})</code></td><td><code>(+ $5.00)</code> — the default</td></tr><tr><td><code>+{{addon}}</code></td><td><code>+$5.00</code> — tighter</td></tr><tr><td><code>{{addon}} extra</code></td><td><code>$5.00 extra</code></td></tr><tr><td><code>Add {{addon}}</code></td><td><code>Add $5.00</code></td></tr><tr><td><code>{{addon}}</code></td><td><code>$5.00</code> — no wrapper at all</td></tr></tbody></table>

Keep the format short. It is displayed beside every priced value, so a long phrase is repeated for each one.

The wording of the **add-on message** is set separately, and can be edited for each storefront language under **Settings > Translations**. See [Translate widget text](../translations/translate-widget-text.md).

## Add add-on price to the product price

This setting controls whether the add-on amount is included in the product price displayed on the page.

<table><thead><tr><th width="230">Off</th><th>On (new stores start here)</th></tr></thead><tbody><tr><td>The product price stays as listed. Each add-on shows its own amount beside the option</td><td>The product price shown updates as the customer chooses</td></tr><tr><td>Customers see the base price and the extras separately</td><td>Customers see one running total</td></tr><tr><td>No surprise about what the product itself costs</td><td>Fewer numbers to add up mentally</td></tr><tr><td>Better when most customers buy without add-ons</td><td>Better when most configurations are paid</td></tr></tbody></table>

{% hint style="warning" %}
When this setting is **on** and an option has a **default value** with a price, the product price is higher than your listed price as soon as the page loads. This is a common cause of customers asking why a product costs more than advertised. Either avoid priced default values, or set the default to a free value. See [Required field and default value](../option-types/shared-settings/required-and-default-value.md#default-value).
{% endhint %}

## Show for inputs and Show for options

Two settings, one for each group of option types:

<table><thead><tr><th width="290">Switch</th><th>Covers</th></tr></thead><tbody><tr><td><strong>Show add-on for inputs</strong></td><td>Text, Textarea, Number — where the price is on the option</td></tr><tr><td><strong>Show add-on for options</strong></td><td>Select, Radio, Checkbox, Button, Color swatch, Image swatch — where the price is on each value</td></tr></tbody></table>

Turning one off does not remove the charge. It only hides the amount on the product page. The customer still pays it and still sees it at checkout.

This is useful in some cases. For example, a per-character engraving charge can be confusing before the customer enters any text. If you turn the display off, state the price in the option's [help text](../option-types/shared-settings/placeholder-and-help-text.md#help-text) so the charge is not unexpected.

## Worked configurations

**A shop where most items are personalized and paid**

<table><thead><tr><th width="330">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Add add-on price to the product price</td><td><strong>On</strong> — one running total</td></tr><tr><td>Show add-on for inputs / options</td><td>On</td></tr><tr><td>Add-on label format</td><td><code>+{{addon}}</code></td></tr><tr><td>Show add-on message</td><td>On</td></tr></tbody></table>

**A shop where add-ons are occasional extras**

Add-on price **not** added to the product price, so the listed price is unchanged. Both display settings on, with the default label format.

**A shop pricing engraving per character**

Show add-on for inputs **off**, with the rate stated in the option's help text, for example `Engraving is $0.50 per character`.

## Notes

* All of these settings are store-wide. They cannot be set per option set.
* They affect display only. The actual charge is applied at checkout. See [How pricing is applied](how-pricing-is-applied.md).
* Amounts use your Shopify money format.
* The add-on message wording, including the "Selections will add {{addon}} to the price" text, is set under **Settings > Translations** for each language.
