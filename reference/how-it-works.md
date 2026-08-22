---
description: >-
  What happens between you saving an option set and the customer being charged the
  right amount — in plain terms first, then the mechanics.
icon: diagram-project
---

# How the app works

You do not need this page to use the app. It is worth reading once, because it explains four things that otherwise look like faults: why the app embed matters, why the price on the product page is only a preview, why your option details reach the order with no setup, and why a change sometimes needs a refresh to appear.

## The five stages

{% stepper %}
{% step %}
### You build and save an option set

You add options, set prices, and choose which products, customers, and countries the set applies to. When you select **Save**, the app stores it and publishes a copy to your Shopify store as store data, so your storefront can read it without waiting on a server request.

That publish step is why a change shows on your storefront within seconds rather than instantly — and why a hard refresh sometimes helps you see it sooner.
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

When they select **Add to cart**, everything is validated first: required fields, character limits, minimum and maximum selections, allowed file types. If something is wrong, the add is blocked and the error shown — optionally scrolling to the first problem.
{% endstep %}

{% step %}
### The selections travel with the cart line

Everything the customer entered is attached to the cart line as line item properties — Shopify's own mechanism for custom order details. That is why the information then appears, with no further setup from you, on the cart page, the checkout, the order in your Shopify admin, and in order confirmation emails, invoices, and packing slips.

Any add-on backed by a product is added as its own cart line, linked to the main item.

See [Line item properties](line-item-properties.md).
{% endstep %}

{% step %}
### The final price is applied at checkout

A Shopify storefront cannot change what a customer is actually charged — only Shopify can, at checkout. So the app works in two steps: while shopping it shows a *preview* of the total, and at checkout Shopify applies the real prices.

