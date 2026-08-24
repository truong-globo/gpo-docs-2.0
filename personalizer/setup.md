---
description: >-
  The background, the layers, and the order to build them in — everything between
  a plain product photo and a working live preview.
icon: sliders
---

# Set up the Personalizer

Two things make a live preview: a **background** and one or more **layers**.

The background belongs to the **option set**. The layers belong to individual **options**. That single fact decides the order of work — layer positions are measured against the background, so choosing the background afterwards means positioning everything twice.

## The three parts

<table><thead><tr><th width="180">Part</th><th width="230">What it is</th><th>Where you set it</th></tr></thead><tbody><tr><td><strong>The background</strong></td><td>The image the layers are drawn on — a product photo, or an image you upload</td><td>Once per option set, from the builder's preview panel</td></tr><tr><td><strong>The layers</strong></td><td>One per option with the Personalizer turned on. Text or image</td><td>Per option, on its <strong>Personalizer Settings</strong> tab</td></tr><tr><td><strong>Customer controls</strong></td><td>Which layers the shopper may move, resize, or rotate themselves</td><td>Per option, per layer</td></tr></tbody></table>

On the storefront these combine into one thing: the product photo with the customer's content drawn on it, redrawing as they type or choose, with no reload and no button to press.

## The order to work in

{% stepper %}
{% step %}
### Set the background

In the builder's preview panel, select **Change background**. Full detail in [Choosing the background](#choosing-the-background) below.

Everything else is positioned against this image, so it comes first.
{% endstep %}

{% step %}
### Build the options normally

Labels, limits, prices, conditional logic. Do the ordinary option work before the personalisation work — see [Build your options](../option-sets/build-options.md).
{% endstep %}

{% step %}
### Turn the Personalizer on for each option

