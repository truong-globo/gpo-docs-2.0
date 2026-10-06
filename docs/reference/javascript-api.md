---
description: The storefront object, the theme selectors you can override, and the events the app fires.
icon: code
---

# JavaScript API

This page is for developers working on a theme. Nothing here is needed to use the app normally — it exists for the cases where a theme does something unusual enough that the app's own settings cannot reach it.

{% hint style="warning" %}
Code you add here is yours to maintain. It is not covered by [Match theme style](../storefront-display-and-design/match-your-theme-style.md), it is not adjusted when the app updates, and it is the first thing to check when something breaks after a theme change.
{% endhint %}

Everything below runs on the storefront and needs the [app embed](../getting-started/enable-the-app-embed.md) enabled. Without it, none of these objects or events exist.

## window.GPOConfigs

The app's storefront object. It is created by the app embed before the app's own script runs, which is what makes the overrides below possible.

<table><thead><tr><th width="210">Property</th><th>What it holds</th></tr></thead><tbody><tr><td><code>theme</code></td><td>The selectors the app uses to find things in your theme. See <a href="#overriding-theme-selectors">Overriding theme selectors</a></td></tr><tr><td><code>page.type</code></td><td>The Shopify page type — <code>product</code>, <code>cart</code>, <code>index</code>, <code>collection</code>, and so on</td></tr><tr><td><code>product</code></td><td>The current product, as Shopify's product JSON, plus <code>product.collections</code> with the collection ids it belongs to. <code>false</code> off a product page</td></tr><tr><td><code>cart</code></td><td>The current cart, as Shopify's cart JSON</td></tr><tr><td><code>customer</code></td><td><code>id</code>, <code>name</code>, <code>email</code>, and <code>tags</code> for a signed-in customer, or <code>false</code>. The tags are what <a href="../option-sets/assign-to-customers.md">customer rules</a> match on</td></tr><tr><td><code>curCountryCode</code></td><td>The visitor's country, as a two-letter code. What <a href="../option-sets/assign-to-countries.md">country rules</a> match on</td></tr><tr><td><code>money_format</code></td><td>The money format the app formats prices with, which follows your add-on price settings</td></tr><tr><td><code>initialize()</code></td><td>Runs the app again. See <a href="#re-running-the-app">Re-running the app</a></td></tr></tbody></table>

{% hint style="danger" %}
**Only the properties listed above are supported.** `GPOConfigs` carries plenty of other things — asset URLs, option set payloads, loading flags, the raw settings blob. They are internal plumbing, they change without notice, and code that reads them will break.

If something you need is not on this list, ask us rather than reaching for an internal field. See [Contact support](../help/contact-support.md).
{% endhint %}

## Overriding theme selectors

The app finds your product form, price, variant picker, and cart by CSS selector. It ships selectors for the themes it supports and a sensible default set for the rest — but a heavily customized theme can put these somewhere the defaults do not reach.

Set your own before the app's script runs. Put this in `theme.liquid`, above `</body>`:

```html
<script>
  window.GPOConfigs = window.GPOConfigs || {};
  window.GPOConfigs.theme = window.GPOConfigs.theme || {};
  window.GPOConfigs.theme.product = {
    ...(window.GPOConfigs.theme.product || {}),
    form: ['#my-product-form'],
    addToCartButton: '.my-atc-button'
  };
</script>
```

Your values are merged over the app's, so you override only the keys you name and the rest keep working.

### The selectors

<table><thead><tr><th width="210">Group</th><th>Keys</th></tr></thead><tbody><tr><td><code>product</code></td><td><code>form</code>, <code>sticky</code>, <code>imageContainer</code>, <code>imageButton</code>, <code>image</code>, <code>images</code>, <code>unitPrice</code>, <code>compareAtPrice</code>, <code>variantWrapper</code>, <code>variantSelector</code>, <code>variantActivator</code>, <code>quantity</code>, <code>addToCartButton</code>, <code>paymentButton</code></td></tr><tr><td><code>collection</code></td><td><code>wrapper</code>, <code>item</code>, <code>productLink</code>, <code>quickViewActivator</code>, <code>quickViewProductForm</code></td></tr><tr><td><code>cart</code></td><td><code>form</code>, <code>page</code>, <code>drawer</code></td></tr></tbody></table>

`form`, `cart.form`, `cart.page`, and `cart.drawer` take an **array** of selectors, tried in order until one matches. The rest take a single selector string.

{% hint style="info" %}
Try the settings first. [Widget placement](../storefront-display-and-design/widget-placement.md) moves the widget, and an [app block](../getting-started/add-the-app-block.md) positions it in the theme editor with no selector to maintain. Overriding selectors is for what those cannot reach.

If your theme needs an override, tell us — theme integration is something support does regularly, and a theme we fix is fixed for everyone on it.
{% endhint %}

## Events

The app fires these on `document`, so listen with `document.addEventListener`.

<table><thead><tr><th width="250">Event</th><th width="210">detail</th><th>Fired when</th></tr></thead><tbody><tr><td><code>gpoRenderCompleted</code></td><td><code>{ form, product }</code></td><td>The options have finished rendering on the page</td></tr><tr><td><code>gpoElementChanged</code></td><td><code>{}</code></td><td>The customer changed an option</td></tr><tr><td><code>gpoProductPriceUpdated</code></td><td><code>{}</code></td><td>The displayed price was recalculated</td></tr><tr><td><code>gpoValidated</code></td><td><code>{ success }</code></td><td>Validation ran on add to cart. <code>success</code> is <code>false</code> when something was wrong</td></tr><tr><td><code>gpoAddedToCart</code></td><td><code>{}</code></td><td>The item and its add-ons were added to the cart</td></tr></tbody></table>

```javascript
document.addEventListener('gpoRenderCompleted', function (event) {
  const { form, product } = event.detail;
  // the options are on the page now
});

document.addEventListener('gpoValidated', function (event) {
  if (!event.detail.success) {
    // the customer missed something required
  }
});
```

`gpoRenderCompleted` is the one to build on. It is the only reliable signal that the option fields exist in the DOM — the app renders them asynchronously, so code that runs on `DOMContentLoaded` is usually too early.

{% hint style="warning" %}
The app fires other events whose names begin with `gpo`. They drive the Personalizer's own internals, they are not part of this API, and they change without notice. Use the five above.
{% endhint %}

## Re-running the app

`GPOConfigs.initialize()` runs the app again from the start. Use it when something replaces the product form after the page has loaded — a page builder swapping sections, or a theme that re-renders the product on variant change.

```javascript
window.GPOConfigs && window.GPOConfigs.initialize();
```

Call it after the new markup is in the DOM, not before. Calling it when nothing has changed re-renders the options unnecessarily, so trigger it from your theme's own "section replaced" signal rather than on a timer.

## Notes

* All of this needs the app embed enabled on the published theme. See [Enable the app embed](../getting-started/enable-the-app-embed.md).
* `GPOConfigs` exists on every page the app embed runs on, but `product` is `false` away from a product page.
* Overriding selectors does not change what the options collect, only where the app finds things in your theme.
* If a theme needs the same override on every store running it, send it to us instead of repeating it per store. See [Contact support](../help/contact-support.md).
