---
description: >-
  Preview your option form directly in the app before publishing it to your
  store. You can also click any option in the preview to quickly find and edit
  its settings.
icon: eye
---

# Live preview and inspector

The preview on the right is a working version of your widget, not just a static mockup. It runs your conditional logic, updates add-on prices, and displays each option type as it will appear on your storefront.

Using the live preview makes it easier to test your option form and fine-tune its settings without constantly switching between the builder and your storefront.

## Before you start

Make sure you have an option set open in the builder with at least one option added.

## What the preview does

<table><thead><tr><th width="270">It does</th><th>It does not</th></tr></thead><tbody><tr><td>Render every option type as shoppers see it</td><td>Use your theme's fonts, colours, or spacing — it uses the app's own styling</td></tr><tr><td>Run conditional logic, so you can test show and hide rules</td><td>Add anything to a real cart</td></tr><tr><td>Show add-on price previews and the running total</td><td>Charge anything</td></tr><tr><td>Run validation, so you can see your error messages</td><td>Apply your customer or country rules</td></tr><tr><td>Draw the Personalizer live preview on the background image</td><td>Show other option sets that also apply to a product</td></tr></tbody></table>

{% hint style="info" %}
Because the preview does not use your theme's styling, differences in font and colour between the preview and your storefront are expected. To align the widget with your theme on the storefront, see [Match your theme style](../storefront/match-your-theme-style.md).
{% endhint %}

## The four header controls

<table><thead><tr><th width="230">Control</th><th>What it does</th></tr></thead><tbody><tr><td>Editor / preview toggle</td><td>On narrow screens, switches between the settings panel and the preview. On wide screens both are visible at once.</td></tr><tr><td>Desktop / mobile toggle</td><td>Renders the preview at desktop or mobile width. Worth checking both — column widths and swatch sliders behave differently.</td></tr><tr><td>Inspector toggle</td><td>Turns the click-to-edit overlay on and off. See below.</td></tr><tr><td>Language switcher</td><td>Renders the preview in one of your storefront languages, using your translated labels and values.</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/placeholder.png" alt="The builder header controls for editor and preview, viewport, inspector, and language"><figcaption><p>The header controls change what the preview shows, not what shoppers get.</p></figcaption></figure>

## The inspector

Turn the inspector on and the preview becomes clickable. Hovering an option highlights it; selecting it opens that option's settings in the panel — so you can go from "this field looks wrong" to its settings in one click.

The inspector also puts a small action bar on the highlighted option:

<table><thead><tr><th width="200">Action</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Duplicate</strong></td><td>Copies the option, exactly like the panel's duplicate action.</td></tr><tr><td><strong>Half width</strong></td><td>Sets the option's <strong>Column width</strong> to 50%.</td></tr><tr><td><strong>Full width</strong></td><td>Sets the option's <strong>Column width</strong> to 100%.</td></tr><tr><td><strong>Hide</strong></td><td>Hides the option from the storefront while keeping it in the set.</td></tr><tr><td><strong>Delete</strong></td><td>Removes the option.</td></tr></tbody></table>

Half width and full width are the two column widths most people actually use, which is why they are here. The full range — 25%, 33%, 50%, 66%, 75%, 100% — is in the option's **Advanced Settings**. See [Column width](../option-types/shared-settings/direction-width-and-css.md#column-width).

<figure><img src="../.gitbook/assets/placeholder.png" alt="The inspector highlighting an option in the preview with its action bar"><figcaption><p>With the inspector on, the preview becomes a second way to edit.</p></figcaption></figure>

## Testing conditional logic in the preview

This is the preview's most useful job. Rules are live, so you can:

* Tick the trigger option and watch the dependent option appear.
* Untick it and confirm it disappears again.
* Change a dropdown value and check which branch shows.

Two things the preview cannot test, because it has no real shopper context:

* **Conditions based on Shopify variants** — the preview has no variant selected, so variant conditions do not evaluate. Test those on a real product page with **View in Store**. See [Conditions based on Shopify variants](../conditional-logic/conditions-on-shopify-variants.md).
* **Customer and country rules** — these decide whether the whole set renders, and are evaluated on the storefront only.

## Preview matching products

When your product rule uses **Automatic Rules**, you can check which products the rule actually catches before you save.

Open **Preview matching products** and the app lists the products your conditions currently match, with each product's image, title, vendor, type, and status. Each row has a **Preview** action that opens that product's page on your storefront.

{% hint style="warning" %}
This preview is unavailable when your automatic conditions include a **Collection** condition. The app tells you so with a notice. Verify collection-based rules by opening a product from that collection with **View in Store** instead.
{% endhint %}

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Preview matching products dialog listing the products an automatic rule catches"><figcaption><p>Check an automatic rule against your real catalogue before saving.</p></figcaption></figure>

## View in Store

**View in Store** in the builder header opens a real product page on your storefront, for a product this option set applies to.

This is the only true test. Use it to check:

* the widget's position in your theme
* how it looks with your theme's fonts and colours
* variant-based conditional logic
* the actual add to cart flow, and what lands on the cart page

For it to work, the option set must be **Active**, published to **Online Store**, and the [app embed](../getting-started/enable-the-app-embed.md) must be enabled.

## When the preview switches itself off

Very large option sets disable the live preview. The app counts your options, counting each option value of a selection option separately, and stops rendering the preview at around 100.

This is deliberate: rendering hundreds of swatches on every keystroke would make the builder unusable. Everything still saves and works normally on the storefront — you just lose the in-app preview.

If you hit this, either split the option set into two, or test with **View in Store**.