The **Personalizer Settings** tab, then **Enable personalize**. See [Turning it on for an option](#turning-it-on-for-an-option) below.
{% endstep %}

{% step %}
### Style each layer

Colour, size, style, font, and effects for text; shape and fit mode for images. See [Text layers](layer-settings/text-layers.md), [Fonts](layer-settings/fonts.md), [Text effects](layer-settings/effects.md), and [Image layers](layer-settings/image-layers.md).
{% endstep %}

{% step %}
### Position each layer

Set the axes and, where the type offers it, the size. Then check a very long entry and a very short one. See [Position, size, and rotation](layer-settings/position-size-rotation.md).
{% endstep %}

{% step %}
### Decide what the customer may adjust

[Customer controls](layer-settings/customer-controls.md) — and a [clip area](layer-settings/clip-area.md) if you are giving them any freedom at all, so they cannot place a design where you cannot print.
{% endstep %}

{% step %}
### Test on a real product page

**View in Store**, with an entry a real customer would type — a full name, not `test`. Check it on a phone too.
{% endstep %}
{% endstepper %}

## Choosing the background

**Change background** in the preview panel opens a panel with two decisions: which image, and which of the product's images it applies to.

<!-- SCREENSHOT: pp-background-panel | App admin → builder → preview → Change background | Panel với nhóm Background (Product image/Custom image) và Apply to (4 lựa chọn) | Khoanh 2 nhóm lựa chọn -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The background panel with the Background and Apply to choices"><figcaption><p>Two decisions: which image, and which of the product's images it applies to.</p></figcaption></figure>

### Product image or custom image

<table><thead><tr><th width="200">Choice</th><th width="250">What it uses</th><th>Best for</th></tr></thead><tbody><tr><td><strong>Product image</strong></td><td>The product's own photographs. You also pick a product to preview against while you work in the builder; on the storefront each shopper's actual product is used</td><td>Almost everything. One option set works across a whole catalogue, and every product shows its own photo</td></tr><tr><td><strong>Custom image</strong></td><td>One image you upload, used for every product this option set applies to</td><td>Products that photograph badly for personalisation, or where a clean mock-up sells better than the real photo</td></tr></tbody></table>

Selecting **Custom image** also reveals the **When to replace product image** setting.

### Apply to: which of the product images

With **Product image** selected, this decides which photograph carries the personalisation.

<table><thead><tr><th width="250">Choice</th><th width="200">Behaviour</th><th>Use when</th></tr></thead><tbody><tr><td><strong>All product images</strong></td><td>Every image gets the layers</td><td>All your photographs show the same personalisable face</td></tr><tr><td><strong>First product image only</strong></td><td>Only the first</td><td>The first image is your clean front-on shot and the rest are details</td></tr><tr><td><strong>Last product image only</strong></td><td>Only the last</td><td>You keep a dedicated personalisation mock-up at the end of the gallery</td></tr><tr><td><strong>Specific product image</strong></td><td>The one at the position number you enter</td><td>Your personalisable shot is always, say, the third image</td></tr></tbody></table>

{% hint style="warning" %}
**All product images** is rarely right. A layer positioned for the front-on shot lands in the wrong place on a close-up or a lifestyle photo, and the result looks broken.

Pick a single image, and keep that image in the same gallery position across your products. **First product image only** with a consistent front-on shot is the most reliable arrangement. **Specific product image** relies on your galleries being ordered identically — check a few products before trusting it.
{% endhint %}

### When to replace product image

Appears only with **Custom image** selected. It decides when the shopper sees your uploaded image instead of the product photo.

<table><thead><tr><th width="250">Choice</th><th width="230">Behaviour</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Immediately on page load</strong></td><td>Your image is shown from the start</td><td>The mock-up is the best sales image you have</td></tr><tr><td><strong>Only after personalization</strong></td><td>The product photo shows first; your image appears once they start personalising</td><td>The real photograph sells better, and the mock-up is only there to show their design</td></tr></tbody></table>

**Only after personalization** is usually better: shoppers see the real product first, and the mock-up appears exactly when it becomes useful.

### What makes a good background

The preview is only as convincing as this image.

<table><thead><tr><th width="290">Do</th><th>Avoid</th></tr></thead><tbody><tr><td>A flat, front-on view of the surface being personalised</td><td>Angled or three-quarter shots — flat text on a perspective surface looks wrong</td></tr><tr><td>Even, diffuse lighting</td><td>Strong shadows or highlights across the personalisation area</td></tr><tr><td>A plain area where the text will sit</td><td>Busy patterns behind the text</td></tr><tr><td>Consistent framing across your products</td><td>Different crops per product, when one option set covers many</td></tr><tr><td>Large enough to stay sharp on a big screen</td><td>Small images that soften when scaled up</td></tr></tbody></table>

If your products are photographed at an angle, a flat-shot **Custom image** mock-up is less authentic but far more convincing.

## Turning it on for an option

Open the option, go to the **Personalizer Settings** tab — beside **Basic Settings** and **Advanced Settings** — and turn on **Enable personalize**. Nothing else on the tab appears until you do.

The tab only exists on the [twelve supported types](README.md#the-twelve-supported-option-types). If it is missing, the type does not support it; if it is greyed out, the Personalizer is not in your plan.

<!-- SCREENSHOT: pp-enable-tab | App admin → builder → option Text → tab Personalizer Settings | Switch "Enable personalize" đã bật, các nhóm setting hiện ra bên dưới | Khoanh switch -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Personalizer Settings tab with Enable personalize turned on and its settings revealed"><figcaption><p>Nothing on the tab appears until the switch is on.</p></figcaption></figure>

### What you get, by option type

The settings offered depend on whether the option produces text or an image.

<table><thead><tr><th width="290">Setting group</th><th width="230">Text, Textarea, Number</th><th>File upload and the eight selection types</th></tr></thead><tbody><tr><td>Colour, font size, font style, font family</td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Text alignment</td><td>Textarea only</td><td>No</td></tr><tr><td>Text effects</td><td><strong>Yes</strong></td><td>No</td></tr><tr><td>Curve and auto-fit max width</td><td>Text and Number only</td><td>No</td></tr><tr><td>Image shape and background mode</td><td>No</td><td><strong>Yes</strong></td></tr><tr><td>Width and height</td><td>Textarea only</td><td><strong>Yes</strong></td></tr><tr><td>X-Axis, Y-Axis, opacity, rotation</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td></tr><tr><td>Clip area</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td></tr><tr><td>Allow customers to</td><td><strong>Yes</strong></td><td><strong>Yes</strong></td></tr></tbody></table>

The pattern: Text and Number are single lines, so they get curve and auto-fit instead of width and height. Textarea is a block, so it gets alignment, width, and height. Image types get shape and fit mode.

### Always give a text layer a default value

A text layer with nothing in it draws nothing, so the page looks broken until the customer types.

Set a **Default value** on **Basic Settings** — `Your name`, `Your text` — and the preview always has something to show. It is the single most effective thing you can do to make a personalised product page look finished.

The default is also what the customer submits if they change nothing, so choose something sensible.

## Several personalised options on one product

Normal, and where most of the design effort goes. Layers are drawn together on one background, and they can overlap.

<table><thead><tr><th width="290">Combination</th><th>What to watch</th></tr></thead><tbody><tr><td>A name and a date</td><td>Different <strong>Y-Axis</strong> values so they sit on separate lines</td></tr><tr><td>Text over an uploaded photo</td><td>Contrast — dark text on a dark photo disappears. Consider a <a href="layer-settings/effects.md">stroke effect</a></td></tr><tr><td>Two alternative designs, never both</td><td><a href="../conditional-logic/README.md">Conditional logic</a>, so only one is ever visible</td></tr><tr><td>Layers that must stay inside a printable area</td><td>Give each one a <a href="layer-settings/clip-area.md">clip area</a></td></tr><tr><td>Many layers</td><td>Performance on older phones. Keep it to what the product really needs</td></tr></tbody></table>

A hidden option draws no layer, which makes conditional logic the clean way to switch between alternative designs.

## What the preview is, and is not

<table><thead><tr><th width="290">It is</th><th>It is not</th></tr></thead><tbody><tr><td>A representation of the finished product, good enough to sell from</td><td>A print-ready proof</td></tr><tr><td>Live, updating as the customer types</td><td>Colour-accurate — screens are not calibrated</td></tr><tr><td>A record of what the customer intended</td><td>A guarantee that production will match it exactly</td></tr></tbody></table>

Say so where it matters. A line of [help text](../option-types/shared-settings/placeholder-and-help-text.md#help-text) — "the preview is a guide; final placement may vary slightly" — prevents disputes about millimetres.

## Notes

* One background per option set. Products needing very different framing want separate option sets — see [Assign to products](../option-sets/assign-to-products.md).
* Layer positions are percentages rather than pixels, so a layer holds its relative place at any display size — but only if your product photography is framed consistently.
* The builder preview uses the product you selected under **Change background**; the storefront uses the shopper's actual product.
* A custom background image is uploaded to your store's files.
* Turning the Personalizer off leaves the option working normally — it just stops drawing. Nothing else is lost.
* Layer settings are per option, so the same option type can be configured differently in two places.
* The customer's text or file reaches the order either way. What the Personalizer adds is the visual design record — see [Designs in cart and orders](cart-and-orders.md).

Anything not behaving as described here is covered by symptom in [Troubleshooting personalizer](troubleshooting.md).
