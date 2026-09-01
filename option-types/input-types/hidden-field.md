---
description: >-
  An option that is not displayed on the product page and attaches a fixed value to
  every order it applies to.
icon: eye-slash
---

# Hidden field

An option that is not displayed on the product page but still sends a value to the cart and the order.

Use it to add information your team needs to an order, such as a production line, a supplier, a campaign, or a template version.

## What customers see

Nothing. There is no label, no field, and no indication that the option exists.

## Basic Settings

Hidden field has fewer settings than other option types, because it is not displayed on the product page.

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a></td><td>Your own reference in the builder. Never shown to anybody.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>The name that appears on the cart and order. This is the one that matters.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>The value sent with the order. This is the whole point of the type.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Send the value only when other conditions are met.</td></tr></tbody></table>

It has no Required field, placeholder, help text, prefix, column width, or HTML class.

{% hint style="info" %}
**Name** and **Default value** are the two settings that matter. The Name is what your team reads on the order, and the Default value is the value it records. For example, `Production line: Line B` is useful, while `hidden: 1` is not.
{% endhint %}

## Where the value ends up

The value is attached to the cart line, in the same way as any other option. It appears on the cart page, at checkout, on the order in your admin, and in order emails, invoices, and packing slips.

This means the customer can see the value once the product is in the cart, even though it was not displayed on the product page. The field is hidden from the form, not from the order.

{% hint style="warning" %}
Do not use a hidden field for confidential information such as cost prices, supplier names, or margins. The customer can see the value on the cart page and in the order confirmation.
{% endhint %}

## Add-on pricing and Personalizer

Neither is supported. A hidden field cannot carry a price and is not displayed in the live preview.

## Examples

**Route orders to the right workshop**

<table><thead><tr><th width="270">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label</td><td><code>Workshop routing</code></td></tr><tr><td>Name</td><td><code>Workshop</code></td></tr><tr><td>Default value</td><td><code>Engraving bench</code></td></tr></tbody></table>

Apply the option set to your engravable products. Each order then records the workshop it is assigned to.

**Mark which option set produced the order**

Name `Option set`, default value `Bracelet personalization v2`. Use this when you run several versions and need to know which one a customer used.

**Flag a conditional path that is otherwise invisible**

A hidden field with a conditional rule, for example Name `Rush`, value `Yes`, applied only when the customer selects express production. The order then records the flag directly, so your team does not have to work it out from the other options.

**Stamp a campaign**

Name `Campaign`, value `Spring gifting`, on an option set applied to a tagged group of products, so the orders can be counted later.

## Notes
* Available on the Advanced plan.
* Works in Shopify POS.
* You set the value. It cannot be changed by a customer or by a URL parameter.
* One value per hidden field. For several pieces of information, add several hidden fields.
* The field is not displayed on the product page, so give it a clear **Label** to identify it in the builder's option list.
* A hidden field with no **Default value** sends nothing. Always set a value.
