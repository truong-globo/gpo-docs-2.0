---
description: Fixes for the most common reasons options are not showing up or not working as expected.
icon: wrench
---

# Troubleshooting

Almost every report comes down to one of the items below. Work through the first one before anything else — it is the single most common cause.

## Options are not showing up

<details>
<summary>Nothing from the app appears on the storefront at all</summary>

Check these four, in order:

1. **The app embed is not enabled on your live theme.** This is the number one cause, and it is per theme — publishing a new theme turns it off again. See [Enable the app embed](../getting-started/enable-the-app-embed.md).
2. **The option set is Draft.** A draft never renders. See [Activate and publish](../option-sets/create-an-option-set.md#activate-and-publish).
3. **Online Store is not ticked** under the option set's **Sales channels**.
4. **The product rule does not match** the product you are looking at. Use **Preview matching products** to check — see [Assign to products](../option-sets/assign-to-products.md).

If all four are correct, that is worth reporting rather than working around. See [Contact support](contact-support.md).
</details>

<details>
<summary>Some options appear and others do not</summary>

Three causes, in order of likelihood: [conditional logic](../conditional-logic/README.md) is hiding them; the **Hide** action is applied to them; or your plan does not include those option types, so they are configured but not rendered.
</details>

<details>
<summary>Options appear on product pages but not in a quickview</summary>

Turn on **Show options on Quickview popups** in **Settings** > **Settings** > **General**. See [Quickview and other pages](../storefront/quickview-and-other-pages.md).
</details>

<details>
<summary>Options appear twice on one product</summary>

Either two active option sets both match the product — filter the list to **Active** and look for one using **Apply to All Products** — or automatic placement and an [app block](../getting-started/add-the-app-block.md) are both placing the widget. Remove one.
</details>

<details>
<summary>Options disappeared after I published a theme</summary>

The new theme does not have the app embed enabled. It is per theme, including a duplicate of the same theme.
</details>

<details>
<summary>Options show on the storefront but not in POS, or the reverse</summary>

Check the option set's **Sales channels** — it needs to be published to the channel you expect it on. Then confirm the option types you used are supported in POS: [Dimension](../option-types/input-types/dimension.md) and [Product links](../option-types/selection-types/product-links.md) are not, and **Add price** add-ons do not apply there. See [POS limitations](../pos/limitations.md).
</details>

## Pricing and add-ons

<details>
<summary>An add-on charge is missing, wrong, or doubled</summary>

* **Nothing is charged** — check the option is not hidden by a conditional rule (hidden options are not charged), that the price is actually set, and that the option set is saved and active.
* **The charge multiplies when a customer buys several** — the option is on **Default** mode, which follows the product quantity. Anything charged once per order, like gift wrap, belongs on **One time charge**. See [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md).
* **Every selected value is charged on a multi-select** — that is correct. Cap it with **Max selections**.
</details>

<details>
<summary>The product looks more expensive than my listed price, before anybody chooses anything</summary>

An option has a **default value** with a price attached, so it is charged from page load. Either remove the default or make the default the free choice. See [Required field and default value](../option-types/shared-settings/required-and-default-value.md#default-value).
</details>

<details>
<summary>No price appears beside an option</summary>

**Settings** > **Settings** > **Add-on price** has two switches: **Show add-on for inputs** covers Text, Textarea, and Number; **Show add-on for options** covers the selection types. Turning off the wrong one looks like a bug. See [Add-on price display settings](../add-on-pricing/price-display-settings.md).
</details>

<details>
<summary>Out of stock options does nothing</summary>

Three causes, in order: the values use **Add price**, which has no product and therefore no stock; the add-on product does not have inventory tracking turned on; or the variant is still set to continue selling when out of stock. Generated products arrive needing the last two done by hand — see [Stock and inventory](../add-on-pricing/stock-and-inventory.md).
</details>

<details>
<summary>Generated add-on products appear in my collections and search</summary>

Exclude the tag `globo-product-options` from those collections. Do not unpublish them from the Online Store — an unpublished product cannot be added to the cart. See [Automatically generate a product](../add-on-pricing/auto-generate-a-product.md).
</details>

## Cart and checkout

<details>
<summary>Add to cart does nothing</summary>

Almost always a validation failure rather than a broken button: a required option is empty, or an entry breaks a limit. Turn on **Auto-scroll to first error message** in **Settings** > **Settings** > **General** so shoppers are taken to the problem. It is on by default — with it off, they get no feedback at all.
</details>

<details>
<summary>Customers can add to cart without seeing the options</summary>

Two routes bypass the form: a quickview without **Show options on Quickview popups** enabled, and a sticky add-to-cart bar whose button does not go through the app. Both produce orders you cannot fulfil, so both are worth reporting if the setting is already correct. See [Theme and third-party notes](../integrations/theme-and-third-party-notes.md).
</details>

<details>
<summary>The accelerated payment buttons disappeared</summary>

Expected on products with options. Those buttons skip the cart, which would skip the option form, so the app hides them where options are present.
</details>

<details>
<summary>Customers delete add-on lines and break their orders</summary>

Turn on **Hide quantity box and remove button for add-on products** in **Settings** > **Settings** > **General**. It is on by default. Without it a shopper can remove the gift box while keeping the "gift wrapped" option.
</details>

<details>
<summary>Option details are missing from my packing slip</summary>

The template does not print line item properties. Add the snippet from [Show options on orders](../storefront/show-options-on-orders.md) inside the line item loop, or use an [Update order notes](../automations/update-order-notes.md) workflow — most templates already print the order note.
</details>

<details>
<summary>Odd technical entries appear on my paperwork</summary>

Your template is printing every property, including the app's internal ones. The snippet in [Show options on orders](../storefront/show-options-on-orders.md) skips names beginning with an underscore.
</details>

<details>
<summary>Order lines read as "text" or "checkbox"</summary>

Those are the options' **Name** values left at their defaults. Set them to something readable — it applies to future orders. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).
</details>

## Appearance and behaviour

<details>
<summary>The widget looks nothing like my theme</summary>

Turn on **Match theme style** in **Settings** > **Design**, and check whether your theme is covered by the **View supported themes** link beside it. If it is not, set the colours, borders, and fonts manually instead. See [Match your theme style](../storefront/match-your-theme-style.md).
</details>

<details>
<summary>The widget is in an odd place on the page</summary>

Change **Widget placement** in **Settings** > **Settings** > **General**, or pin it exactly with an [app block](../getting-started/add-the-app-block.md). See [Widget placement](../storefront/widget-placement.md).
</details>

<details>
<summary>The widget appears late, after the page has loaded</summary>

Usually a speed or script optimisation app deferring the app's scripts. Add this app to its exclusion list. See [Theme and third-party notes](../integrations/theme-and-third-party-notes.md).
</details>

<details>
<summary>A feature or option type is greyed out, or shows an upgrade prompt</summary>

It is not included on your current plan. See [Compare plans](../plans/compare-plans.md).
</details>

## Conditional logic and the Personalizer

Both have their own troubleshooting page, organised by symptom:

* [Troubleshooting conditional logic](../conditional-logic/troubleshooting.md) — rules firing at the wrong moment, options that will not hide, variant conditions.
* [Troubleshooting personalizer](../personalizer/troubleshooting.md) — nothing drawn, wrong position, wrong font, unusable customer designs.

## Still stuck?

See the [FAQ](faq.md) for quick answers, or [Contact support](contact-support.md) to reach us — with your theme name, the option set name, and a link to the product page.
