---
description: Use your option sets when you take an order in person through the Shopify POS app.
icon: cash-register
---

# Overview

The same option sets you built for your storefront can be used at the counter. A staff member adds a product to the POS cart, opens the app, fills in the options, and the cart is updated with the customer's choices and any add-ons.

## What it is for

* Taking a personalised order in a shop or at a market
* Adding a paid extra to an in-person sale
* Recording production details for something made to order
* Keeping in-person and online orders consistent, using one set of options

## Before you rely on it

Three things to check, in order.

{% stepper %}
{% step %}
### Your plan includes POS

Point of Sale is plan-gated. See [Compare plans](../plans/compare-plans.md).
{% endstep %}

{% step %}
### The option set is published to Point of Sale

Each option set has its own **Sales channels** setting. Tick **Point of Sale**. See [Activate and publish](../option-sets/create-an-option-set.md#activate-and-publish).
{% endstep %}

{% step %}
### Your options are POS-compatible

Two option types and one add-on mode do not work in POS. **This is the part that catches people out** — read [POS limitations](limitations.md) before building a POS workflow.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
The short version of the limitations: [Dimension](../option-types/input-types/dimension.md) and [Product links](../option-types/selection-types/product-links.md) do not work in POS, and the [Add price](../add-on-pricing/add-price-directly.md) add-on mode is not supported there. Use a product-backed add-on mode instead.
{% endhint %}

## Pages in this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Set up and use options in POS</strong></td><td>Publishing to POS, adding the app tile, and the counter workflow.</td><td><a href="set-up-and-use.md">set-up-and-use.md</a></td></tr><tr><td><strong>POS limitations</strong></td><td>Everything that does not work, and what to use instead.</td><td><a href="limitations.md">limitations.md</a></td></tr></tbody></table>
