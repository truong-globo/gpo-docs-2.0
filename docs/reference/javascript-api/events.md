---
description: The five events the app fires on the storefront, each with a worked example.
icon: bolt
---

# Events

The app fires these on `document`, so listen with `document.addEventListener`. Put the code in a theme asset, or in `theme.liquid` above `</body>`.

<table><thead><tr><th width="250">Event</th><th width="200">detail</th><th>Fired when</th></tr></thead><tbody><tr><td><code>gpoRenderCompleted</code></td><td><code>{ form, product }</code></td><td>The options have finished rendering</td></tr><tr><td><code>gpoElementChanged</code></td><td><code>{}</code></td><td>The customer changed an option</td></tr><tr><td><code>gpoProductPriceUpdated</code></td><td><code>{}</code></td><td>The displayed price was recalculated</td></tr><tr><td><code>gpoValidated</code></td><td><code>{ success }</code></td><td>Validation ran on add to cart</td></tr><tr><td><code>gpoAddedToCart</code></td><td><code>{}</code></td><td>The item and its add-ons reached the cart</td></tr></tbody></table>

{% hint style="warning" %}
The app fires other events beginning with `gpo`. They drive the Personalizer's internals, they are not part of this API, and they change without notice. Use the five above.
{% endhint %}

## gpoRenderCompleted

Fired once the option fields exist in the DOM. **This is the one to build on.** The app renders asynchronously, so code that runs on `DOMContentLoaded` runs before the options exist and finds nothing.

`detail` carries `form`, the product form the options were rendered into, and `product`, the product they were rendered for.

```javascript
document.addEventListener('gpoRenderCompleted', function (event) {
  const { form, product } = event.detail;
  if (!form) return; // no option set applies to this product

  // Safe to query the option fields now
  form.querySelectorAll('.gpo-form__group').forEach(function (group) {
    group.classList.add('my-theme-option');
  });
});
```

It fires again whenever the options are re-rendered — after a variant change on themes that re-render the product, or after you call `GPOConfigs.initialize()`. Write the handler so running twice is harmless.

## gpoElementChanged

Fired each time the customer changes an option: typing in a field, picking a swatch, ticking a checkbox.

```javascript
document.addEventListener('gpoElementChanged', function () {
  const engraving = document.querySelector('[name="properties[Engraving text]"]');
  const note = document.querySelector('.my-engraving-note');
  if (!engraving || !note) return;

  note.hidden = engraving.value.trim() === '';
});
```

It fires on every keystroke in a text field, so debounce anything expensive — a network request, a heavy re-layout.

## gpoProductPriceUpdated

Fired after the app has rewritten the displayed price to include the options the customer chose. Use it to keep your own price display in step — a sticky bar, a summary block, an instalment estimate.

```javascript
document.addEventListener('gpoProductPriceUpdated', function () {
  const main = document.querySelector('[data-gpo-product-unit-price]');
  const sticky = document.querySelector('.my-sticky-bar .price');
  if (main && sticky) sticky.textContent = main.textContent;
});
```

The price shown on the page is a preview. What the customer is actually charged is applied by Shopify at checkout, so never treat this figure as the final amount. See [How pricing is applied](../../add-on-pricing/how-pricing-is-applied.md).

## gpoValidated

Fired when the customer tries to add to cart and the app has checked the options. `detail.success` is `false` when something is wrong — a required option empty, a character limit exceeded, too few selections.

```javascript
document.addEventListener('gpoValidated', function (event) {
  if (event.detail.success) return;

  // The add to cart was blocked
  if (window.analytics) {
    window.analytics.track('Option validation failed', {
      product: window.GPOConfigs?.product?.handle
    });
  }
});
```

The app already scrolls to the first error when **Auto-scroll to first error message** is on, so there is no need to do that yourself. See [Widget behavior](../../storefront-display-and-design/widget-behavior.md).

## gpoAddedToCart

Fired after the item and any add-on products have been added. This is the point at which the cart really has changed, which makes it the right place for cart-opening and analytics.

```javascript
document.addEventListener('gpoAddedToCart', function () {
  fetch(window.Shopify.routes.root + 'cart.js')
    .then(function (res) { return res.json(); })
    .then(function (cart) {
      document.querySelector('.my-cart-count').textContent = cart.item_count;
    });
});
```

An add-on backed by a product is its own cart line, so one add to cart can add several lines. Read the cart back rather than assuming one item was added. See [Merge main product and add-ons](../../add-on-pricing/merge-as-bundle.md).

## Notes

* All five need the [app embed](../../getting-started/enable-the-app-embed.md) enabled. Without it the app never runs and nothing fires.
* The events carry no customer data beyond what is already on the page. Read [window.GPOConfigs](README.md) for the product, cart, and customer.
* Code you attach here is yours to maintain, and is the first thing to check when the storefront misbehaves after a theme or app update.
