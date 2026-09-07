---
description: Show options in collection quickview popups, and in featured product sections on home and regular pages.
icon: window-maximize
---

# Quickview and other pages

Customers can also add to cart from places other than the product page. Three settings in **Settings** > **Settings** > **General** control those.

## Collection page quickview

<table><thead><tr><th width="290">Setting</th><th width="130">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Show options on Quickview popups</strong></td><td>On</td><td>Renders your options inside the quickview popups on collection pages</td></tr></tbody></table>

Many themes let customers open a product in a popup directly from a collection page. Without this setting on, a customer can add to cart from that popup **without seeing your options**, which for a personalized product means an order you cannot fulfill.

Keep it on if your theme has quickviews. The only effect of turning it on is that the app also runs on collection pages.

{% hint style="info" %}
Every theme builds quickviews differently, and some quickviews are added by other apps. The app supports the common patterns. If your options do not appear in your quickview, see [Contact support](../help/contact-support.md).
{% endhint %}

## Home page and regular pages

<table><thead><tr><th width="330">Setting</th><th width="130">Default</th><th>Covers</th></tr></thead><tbody><tr><td><strong>Show widget on home page</strong></td><td>On</td><td>Featured product sections on your home page</td></tr><tr><td><strong>Show widget on regular page</strong></td><td>On</td><td>Featured product sections on other pages</td></tr></tbody></table>

Both settings apply only to **featured product sections**, which display one product with its buy button. They do not add options to a page in general.

You also need to place the app block inside that section:

{% stepper %}
{% step %}
### Add a Featured product section

In the theme editor, on the page where you want the product.
{% endstep %}

{% step %}
### Add the app block inside it

**Add block** > **Globo Product Options**. See [Add the app block](../getting-started/add-the-app-block.md).
{% endstep %}

{% step %}
### Check the block's Product setting

The block fills this in from the section. Confirm that it points to the correct product.
{% endstep %}

{% step %}
### Turn on the matching setting

**Show widget on home page** or **Show widget on regular page**.
{% endstep %}

{% step %}
### Test the page

Add to cart from that page as part of the test.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: store-other-pages | App admin → Settings → General | Nhóm Collection page và Other pages với các switch | Khoanh 2 nhóm -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The collection page and other pages settings groups"><figcaption><p>Three switches, covering quickviews and featured product sections.</p></figcaption></figure>

## When to turn these off

These settings cause the app to run on those pages. If you have no featured product sections and no quickviews, turning the matching setting off stops the app from running there.

Keep the quickview setting on if your theme has quickviews. A quickview that adds to cart without displaying options causes orders you cannot fulfill.

## Where options do not appear

<table><thead><tr><th width="290">Place</th><th>Why</th></tr></thead><tbody><tr><td>Collection page product cards</td><td>There is no room and no context for a form. Quickview is the answer</td></tr><tr><td>Search results</td><td>Same</td></tr><tr><td>General page content, outside a featured product section</td><td>No product in context</td></tr><tr><td>Checkout</td><td>Options are collected before the cart. Their values <em>appear</em> at checkout — see <a href="show-options-on-orders.md">Show options on orders</a></td></tr><tr><td>Shopify's dynamic checkout buttons, such as accelerated payment</td><td>Those bypass the cart. The app hides them where options would otherwise be skipped</td></tr></tbody></table>

## Notes

* These settings are store-wide.
* Each option set's own rules still apply on these pages, including status, sales channel, and the product, customer, and country rules.
* Quickview support depends on your theme, and on any quickview app you use.
* The cart page has its own settings. See [Cart page](cart-page.md).
