---
description: >-
  Why the product page shows a preview while checkout applies the final price,
  and what that means in practice.
icon: shield-halved
---

# How pricing is applied

The amount displayed beside an option on the product page and the amount the customer is charged are calculated in two different places. This explains several behaviors that might otherwise look like errors.

## The two stages

{% stepper %}
{% step %}
### While shopping: a preview

As the customer makes selections, the app adds up the add-ons and displays the result beside each option, and optionally in the product price.

This calculation runs in the customer's browser. It updates instantly, but it is only a display.
{% endstep %}

{% step %}
### At checkout: the real prices

When the order is placed, Shopify applies the actual add-on prices.

This is the amount the customer is charged. The value displayed in the browser does not affect it.
{% endstep %}
{% endstepper %}

## Why it works this way

A Shopify storefront cannot change the amount a customer is charged. If it could, anyone could edit the page and buy a $500 product for $5.

The app therefore displays a preview in the browser and lets Shopify apply the real price at checkout. This means add-on pricing cannot be changed by the customer, and the amount charged always matches their selections.

## What that explains

<table><thead><tr><th width="330">Behavior</th><th>Reason</th></tr></thead><tbody><tr><td>Add-on products appear as their own cart lines</td><td>That is how a real product is added to a real cart. You can present them as one item — see <a href="merge-as-bundle.md">Merge main product and add-ons</a></td></tr><tr><td>The displayed product price is configurable</td><td>It is a preview, so you choose whether it includes add-ons. See <a href="price-display-settings.md">Add-on price display settings</a></td></tr><tr><td>A customer cannot fiddle the price in their browser</td><td>Editing the preview changes nothing that matters</td></tr><tr><td>The option details travel with the order automatically</td><td>They are attached to the cart line as line item properties, which is Shopify's own mechanism. See <a href="../storefront/show-options-on-orders.md">Show options on orders</a></td></tr><tr><td>Hidden options are not charged</td><td>A hidden option contributes nothing to the cart in the first place</td></tr><tr><td>An <strong>Add price</strong> charge has no separate cart line</td><td>There is no product — the amount is applied to the main item</td></tr></tbody></table>

## Do I need to set anything up?

No. The pricing mechanism is set up for your store automatically the first time the app runs. There is no setting to enable, no installation step, and no change to your theme.

If add-on pricing is not applied at checkout at all, and the amount is genuinely not charged rather than only displayed incorrectly, contact support. See [Contact support](../help/contact-support.md).

## What reaches the order

<table><thead><tr><th width="290">On the order you see</th><th>Where it comes from</th></tr></thead><tbody><tr><td>The main product, at its price plus any <strong>Add price</strong> amounts</td><td>Your product, adjusted at checkout</td></tr><tr><td>The option details, listed under the item</td><td>The customer's choices, as line item properties</td></tr><tr><td>One line per product-backed add-on, at its own price</td><td>The linked or generated products</td></tr><tr><td>A few technical properties linking the add-ons to their parent item</td><td>The app, so the pieces stay associated</td></tr></tbody></table>

For more information, see [Show options on orders](../storefront/show-options-on-orders.md).

## Sync Add-on data

**Sync Add-on data** is available in the builder's more-actions menu. It re-reads the linked and generated products, so the prices and variants shown in the app match Shopify.

Use it when an add-on's price or variant is out of date in the app, for example after editing the product in Shopify admin or after an import. It is safe to run at any time.

## Notes

* Add-on prices are in your store's currency, and are converted for other currencies by Shopify like any other price.
* Discount codes apply to the order as Shopify calculates it, which includes add-on lines.
* Taxes follow each product's own tax settings. Use a product-backed add-on when the tax treatment differs from the main product.
* Shipping calculated by weight uses the add-on products' weights, so set a weight on each one. See [Stock and inventory](stock-and-inventory.md).
