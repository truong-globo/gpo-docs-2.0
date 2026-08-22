---
description: Choose which image the personalisation is drawn on, which product images it applies to, and when it replaces the product photo.
icon: image
---

# Set the preview background

The background is the image your layers are drawn onto. It belongs to the **option set**, so every personalised option in that set uses the same one.

Set it before you position anything. Changing it later means repositioning every layer.

## Where it is

In the builder's preview panel, select **Change background**. A panel opens with two choices and their settings.

<!-- SCREENSHOT: pp-background-panel | App admin → builder → preview → Change background | Panel với nhóm Background (Product image/Custom image) và Apply to (4 lựa chọn) | Khoanh 2 nhóm lựa chọn -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The background panel with the Background and Apply to choices"><figcaption><p>Two decisions: which image, and which of the product's images it applies to.</p></figcaption></figure>

## Background: product image or custom image

<table><thead><tr><th width="230">Choice</th><th>What it uses</th><th>Best for</th></tr></thead><tbody><tr><td><strong>Product image</strong></td><td>The product's own photographs</td><td>Almost everything. The customer sees personalisation on the actual product they are buying</td></tr><tr><td><strong>Custom image</strong></td><td>An image you upload once, used for every product in this option set</td><td>A shared mock-up or template that suits many products</td></tr></tbody></table>

### Product image

The recommended choice. With it selected you also pick a product to preview against while you work in the builder, so you can position layers accurately.

On the storefront the customer's own product's images are used — so one option set works across a whole catalogue, and each product shows its own photograph.

### Custom image

You upload one image, and it is used for every product this option set applies to.

Use it when your products photograph badly for personalisation, or when a clean template mock-up sells better than the real photo. Selecting it also reveals the **When to replace product image** setting below.

## Apply to: which of the product images

With **Product image** selected, this decides which of the product's photographs carries the personalisation.

<table><thead><tr><th width="290">Choice</th><th>Behaviour</th><th>Use when</th></tr></thead><tbody><tr><td><strong>All product images</strong></td><td>Every image gets the layers</td><td>All your photographs show the same personalisable face</td></tr><tr><td><strong>First product image only</strong></td><td>Only the first</td><td>The first image is your clean front-on shot and the rest are details</td></tr><tr><td><strong>Last product image only</strong></td><td>Only the last</td><td>You keep a dedicated personalisation mock-up at the end of the gallery</td></tr><tr><td><strong>Specific product image</strong></td><td>The one at the position you enter</td><td>Your personalisable shot is always, say, the third image</td></tr></tbody></table>

{% hint style="warning" %}
**All product images** is rarely right. A layer positioned for the front-on shot lands in the wrong place on a close-up or a lifestyle photo, and the result looks broken.

Pick a single image, and keep that image in the same position in the gallery across your products. **First product image only** with a consistent front-on shot is the most reliable arrangement.
{% endhint %}

**Specific product image** takes a position number. It relies on your product galleries being ordered consistently — worth checking across a few products before you rely on it.

## When to replace product image

This appears only with **Custom image** selected. It decides when the shopper sees your uploaded image instead of the product photo.

<table><thead><tr><th width="290">Choice</th><th>Behaviour</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Immediately on page load</strong></td><td>Your image is shown from the start</td><td>The mock-up is the best sales image you have</td></tr><tr><td><strong>Only after personalization</strong></td><td>The product photo shows first; your image appears once they start personalising</td><td>The real photograph sells better, and the mock-up is only for showing their design</td></tr></tbody></table>

**Only after personalization** is usually the better choice. Shoppers see the real product first, and the mock-up appears exactly when it becomes useful.

## Choosing a good background image

The preview is only as convincing as this image.

<table><thead><tr><th width="290">Do</th><th>Avoid</th></tr></thead><tbody><tr><td>A flat, front-on view of the surface being personalised</td><td>Angled or three-quarter shots — flat text on a perspective surface looks wrong</td></tr><tr><td>Even, diffuse lighting</td><td>Strong shadows or highlights across the personalisation area</td></tr><tr><td>A plain area where the text will sit</td><td>Busy patterns behind the text</td></tr><tr><td>Consistent framing across your products</td><td>Different crops per product, if one option set covers many</td></tr><tr><td>Large enough to look sharp on a big screen</td><td>Small images that soften when scaled up</td></tr></tbody></table>

If your products are photographed at an angle, consider a **Custom image** mock-up shot flat instead. It is less authentic but far more convincing.

## Notes

* One background per option set. Products needing very different framing want separate option sets — see [Assign to products](../option-sets/assign-to-products.md).
* Layer positions are percentages, so they hold as the image scales — but only if the framing is consistent.
* The builder preview uses the product you selected here; the storefront uses the shopper's actual product.
* A custom background image is uploaded to your store's files.

## Troubleshooting

<details>
<summary>The preview has no background</summary>

No background is configured. Open **Change background** and choose one.
</details>

<details>
<summary>My layers are in the wrong place on some products</summary>

Their photographs are framed differently, or the gallery order varies. Standardise the images, switch to **First product image only**, or split the products into separate option sets.
</details>

<details>
<summary>Personalisation appears on close-up photos where it makes no sense</summary>

You are on **All product images**. Choose a single image instead.
</details>

<details>
<summary>The custom image never appears</summary>

Check **When to replace product image**. On **Only after personalization** it waits until the shopper enters something.
</details>

<details>
<summary>Specific product image picks the wrong photo</summary>

The position number counts through the product's gallery, and your galleries are not consistently ordered. Reorder them, or use first or last.
</details>

<details>
<summary>The preview looks soft or pixelated</summary>

The background image is too small for the size it is displayed at. Upload a larger one.
</details>
