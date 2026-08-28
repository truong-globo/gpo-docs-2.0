---
description: >-
  The three ways to choose which products an option set appears on, and how
  automatic rules and their operators work.
icon: bullseye
---

# Assign to products

Every option set needs a product rule. This tells the app which products the options should appear on, and the builder won't let you save an option set without one.

You can choose from three methods. They are **mutually exclusive**, so enabling one automatically disables the other two.

## Before you start

Make sure you have an option set open in the builder and are on **Setup flow** > **Assign products**.

## The three methods

<table><thead><tr><th width="210">Method</th><th>How it decides</th><th>Best for</th></tr></thead><tbody><tr><td><strong>Manual Selection</strong></td><td>You pick products by hand.</td><td>A short, stable list. Options for one flagship product.</td></tr><tr><td><strong>Automatic Rules</strong></td><td>Conditions on product title, type, vendor, price, tag, or collection.</td><td>Best for rules that should continue to apply as you add new products. This is the most common choice.</td></tr><tr><td><strong>Apply to All Products</strong></td><td>Every product in the store.</td><td>Store-wide options such as a delivery note or gift message.</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/2026-08-28_13-59-36.png" alt="The Assign products step showing the Manual Selection, Automatic Rules, and Apply to All Products blocks"><figcaption><p>Three targeting methods; switching one on switches the others off.</p></figcaption></figure>

## Manual Selection

{% stepper %}
{% step %}
### Turn on Manual Selection

The section expands to show a product table and a **Select products** button.
{% endstep %}

{% step %}
### Select products

Click **Select products** to open Shopify's product picker. Search your catalogue and select multiple products at once.

You can also select individual variants.
{% endstep %}

{% step %}
### Review the list

Selected products appear in a table showing each product's image, title, vendor, type, and Shopify status (**Active** or **Draft**).

To remove a product, click the Remove action on its row. To clear the entire list, click **Deselect all products**. You'll be asked to confirm before clearing the list because this action cannot be undone.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
A manual rule with no products selected is incomplete. The builder displays **“Please select product to apply this option set.”** and prevents you from clicking **Save**.
{% endhint %}

Manual selection has one important limitation: it does not automatically update as your catalogue changes. If you add a new engravable bracelet next month, you'll need to come back and add it manually. If you expect to add products regularly, an automatic rule is a better choice.

<figure><img src="../.gitbook/assets/2026-08-28_14-02-56.png" alt="The manual selection product table with selected products and the select and deselect controls"><figcaption><p>Manually selected products are listed with their Shopify status.</p></figcaption></figure>

## Automatic Rules

Automatic rules describe the products rather than list them. Any product matching the description picks the option set up, now and in future.

{% stepper %}
{% step %}
### Turn on Automatic Rules

The block expands with one empty condition, and a **Products must match** selector above it.
{% endstep %}

{% step %}
### Choose all conditions or any condition

<table><thead><tr><th width="230">Setting</th><th>Meaning</th></tr></thead><tbody><tr><td><strong>all conditions</strong></td><td>A product must satisfy <strong>every</strong> condition. Conditions narrow the match.</td></tr><tr><td><strong>any condition</strong></td><td>A product needs to satisfy <strong>at least one</strong>. Conditions widen the match.</td></tr></tbody></table>

With one condition the setting makes no difference. It matters as soon as you add a second.
{% endstep %}

{% step %}
### Build a condition

A condition is three parts: a product field, an operator, and a value.

<table><thead><tr><th width="200">Field</th><th>Matches against</th></tr></thead><tbody><tr><td><strong>Product title</strong></td><td>The product's title in Shopify.</td></tr><tr><td><strong>Product type</strong></td><td>The product's <strong>Type</strong> that set up in Shopify.</td></tr><tr><td><strong>Product vendor</strong></td><td>The product's <strong>Vendor</strong> that set up in Shopify.</td></tr><tr><td><strong>Product price</strong></td><td>The product's price.</td></tr><tr><td><strong>Product tag</strong></td><td>The product's tag that set up in Shopify</td></tr><tr><td><strong>Collection</strong></td><td>The products that are included in the collection.</td></tr></tbody></table>

