---
description: Every selector the app uses to find things in your theme, and the two ways to change one.
icon: crosshairs
---

# Theme selectors

The app finds your product form, price, variant picker, and cart lines by CSS selector. It ships a tuned set for every [supported theme](../../storefront-display-and-design/match-your-theme-style.md) and a broad default set for the rest, which is why it works on most themes with no help.

A heavily customized theme can still put something where the defaults do not reach. There are two ways to fix that, and the first is almost always the better one.

## 1. Add the app's own attribute

Nearly every selector begins with a `data-gpo-…` attribute that exists purely as a hook for you. Put that attribute on the element in your theme and the app finds it, with no selector to maintain and nothing that a theme update can rename.

```html
<form action="/cart/add" method="post" data-gpo-product-form>
  …
  <button type="submit" data-gpo-product-atc>Add to cart</button>
</form>
```

The attribute for each selector is in the tables below.

## 2. Override the selector

Use this when you cannot edit the markup — a section you do not control, or an app rendering the form. Set it before the app's script runs, in `theme.liquid` above `</body>`:

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

Your values are merged over the app's, so you override only the keys you name.

{% hint style="info" %}
Before either of these, check whether a setting does it. [Widget placement](../../storefront-display-and-design/widget-placement.md) moves the widget, and an [app block](../../getting-started/add-the-app-block.md) positions it in the theme editor.

And tell us when a theme needs an override — a theme we fix is fixed for every store running it. See [Contact support](../../help/contact-support.md).
{% endhint %}

## product

Used on product pages, and on featured-product sections elsewhere.

<table><thead><tr><th width="190">Key</th><th width="270">Attribute hook</th><th>What the app does with it</th></tr></thead><tbody><tr><td><code>form</code></td><td><code>data-gpo-product-form</code></td><td>The product form. This is the anchor for everything else — the options are rendered into it and validated on submit. Takes an <strong>array</strong>, tried in order</td></tr><tr><td><code>addToCartButton</code></td><td><code>data-gpo-product-atc</code></td><td>The add-to-cart button. Used to place the widget above it, and to block the submit when validation fails</td></tr><tr><td><code>paymentButton</code></td><td>—</td><td>The accelerated payment button. Hidden on products with options, because it would skip the form</td></tr><tr><td><code>quantity</code></td><td>—</td><td>The quantity input. Read so add-on quantities can follow the main product quantity</td></tr><tr><td><code>unitPrice</code></td><td><code>data-gpo-product-unit-price</code></td><td>The displayed price. Rewritten as the customer picks priced options</td></tr><tr><td><code>compareAtPrice</code></td><td><code>data-gpo-product-compare-at-price</code></td><td>The compare-at price, updated alongside it</td></tr><tr><td><code>variantSelector</code></td><td><code>data-gpo-product-variant-selector</code></td><td>The hidden input holding the chosen variant id. Read to know which variant is selected</td></tr><tr><td><code>variantActivator</code></td><td><code>data-gpo-product-variant-activator</code></td><td>The controls the customer clicks to change variant. Watched so <a href="../../conditional-logic/conditions-on-shopify-variants.md">variant conditions</a> can react</td></tr><tr><td><code>variantWrapper</code></td><td><code>data-gpo-product-variant-wrapper</code></td><td>The block containing the variant pickers. Used to position the widget relative to them</td></tr><tr><td><code>imageContainer</code></td><td><code>data-gpo-product-image-container</code></td><td>The main image area. Where the <a href="../../product-personalizer/personalizer.md">Personalizer</a> draws its live preview</td></tr><tr><td><code>image</code></td><td><code>data-gpo-product-image</code></td><td>The main product image itself</td></tr><tr><td><code>images</code></td><td><code>data-gpo-product-images</code></td><td>The gallery images, for the preview's <strong>Apply to</strong> setting</td></tr><tr><td><code>imageButton</code></td><td><code>data-gpo-product-image-button</code></td><td>The gallery thumbnails or arrows, watched so the preview follows the image on show</td></tr><tr><td><code>sticky.atcButton</code></td><td><code>data-gpo-sticky-atc</code></td><td>The add-to-cart button in a sticky bar, so it validates like the real one</td></tr><tr><td><code>sticky.variantActivator</code></td><td><code>data-gpo-sticky-variant-activator</code></td><td>The variant control in a sticky bar</td></tr></tbody></table>

