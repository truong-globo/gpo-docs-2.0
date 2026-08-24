---
description: >-
  An option the customer never sees, which attaches a fixed value to every order
  it applies to.
icon: eye-slash
---

# Hidden field

An option that renders nothing on the product page but still sends a value through to the cart and the order.

Use it to stamp orders with information your team needs and the customer does not: which production line, which supplier, which campaign, which template version.

## What customers see

Nothing. There is no label, no field, and no indication that the option exists.

## Basic Settings

Hidden field has the shortest settings list in the app, because most settings describe an appearance it does not have.

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a></td><td>Your own reference in the builder. Never shown to anybody.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>The name that appears on the cart and order. This is the one that matters.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#default-value">Default value</a></td><td>The value sent with the order. This is the whole point of the type.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Send the value only when other conditions are met.</td></tr></tbody></table>

There is no Required field, no placeholder, no help text, no prefix, no column width, and no HTML class — none of them would do anything.

{% hint style="info" %}
**Name** and **Default value** are the two settings to get right. The Name is the label your team reads on the order; the Default value is what it says. `Production line: Line B` is useful; `hidden: 1` is not.
{% endhint %}

## Where the value ends up

Exactly where every other option's value goes: attached to the cart line, and from there onto the cart page, the checkout, the order in your admin, and order emails, invoices, and packing slips.

That means a hidden field is visible to the customer once the item is in their cart, even though it was invisible on the product page. It is hidden from the *form*, not from the *order*.

{% hint style="warning" %}
Do not put anything confidential in a hidden field — cost prices, supplier names, internal margins. The customer can see it on their own cart page and order confirmation.
{% endhint %}

## Add-on pricing and Personalizer

Neither is supported. A hidden field cannot carry a price and cannot appear in the live preview.

## Examples

**Route orders to the right workshop**

<table><thead><tr><th width="270">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label</td><td><code>Workshop routing</code></td></tr><tr><td>Name</td><td><code>Workshop</code></td></tr><tr><td>Default value</td><td><code>Engraving bench</code></td></tr></tbody></table>

Applied to your engravable products, every such order now says which bench it belongs to.

**Mark which option set produced the order**

Name `Option set`, default value `Bracelet personalization v2`. Handy when you run several versions and want to know which one a customer used.

**Flag a conditional path that is otherwise invisible**

A hidden field with a conditional rule — for example Name `Rush`, value `Yes`, shown only when the customer picked express production. The order then carries a plain flag rather than requiring your team to infer it from the other options.

**Stamp a campaign**

Name `Campaign`, value `Spring gifting`, on an option set targeted at a tagged group of products, so orders can be counted later.

## Notes
* Available on the Advanced plan.
* Works in Shopify POS.
* The value is fixed by you. There is no way for a customer or a URL parameter to change it.
* One value per hidden field. For several pieces of information, add several hidden fields.
* Because it is invisible, it is easy to forget. Give it a clear **Label** so it reads sensibly in the builder's option list.
* A hidden field with no **Default value** sends nothing and is pointless — always set the value.
