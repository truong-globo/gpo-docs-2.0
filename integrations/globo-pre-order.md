---
description: Using product options on pre-order products.
icon: clock
---

# Globo Pre-order

A pre-order app changes what the add-to-cart button does: instead of a normal purchase it takes an order for something not yet available. Product options and pre-orders both attach themselves to the same button, so they need to cooperate.

## What to expect

Both features are commonly used together — a made-to-order product that is also on pre-order is a perfectly ordinary thing to sell. The options are collected in the usual way and travel with the pre-order like any other order.

Because both work through the product form, whether they cooperate out of the box depends on your theme and on the pre-order app.

## What to test

Test the whole flow on a real pre-order product before you rely on it.

<table><thead><tr><th width="290">Test</th><th>What you are checking</th></tr></thead><tbody><tr><td>Options appear on the pre-order product page</td><td>The widget is not being displaced by the pre-order interface</td></tr><tr><td>Required options block the pre-order button</td><td>Validation is hooking into the right button</td></tr><tr><td>Add-ons are added and priced correctly</td><td>Add-on lines survive the pre-order flow</td></tr><tr><td>The option details appear on the resulting order</td><td>The choices reached the order record</td></tr><tr><td>The same on mobile</td><td>Sticky bars and mobile buttons are frequent culprits</td></tr></tbody></table>

{% hint style="warning" %}
The one that matters is the second: if required options do not block the pre-order button, you can take pre-orders with the personalisation details missing — and you will not find out until you come to produce them.
{% endhint %}

## If something does not work

This is integration work rather than a setting you have missed. Contact support with:

* your theme name
* the pre-order app you use
* a link to a pre-order product page
* what you expected against what happened

See [Contact support](../help/contact-support.md).

## Practical advice

<table><thead><tr><th width="290">Do</th><th>Why</th></tr></thead><tbody><tr><td>Say the lead time in the option's help text</td><td>A customer ordering a personalised pre-order needs to know both waits</td></tr><tr><td>Use an <a href="../automations/update-order-tags.md">order tag</a> for pre-orders with options</td><td>So you can find them when stock arrives and production starts</td></tr><tr><td>Consider a proofing step for long lead times</td><td>A design approved four weeks ago may need re-confirming</td></tr></tbody></table>