{% hint style="warning" %}
`form` is the one that matters most. If the app cannot find the form, no options render at all — every other selector depends on it.

A sticky add-to-cart bar whose button is not covered by `addToCartButton` or `sticky.atcButton` can add to cart **without validating**, which produces orders with required options empty. See [Theme and third-party notes](../../integrations/theme-and-third-party-notes.md).
{% endhint %}

## collection

Used for quickview popups on collection pages.

<table><thead><tr><th width="190">Key</th><th width="270">Attribute hook</th><th>What the app does with it</th></tr></thead><tbody><tr><td><code>wrapper</code></td><td><code>data-gpo-collection-wrapper</code></td><td>The collection section, the area the app watches</td></tr><tr><td><code>item</code></td><td><code>data-gpo-collection-item</code></td><td>One product card inside it</td></tr><tr><td><code>productLink</code></td><td><code>data-gpo-collection-productLink</code></td><td>The link to the product, read to know which product a card is</td></tr><tr><td><code>quickViewActivator</code></td><td><code>data-gpo-collection-qvActivator</code></td><td>The control that opens the quickview, watched so the app knows to render</td></tr><tr><td><code>quickViewProductForm</code></td><td><code>data-gpo-collection-qvForm</code></td><td>The product form inside the quickview, where the options go</td></tr></tbody></table>

## cart

Used on the cart page and in the cart drawer, for editing options and for keeping add-on lines tied to their parent item.

<table><thead><tr><th width="190">Key</th><th width="270">Attribute hook</th><th>What the app does with it</th></tr></thead><tbody><tr><td><code>form</code></td><td><code>data-gpo-cart-form</code></td><td>The cart form. Takes an <strong>array</strong>, tried in order</td></tr><tr><td><code>page</code></td><td>see below</td><td>How to read a line item on the cart page. Takes an <strong>array</strong> of shapes, tried in order</td></tr><tr><td><code>drawer</code></td><td>see below</td><td>The same for the cart drawer</td></tr></tbody></table>

`page` and `drawer` each hold a `lineItem` describing the parts of one cart row:

<table><thead><tr><th width="230">Part</th><th width="300">Attribute hook (cart page)</th><th>What it is</th></tr></thead><tbody><tr><td><code>key</code></td><td><code>data-gpo-cart-item-key</code></td><td>The row itself, carrying the line item key</td></tr><tr><td><code>image</code></td><td><code>data-gpo-cart-item-image</code></td><td>The row's thumbnail</td></tr><tr><td><code>details</code></td><td><code>data-gpo-cart-item-details</code></td><td>The title and properties block, where <strong>Edit Options</strong> is added</td></tr><tr><td><code>quantity.wrapper</code></td><td><code>data-gpo-cart-item-qty-wrapper</code></td><td>The quantity control, hidden on add-on lines</td></tr><tr><td><code>quantity.input</code></td><td><code>data-gpo-cart-item-qty</code></td><td>The quantity field</td></tr><tr><td><code>quantity.decrease</code> / <code>increase</code></td><td><code>data-gpo-cart-item-qty-decrease</code> / <code>-increase</code></td><td>The minus and plus buttons</td></tr><tr><td><code>removeButton</code></td><td><code>data-gpo-cart-item-remove-button</code></td><td>The remove link, hidden on add-on lines</td></tr></tbody></table>

The drawer uses the same parts with `data-gpo-drawer-item-…` instead of `data-gpo-cart-item-…`.

{% hint style="info" %}
These only matter if you use **Hide quantity box and remove button for add-on products** or **Show "Edit Options" button in cart**. With both off, the app does not touch the cart. See [Cart page](../../storefront-display-and-design/cart-page.md).
{% endhint %}

## Notes

* Keys taking an array are tried in order and the first match wins, so you can add yours in front of the defaults rather than replacing them.
* Overriding a selector changes only where the app looks. It does not change what the options collect or how they are priced.
* An override applies to every product page on the store. For one product, target it in the selector itself.
