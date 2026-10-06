---
description: The storefront object, the theme selectors you can override, and the events the app fires.
icon: code
---

# JavaScript API

This page is for developers working on a theme. Nothing here is needed to use the app normally — it exists for the cases where a theme does something unusual enough that the app's own settings cannot reach it.

{% hint style="warning" %}
Code you add here is yours to maintain. It is not covered by [Match theme style](../../storefront-display-and-design/match-your-theme-style.md), it is not adjusted when the app updates, and it is the first thing to check when something breaks after a theme change.
{% endhint %}

Everything below runs on the storefront and needs the [app embed](../../getting-started/enable-the-app-embed.md) enabled. Without it, none of these objects or events exist.

## window.GPOConfigs

The app's storefront object. It is created by the app embed before the app's own script runs, which is what makes the overrides below possible.

<table><thead><tr><th width="210">Property</th><th>What it holds</th></tr></thead><tbody><tr><td><code>theme</code></td><td>The selectors the app uses to find things in your theme. See <a href="theme-selectors.md">Theme selectors</a></td></tr><tr><td><code>page.type</code></td><td>The Shopify page type — <code>product</code>, <code>cart</code>, <code>index</code>, <code>collection</code>, and so on</td></tr><tr><td><code>product</code></td><td>The current product, as Shopify's product JSON, plus <code>product.collections</code> with the collection ids it belongs to. <code>false</code> off a product page</td></tr><tr><td><code>cart</code></td><td>The current cart, as Shopify's cart JSON</td></tr><tr><td><code>customer</code></td><td><code>id</code>, <code>name</code>, <code>email</code>, and <code>tags</code> for a signed-in customer, or <code>false</code>. The tags are what <a href="../../option-sets/assign-to-customers.md">customer rules</a> match on</td></tr><tr><td><code>curCountryCode</code></td><td>The visitor's country, as a two-letter code. What <a href="../../option-sets/assign-to-countries.md">country rules</a> match on</td></tr><tr><td><code>money_format</code></td><td>The money format the app formats prices with, which follows your add-on price settings</td></tr><tr><td><code>initialize()</code></td><td>Runs the app again. See <a href="#re-running-the-app">Re-running the app</a></td></tr></tbody></table>

{% hint style="danger" %}
**Only the properties listed above are supported.** `GPOConfigs` carries plenty of other things — asset URLs, option set payloads, loading flags, the raw settings blob. They are internal plumbing, they change without notice, and code that reads them will break.

If something you need is not on this list, ask us rather than reaching for an internal field. See [Contact support](../../help/contact-support.md).
{% endhint %}

## The rest of this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Theme selectors</strong></td><td>Every selector the app uses to find things in your theme, and the two ways to change one.</td><td><a href="theme-selectors.md">theme-selectors.md</a></td></tr><tr><td><strong>Events</strong></td><td>The five events the app fires, each with a worked example.</td><td><a href="events.md">events.md</a></td></tr></tbody></table>

## Re-running the app

`GPOConfigs.initialize()` runs the app again from the start. Use it when something replaces the product form after the page has loaded — a page builder swapping sections, or a theme that re-renders the product on variant change.

```javascript
window.GPOConfigs && window.GPOConfigs.initialize();
```

Call it after the new markup is in the DOM, not before. Calling it when nothing has changed re-renders the options unnecessarily, so trigger it from your theme's own "section replaced" signal rather than on a timer.

## Notes

* All of this needs the app embed enabled on the published theme. See [Enable the app embed](../../getting-started/enable-the-app-embed.md).
* `GPOConfigs` exists on every page the app embed runs on, but `product` is `false` away from a product page.
* Overriding selectors does not change what the options collect, only where the app finds things in your theme.
* If a theme needs the same override on every store running it, send it to us instead of repeating it per store. See [Contact support](../../help/contact-support.md).
