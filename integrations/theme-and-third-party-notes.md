---
description: >-
  Sticky add-to-cart bars, quickview apps, speed optimizers, subscriptions, and
  other apps that share your product page.
icon: layer-group
---

# Theme and third-party notes

Other apps and theme features run on the same product page as the option widget. This page covers the ones that most often interact with it, and what to check for each.

## Sticky add-to-cart bars

Many themes and apps add a bar with a buy button that follows the customer down the page.

<table><thead><tr><th width="230">Risk</th><th>What to check</th></tr></thead><tbody><tr><td>The bar's button bypasses the options</td><td>Scroll down until the bar appears, then use its button. Are required options enforced? Are add-ons priced?</td></tr><tr><td>The bar covers the widget on mobile</td><td>Whether the last option is reachable on a phone</td></tr></tbody></table>

The app supports the common patterns. If the bar's button skips validation, report it, because it produces orders you cannot fulfill.

## Quickview apps and theme quickviews

A quickview lets customers buy from a collection page without opening the product page.

Turn on **Show options on Quickview popups** in **Settings** > **Settings** > **General**, then test it. If your quickview can add to cart without displaying your options, you receive orders with no personalization details.

See [Quickview and other pages](/broken/pages/z3MOr9S1i9k8wdOYumws).

## Speed and script optimization apps

Apps that defer or delay JavaScript can delay the option widget, so it appears late or, with an aggressive delay, not at all.

The app requests to be excluded from deferral by the common optimizers. If you use one and the widget is slow to appear or missing:

{% stepper %}
{% step %}
### Check the optimizer's exclusion list

Most optimizers have one. Add the app's scripts to it.
{% endstep %}

{% step %}
### Test with the optimizer turned off

This confirms whether the optimizer is the cause.
{% endstep %}

{% step %}
### Contact support if you cannot find the setting

Include the optimizer's name. See [Contact support](../help/contact-support.md).
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
A widget that appears half a second late can be missed by a customer who has already scrolled past it. If you use an optimizer, test your product page on a slow connection.
{% endhint %}

## Other options or swatch apps

Running two apps that both add options to a product page causes duplicated fields, conflicting validation, and two sets of prices.

Use one app. If you are migrating, [import your option sets](../option-sets/import-and-export.md) from the other app, test them, and then uninstall it, in that order.

## Subscription apps

A subscription turns the purchase into a recurring one, which affects how add-ons behave.

Test whether add-ons recur with the subscription or are charged once. The answer depends on the subscription app, and a one-off add-on charged every month leads to refund requests.

## Currency and market apps

Add-on prices are in your store's currency and are converted in the same way as any other price. If you use a currency switcher, check a converted add-on price on the product page and again at checkout.

Country-specific behavior is available in the app itself through [country rules](../option-sets/assign-to-countries.md).

## Product review and badge apps

These apps usually appear near the buy button, where the widget is. If they overlap, change the [widget placement](../storefront/widget-placement.md) or set the position with an [app block](../getting-started/add-the-app-block.md).

## Fulfillment and printing apps

Any app that prints or forwards order data has to include line item properties, otherwise your options are not passed to it.

Most of these tools let you edit a template. See [Show options on orders](../storefront/show-options-on-orders.md) for the snippet, or use an [Update order notes](../automations/update-order-notes.md) workflow, which writes the options into the order note that most tools already read.

## What to test after installing an app

After installing any app that affects the product page or the order:

{% stepper %}
{% step %}
### Open a product with options

Check that they still appear in the correct place.
{% endstep %}

{% step %}
### Try to add to cart with a required option empty

Check that adding to cart is still blocked.
{% endstep %}

{% step %}
### Add a product with an add-on

Check that the price in the cart is correct.
{% endstep %}

{% step %}
### Complete a test order

Check that the option details are stored in the order.
{% endstep %}

{% step %}
### Repeat on mobile
{% endstep %}
{% endstepper %}

This takes a few minutes and catches the problems that otherwise appear as orders you cannot fulfill.
