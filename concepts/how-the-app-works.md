---
description: >-
  What happens between you saving an option set and the customer being charged
  the right amount at checkout.
icon: diagram-project
---

# How the app works

You do not need to know this to use the app. But knowing it explains three things that surprise people: why the app embed matters, why the price on the product page is a preview, and why your option details show up on the order without you doing anything.

## The five stages

{% stepper %}
{% step %}
### You build and save an option set

You add options, set prices, and choose which products, customers, and countries the set applies to. When you select **Save**, the app stores it and publishes a copy of it to your Shopify store as store data, so your storefront can read it without waiting on a server request.

That publish step is why a change you make in the app shows on your storefront within seconds rather than instantly — and why a hard refresh sometimes helps you see it sooner.
{% endstep %}

{% step %}
### The app embed loads on your storefront

The [app embed](../getting-started/enable-the-app-embed.md) is a small piece of the app that your theme loads on every page. On each page it works out which of your option sets apply, by checking:

* the product being viewed
* whether the visitor is logged in, and which customer they are
* which country or market they are shopping from
* whether the option set is **Active** and published to the **Online Store**

If nothing applies, it does nothing and gets out of the way.
{% endstep %}

{% step %}
### The widget renders and the customer fills it in

Matching option sets are rendered as the widget, in the position you chose, styled the way you configured.

As the customer interacts with it, the app also runs:

* **conditional logic** — showing and hiding options as their choices change
* **the live preview** — redrawing their text or uploaded image on the product photo
* **a running price preview** — adding up the add-ons they have selected

When they select **Add to cart**, the app validates everything first: required fields, character limits, minimum and maximum selections, allowed file types, and so on. If something is wrong, the add is blocked and the error is shown — optionally scrolling to the first problem.
{% endstep %}

{% step %}
### The selections travel with the cart line

Everything the customer entered is attached to the cart line as line item properties. That is Shopify's own mechanism for custom order details, which is why the information then appears — with no further setup from you — on:

* the cart page
* the checkout
* the order in your Shopify admin
* order confirmation emails, invoices, and packing slips

Any add-on that is backed by a product is added as its own separate cart line, linked to the main item.

See [Show options on orders](../storefront/show-options-on-orders.md) and [Line item properties](../reference/line-item-properties.md).
{% endstep %}

{% step %}
### The final price is applied at checkout

This is the part worth understanding. A Shopify storefront cannot change what a customer is actually charged — only Shopify can, at checkout. So the app works in two steps:

* **While shopping**, the app shows a *preview* of the total, so the customer can see what their choices cost.
* **At checkout**, Shopify applies the real prices for the add-ons the customer selected, using a secure pricing step that runs on Shopify's side.

The result is that the amount charged always matches the choices made — even though the number shown on the product page was calculated in the browser.

See [How pricing is applied](../add-on-pricing/how-pricing-is-applied.md).
{% endstep %}
{% endstepper %}

## What this means in practice

<table><thead><tr><th width="330">Because…</th><th>…this happens</th></tr></thead><tbody><tr><td>The app embed is what runs the app</td><td>Nothing appears on the storefront until it is enabled — and it must be enabled again on any new theme you publish.</td></tr><tr><td>Option sets are published to your store</td><td>Changes appear on the storefront within seconds, not instantly. If you do not see a change, refresh the page.</td></tr><tr><td>Selections become line item properties</td><td>Option details reach the cart, order, invoice, packing slip, and emails with no extra configuration.</td></tr><tr><td>Add-on products are separate cart lines</td><td>They can have their own stock, SKU, and weight — and they can be merged visually with the main item if you prefer. See <a href="../add-on-pricing/merge-as-bundle.md">Merge main product and add-ons</a>.</td></tr><tr><td>Final pricing happens at checkout</td><td>A shopper cannot tamper with add-on prices in the browser, and the price shown while shopping is a preview.</td></tr><tr><td>Validation runs in the browser before add to cart</td><td>Error messages are yours to word — see <a href="../translations/translate-widget-text.md">Translate widget text</a>.</td></tr></tbody></table>

<!-- SCREENSHOT-OPTIONAL: concept-flow-diagram | Sơ đồ 5 bước từ builder → storefront → cart → checkout. Nếu vẽ thì dùng SVG, không cần screenshot app. -->

## What the app does not do

* It does not create Shopify variants. Options are added alongside your product's variants rather than multiplying them, which is how it gets past Shopify's 100-variant limit.
* It does not edit your theme's code. Everything runs through Shopify's theme app extension system.
* It does not change your product prices in Shopify. Add-ons are charged on top at checkout; your product's own price is untouched.

## Next steps

* [Option sets, options, and values](option-set-option-value.md)
* [How pricing is applied](../add-on-pricing/how-pricing-is-applied.md) — the pricing step in detail.
* [How it works in detail](../reference/how-it-works-technical.md) — the technical version of this page.
