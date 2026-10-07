---
description: >-
  Apps that replace your theme's cart drawer, and what the option widget does
  inside them.
icon: basket-shopping
---

# Cart drawer apps

A cart drawer app replaces your theme's cart with its own slide-out drawer, usually to show upsells and free-gift offers there. That drawer is where your customers see add-on lines after adding a personalized product, so the app has to work inside it.

Two cart drawer apps are recognized automatically. There is nothing to connect and no selector to enter.

## Pages in this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>UpCart</strong></td><td>Setting up options with the UpCart drawer, end to end.</td><td><a href="upcart.md">upcart.md</a></td></tr><tr><td><strong>Monster Cart</strong></td><td>Setting up options with the Monster Cart drawer, end to end.</td><td><a href="monster-cart.md">monster-cart.md</a></td></tr></tbody></table>

## What is the same for both

<table><thead><tr><th width="330">In the drawer</th><th>What the app does</th></tr></thead><tbody><tr><td>Add-on lines</td><td>Hides their quantity box and Remove button, so an add-on cannot be changed or deleted separately from the item it belongs to</td></tr><tr><td>The main item's quantity is changed</td><td>Recalculates the quantity of every add-on linked to it, following each add-on's own quantity mode</td></tr><tr><td>The drawer is opened, reloaded, or updated</td><td>Re-checks every line, so it stays correct after a customer edits the cart</td></tr><tr><td>The drawer's upsell list</td><td>Leaves out the add-on products the app generated for you, so customers are not offered a gift box or an engraving fee as an upsell. A product you already sell and use as an add-on is a normal product, and can still be upsold</td></tr></tbody></table>

## Two settings decide whether this works

<table><thead><tr><th width="330">Setting</th><th>What it has to be</th></tr></thead><tbody><tr><td><strong>Go to cart immediately after adding to cart</strong><br>General > Product page</td><td><strong>Off.</strong> While it is on, customers are sent to your cart page and the drawer never opens. It is on by default, so this is the one you have to change</td></tr><tr><td><strong>Hide quantity box and remove button for add-on products</strong><br>General > Cart page</td><td><strong>On.</strong> This is what switches the drawer handling on. It is on by default</td></tr></tbody></table>

A third setting, **Send cart drawer app upsells to the product page**, is optional but worth reading about. The drawer's own upsells add products straight to the cart, which skips the option form. Each page below covers it.

## If you use a different cart drawer app

Only the two apps above are recognized. With any other one, test that add-on lines appear in the drawer and that their quantity boxes and Remove buttons are hidden. If they are not, [contact support](../../help/contact-support.md) with the app's name.

Your theme's own cart drawer is a separate case and is supported on a wide range of themes. See [Ajax cart and redirect to cart](../../storefront-display-and-design/ajax-cart-and-redirect.md).

## Next steps

* [UpCart](upcart.md)
* [Monster Cart](monster-cart.md)
* [Cart page](../../storefront-display-and-design/cart-page.md) — every setting that affects add-on lines in the cart
