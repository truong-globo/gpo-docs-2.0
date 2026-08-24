---
description: What happens after Add to cart — going straight to the cart, and why it depends on your theme.
icon: right-to-bracket
---

# Ajax cart and redirect to cart

One setting, with a theme dependency worth understanding. **Settings** > **Settings** > **General** > **Product page** > **Go to cart immediately after adding to cart**.

## What it does

<table><thead><tr><th width="180">Default</th><td>On</td></tr></thead></table>

With it on, adding a product with add-ons takes the shopper straight to the cart page instead of leaving them on the product page.

## Why it exists

A personalised product with add-ons is not one thing being added to the cart — it is the main item plus its add-on products, associated with each other.

Most themes have a cart drawer or a small cart notification that expects one simple addition. Sending the shopper to the full cart page instead means they see the complete result: the item, its options, and its add-on lines, all correctly priced.

## When to turn it off

<table><thead><tr><th width="290">Turn it off when</th><th>Leave it on when</th></tr></thead><tbody><tr><td>Your theme's cart drawer handles the addition correctly, and you would rather shoppers kept browsing</td><td>Anything looks wrong in the drawer after adding a product with add-ons</td></tr><tr><td>You have tested it thoroughly with add-ons, on desktop and mobile</td><td>You are not sure. This is the safe setting</td></tr></tbody></table>

Test it properly if you turn it off: add a product with two add-ons, and check the drawer shows every line at the right price. A drawer that silently drops an add-on is worse than a redirect.

## Theme dependency

Whether the cart can be updated without a page reload — and whether the drawer shows the result correctly — depends entirely on how your theme builds its cart.

The app supports this on a wide range of themes. On others the redirect is the reliable path, which is why it is on by default.

{% hint style="info" %}
The setting carries a link to the list of themes where this is supported. That list is maintained as themes are tested, so check it there rather than assuming. If your theme is not covered, [contact support](../help/contact-support.md) — it is usually a small piece of integration.
{% endhint %}

## Related settings

<table><thead><tr><th width="330">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Auto-scroll to first error message</strong></td><td>Same settings group. On by default. When add to cart is blocked, scrolls to the first problem. Keep it on — otherwise a shopper sees nothing happen and assumes the button is broken</td></tr><tr><td><strong>Hide quantity box and remove button for add-on products</strong></td><td>Protects add-on lines once they are in the cart. See <a href="cart-page.md">Cart page</a></td></tr><tr><td><strong>Merge Main product &amp; Add-on products</strong></td><td>Presents add-ons as part of the item. See <a href="../add-on-pricing/merge-as-bundle.md">Merge main product and add-ons</a></td></tr></tbody></table>

## Dynamic checkout buttons

Shopify's accelerated payment buttons — the ones that skip the cart entirely — are a problem for any product with options, because they would bypass the form.

The app hides those buttons where options are present, so shoppers cannot buy without answering. If you rely on those buttons for products **without** options, they continue to work normally there.

## Notes

* Store-wide.
* It applies to products with add-ons. A product with options but no add-ons behaves as your theme normally would.
* It does not affect what is charged or what reaches the order — only where the shopper lands.