The amount charged always matches the choices made, even though the number on the product page was calculated in the browser. See [Why prices are applied at checkout](#why-prices-are-applied-at-checkout) below.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT-OPTIONAL: concept-flow-diagram | Không phải ảnh app — sơ đồ tự vẽ | Sơ đồ 5 bước: builder → storefront → cart → checkout | Không khoanh vùng, ưu tiên SVG -->

## What this means in practice

<table><thead><tr><th width="330">Because…</th><th>…this happens</th></tr></thead><tbody><tr><td>The app embed is what runs the app</td><td>Nothing appears on the storefront until it is enabled — and it must be enabled again on any new theme you publish</td></tr><tr><td>Option sets are published to your store as store data</td><td>Changes appear within seconds, not instantly. If you do not see one, refresh the page</td></tr><tr><td>Selections become line item properties</td><td>Option details reach the cart, order, invoice, packing slip, and emails with no extra configuration</td></tr><tr><td>Add-on products are separate cart lines</td><td>They can have their own stock, SKU, and weight — and can be merged visually with the main item. See <a href="../add-on-pricing/merge-as-bundle.md">Merge main product and add-ons</a></td></tr><tr><td>Final pricing happens at checkout</td><td>A shopper cannot tamper with add-on prices, and the price shown while shopping is a preview</td></tr><tr><td>Validation runs before add to cart</td><td>The error messages are yours to word — see <a href="../translations/translate-widget-text.md">Translate widget text</a></td></tr></tbody></table>

## What the app does not do

* It does not create Shopify variants. Options sit alongside your product's variants rather than multiplying them, which is how it gets past Shopify's variant limit.
* It does not edit your theme's code. Everything runs through Shopify's theme app extension system.
* It does not change your product prices in Shopify. Add-ons are charged on top at checkout; your product's own price is untouched.

## The pieces

For when you are diagnosing something odd, or working with a developer.

<table><thead><tr><th width="230">Piece</th><th width="250">Lives</th><th>Job</th></tr></thead><tbody><tr><td><strong>The admin app</strong></td><td>Inside Shopify admin</td><td>Where you build option sets and change settings</td></tr><tr><td><strong>The app embed</strong></td><td>In your theme, through Shopify's app embed system</td><td>Loads the widget's script on your storefront</td></tr><tr><td><strong>The app block</strong> (optional)</td><td>In your product template</td><td>Pins the widget to an exact position</td></tr><tr><td><strong>Shop settings metafield</strong></td><td>On your shop, namespace <code>globo_option</code></td><td>Carries your settings and option-set assignments to the storefront without a round trip</td></tr><tr><td><strong>The cart transform function</strong></td><td>A Shopify Function on your store</td><td>Applies add-on prices at checkout</td></tr><tr><td><strong>Line item properties</strong></td><td>On each cart line</td><td>Carry the customer's answers into the order</td></tr></tbody></table>

{% hint style="info" %}
The metafield is why changes appear quickly but not always instantaneously, and why a hard refresh sometimes shows an update a cached page did not. If something looks stale for more than a minute or two, that is worth reporting.
{% endhint %}

## Why prices are applied at checkout

The product page shows a **preview** of what the add-ons will cost. It is calculated in the browser so it can update instantly as the customer chooses. But a price calculated in a browser cannot be trusted — anyone can change it.

So the actual charge is applied by a **Shopify Cart Transform function** running on Shopify's own infrastructure, at checkout. It reads the line item properties on each cart line and adjusts the prices accordingly.

What follows from that:

<table><thead><tr><th width="330">Consequence</th><th>Why</th></tr></thead><tbody><tr><td>Prices cannot be tampered with</td><td>The charge is computed server-side from your configuration, not from anything the browser sent</td></tr><tr><td>The cart page may briefly show pre-transform amounts</td><td>The transform is applied for checkout. Confirm against the checkout total, not an intermediate screen</td></tr><tr><td>Discount interactions need testing</td><td>How a discount code lands relative to the transform depends on how the discount is written. Test your real codes — see <a href="../add-on-pricing/limitations.md">Add-on pricing limitations</a></td></tr><tr><td>Hidden options are not charged</td><td>A hidden option contributes no properties, so there is nothing for the transform to act on</td></tr><tr><td>Third-party cart apps can conflict</td><td>Anything that rewrites cart lines can disturb the properties the transform depends on — see <a href="../integrations/theme-and-third-party-notes.md">Theme and third-party notes</a></td></tr></tbody></table>

## Where the widget gets placed

Two mechanisms, mutually exclusive in practice:

<table><thead><tr><th width="250">Mechanism</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>Automatic placement</strong></td><td>The app finds a suitable anchor in your product form and inserts the widget relative to it, following the <strong>Widget placement</strong> setting</td></tr><tr><td><strong>App block</strong></td><td>You place the block in the theme editor. The widget renders exactly there, and automatic placement stands aside</td></tr></tbody></table>

An app block is worth using on a heavily customised theme, where automatic placement has less to work with. See [Add the app block](../getting-started/add-the-app-block.md) and [Widget placement](../storefront/widget-placement.md).

## The Personalizer

The live preview is drawn in the customer's browser onto a canvas, from your background image and your layer configuration. When the customer adds to cart, the finished design is saved and referenced from the cart line so you can produce it.

That is why a Personalizer design survives the order, and why what you receive is what the customer actually saw. See [Cart and orders](../personalizer/cart-and-orders.md).

## What the app is notified about

<table><thead><tr><th width="290">Event</th><th>Used for</th></tr></thead><tbody><tr><td>An order is created</td><td>Analytics figures, and running your <a href="../automations/README.md">automation workflows</a></td></tr><tr><td>A theme is created</td><td>Keeping the app-embed status on <strong>Theme Setup</strong> accurate</td></tr><tr><td>The app is uninstalled</td><td>Cleaning up what the app added to your store</td></tr></tbody></table>

## What happens on uninstall

<table><thead><tr><th width="330">Removed automatically by Shopify</th><th>Left in your store</th></tr></thead><tbody><tr><td>The app embed, and anything the app added to your theme</td><td>Automatically generated add-on products — they are ordinary products in your catalogue</td></tr><tr><td>The cart transform function</td><td>Line item properties on existing orders — they are part of that order's record</td></tr><tr><td>The app's access to your store</td><td></td></tr></tbody></table>

There is no theme code to clean up by hand. If you want the generated products gone, filter your products by the tag `globo-product-options` and delete them — but only once no orders depend on them for their records.

See [Permissions and data](permissions-and-data.md) for what happens to your data.

## Reading a cart line

If you are debugging with a developer, the useful move is to look at a cart line's properties. Everything the app did on that line is visible there: which option set applied, what the customer answered, and how any add-on was configured to behave.

Full key-by-key breakdown: [Line item properties](line-item-properties.md).
