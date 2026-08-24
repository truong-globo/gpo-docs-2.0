---
description: How an option set goes from the builder to a live price change at checkout.
icon: diagram-project
---

# How it works

You do not need this to use the app. It is worth reading once, because it explains four things that otherwise look like faults:

* why the app embed matters
* why the price on the product page is only a preview
* why your option details reach the order with no setup from you
* why a change sometimes needs a refresh before it appears

{% stepper %}
{% step %}
### You build an option set

You add options, set add-on pricing, and choose which products, customers, and countries it applies to. When you save, the app also publishes a copy of it to your Shopify store as store data, so your storefront can read it without waiting on a request to the app.

That publish step is why a change appears within seconds rather than instantly — and why a hard refresh sometimes shows an update a cached page did not.
{% endstep %}

{% step %}
### The theme app embed renders it

Once the [app embed](../getting-started/enable-the-app-embed.md) is enabled on your theme, it checks every page a shopper visits and works out which of your option sets apply. Four things decide that: the product, the customer, their country, and whether the set is active on this sales channel. Matching sets are rendered as the widget.

If nothing applies, it does nothing and gets out of the way.
{% endstep %}

{% step %}
### The customer fills it in

As they interact, the app runs [conditional logic](../conditional-logic/README.md), redraws [the live preview](../personalizer/README.md), and adds up a running price preview.

When they select **Add to cart**, everything is validated first — required fields, character limits, minimum and maximum selections, allowed file types. If something is wrong the add is blocked and the error is shown.
{% endstep %}

{% step %}
### The selections travel with the order

What the customer entered is attached to the cart line as line item properties — Shopify's own mechanism for custom order details. That is why the information appears, with no further setup from you, on the cart, at checkout, on the order in your admin, and in order confirmation emails, invoices, and packing slips.

Properties whose name starts with an underscore are the app's own bookkeeping, and Shopify keeps them out of the way. A custom template may print them anyway — see [Show options on orders](../storefront/show-options-on-orders.md).

Any add-on backed by a product is added as its own cart line, linked to the main item.
{% endstep %}

{% step %}
### Pricing is finalised at checkout

A storefront cannot change what a customer is actually charged — only Shopify can. So while shopping the app shows a *preview* of the total, and at checkout Shopify applies the real prices for the add-ons that were selected.

The amount charged always matches the choices made, even though the number on the product page was calculated in the browser. It also means a shopper cannot tamper with add-on prices, and that discount codes are worth testing against a real order — see [Add-on pricing limitations](../add-on-pricing/limitations.md).
{% endstep %}
{% endstepper %}

## What this means in practice

<table><thead><tr><th width="330">Because…</th><th>…this happens</th></tr></thead><tbody><tr><td>The app embed is what runs the app</td><td>Nothing appears until it is enabled — and it must be enabled again on any new theme you publish</td></tr><tr><td>Option sets are published to your store as store data</td><td>Changes appear within seconds, not instantly. If you do not see one, refresh</td></tr><tr><td>Selections become line item properties</td><td>Option details reach the cart, order, invoice, packing slip, and emails with no extra configuration</td></tr><tr><td>Add-on products are separate cart lines</td><td>They can have their own stock, SKU, and weight — and can be merged visually with the main item. See <a href="../add-on-pricing/merge-as-bundle.md">Merge main product and add-ons</a></td></tr><tr><td>Final pricing happens at checkout</td><td>Add-on prices cannot be tampered with, and the price shown while shopping is a preview</td></tr><tr><td>Hidden options contribute nothing</td><td>An option hidden by a rule is neither validated nor charged</td></tr></tbody></table>

## What the app does not do

* It does not create Shopify variants. Options sit alongside your product's variants rather than multiplying them, which is how it gets past Shopify's variant limit.
* It does not edit your theme's code. Everything runs through Shopify's theme app extension system.
* It does not change your product prices in Shopify. Add-ons are charged on top at checkout; your product's own price is untouched.
