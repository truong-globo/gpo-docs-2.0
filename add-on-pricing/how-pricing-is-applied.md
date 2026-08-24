---
description: Why the product page shows a preview and checkout shows the truth — and what that means in practice.
icon: shield-halved
---

# How pricing is applied

The number beside an option on your product page and the number the customer is charged come from two different places. Understanding why explains several behaviours that would otherwise look like bugs.

## The two stages

{% stepper %}
{% step %}
### While shopping: a preview

As the customer makes choices, the app adds up the add-ons and shows the result — beside each option, and optionally in the product price itself.

This runs in the shopper's browser. It is fast, it updates instantly, and it is only a display.
{% endstep %}

{% step %}
### At checkout: the real prices

When the order goes through, Shopify applies the actual add-on prices, on Shopify's own side.

This is where the money is decided. Whatever was shown in the browser has no authority over it.
{% endstep %}
{% endstepper %}

## Why it works this way

A Shopify storefront cannot change what a customer is charged. If it could, anybody could edit the page and buy a $500 product for $5.

So the app does what every well-behaved Shopify app does: it previews in the browser and lets Shopify apply the real price at checkout. The result is that add-on pricing cannot be tampered with, and the amount charged always matches the choices made.

## What that explains

<table><thead><tr><th width="330">Behaviour</th><th>Reason</th></tr></thead><tbody><tr><td>Add-on products appear as their own cart lines</td><td>That is how a real product is added to a real cart. You can present them as one item — see <a href="merge-as-bundle.md">Merge main product and add-ons</a></td></tr><tr><td>The displayed product price is configurable</td><td>It is a preview, so you choose whether it includes add-ons. See <a href="price-display-settings.md">Add-on price display settings</a></td></tr><tr><td>A shopper cannot fiddle the price in their browser</td><td>Editing the preview changes nothing that matters</td></tr><tr><td>The option details travel with the order automatically</td><td>They are attached to the cart line as line item properties, which is Shopify's own mechanism. See <a href="../storefront/show-options-on-orders.md">Show options on orders</a></td></tr><tr><td>Hidden options are not charged</td><td>A hidden option contributes nothing to the cart in the first place</td></tr><tr><td>An <strong>Add price</strong> charge has no separate cart line</td><td>There is no product — the amount is applied to the main item</td></tr></tbody></table>

## Do I need to set anything up?

No. The pricing mechanism is prepared for your store automatically, in the background, the first time the app runs. There is no switch, no installation step, and nothing on the theme side.

If add-on pricing is not being applied at checkout at all — not a display problem but genuinely not charged — that is worth reporting rather than working around. See [Contact support](../help/contact-support.md).

## What reaches the order

<table><thead><tr><th width="290">On the order you see</th><th>Where it comes from</th></tr></thead><tbody><tr><td>The main product, at its price plus any <strong>Add price</strong> amounts</td><td>Your product, adjusted at checkout</td></tr><tr><td>The option details, listed under the item</td><td>The customer's choices, as line item properties</td></tr><tr><td>One line per product-backed add-on, at its own price</td><td>The linked or generated products</td></tr><tr><td>A few technical properties linking the add-ons to their parent item</td><td>The app, so the pieces stay associated</td></tr></tbody></table>

Full detail on the last one: [Line item properties](../storefront/show-options-on-orders.md).

## Sync Add-on data

The builder's more-actions menu has **Sync Add-on data**. It re-reads the linked and generated products so the app's view of their prices and variants matches Shopify.

Use it when an add-on's price or variant looks stale in the app — for example after editing the product in Shopify admin, or after an import. It is safe to run at any time.

## Notes

* Add-on prices are in your store's currency, and are converted for other currencies by Shopify like any other price.
* Discount codes apply to the order as Shopify calculates it, which includes add-on lines.
* Taxes follow each product's own tax settings. That is one reason to prefer product-backed add-ons where tax treatment differs.
* Shipping calculated by weight uses the add-on products' weights, so set them. See [Stock and inventory](stock-and-inventory.md).
