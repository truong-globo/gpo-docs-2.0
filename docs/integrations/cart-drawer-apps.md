---
description: >-
  Options and add-on lines inside the UpCart, Monster Cart, and Kaching
  drawers — the two settings to change, and what a drawer cannot do.
icon: basket-shopping
---

# Cart drawer apps

A cart drawer app replaces your theme's cart with its own slide-out drawer, usually to show upsells and free-gift offers there. That drawer is where your customers see add-on lines after adding a personalized product, so the app has to work inside it.

Three cart drawer apps are recognized automatically. There is nothing to connect and no selector to enter. The setup is the same for all three.

## Supported apps

<table><thead><tr><th width="230">App</th><th>Anything specific to it</th></tr></thead><tbody><tr><td><a href="https://apps.shopify.com/upcart-cart-builder">UpCart — Cart Drawer Cart Upsell</a></td><td>Nothing. Follow the setup below</td></tr><tr><td><a href="https://apps.shopify.com/monster-upsells">Monster Cart Upsell+ Free Gift</a></td><td>You no longer have to merge add-ons. See <a href="cart-drawer-apps.md#monster-cart-merging-add-ons-is-now-optional">Merging add-ons is now optional</a></td></tr><tr><td><a href="https://apps.shopify.com/cart-upsell">Kaching CartDrawer Cart Upsell</a></td><td>The variant selector is hidden on add-on lines, and upsell filtering works differently. See <a href="cart-drawer-apps.md#kaching-cart-variant-selectors-and-upsell-filtering">Variant selectors and upsell filtering</a></td></tr></tbody></table>

