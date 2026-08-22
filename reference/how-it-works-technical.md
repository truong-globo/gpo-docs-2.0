---
description: >-
  The mechanics behind the widget — where your configuration lives, how it reaches
  the storefront, and why prices are applied at checkout.
icon: gears
---

# How it works in detail

[How the app works](../concepts/how-the-app-works.md) covers the five stages in plain terms. This page goes a level deeper, for when you are diagnosing something odd or working with a developer.

Nothing here needs doing. It is background.

## The pieces

<table><thead><tr><th width="230">Piece</th><th width="250">Lives</th><th>Job</th></tr></thead><tbody><tr><td><strong>The admin app</strong></td><td>Inside Shopify admin</td><td>Where you build option sets and change settings</td></tr><tr><td><strong>The app embed</strong></td><td>In your theme, through Shopify's app embed system</td><td>Loads the widget's script on your storefront</td></tr><tr><td><strong>The app block</strong> (optional)</td><td>In your product template</td><td>Pins the widget to an exact position</td></tr><tr><td><strong>Shop settings metafield</strong></td><td>On your shop, namespace <code>globo_option</code></td><td>Carries your settings and option-set assignments to the storefront without a round trip</td></tr><tr><td><strong>The cart transform function</strong></td><td>A Shopify Function on your store</td><td>Applies add-on prices at checkout</td></tr><tr><td><strong>Line item properties</strong></td><td>On each cart line</td><td>Carry the customer's answers into the order</td></tr></tbody></table>

## Why prices are applied at checkout

This is the part worth understanding, because it explains several things that otherwise look like bugs.

The product page shows a **preview** of what the add-ons will cost. It is calculated in the browser so it can update instantly as the customer chooses. But a price calculated in a browser cannot be trusted — anyone can change it.

So the actual charge is applied by a **Shopify Cart Transform function** running on Shopify's own infrastructure, at checkout. It reads the line item properties on each cart line and adjusts the prices accordingly.

What follows from that:

<table><thead><tr><th width="330">Consequence</th><th>Why</th></tr></thead><tbody><tr><td>Prices cannot be tampered with</td><td>The charge is computed server-side from your configuration, not from anything the browser sent</td></tr><tr><td>The cart page may briefly show pre-transform amounts</td><td>The transform is applied for checkout. Confirm against the checkout total, not an intermediate screen</td></tr><tr><td>Discount interactions need testing</td><td>How a discount code lands relative to the transform depends on how the discount is written. Test your real codes — see <a href="../add-on-pricing/limitations.md">Add-on pricing limitations</a></td></tr><tr><td>Hidden options are not charged</td><td>A hidden option contributes no properties, so there is nothing for the transform to act on</td></tr><tr><td>Third-party cart apps can conflict</td><td>Anything that rewrites cart lines can disturb the properties the transform depends on — see <a href="../integrations/theme-and-third-party-notes.md">Theme and third-party notes</a></td></tr></tbody></table>

## How your configuration reaches the storefront

{% stepper %}
{% step %}
### You save an option set

It is stored against your shop, with its options, values, prices, rules, and translations.
{% endstep %}

{% step %}
### The assignment map is refreshed

Your settings and the map of which option set applies to which products are written to a shop metafield in the `globo_option` namespace. The storefront can read that directly, without waiting on a request to the app.
{% endstep %}

{% step %}
### The storefront loads

The app embed loads the widget script on your product page. It reads the settings and the assignment map, works out whether this product has an option set, and if so renders it.
{% endstep %}

{% step %}
### Rules are evaluated

Product, customer, and country rules decide whether this visitor sees the set. Conditional logic then decides which individual options are visible.
{% endstep %}

{% step %}
### The customer fills it in and adds to cart

Answers become line item properties on the cart line. See [Line item properties](line-item-properties.md).
{% endstep %}

{% step %}
### Checkout applies the prices

The cart transform function computes the real amounts.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
The metafield step is why changes appear quickly but not always instantaneously, and why a hard refresh sometimes shows an update that a cached page did not. If something looks stale for longer than a minute or two, that is worth reporting.
{% endhint %}

## Where the widget gets placed

Two mechanisms, and they are mutually exclusive in practice:

<table><thead><tr><th width="250">Mechanism</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>Automatic placement</strong></td><td>The app finds a suitable anchor in your product form and inserts the widget relative to it, following the <strong>Widget placement</strong> setting</td></tr><tr><td><strong>App block</strong></td><td>You place the block in the theme editor. The widget renders exactly there, and automatic placement stands aside</td></tr></tbody></table>

An app block is worth using on a heavily customised theme, where automatic placement has less to work with. See [Add the app block](../getting-started/add-the-app-block.md) and [Widget placement](../storefront/widget-placement.md).

## What the app is notified about

The app subscribes to a small number of Shopify notifications:

<table><thead><tr><th width="290">Event</th><th>Used for</th></tr></thead><tbody><tr><td>An order is created</td><td>Analytics figures, and running your <a href="../automations/README.md">automation workflows</a></td></tr><tr><td>A theme is created</td><td>Keeping the app-embed status on <strong>Theme Setup</strong> accurate</td></tr><tr><td>The app is uninstalled</td><td>Cleaning up what the app added to your store</td></tr></tbody></table>

## What happens on uninstall

<table><thead><tr><th width="330">Removed automatically by Shopify</th><th>Left in your store</th></tr></thead><tbody><tr><td>The app embed, and anything the app added to your theme</td><td>Automatically generated add-on products — they are ordinary products in your catalogue</td></tr><tr><td>The cart transform function</td><td>Line item properties on existing orders — they are part of that order's record</td></tr><tr><td>The app's access to your store</td><td></td></tr></tbody></table>

There is no theme code to clean up by hand. If you want the generated products gone, filter your products by the tag `globo-product-options` and delete them — but only once no orders depend on them for their records.

See [Permissions and data](permissions-and-data.md) for what happens to your data.

## The Personalizer

The live preview is drawn in the customer's browser onto a canvas, from your background image and your layer configuration. When the customer adds to cart, the finished design is saved and referenced from the cart line so you can produce it.

That is why a Personalizer design survives the order, and why the design in the order is what the customer actually saw. See [Cart and orders](../personalizer/cart-and-orders.md).

## Reading a cart line

If you are debugging with a developer, the useful move is to look at a cart line's properties. Everything the app did on that line is visible there: which option set applied, what the customer answered, and how any add-on was configured to behave.

Full key-by-key breakdown: [Line item properties](line-item-properties.md).

## Next steps

* [Line item properties](line-item-properties.md)
* [Permissions and data](permissions-and-data.md)
* [How pricing is applied](../add-on-pricing/how-pricing-is-applied.md)
