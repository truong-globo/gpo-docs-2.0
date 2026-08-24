---
description: The Shopify access the app requests, what it does with your data, and what happens when you uninstall.
icon: shield-halved
---

# Permissions and data

## What the app can access

Shopify asks you to approve this access when you install.

<table><thead><tr><th width="250">Access</th><th>Why the app needs it</th></tr></thead><tbody><tr><td><strong>Products</strong> — read and write</td><td>To show your products and variants in the pickers when you assign an option set or link an add-on, and to create add-on products when you choose <a href="../add-on-pricing/auto-generate-a-product.md">Automatically generate a product</a></td></tr><tr><td><strong>Product inventory and listings</strong> — read</td><td>So the widget can read the product it is rendering for, and so <a href="../option-types/shared-settings/out-of-stock-options.md">Out of stock options</a> knows when an add-on has run out</td></tr><tr><td><strong>Themes</strong> — read</td><td>To tell you on <strong>Theme Setup</strong> whether the app embed is enabled, and to identify your theme for <a href="../storefront/match-your-theme-style.md">Match theme style</a></td></tr><tr><td><strong>Files</strong> — read and write</td><td>For images and fonts you upload — swatch images, Personalizer backgrounds, custom fonts — and for files your customers upload</td></tr><tr><td><strong>Orders</strong> — read</td><td>For the figures on <a href="../option-sets/analytics.md">Analytics</a>, and to run your <a href="../automations/README.md">automation workflows</a></td></tr><tr><td><strong>Draft orders</strong> — read and write</td><td>An alternative checkout route, in which a cart is sent to a draft-order invoice rather than the standard checkout</td></tr><tr><td><strong>Store languages</strong> — read</td><td>So <a href="../translations/README.md">Translations</a> offers exactly the languages your store publishes</td></tr><tr><td><strong>Product publishing</strong> — read and write</td><td>To manage which sales channels an option set applies to, and to publish a generated add-on product so it can be bought</td></tr><tr><td><strong>Cart pricing</strong> — read and write</td><td>The mechanism that applies add-on prices at checkout. See <a href="how-it-works.md">How it works</a></td></tr><tr><td><strong>Storefront scripts and app proxy</strong></td><td>How the widget is delivered to your storefront and how it talks back to the app</td></tr></tbody></table>

## Requested only when you use the feature

Some access is asked for later rather than upfront:

* **Write access to orders** — the first time you open [Automations](../automations/README.md), because the order-note and order-tag workflows change the order. Until you approve it, no workflow runs.
* **Customer data** — the first time you pick specific customers in a [customer rule](../option-sets/assign-to-customers.md).

In both cases the app explains what it is asking for and Shopify shows its own approval screen, exactly like the original install.

## What the app does not ask for

<table><thead><tr><th width="290">Not requested</th><th>Consequence</th></tr></thead><tbody><tr><td>Write access to orders, at install</td><td>The app cannot change an order's contents, prices, or fulfilment unless you enable Automations</td></tr><tr><td>Payment or payout access</td><td>The app never handles money. All charging is Shopify's</td></tr><tr><td>Write access to your theme's code</td><td>The app cannot alter your templates or Liquid</td></tr><tr><td>Access to your Shopify account or billing</td><td>Plan changes go through Shopify's own billing screens</td></tr></tbody></table>

## Your customers' data

The app sees customer data only where it has to, and only through Shopify:

* the answers a customer gives, and any file they upload
* the design they created, if you use the Personalizer
* their tags, account status, and country, read at page load to evaluate your [customer](../option-sets/assign-to-customers.md) and [country](../option-sets/assign-to-countries.md) rules

{% hint style="warning" %}
**You decide what customers are asked for.** A field asking for a date of birth, an ID number, or a phone number puts that data on your orders, and handling it appropriately is your responsibility as the merchant. Ask for what you need to fulfil the order, and no more.
{% endhint %}

The app supports Shopify's mandatory privacy notifications, so a customer data request, a customer erasure request, or a store erasure request raised through Shopify is handled. Raise these through Shopify's own privacy tooling rather than by email — that way they reach every app on your store, not just this one.

## Uninstalling

<table><thead><tr><th width="330">Removed automatically</th><th>Left in your store</th></tr></thead><tbody><tr><td>The app's access to your store</td><td>Automatically generated add-on products — ordinary products in your catalogue, tagged <code>globo-product-options</code></td></tr><tr><td>The app embed and anything the app added to your theme</td><td>Line item properties on existing orders, which are part of those orders' records</td></tr><tr><td>The checkout pricing mechanism</td><td>Files uploaded to your Shopify files, which belong to you</td></tr></tbody></table>

There is no theme code to clean up by hand.

{% hint style="danger" %}
**Export before you uninstall.** Option sets are not recoverable once the app's data is erased. A CSV export takes seconds — see [Import and export](../option-sets/import-and-export.md).
{% endhint %}

The app's privacy policy and terms of service are linked from its Shopify App Store listing at [apps.shopify.com/product-options-pro](https://apps.shopify.com/product-options-pro), which is always the current version. Those documents, not this page, are the authoritative statement — this page explains what the access is *for*. See [Contact support](../help/contact-support.md) if you would like your stored data removed after uninstalling.
