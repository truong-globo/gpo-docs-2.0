---
description: >-
  Add-on lines and upsells in the UpCart drawer, and the setting you have to
  turn off first.
icon: cart-flatbed
---

# UpCart

If your store uses [UpCart — Cart Drawer Cart Upsell](https://apps.shopify.com/upcart-cart-builder), the app works with its drawer automatically. There is nothing to connect and no selector to enter — the app recognizes the drawer and manages add-on lines inside it the same way it does on your cart page.

One setting in this app has to be turned off first, and it is on by default.

## Turn off "Go to cart immediately after adding to cart"

{% hint style="warning" %}
**This is the step that is easy to miss.** While this setting is on, adding a product sends the customer straight to your cart page. The UpCart drawer never opens, so the integration has nothing to act on and customers never see the drawer you paid for.
{% endhint %}

{% stepper %}
{% step %}
### Open the app's general settings

Go to **Settings** > **Settings** > **General**.
{% endstep %}

{% step %}
### Find the Product page group

It is the group containing **Go to cart immediately after adding to cart**.
{% endstep %}

{% step %}
### Turn the setting off

Then save. See [Ajax cart and redirect to cart](../../storefront-display-and-design/ajax-cart-and-redirect.md) for what this setting does elsewhere.
{% endstep %}

{% step %}
### Add a product with an add-on from your storefront

The UpCart drawer should open, with the main item and its add-on line both displayed.
{% endstep %}
{% endstepper %}

## Leave "Hide quantity box and remove button for add-on products" on

| Default | On |
| ------- | -- |

This setting, in **Settings** > **Settings** > **General** > **Cart page**, is what switches the drawer handling on. With it off, the app leaves the UpCart drawer alone entirely, and add-on lines appear in it as ordinary, independently editable cart lines.

Leave it on. See [Cart page](../../storefront-display-and-design/cart-page.md).

## What the integration does

<table><thead><tr><th width="300">In the drawer</th><th>What the app does</th></tr></thead><tbody><tr><td>An add-on line</td><td>Hides its quantity box and its Remove button, so the add-on cannot be changed or deleted separately from the item it belongs to</td></tr><tr><td>The main item's quantity is changed</td><td>Recalculates the quantity of every add-on linked to it, following each add-on's own quantity mode</td></tr><tr><td>The drawer is opened, reloaded, or updated</td><td>Re-checks every line, so the drawer stays correct after a customer edits the cart</td></tr><tr><td>The upsell list</td><td>Leaves out the add-on products the app generated for you, so an auto-generated gift box is not offered as an upsell</td></tr></tbody></table>

How an add-on's quantity is recalculated depends on the **Add-on quantity** mode you chose for that option — a **One time charge** stays at one, **Dynamic quantity** multiplies, and so on. See [Advanced add-on modes](../../add-on-pricing/advanced-add-on-modes.md).

## Upsells in the drawer skip your option form

UpCart's upsells add a product to the cart in one click, without opening a product page. If one of those products has options, the customer buys it without filling them in, and you receive an order you cannot fulfill.

The setting for this is **Send cart drawer app upsells to the product page**, in **Settings** > **Settings** > **General** > **Cart page**.

| Default | Off |
| ------- | --- |

{% hint style="warning" %}
**Turn this on if any product you upsell in the drawer uses options.** It is off by default only so that installing this app does not silently change how your upsell app behaves.
{% endhint %}

With it on, the upsell's Add button reads **Choose options** and opens the product page, where the customer fills the form and adds to cart normally.

<table><thead><tr><th width="290">Turn it on when</th><th>Leave it off when</th></tr></thead><tbody><tr><td>Any upsell product has options, now or later</td><td>None of your upsell products use options</td></tr><tr><td>You would rather be safe than lose the occasional impulse add</td><td>You want to keep one-click upsells exactly as they are</td></tr></tbody></table>

It applies to **every** upsell in the drawer, not only the ones with options, because the drawer does not tell the app which products have an option set. Decide based on whether any of them do.

The button text is translatable per language, as **Choose options** in the **Cart widget** group. See [Translate widget text](../../translations-and-languages/translate-widget-text.md).

## What this applies to

Only add-ons that have their own cart line, which means add-ons priced as an [Existing product](../../add-on-pricing/use-an-existing-product.md) or a [New product](../../add-on-pricing/auto-generate-a-product.md).

A [Fixed amount](../../add-on-pricing/add-price-directly.md) charge is added to the main item's price and has no separate line, so there is nothing in the drawer for the app to manage.

If you would rather add-ons were not shown as separate lines at all, see [Merge main product and add-ons](../../add-on-pricing/merge-as-bundle.md). It is not required for this integration.

## Test it

{% stepper %}
{% step %}
### Add a product with two add-ons

The drawer should open, with both add-on lines shown, each without a quantity box or a Remove button.
{% endstep %}

{% step %}
### Change the main item's quantity in the drawer

The add-on quantities and the drawer total should update to match.
{% endstep %}

{% step %}
### Remove the main item

Its add-on lines should go with it.
{% endstep %}

{% step %}
### Check the upsell list

Your add-on products should not appear in it. If you turned the redirect on, the Add button should read **Choose options** and open the product page.
{% endstep %}

{% step %}
### Go to checkout

Check that the total matches what the drawer showed.
{% endstep %}

{% step %}
### Repeat on a phone
{% endstep %}
{% endstepper %}

## If something looks wrong

<table><thead><tr><th width="330">What you see</th><th>What to check</th></tr></thead><tbody><tr><td>The drawer does not open after adding to cart</td><td><strong>Go to cart immediately after adding to cart</strong> is still on</td></tr><tr><td>Add-on lines still have a quantity box and a Remove button</td><td><strong>Hide quantity box and remove button for add-on products</strong> is off</td></tr><tr><td>Add-on quantities do not follow the main item</td><td>The <strong>Add-on quantity</strong> mode set on that option. <strong>Fixed quantity</strong> and <strong>One time charge</strong> are not supposed to follow it</td></tr><tr><td>An upsell was bought without its options</td><td>Turn on <strong>Send cart drawer app upsells to the product page</strong></td></tr><tr><td>Nothing in the drawer behaves as described</td><td>That the app embed is enabled on the published theme. See <a href="../../getting-started/enable-the-app-embed.md">Enable the app embed</a></td></tr></tbody></table>

If it still looks wrong, [contact support](../../help/contact-support.md) with your theme name and a link to a product that has an add-on.

## Next steps

* [Monster Cart](monster-cart.md) — the other recognized cart drawer app
* [Cart page](../../storefront-display-and-design/cart-page.md) — the same protection on your full cart page
* [Ajax cart and redirect to cart](../../storefront-display-and-design/ajax-cart-and-redirect.md) — the setting you turned off, and what it affects elsewhere