The available operators depend on the field:

<table><thead><tr><th width="240">Field</th><th>Operators</th></tr></thead><tbody><tr><td>Product title, Product type, Product vendor</td><td>is equal to, is not equal to, starts with, ends with, contains, does not contain</td></tr><tr><td>Product price</td><td>is equal to, is not equal to, is greater than, is less than</td></tr><tr><td>Product tag, Collection</td><td>is equal to, is not equal to</td></tr></tbody></table>

For **Collection**, the value is chosen with a collection picker rather than typed.

{% hint style="info" %}
Changing a condition's field resets its operator and value. That is intentional — the operators differ per field — but it means you should pick the field first, then the operator, then the value.
{% endhint %}
{% endstep %}

{% step %}
### Add more conditions if you need them

**Add another condition** appends a row. Remove a row with its delete action.

Combine conditions with the **all** / **any** setting above.
{% endstep %}

{% step %}
### Check what it matches

Use **Preview matching products** to list the products your conditions currently catch, before you save. See [Live preview and inspector](live-preview-and-inspector.md).

This preview is unavailable when any condition uses **Collection** — verify those by opening a product from that collection with **View in Store**.
{% endstep %}
{% endstepper %}

<figure><img src="../.gitbook/assets/placeholder.png" alt="Automatic rules with two conditions and the all conditions match setting"><figcaption><p>Conditions combine with all or any, and the operators change with the field.</p></figcaption></figure>

<details>

<summary>Worked examples of automatic rules</summary>

<table><thead><tr><th width="300">You want</th><th>Set up</th></tr></thead><tbody><tr><td>Every product tagged <code>engravable</code></td><td>Product tag — is equal to — <code>engravable</code></td></tr><tr><td>Everything in the Wedding collection</td><td>Collection — is equal to — pick <em>Wedding</em></td></tr><tr><td>All t-shirts from one brand</td><td><strong>all conditions</strong>; Product type — is equal to — <code>T-Shirt</code>; Product vendor — is equal to — the brand name</td></tr><tr><td>Anything over $100, for insurance options</td><td>Product price — is greater than — <code>100</code></td></tr><tr><td>Anything tagged <code>custom</code> or <code>bespoke</code></td><td><strong>any condition</strong>; Product tag — is equal to — <code>custom</code>; Product tag — is equal to — <code>bespoke</code></td></tr><tr><td>Personalised products, except sale items</td><td><strong>all conditions</strong>; Product tag — is equal to — <code>personalised</code>; Product tag — is not equal to — <code>sale</code></td></tr><tr><td>Everything whose title mentions "Gift"</td><td>Product title — contains — <code>Gift</code></td></tr></tbody></table>

</details>

{% hint style="success" %}
**Tags are the most reliable lever.** You control them entirely, they bulk-edit quickly in Shopify, and they read clearly in a rule. Consider a dedicated tag per option set, such as `opt-engraving`.
{% endhint %}

Three things to know about matching:

* **Text matching is exact on characters.** `T-Shirt` and `T-shirt` are different values for **is equal to** — use **contains** when unsure of the casing.
* **Price conditions test the variant price.** On a product whose variants differ in price, the rule matches if any variant price satisfies it.
* **A product must be saved** in Shopify before a rule can see its tags or type.

## Apply to All Products

One switch. Every product in the store gets this option set — including products you add later.

Use it deliberately. It is right for a delivery note or a gift message, and wrong for anything product-specific, because it will also appear on gift cards, digital downloads, and add-on products.

{% hint style="info" %}
If you want "almost all products", use **Automatic Rules** with a **Product tag — is not equal to** condition and tag the exceptions. That gives you a store-wide default with an escape hatch.
{% endhint %}

## Notes

* Current plans place no limit on how many products an option set may target. On a plan that does limit it, the manual selection block warns you when you reach the ceiling.
* **Automatic Rules** and **Apply to All Products** are plan-gated on some plans. If a switch is unavailable, see [Compare plans](../plans/compare-plans.md).
* Product rules are evaluated on the storefront each time a page loads, so a tag change takes effect on the next page load.
* Draft products in Shopify can still match a rule. You will see the option set when previewing the draft product.
