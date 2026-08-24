---
description: >-
  Link an option to a product and variant you already sell, so the add-on inherits
  its price, stock, SKU, and weight.
icon: box
---

# Use an existing product

The **Use existing product** mode connects an option — or one of its values — to a product already in your Shopify catalogue. The add-on then behaves like that product: its price, its stock, its SKU, its weight.

Use it when the add-on is something you genuinely sell. A gift box you list separately, a spare part, a matching accessory.

## Steps

{% stepper %}
{% step %}
### Make sure the product exists

Create it in Shopify first if you need to, with the price and variants you want. The app links to it; it does not create it.
{% endstep %}

{% step %}
### Open the price field

**Price** under **Add-on Settings** for an input type, or the **Price** cell on an option value's row for a selection type.
{% endstep %}

{% step %}
### Stay on the Use existing product tab

It is the first of the three tabs, and the default.
{% endstep %}

{% step %}
### Find and select the product

Search your catalogue by name. The list is paged, so use the search box rather than scrolling for anything but a small catalogue.
{% endstep %}

{% step %}
### Select the variant

Once a product is selected, its variants are listed. Choose the exact one.

This matters: the add-on's price and stock come from the **variant**, not the product. A product with `Small` at $3.00 and `Large` at $5.00 behaves completely differently depending on which you pick.
{% endstep %}

{% step %}
### Select Select

The dialog closes. The values table now shows a **Product** column with a link that opens that product in Shopify admin.
{% endstep %}

{% step %}
### Set how it scales

The **Advanced settings** dropdown on **Advanced Settings** decides how the quantity behaves. See [Advanced add-on modes](advanced-add-on-modes.md).
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: addon-existing-product | App admin → builder → dialog Add-on Configuration | Tab "Use existing product": danh sách sản phẩm có search, đã chọn 1 sản phẩm và đang hiện danh sách variant | Khoanh danh sách variant -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Use existing product tab with a product selected and its variants listed"><figcaption><p>Selecting the right variant matters — price and stock come from the variant.</p></figcaption></figure>

## What you get

<table><thead><tr><th width="290">Behaviour</th><th>Detail</th></tr></thead><tbody><tr><td>The price follows the product</td><td>Change the variant's price in Shopify and the add-on price changes with it. You do not edit it in two places.</td></tr><tr><td>Stock is real</td><td>Selling the add-on draws down that variant's inventory, exactly as a normal sale does.</td></tr><tr><td>Out-of-stock handling works</td><td>The <a href="../option-types/shared-settings/out-of-stock-options.md">Out of stock options</a> setting can hide, blur, or strike through the value when the variant runs out.</td></tr><tr><td>Its own SKU, weight, and tax setting</td><td>Fulfilment and shipping calculations treat it as the real product it is.</td></tr><tr><td>Reported properly</td><td>It appears in your Shopify product reports as sales of that product.</td></tr><tr><td>Works in POS</td><td>Unlike <strong>Add price</strong>.</td></tr><tr><td>Its own cart line</td><td>Linked to the main item. You can merge them visually — see <a href="merge-as-bundle.md">Merge main product and add-ons</a>.</td></tr></tbody></table>

## When to use it, and when not

<table><thead><tr><th width="330">Use it when</th><th>Use something else when</th></tr></thead><tbody><tr><td>You already sell the item separately</td><td>You do not — use <a href="auto-generate-a-product.md">Automatically generate a product</a></td></tr><tr><td>You want one inventory figure for both routes</td><td>You want the add-on counted separately from direct sales</td></tr><tr><td>The price should stay in step with your catalogue</td><td>The add-on price should differ from the shelf price</td></tr><tr><td>The add-on has a real weight and SKU</td><td>It is a service — use <a href="add-price-directly.md">Add price</a></td></tr></tbody></table>

{% hint style="info" %}
One inventory figure is usually what you want — a gift box sold as an add-on and a gift box sold on its own come out of the same cupboard. If you need to count them separately, generate a product instead.
{% endhint %}

## Examples

**A gift box you also sell**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Option</td><td><code>Gift box</code>, a Switch</td></tr><tr><td>Price</td><td><strong>Use existing product</strong> → <em>Gift Box</em> → <em>Medium</em></td></tr><tr><td>Advanced settings</td><td><strong>One time charge</strong> — one box per order</td></tr><tr><td>Out of stock options</td><td>Not applicable on a Switch — but the box's stock still applies</td></tr></tbody></table>

**Pack sizes as separate SKUs**

A [Button](../option-types/selection-types/button.md) option with `1 pack`, `3 pack`, `5 pack`, each value linked to that pack's own product variant. Stock is accurate per pack size.

**Premium fabrics you stock by the metre**

An [Image swatch](../option-types/selection-types/image-swatch.md) with standard fabrics free and premium ones linked to your existing fabric products, so a fabric running out blurs itself in the swatch grid.

**A matching accessory**

A Checkbox `Add the matching case`, linked to the case product, **Default** mode so somebody buying two of the main product gets two cases.

## Keeping it working

<table><thead><tr><th width="290">If you do this in Shopify</th><th>Then</th></tr></thead><tbody><tr><td>Change the variant's price</td><td>Nothing to do — the add-on price follows</td></tr><tr><td>Change its stock</td><td>Nothing to do — availability follows</td></tr><tr><td>Delete the product or variant</td><td><strong>The link breaks.</strong> The app tells you the product or variant no longer exists when you next open the dialog. Relink to something else</td></tr><tr><td>Rename the product</td><td>The link holds — it is not by name</td></tr><tr><td>Unpublish it from the Online Store</td><td>It can no longer be purchased through the widget. Keep add-on products published</td></tr></tbody></table>

## Notes

* Link to a **variant**, not just a product. A product with several variants needs one chosen.
* The same product can back several options and several values. That is fine, and they all share its stock.
* Duplicating an option set does **not** duplicate the linked product — both sets point at the same one and draw down the same stock. See [Duplicate and delete](../option-sets/duplicate-and-delete.md).
* Use **Sync Add-on data** in the builder's more-actions menu if the linked product's details look stale.
