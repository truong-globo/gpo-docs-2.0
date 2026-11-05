---
description: >-
  Using product options with the Unicorn upsell cart drawer, including its
  cross-sell list.
icon: cart-shopping
---

# Unicorn Cart Drawer

[Unicorn ‑ Upsell Cart Drawer](https://apps.shopify.com/unicorn) is recognized automatically. There is nothing to connect and no selector to enter.

{% hint style="info" %}
**Set it up first.** The two settings to change are the same for every cart drawer app, and they are on [Cart drawer apps](./#set-up). This page covers what is specific to Unicorn.
{% endhint %}

## Add-on lines in the drawer

After a customer adds a product with add-ons, the app refreshes the Unicorn drawer so the new lines show straight away. In the drawer, each add-on line has no quantity box and no Remove button, so it cannot be changed or removed apart from the item it belongs to.

When the customer changes the main item's quantity in the drawer, the add-on quantities follow it, according to each add-on's [quantity mode](../../add-on-pricing/advanced-add-on-modes.md). Removing the main item removes its add-ons with it.

## The cross-sell list

Unicorn can show recommended products in the drawer, with a button that adds them in one click.

* **Your generated add-on products are hidden from that list.** The app checks each recommended product after Unicorn draws the list and hides the ones it created for you. One may show for a moment before it disappears.
* **If every recommendation is hidden, the whole cross-sell block is hidden too**, so customers do not see an empty heading.
* **Products with options should open the product page.** Turn on **Send cart drawer app upsells to the product page**, and the recommendation's button reads **Choose options** and opens the product page instead. See [Upsells in the drawer skip your option form](./#upsells-in-the-drawer-skip-your-option-form).

Unicorn's other drawer features, such as free gifts and its reward bar, are Unicorn's own. They work as usual and are not affected by the app.

## Test it

{% stepper %}
{% step %}
### Add a product with an add-on from the product page

The Unicorn drawer opens with the main item and its add-on line. The add-on line has no quantity box and no Remove button.
{% endstep %}

{% step %}
### Change the main item's quantity in the drawer

The add-on quantity and the drawer total update to match.
{% endstep %}

{% step %}
### Check the cross-sell list

Your generated add-on products are not in it. With the upsell redirect on, the button reads **Choose options** and opens the product page.
{% endstep %}
{% endstepper %}

## Next steps

* [Set up](./#set-up): the two settings, with screenshots
* [What a drawer cannot do](./#what-a-drawer-cannot-do): Edit Options, design previews, and the other limits
* [UpCart](upcart.md), [Monster Cart](monster-cart.md), [Kaching Cart](kaching-cart.md), [Qikify Slide Cart](qikify-slide-cart.md), and [Essent Cart Drawer](essent-cart-drawer.md): the other recognized cart drawer apps
