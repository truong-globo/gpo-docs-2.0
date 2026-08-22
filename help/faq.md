---
description: Short answers to the questions merchants ask most, grouped by subject.
icon: circle-question
---

# FAQ

Short answers, each linking to the full page. If you are chasing a specific fault, start with [Options are not showing up](troubleshooting-not-showing.md) instead.

## Getting started

<details>
<summary>Do I need to edit my theme code?</summary>

No. The app installs through Shopify's app embed system, which requires no code editing. Turning it on takes about thirty seconds — see [Enable the app embed](../getting-started/enable-the-app-embed.md).

You only touch code if you want option details printed on packing slips, which needs a small snippet in that template. See [Show options on orders](../storefront/show-options-on-orders.md).

</details>

<details>
<summary>Will uninstalling the app leave code behind in my theme?</summary>

No. The app embed is Shopify's own mechanism — removing the app removes it. There is nothing to clean up.

</details>

<details>
<summary>Will it work with my theme?</summary>

The app is built for Online Store 2.0 themes, which covers everything in Shopify's current theme store and most themes sold elsewhere. **Match theme style** has ready-made styling for a long list of popular themes, and falls back to your theme's own fonts and colours for the rest. See [Supported themes](../reference/supported-themes.md).

</details>

<details>
<summary>Does it slow my store down?</summary>

The widget loads with the page and renders once the page is interactive. If it appears noticeably late, a speed-optimisation app is usually deferring its scripts — see [Theme and third-party notes](../integrations/theme-and-third-party-notes.md).

</details>

<details>
<summary>What is the difference between the app embed and the app block?</summary>

The **app embed** switches the app on for a theme. Nothing works without it.

The **app block** is optional, and pins the widget to an exact spot in your product template. Without it, the app places the widget automatically. See [Add the app block](../getting-started/add-the-app-block.md).

</details>

## Option sets and options

<details>
<summary>How many option sets can I have?</summary>

Depends on your plan. Check **Pricing** in the app for the limits on each.

</details>

<details>
<summary>How many options can one set have?</summary>

There is no practical limit on the count. Very long forms are worth splitting with [sections](../option-sets/build-options.md#sections) and [conditional logic](../conditional-logic/README.md) so shoppers see only what applies to them.

</details>

<details>
<summary>Can two option sets apply to the same product?</summary>

Yes, and both render. That is often not what people intend — if options are appearing twice, this is why. See [Manage option sets](../option-sets/manage-option-sets.md).

</details>

<details>
<summary>What is the difference between Label and Name?</summary>

**Label** is what the shopper reads on the page. **Name** is what appears on the cart, the order, and your paperwork. They can differ, which is useful when the shopper-facing wording is long. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).

</details>

<details>
<summary>Can I reorder options after building them?</summary>

Yes, by dragging. One caveat: conditional logic can only reference options **above** the one being configured, so moving an option upwards can break rules that pointed at it. See [Build a condition](../conditional-logic/build-a-condition.md).

</details>

<details>
<summary>Can I copy an option set to another store?</summary>

Export it to CSV from one store and import it into the other. See [Import and export](../option-sets/import-and-export.md).

</details>

<details>
<summary>Can I import from another options app?</summary>

Yes — the importer reads files exported from several other option apps as well as its own format. See [Import and export](../option-sets/import-and-export.md).

</details>

## Add-on pricing

<details>
<summary>What is the difference between the three add-on modes?</summary>

* **Add price** — money is added, no product exists. Simplest; no stock, no POS.
* **Use existing product** — links to something you already sell. Real stock, real SKU.
* **Automatically generate a product** — the app makes the product for you. Real stock without building it by hand.

See [Add-on pricing](../add-on-pricing/README.md).

</details>

<details>
<summary>Which should I use?</summary>

Services — **Add price**. Something you already sell — **Use existing product**. Anything else physical — **Automatically generate a product**. Anything sold in person — never **Add price**.

</details>

<details>
<summary>Why is gift wrap being charged five times?</summary>

The add-on is on **Default** mode, which follows the product quantity. Switch it to **One time charge**. See [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md).

</details>

<details>
<summary>Can I charge by the letter?</summary>

Yes — **Per character** mode on a Text or Textarea option. Always pair it with a **Max character** limit.

</details>

<details>
<summary>Can I price by size?</summary>

Yes — the [Dimension](../option-types/input-types/dimension.md) type with a formula. See [Dimension add-on formula](../add-on-pricing/dimension-formula.md).

</details>

<details>
<summary>Can I offer a discount rather than a surcharge?</summary>

No. Negative amounts are rejected. Set the base product price at the higher figure and charge nothing for the cheaper choice instead.

</details>

<details>
<summary>Can I hide the add-on lines in the cart?</summary>

Turn on **Merge Main product & Add-on products**, which presents them as one item. New stores start with it on. See [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).

</details>

<details>
<summary>Do Shopify discount codes apply to add-ons?</summary>

Behaviour depends on how the discount is written and which mode the add-on uses. Test your actual codes against a real order before relying on it — see [Add-on pricing limitations](../add-on-pricing/limitations.md).

</details>

