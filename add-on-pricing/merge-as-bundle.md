---
description: Show add-on products as part of the main item in the cart instead of as separate lines.
icon: object-group
---

# Merge main product and add-ons

By default, an add-on backed by a product becomes its own cart line, linked to the main item. That is accurate, and some merchants find it noisy: one bracelet with three add-ons is four lines.

**Merge Main product & Add-on products** presents them as one item instead. New stores start with it **on**, so if you have never touched it, your carts are already merged.

## Where the setting is

**Settings** > **Settings** > **Add-on price**, labelled **Merge Main product & Add-on products**. It is store-wide — it applies to every option set, not one at a time.

<!-- SCREENSHOT: addon-merge-setting | App admin → Settings → Add-on price | Switch "Merge Main product & Add-on products" | Khoanh switch -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The merge main product and add-on products switch in the add-on price settings"><figcaption><p>One switch, applied store-wide.</p></figcaption></figure>

## What changes

<table><thead><tr><th width="230">In the cart</th><th width="230">Off</th><th>On</th></tr></thead><tbody><tr><td>Lines shown</td><td>The main item plus one line per add-on product</td><td>The main item, with its add-ons presented as part of it</td></tr><tr><td>Price shown</td><td>Each line priced separately</td><td>Combined</td></tr><tr><td>Option details</td><td>Listed under the main item</td><td>Listed under the main item</td></tr></tbody></table>

What does **not** change is anything behind the scenes. The add-on products are still real products, their stock is still drawn down, their weight still counts towards shipping, and your Shopify reports still show them as sales of those products.

## Which to choose

<table><thead><tr><th width="290">Leave it off when</th><th>Turn it on when</th></tr></thead><tbody><tr><td>Customers benefit from seeing exactly what they are paying for</td><td>The cart looks cluttered with add-on lines</td></tr><tr><td>Add-ons are substantial items in their own right</td><td>Add-ons are small components of one customised thing</td></tr><tr><td>You want each add-on's price visible in the cart</td><td>You want the cart to read as "one personalised product, one price"</td></tr><tr><td>You are troubleshooting a pricing problem</td><td>Your products are heavily configured, with many add-ons per item</td></tr></tbody></table>

For a made-to-order product with six components, merging is much closer to how the customer thinks about what they are buying. For a bracelet plus a separately-sold gift box, separate lines are more honest.

## Related cart settings

Two other settings shape the cart experience for add-ons. Both are in **Settings** > **Settings** > **General** > **Cart page**.

<table><thead><tr><th width="330">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Hide quantity box and remove button for add-on products</strong></td><td>Stops customers changing or deleting an add-on line independently of the item it belongs to. On by default, and worth leaving on — a customer who removes the gift box but keeps the "gift wrapped" option creates an order you cannot fulfil as described.</td></tr><tr><td><strong>Show "Edit Options" button in cart</strong></td><td>Lets customers reopen the option form from the cart and change their choices. See <a href="../storefront/cart-page.md">Cart page</a>.</td></tr></tbody></table>

## Notes

* Store-wide, not per option set.
* Purely presentational. Stock, weight, tax, and reporting are unaffected.
* Only applies to product-backed add-ons. An [Add price](add-price-directly.md) charge has no separate line to merge in the first place.
* Test on your own cart page after changing it — themes render carts differently, and the result is worth seeing before customers do.

## Troubleshooting

<details>
<summary>Nothing changed after turning it on</summary>

Save the settings, then reload your cart page with an item that actually has a product-backed add-on. A cart whose add-ons all use **Add price** has nothing to merge.
</details>

<details>
<summary>My theme's cart still shows separate lines</summary>

Themes vary in how much of the cart they build themselves. If your theme does not reflect the setting, [contact support](../help/contact-support.md) with your theme name.
</details>

<details>
<summary>Customers are removing add-on lines and breaking their order</summary>

Turn on **Hide quantity box and remove button for add-on products** in **Settings > Settings > General**.
</details>

<details>
<summary>I want this for some products only</summary>

Not possible — the setting is store-wide. Choose whichever suits the majority of your catalogue.
</details>
