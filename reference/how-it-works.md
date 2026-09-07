---
description: How an option set goes from the builder to a live price change at checkout.
icon: diagram-project
---

# How it works

You do not need to read this to use the app, but it explains four things that can otherwise look like faults:

* why the app embed matters
* why the price on the product page is only a preview
* why your option details are stored in the order with no setup from you
* why a change sometimes needs a refresh before it appears

{% stepper %}
{% step %}
### You build an option set

You add options, set add-on pricing, and select which products, customers, and countries the option set applies to. When you save, the app publishes a copy of it to your Shopify store as store data, so your storefront can read it without sending a request to the app.

This publish step is why a change appears within a few seconds rather than immediately, and why a hard refresh sometimes displays an update that a cached page did not.
{% endstep %}

{% step %}
### The theme app embed displays it

Once the [app embed](../getting-started/enable-the-app-embed.md) is enabled on your theme, it checks every page a customer visits and determines which of your option sets apply. Four things decide this: the product, the customer, their country, and whether the option set is active on that sales channel. Matching option sets are displayed as the widget.

If no option set applies, the app displays nothing.
{% endstep %}

{% step %}
### The customer completes the form

As the customer makes selections, the app runs [conditional logic](../conditional-logic/README.md), redraws [the live preview](../personalizer/README.md), and updates the price preview.

When they select **Add to cart**, the app validates everything first: required fields, character limits, minimum and maximum selections, and allowed file types. If something is invalid, the item is not added and an error message is displayed.
{% endstep %}

{% step %}
### The selections are stored in the order

What the customer entered is attached to the cart line as line item properties, which is Shopify's own mechanism for custom order details. This is why the information appears without further setup on the cart, at checkout, on the order in your admin, and in order confirmation emails, invoices, and packing slips.

Properties whose name starts with an underscore are internal to the app, and Shopify hides them. A custom template can still print them. See [Show options on orders](../storefront/show-options-on-orders.md).

Any add-on backed by a product is added as its own cart line, linked to the main item.
{% endstep %}

{% step %}
### Pricing is applied at checkout

A storefront cannot change what a customer is charged. Only Shopify can. While the customer is shopping, the app displays a *preview* of the total, and at checkout Shopify applies the actual prices of the add-ons that were selected.

The amount charged always matches the customer's selections, even though the figure on the product page was calculated in the browser. This also means a customer cannot change add-on prices, and that you should test discount codes against a real order. See [Add-on pricing limitations](../add-on-pricing/limitations.md).
{% endstep %}
{% endstepper %}

## What this means in practice

<table><thead><tr><th width="330">Because…</th><th>…this happens</th></tr></thead><tbody><tr><td>The app embed is what runs the app</td><td>Nothing appears until it is enabled — and it must be enabled again on any new theme you publish</td></tr><tr><td>Option sets are published to your store as store data</td><td>Changes appear within seconds, not instantly. If you do not see one, refresh</td></tr><tr><td>Selections become line item properties</td><td>Option details reach the cart, order, invoice, packing slip, and emails with no extra configuration</td></tr><tr><td>Add-on products are separate cart lines</td><td>They can have their own stock, SKU, and weight — and can be merged visually with the main item. See <a href="../add-on-pricing/merge-as-bundle.md">Merge main product and add-ons</a></td></tr><tr><td>Final pricing happens at checkout</td><td>Add-on prices cannot be tampered with, and the price shown while shopping is a preview</td></tr><tr><td>Hidden options contribute nothing</td><td>An option hidden by a rule is neither validated nor charged</td></tr></tbody></table>

## What the app does not do

* It does not create Shopify variants. Options are displayed alongside your product's variants rather than multiplying them, which is how the app works around Shopify's variant limit.
* It does not edit your theme's code. Everything runs through Shopify's theme app extension system.
* It does not change your product prices in Shopify. Add-ons are charged in addition at checkout, and your product's own price is not changed.