Using a different cart drawer app? See [If you use another cart drawer app](cart-drawer-apps.md#if-you-use-another-cart-drawer-app) at the end.

## Set up

Two settings decide whether this works. One of them is on by default and has to be turned off, which is the step most people miss.

{% stepper %}
{% step %}
### Turn off "Go to cart immediately after adding to cart"

In **Settings** > **Settings** > **General** > **Product page**. It is **on** by default.

While it is on, adding a product sends the customer straight to your cart page. The drawer never opens, so the integration has nothing to act on and customers never see the drawer you paid for. See [Ajax cart and redirect to cart](../storefront-display-and-design/ajax-cart-and-redirect.md) for what this setting does elsewhere.
{% endstep %}

{% step %}
### Check that "Hide quantity box and remove button for add-on products" is on

In **Settings** > **Settings** > **General** > **Cart page**. It is **on** by default, so usually there is nothing to change.

This is what switches the drawer handling on. With it off, the app leaves the drawer alone entirely, and add-on lines appear in it as ordinary, independently editable cart lines. See [Cart page](../storefront-display-and-design/cart-page.md).
{% endstep %}

{% step %}
### Save, then add a product with an add-on from your storefront

The drawer should open, with the main item and its add-on line both displayed.
{% endstep %}

{% step %}
### Decide about drawer upsells

Read [Upsells in the drawer skip your option form](cart-drawer-apps.md#upsells-in-the-drawer-skip-your-option-form) below. If any product you upsell in the drawer uses options, turn on the third setting.
{% endstep %}
{% endstepper %}

## What the app does in the drawer

<table><thead><tr><th width="330">In the drawer</th><th>What the app does</th></tr></thead><tbody><tr><td>Add-on lines</td><td>Hides their quantity box and Remove button, so an add-on cannot be changed or deleted separately from the item it belongs to</td></tr><tr><td>The main item's quantity is changed</td><td>Recalculates the quantity of every add-on linked to it, following each add-on's own quantity mode</td></tr><tr><td>The drawer is opened, reloaded, or updated</td><td>Re-checks every line, so it stays correct after a customer edits the cart</td></tr><tr><td>The drawer's upsell list</td><td>Leaves out the add-on products the app generated for you, so customers are not offered a gift box or an engraving fee as an upsell. A product you already sell and use as an add-on is a normal product, and can still be upsold</td></tr></tbody></table>

How an add-on's quantity is recalculated depends on the **Add-on quantity** mode you chose for that option — a **One time charge** stays at one, **Dynamic quantity** multiplies, and so on. See [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md).

This applies only to add-ons that have their own cart line, which means add-ons priced as an [Existing product](../add-on-pricing/use-an-existing-product.md) or a [New product](../add-on-pricing/auto-generate-a-product.md). A [Fixed amount](../add-on-pricing/add-price-directly.md) charge is added to the main item's price and has no separate line, so there is nothing in the drawer for the app to manage.

## Upsells in the drawer skip your option form

Every one of these apps shows upsells inside the drawer, and their Add button puts the product in the cart in one click, without opening a product page. If one of those products has options, the customer buys it without filling them in, and you receive an order you cannot fulfill.

The setting for this is **Send cart drawer app upsells to the product page**, in **Settings** > **Settings** > **General** > **Cart page**.

| Default | Off |
| ------- | --- |

{% hint style="warning" %}
**Turn this on if any product you upsell in the drawer uses options.** It is off by default only so that installing this app does not silently change how your upsell app behaves.
{% endhint %}

With it on, the upsell's Add button reads **Choose options** and opens the product page, where the customer fills the form and adds to cart normally.

<table><thead><tr><th width="290">Turn it on when</th><th>Leave it off when</th></tr></thead><tbody><tr><td>Any upsell product has options, now or later</td><td>None of your upsell products use options</td></tr><tr><td>You would rather be safe than lose the occasional impulse add</td><td>You want to keep one-click upsells exactly as they are</td></tr></tbody></table>

It applies to **every** upsell in the drawer, not only the ones with options, because the drawer does not tell the app which products have an option set. Decide based on whether any of them do.

The button text is translatable per language, as **Choose options** in the **Cart widget** group. See [Translate widget text](../translations-and-languages/translate-widget-text.md).

## Notes for each app

Everything above applies to all three. These are the differences.

### UpCart

None. The setup above is all of it.

### Monster Cart: merging add-ons is now optional

Previously, the Monster Cart drawer would only open if **Merge Main product & Add-on products** was on, because the drawer could not handle several linked lines being added at once. That restriction is gone. Adding to cart now adds every add-on product and opens the drawer, with the add-on lines displayed separately.

Merging is now a presentation choice like any other: leave it off to show each add-on as its own line with its own price, or turn it on to show one combined item. Both work in the drawer. The setting is in **Settings** > **Settings** > **Add-on price**, and it is off by default on new stores. See [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).

### Kaching Cart: variant selectors and upsell filtering

Kaching's slide cart lets customers switch an item's variant from inside the drawer. That control is hidden on add-on lines, because changing it would leave the add-on no longer matching the option the customer chose.

Kaching also offers no way to filter its own upsell list, which the other two do. Instead, the app hides your generated add-on products by checking each upsell product's tags after the list is drawn. Two things follow from that, and both are visible to shoppers:

* An add-on product can be visible in the upsell list for a moment before it disappears.
* If that check cannot complete, the add-on product stays in the list.

Turning on **Send cart drawer app upsells to the product page** covers you in the second case, because the customer is taken to the product page rather than buying it in one click.

## What a drawer cannot do

A cart drawer is the upsell app's own interface, not your cart page. These limits apply whichever of the three you use, and they are worth knowing before you decide to run personalized products through a drawer.

<table><thead><tr><th width="290">Limitation</th><th>What it means for you</th></tr></thead><tbody><tr><td><strong>Edit Options is not available</strong></td><td>The <strong>Edit Options</strong> button is only rendered on your cart page. A customer who spots a misspelled engraving in the drawer has to open the cart page to fix it, or remove the item and start again. See <a href="../storefront-display-and-design/cart-page.md">Cart page</a></td></tr><tr><td><strong>A personalized design cannot be previewed</strong></td><td><strong>Preview Your Design</strong> is also cart-page only, for the same reason. Customers using the <a href="../product-personalizer/personalizer.md">Personalizer</a> cannot check their artwork from the drawer</td></tr><tr><td><strong>A quantity correction reloads the page</strong></td><td>If an add-on's quantity no longer matches the item it belongs to, or the add-on product does not have the stock for it, the app writes the correction to the cart and the page reloads, which closes the drawer. The cart is right afterwards, but the customer sees the drawer disappear</td></tr><tr><td><strong>Add-on quantities cannot be edited by the customer</strong></td><td>By design. Add-on quantities follow their <a href="../add-on-pricing/advanced-add-on-modes.md">quantity mode</a>, and the controls are hidden rather than made editable</td></tr><tr><td><strong>Whether option details are listed is up to the drawer app</strong></td><td>The choices a customer made are stored on the cart line either way, and they always appear at checkout and on the order. Whether the drawer prints them under the item is the drawer app's own setting, not ours</td></tr><tr><td><strong>The upsell redirect is all or nothing</strong></td><td>Turning on <strong>Send cart drawer app upsells to the product page</strong> changes every upsell button in the drawer, not only the ones for products with options</td></tr></tbody></table>

{% hint style="info" %}
None of this affects what is charged or what reaches the order. Option values and add-on lines are stored on the cart the moment the customer adds to cart, so checkout and your orders are correct even when the drawer displays less than your cart page would.
{% endhint %}

## Test it

{% stepper %}
{% step %}
### Add a product with two add-ons

The drawer should open, with both add-on lines shown, each without a quantity box or a Remove button. On Kaching, without a variant selector either.
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

Your generated add-on products should not stay in it. If you turned the redirect on, the Add button should read **Choose options** and open the product page.
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

<table><thead><tr><th width="330">What you see</th><th>What to check</th></tr></thead><tbody><tr><td>The drawer does not open after adding to cart</td><td><strong>Go to cart immediately after adding to cart</strong> is still on</td></tr><tr><td>Add-on lines still have a quantity box and a Remove button</td><td><strong>Hide quantity box and remove button for add-on products</strong> is off</td></tr><tr><td>Add-on quantities do not follow the main item</td><td>The <strong>Add-on quantity</strong> mode set on that option. <strong>Fixed quantity</strong> and <strong>One time charge</strong> are not supposed to follow it</td></tr><tr><td>An upsell was bought without its options</td><td>Turn on <strong>Send cart drawer app upsells to the product page</strong></td></tr><tr><td>Nothing in the drawer behaves as described</td><td>That the app embed is enabled on the published theme. See <a href="../getting-started/enable-the-app-embed.md">Enable the app embed</a></td></tr></tbody></table>

If it still looks wrong, [contact support](../help/contact-support.md) with your theme name and a link to a product that has an add-on.

## If you use another cart drawer app

Only the three above are recognized. With any other one, test that add-on lines appear in the drawer and that their quantity boxes and Remove buttons are hidden. If they are not, [contact support](../help/contact-support.md) with the app's name.

Your theme's own cart drawer is a separate case and is supported on a wide range of themes. See [Ajax cart and redirect to cart](../storefront-display-and-design/ajax-cart-and-redirect.md).

## Next steps

* [Cart page](../storefront-display-and-design/cart-page.md) — every setting that affects add-on lines in the cart
* [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md) — showing add-ons as part of the item instead
* [Theme and third-party notes](theme-and-third-party-notes.md) — other apps that share your product page
