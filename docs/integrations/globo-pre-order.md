---
description: Using product options on pre-order products.
icon: clock
---

# Globo Pre-order

A pre-order app changes what the add-to-cart button does. Instead of a normal purchase, it takes an order for a product that is not yet available. Product options and pre-orders both work through the same button, so they have to work together.

## What to expect

These two features are often used together. A made-to-order product can also be on pre-order. The options are collected as usual and are stored in the pre-order like any other order.

Because both work through the product form, whether they work together without changes depends on your theme and on the pre-order app.

## What to test

Test the full flow on a real pre-order product before you use it.

<table><thead><tr><th width="290">Test</th><th>What you are checking</th></tr></thead><tbody><tr><td>Options appear on the pre-order product page</td><td>The widget is not being displaced by the pre-order interface</td></tr><tr><td>Required options block the pre-order button</td><td>Validation is hooking into the right button</td></tr><tr><td>Add-ons are added and priced correctly</td><td>Add-on lines survive the pre-order flow</td></tr><tr><td>The option details appear on the resulting order</td><td>The choices reached the order record</td></tr><tr><td>The same on mobile</td><td>Sticky bars and mobile buttons are frequent culprits</td></tr></tbody></table>

{% hint style="warning" %}
Check the second item carefully. If required options do not block the pre-order button, you can take pre-orders with the personalization details missing, and you will not find out until you produce them.
{% endhint %}

## If something does not work

This is integration work rather than a setting. Contact support with the following:

* your theme name
* the pre-order app you use
* a link to a pre-order product page
* what you expected, and what happened instead

See [Contact support](../help/contact-support.md).

## Practical advice

<table><thead><tr><th width="290">Do</th><th>Why</th></tr></thead><tbody><tr><td>Say the lead time in the option's help text</td><td>A customer ordering a personalized pre-order needs to know both waits</td></tr><tr><td>Use an <a href="../automations/update-order-tags.md">order tag</a> for pre-orders with options</td><td>So you can find them when stock arrives and production starts</td></tr><tr><td>Consider a proofing step for long lead times</td><td>A design approved four weeks ago may need re-confirming</td></tr></tbody></table>