<details>
<summary>Why do generated products appear in my collections?</summary>

They are published so they can be bought. Exclude the tag `globo-product-options` from those collections. Do not unpublish them — an unpublished product cannot be added to the cart. See [Automatically generate a product](../add-on-pricing/auto-generate-a-product.md).

</details>

## Conditional logic

<details>
<summary>Can options react to a Shopify variant?</summary>

Yes. Alongside conditions on your own options, you can build conditions on the product's Shopify variants — so choosing `Large` in your theme's variant picker can reveal an option in the app's widget. See [Conditions on Shopify variants](../conditional-logic/conditions-on-shopify-variants.md).

</details>

<details>
<summary>Can an option depend on one below it?</summary>

No. Rules can only reference options **above** the one being configured, because the form is evaluated top to bottom. Reorder them. See [Build a condition](../conditional-logic/build-a-condition.md).

</details>

<details>
<summary>Is a hidden required option still enforced?</summary>

No — hidden options are skipped by validation, deliberately. Otherwise a hidden required field would make the product unbuyable.

</details>

<details>
<summary>Is a hidden option still charged?</summary>

No. Hiding an option removes its add-on charge.

</details>

<details>
<summary>Why can't I add conditional logic to this option?</summary>

A few types cannot be the **target** of a rule, and a few cannot be used as a **source**. See [Operators reference](../conditional-logic/operators-reference.md).

</details>

## Personalizer

<details>
<summary>What does the Personalizer actually do?</summary>

It draws the customer's text and images onto your product photo, live, as they type — so they see the mug with their name on it before they buy. See [Personalizer](../personalizer/README.md).

</details>

<details>
<summary>Can customers upload their own image?</summary>

Yes, with a File upload option enabled for the Personalizer. See [Image layers](../personalizer/image-layers.md).

</details>

<details>
<summary>Can I use my own fonts?</summary>

Yes, custom fonts can be uploaded on qualifying plans. See [Fonts](../personalizer/fonts.md).

</details>

<details>
<summary>How do I stop customers dragging text off the printable area?</summary>

Set a [clip area](../personalizer/clip-area.md). Any customer control — drag, resize, rotate — needs one.

</details>

<details>
<summary>Do I get the finished design with the order?</summary>

Yes, the design is available from the order. See [Cart and orders](../personalizer/cart-and-orders.md).

</details>

<details>
<summary>Can text follow a curve?</summary>

Yes, on Text and Number layers. See [Curve and auto-fit](../personalizer/curve-and-auto-fit.md).

</details>

## Storefront and cart

<details>
<summary>Can customers edit their options from the cart?</summary>

Yes — turn on **Show "Edit Options" button in cart**. See [Cart page](../storefront/cart-page.md).

</details>

<details>
<summary>Why did the accelerated payment buttons disappear?</summary>

They skip the cart, which would skip the option form. The app hides them on products with options. Products without options keep them.

</details>

<details>
<summary>Do options show in quickview popups?</summary>

With **Show options on Quickview popups** on, yes. See [Quickview and other pages](../storefront/quickview-and-other-pages.md).

</details>

<details>
<summary>Do options show on collection pages?</summary>

Only where a quickview or a featured-product section renders the product form. There is no option form on a plain collection grid.

</details>

<details>
<summary>How do I get options onto my packing slips?</summary>

Either add the Liquid snippet to your packing slip template, or use an [Update order notes](../automations/update-order-notes.md) workflow — most templates already print the order note.

</details>

<details>
<summary>Why does my paperwork show odd technical lines?</summary>

Your template prints every line item property, including the app's internal ones. The snippet in [Show options on orders](../storefront/show-options-on-orders.md) skips names that begin with an underscore.

</details>

## Translations and locales

<details>
<summary>Can I translate my options?</summary>

Yes — labels, values, help text, placeholders, and the widget's own wording, per locale. See [Translations](../translations/README.md).

</details>

<details>
<summary>Does it work with right-to-left languages?</summary>

Yes. See [RTL and non-Latin languages](../translations/rtl-and-non-latin.md).

</details>

<details>
<summary>Can I show different options in different countries?</summary>

Yes, with a country rule on the option set. See [Assign to countries](../option-sets/assign-to-countries.md).

</details>

## POS

<details>
<summary>Does the app work in Shopify POS?</summary>

Yes, for option sets published to the Point of Sale channel. See [Point of Sale](../pos/README.md).

</details>

<details>
<summary>What does not work in POS?</summary>

**Add price** add-ons, and a couple of option types. See [POS limitations](../pos/limitations.md).

</details>

## Plans and billing

<details>
<summary>How do I see what my plan includes?</summary>

Open **Pricing** in the app. Locked features are marked in the builder too. See [Locked features](../plans/locked-features.md).

</details>

<details>
<summary>What happens to my work if I downgrade?</summary>

It is kept, but features the lower plan does not include stop working on your storefront straight away — including add-on charges. Read [What happens on downgrade](../plans/what-happens-on-downgrade.md) before you do it.

</details>

<details>
<summary>Where is billing handled?</summary>

Through Shopify, on your Shopify invoice. See [Change your plan](../plans/change-your-plan.md).

</details>
