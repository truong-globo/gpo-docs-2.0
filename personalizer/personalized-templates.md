---
description: Twenty ready-made personalised option sets, already positioned — the fastest way to a working setup.
icon: layer-group
---

# Personalized templates

The app ships with twenty complete personalised option sets. Each one has its options, its background, and its layers already positioned for a particular kind of product.

Adapting one is much faster than starting from an empty canvas, and it shows you how a working setup is put together.

## Where they are

**Templates** in the app menu, then the **Personalized Templates** tab.

The other two tabs are [Pre-designed templates](../templates/pre-designed-templates.md), which are option sets without personalisation, and [Custom templates](../templates/custom-templates.md), which are your own.

<!-- SCREENSHOT: pp-templates-tab | App admin → Templates → tab Personalized Templates | Grid các template có ảnh xem trước và nút Use template | Không khoanh -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Personalized Templates tab showing the available template cards"><figcaption><p>Twenty personalised setups, each with a preview and a demo.</p></figcaption></figure>

## The twenty

<table><thead><tr><th width="290">Template</th><th>Product it is built for</th></tr></thead><tbody><tr><td>Personalized Photo Frame</td><td>A frame with a customer photo</td></tr><tr><td>Custom Picture Frames</td><td>A frame with size and mount choices</td></tr><tr><td>Custom Couple Mugs</td><td>Mugs with names, curved to the surface</td></tr><tr><td>Personalized Broken Heart Pendant Necklace</td><td>A two-part engraved pendant</td></tr><tr><td>Personalized Birthstone Pendant</td><td>A pendant with a stone choice and engraving</td></tr><tr><td>Custom T-Shirts</td><td>Printed text and artwork on a garment</td></tr><tr><td>Custom Football Jerseys</td><td>A name and number on a shirt</td></tr><tr><td>Custom Phone Case</td><td>An uploaded image on a case</td></tr><tr><td>Embroidered Bag</td><td>An embroidered name or initials</td></tr><tr><td>Personalized Wooden Bears Family</td><td>Several names on a multi-part item</td></tr><tr><td>Custom LED Acrylic Light Stands</td><td>Engraved text on an illuminated panel</td></tr><tr><td>Unisex Crocs Classic</td><td>Personalised footwear</td></tr><tr><td>Personalised Tie</td><td>An embroidered monogram</td></tr><tr><td>Custom Notebook</td><td>A name on a cover</td></tr><tr><td>Engraved Pen</td><td>A short engraving on a small surface</td></tr><tr><td>Personalized Cushion</td><td>Printed text and images on fabric</td></tr><tr><td>Personalised Wooden Serving Platter</td><td>Engraving on wood</td></tr><tr><td>Personalised BBQ Fork</td><td>A short engraving on a narrow surface</td></tr><tr><td>Personalised Trophy Gold</td><td>Engraved presentation text</td></tr><tr><td>Personalised Wooden Ramp Racer Toy</td><td>A name on a toy</td></tr></tbody></table>

## Using one

{% stepper %}
{% step %}
### Look at the demo first

Each template offers a demo so you can see the finished behaviour on a storefront before committing.
{% endstep %}

{% step %}
### Select Use template

A new option set is created from it, and the builder opens.
{% endstep %}

{% step %}
### Rename it

Give it a name that describes your products rather than the template.
{% endstep %}

{% step %}
### Replace the background with your own product

This is the step that matters most. The template is positioned against its own demo image, so the layers will not line up with your photograph.

Open **Change background**, select **Product image**, and choose one of your own products. See [Set the preview background](set-the-background.md).
{% endstep %}

{% step %}
### Reposition every layer

Go through each personalised option and adjust its position and size against your image. This is the real work, and it is much less than building from scratch.
{% endstep %}

{% step %}
### Adjust the options themselves

Your character limits, your fonts, your prices. Templates carry example values that are almost certainly not yours.
{% endstep %}

{% step %}
### Assign it to your products

On **Assign products**. A template arrives with no product rule — see [Assign to products](../option-sets/assign-to-products.md).
{% endstep %}

{% step %}
### Save, activate, and test on a real product page

With **View in Store**.
{% endstep %}
{% endstepper %}

## What to check after using a template

<table><thead><tr><th width="290">Check</th><th>Why</th></tr></thead><tbody><tr><td>The background is your product</td><td>Otherwise every layer is positioned for somebody else's photograph</td></tr><tr><td>Every layer's position</td><td>The single biggest source of "the template looks wrong"</td></tr><tr><td>Character limits</td><td>The template's limit reflects its example product, not your engraving area</td></tr><tr><td>Fonts</td><td>Change them to fonts you can actually produce. See <a href="fonts.md">Fonts</a></td></tr><tr><td>Prices</td><td>Templates carry example prices, or none</td></tr><tr><td>Option <strong>Name</strong> fields</td><td>So your orders read properly. See <a href="../concepts/label-vs-name.md">Label vs Name</a></td></tr><tr><td>The product rule</td><td>A template arrives unassigned</td></tr></tbody></table>

## Choosing which template to start from

Pick by **shape of the problem**, not by product name. If you sell engraved hip flasks, the closest template is not the one named after a flask — it is whichever has a short engraving on a small curved surface, which is probably the pen or the BBQ fork.

<table><thead><tr><th width="290">Your product needs</th><th>Start from</th></tr></thead><tbody><tr><td>A customer photo in a window</td><td>Personalized Photo Frame, Custom Phone Case</td></tr><tr><td>Text curved around a surface</td><td>Custom Couple Mugs</td></tr><tr><td>A name and a number</td><td>Custom Football Jerseys</td></tr><tr><td>A short engraving on a small area</td><td>Engraved Pen, Personalised BBQ Fork</td></tr><tr><td>Several names on one item</td><td>Personalized Wooden Bears Family</td></tr><tr><td>Text plus artwork on fabric</td><td>Custom T-Shirts, Personalized Cushion</td></tr></tbody></table>

## Notes

* Using a template creates a new option set. It does not modify the template, and you can use the same one repeatedly.
* Templates arrive as **Draft** with no product rule, so nothing reaches your storefront until you set that up.
* Personalized templates need the Personalizer on your plan. Without it the option sets are created but the layers do not draw.
* Once you have adapted one to your products, save it as a [custom template](../templates/custom-templates.md) so your next product starts from your version rather than ours.

## Troubleshooting

<details>
<summary>The layers are in the wrong place</summary>

Expected — they were positioned against the template's own demo image. Change the background to your product and reposition.
</details>

<details>
<summary>Nothing is drawn on the product photo</summary>

Either no background is configured, or the Personalizer is not on your plan.
</details>

<details>
<summary>The template has options I do not need</summary>

Delete them. It is an ordinary option set once created.
</details>

<details>
<summary>Nothing appears on my storefront</summary>

The template has no product rule and is created as **Draft**. Assign products and set it to **Active**.
</details>

<details>
<summary>I want my adapted version as a starting point next time</summary>

Save it as a custom template. See [Custom templates](../templates/custom-templates.md).
</details>

## Next steps

* [Walkthrough: custom printed mug](walkthrough-custom-mug.md) — the same job done by hand.
* [Templates](../templates/README.md)
* [Set the preview background](set-the-background.md)
