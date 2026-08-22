---
description: >-
  What the app asks permission for and why, what data it handles, and what happens
  to it when you uninstall.
icon: shield-halved
---

# Permissions and data

Installing any Shopify app means granting it access to parts of your store. This page explains what this app asks for, why each piece is needed, and what happens to your data afterwards.

Worth reading before installing, and worth having to hand if a client or a compliance review asks.

## Access the app requests

Shopify shows the list at install. In plain terms:

<table><thead><tr><th width="250">Access to</th><th>Why the app needs it</th></tr></thead><tbody><tr><td><strong>Products</strong> — read and write</td><td>To let you assign option sets to products and collections, to link add-ons to products you already sell, and to create add-on products when you choose <a href="../add-on-pricing/auto-generate-a-product.md">Automatically generate a product</a></td></tr><tr><td><strong>Product inventory</strong> — read</td><td>So <a href="../option-types/shared-settings/out-of-stock-options.md">Out of stock options</a> can hide, blur, or strike through a value when its add-on product runs out</td></tr><tr><td><strong>Product listings</strong> — read</td><td>So the widget on your storefront can read the product it is rendering for</td></tr><tr><td><strong>Orders</strong> — read</td><td>For the figures on <a href="../option-sets/analytics.md">Analytics</a>, and to run your <a href="../automations/README.md">automation workflows</a></td></tr><tr><td><strong>Draft orders</strong> — read and write</td><td>Used by <a href="../pos/README.md">Point of Sale</a>, where a sale is assembled before it is taken</td></tr><tr><td><strong>Themes</strong> — read</td><td>To tell you on <strong>Theme Setup</strong> whether the app embed is enabled, and to identify your theme and its version for <a href="../storefront/match-your-theme-style.md">Match theme style</a></td></tr><tr><td><strong>Files</strong> — read and write</td><td>For images you upload — swatch images, Personalizer backgrounds, custom fonts — and for files your customers upload</td></tr><tr><td><strong>Store languages</strong> — read</td><td>So <a href="../translations/README.md">Translations</a> offers exactly the languages your store publishes</td></tr><tr><td><strong>Product publishing</strong> — read and write</td><td>So a generated add-on product is published where it needs to be to be purchasable</td></tr><tr><td><strong>Cart transformation</strong> — read and write</td><td>The mechanism that applies add-on prices at checkout. See <a href="how-it-works-technical.md">How it works in detail</a></td></tr><tr><td><strong>Storefront scripts and app proxy</strong></td><td>How the widget is delivered to your storefront and how it talks back to the app</td></tr></tbody></table>

{% hint style="info" %}
Two of these do more than they look. **Write products** is what makes generated add-on products possible — without it, only **Add price** and existing products would work. **Cart transformation** is what makes add-on charges tamper-proof; a browser-side price could be edited by anyone.
{% endhint %}

## What the app does not ask for

<table><thead><tr><th width="290">Not requested</th><th>Consequence</th></tr></thead><tbody><tr><td>Write access to orders</td><td>The app cannot change an order's contents, prices, or fulfilment</td></tr><tr><td>Payment or payout access</td><td>The app never handles money. All charging is Shopify's</td></tr><tr><td>Write access to your theme's code</td><td>The app cannot alter your theme's templates or Liquid</td></tr><tr><td>Access to your Shopify account or billing</td><td>Plan changes go through Shopify's own billing screens</td></tr></tbody></table>

The one apparent exception is [Automations](../automations/README.md). Workflows that tag an order or write to its order note need write access to orders, which is not part of the original install — so the app asks for it separately the first time you open **Automations**, and Shopify shows its own approval screen. Until you approve it, no workflow runs.

## What data the app handles

### Yours

<table><thead><tr><th width="290">Data</th><th>Purpose</th></tr></thead><tbody><tr><td>Your option sets — options, values, prices, rules, translations</td><td>The app's core function</td></tr><tr><td>Your settings and design choices</td><td>Rendering the widget as you configured it</td></tr><tr><td>Images and fonts you upload</td><td>Swatches, Personalizer backgrounds, custom fonts</td></tr><tr><td>Your store's name, plan, and published languages</td><td>Showing the right options in the admin, and billing through Shopify</td></tr><tr><td>Order totals and option usage</td><td>The figures on <a href="../option-sets/analytics.md">Analytics</a></td></tr></tbody></table>

### Your customers'

The app sees customer data only where it has to, and only through Shopify:

<table><thead><tr><th width="290">Data</th><th>Why</th></tr></thead><tbody><tr><td>The answers a customer gives</td><td>They are the order. Without them you cannot fulfil it</td></tr><tr><td>Files a customer uploads</td><td>Stored in your Shopify files and attached to the order, so you can produce the item</td></tr><tr><td>A Personalizer design</td><td>Saved so you can produce exactly what the customer approved</td></tr><tr><td>Customer tags, account status, and country</td><td>Read at page load to evaluate your <a href="../option-sets/assign-to-customers.md">customer</a> and <a href="../option-sets/assign-to-countries.md">country</a> rules</td></tr></tbody></table>

{% hint style="warning" %}
**You decide what customers are asked for.** If you add a field asking for a date of birth, an ID number, or a phone number, that data ends up on your orders, and handling it appropriately is your responsibility as the merchant. Ask for what you need to fulfil the order, and no more.
{% endhint %}

## Privacy requests

The app supports Shopify's mandatory privacy notifications, so requests raised through Shopify are handled:

<table><thead><tr><th width="290">Request</th><th>Handling</th></tr></thead><tbody><tr><td>A customer requests their data</td><td>Shopify notifies the app, and the app responds with what it holds for that customer</td></tr><tr><td>A customer requests erasure</td><td>Shopify notifies the app, and the app erases what it holds for that customer</td></tr><tr><td>A store requests erasure after uninstall</td><td>Shopify notifies the app, and the app erases that store's data</td></tr></tbody></table>

Raise these through Shopify's own privacy tooling rather than by email — that way they are recorded properly and reach every app on your store, not just this one.

## Uninstalling

<table><thead><tr><th width="330">Happens automatically</th><th>Stays behind</th></tr></thead><tbody><tr><td>The app loses all access to your store</td><td>Automatically generated add-on products, which are ordinary products in your catalogue</td></tr><tr><td>The app embed and anything the app added to your theme are removed by Shopify</td><td>Line item properties on existing orders, which are part of those orders' records</td></tr><tr><td>The checkout pricing function is removed</td><td>Files uploaded to your Shopify files, which belong to you</td></tr><tr><td>Your options stop rendering on your storefront</td><td></td></tr></tbody></table>

There is no theme code to clean up by hand.

{% hint style="danger" %}
**Export before you uninstall.** Option sets are not recoverable after the app's data is erased. Exporting to CSV takes seconds and gives you a file you can import if you ever reinstall. See [Import and export](../option-sets/import-and-export.md).
{% endhint %}

To remove the generated products afterwards, filter your Shopify products by the tag `globo-product-options`. Only delete them once you no longer need them for the record of past orders.

## The formal documents

The app's privacy policy and terms of service are linked from its Shopify App Store listing at [apps.shopify.com/product-options-pro](https://apps.shopify.com/product-options-pro), which is always the current version. Those documents, not this page, are the authoritative statement — this page explains what the access is *for*.

## Next steps

* [How it works in detail](how-it-works-technical.md)
* [Line item properties](line-item-properties.md)
* [Contact support](../help/contact-support.md)
