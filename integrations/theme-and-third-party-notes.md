---
description: Sticky add-to-cart bars, quickview apps, speed optimisers, subscriptions, and other things sharing your product page.
icon: layer-group
---

# Theme and third-party notes

Your product page is shared. This page covers the neighbours that most often interact with the option widget, and what to check for each.

## Sticky add-to-cart bars

Many themes and apps add a bar that follows the shopper down the page with a buy button in it.

<table><thead><tr><th width="230">Risk</th><th>What to check</th></tr></thead><tbody><tr><td>The bar's button bypasses the options</td><td>Scroll down until the bar appears, then use its button. Are required options enforced? Are add-ons priced?</td></tr><tr><td>The bar covers the widget on mobile</td><td>Whether the last option is reachable on a phone</td></tr></tbody></table>

The app handles the common patterns. If the bar's button skips validation, that is worth reporting — it is the kind of thing that quietly produces unfulfillable orders.

## Quickview apps and theme quickviews

A quickview lets shoppers buy from a collection page without opening the product.

Turn on **Show options on Quickview popups** in **Settings** > **Settings** > **General**, and then test it. If your quickview can add to cart without showing your options, you will receive orders with no personalisation.

See [Quickview and other pages](../storefront/quickview-and-other-pages.md).

## Speed and script optimisation apps

Apps that defer or delay JavaScript can delay the option widget, so it appears late — or, if the delay is aggressive, not at all.

The app cooperates with the common optimisers by asking to be excluded from deferral. If you use one and the widget is slow to appear or missing:

{% stepper %}
{% step %}
### Check the optimiser's exclusion list

Most have one. Add the app's scripts to it.
{% endstep %}

{% step %}
### Test with the optimiser temporarily off

That tells you quickly whether it is the cause.
{% endstep %}

{% step %}
### Ask us if you cannot find the setting

With the optimiser's name. See [Contact support](../help/contact-support.md).
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
A widget that appears half a second late is a shopper who has already scrolled past it. If you use an optimiser, test your product page on a slow connection rather than assuming.
{% endhint %}

## Other options or swatch apps

Running two apps that both add options to a product page is asking for trouble: duplicated fields, competing validation, and two sets of prices.

Pick one. If you are migrating, [import your option sets](../option-sets/import-and-export.md) from the other app, test, then uninstall it — in that order, so you are never without coverage.

## Subscription apps

A subscription changes the purchase into a recurring one, which affects how add-ons behave.

Test explicitly: do add-ons recur with the subscription, or are they charged once? The answer depends on the subscription app, and it matters — a gift box charged every month is a refund request.

## Currency and market apps

Add-on prices are in your store's currency and are converted like any other price. If you use a currency switcher, check a converted add-on price on the product page and again at checkout.

Country-specific behaviour is available in the app itself through [country rules](../option-sets/assign-to-countries.md).

## Product review and badge apps

These usually sit near the buy button, which is where the widget is too. If they collide, either change the [widget placement](../storefront/widget-placement.md) or pin it with an [app block](../getting-started/add-the-app-block.md).

## Fulfilment and printing apps

Anything that prints or forwards order data needs to include line item properties, or your options will not reach it.

Most such tools let you edit a template. See [Show options on orders](../storefront/show-options-on-orders.md) for the snippet, or use an [Update order notes](../automations/update-order-notes.md) workflow, which puts the options somewhere almost every tool already reads.

## A test list for any new app

Whenever you install something that touches the product page or the order:

{% stepper %}
{% step %}
### Open a product with options

Do they still appear, in the right place?
{% endstep %}

{% step %}
### Try to add to cart with a required option empty

Is it still blocked?
{% endstep %}

{% step %}
### Add a product with an add-on

Is the price right in the cart?
{% endstep %}

{% step %}
### Complete a test order

Do the option details reach the order?
{% endstep %}

{% step %}
### Repeat on mobile
{% endstep %}
{% endstepper %}

Five minutes, and it catches the problems that otherwise surface as unfulfillable orders.

## Next steps

* [Options are not showing up](../help/troubleshooting-not-showing.md)
* [Widget placement](../storefront/widget-placement.md)
* [Contact support](../help/contact-support.md)
