---
description: Add to cart doing nothing, add-on lines behaving oddly, and option details missing from orders.
icon: cart-plus
---

# Cart and checkout problems

## Add to cart

<details>
<summary>Nothing happens when the customer selects Add to cart</summary>

Almost always a validation failure rather than a broken button. A required option is empty, or an entry breaks a limit, and the add is blocked.

Turn on **Auto-scroll to first error message** in **Settings** > **Settings** > **General**. It is on by default — if it has been turned off, shoppers get no feedback at all, which looks exactly like a broken button.

</details>

<details>
<summary>A required option is being skipped</summary>

It is hidden by a conditional logic rule. Hidden options are not validated, by design — otherwise a hidden field could make a product unbuyable.

If it must always be answered, it cannot be conditional. See [Troubleshooting conditional logic](../conditional-logic/troubleshooting.md).

</details>

<details>
<summary>Shoppers can add to cart without seeing the options at all</summary>

Two routes let them bypass the form:

1. **A quickview.** Turn on **Show options on Quickview popups**. See [Quickview and other pages](../storefront/quickview-and-other-pages.md).
2. **A sticky add-to-cart bar** whose button does not go through the app. See [Theme and third-party notes](../integrations/theme-and-third-party-notes.md).

Both are worth reporting if the setting is already correct — they produce orders you cannot fulfil.

</details>

<details>
<summary>The accelerated payment button disappeared</summary>

Expected on products with options. Those buttons skip the cart, which would skip the option form, so the app hides them where options are present. They still work on products without options.

</details>

## The cart

<details>
<summary>Add-on products appear as separate lines</summary>

That is how product-backed add-ons work — they are real products in a real cart.

Turn on **Merge Main product & Add-on products** in **Settings** > **Settings** > **Add-on price** to present them as one item. New stores start with it on. See [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).

</details>

<details>
<summary>Customers remove add-on lines and break their orders</summary>

Turn on **Hide quantity box and remove button for add-on products** in **Settings** > **Settings** > **General**. It is on by default.

Without it a shopper can delete the gift box while keeping the "gift wrapped" option, and you receive an order describing something that was not paid for.

</details>

<details>
<summary>The cart drawer shows the wrong total after adding add-ons</summary>

Turn on **Go to cart immediately after adding to cart**, so shoppers see the full cart page instead of a drawer that may not have handled the addition. See [Ajax cart and redirect to cart](../storefront/ajax-cart-and-redirect.md).

</details>

<details>
<summary>Option details are missing from the cart</summary>

They travel automatically, so their absence means the item was not added through the widget — usually via a quickview or sticky bar that bypassed it, or a dynamic checkout button.

</details>

<details>
<summary>Customers cannot correct a typo without starting again</summary>

Turn on **Show "Edit Options" button in cart**. For personalised products this reduces abandoned carts noticeably. See [Cart page](../storefront/cart-page.md).

</details>

<details>
<summary>There is no design preview for a personalised item</summary>

Check **Personalize preview mode** in **Settings** > **Settings** > **General** > **Cart page**, and that it is included in your plan. If it downloads instead of opening, it is set to **Download file**.

</details>

## Orders

<details>
<summary>Option details are on the order but not on my packing slip</summary>

Your packing slip template does not print line item properties. Add the snippet from [Show options on orders](../storefront/show-options-on-orders.md), inside the line item loop.

Or use an [Update order notes](../automations/update-order-notes.md) workflow — most templates already print the order note, so that puts the options on your paperwork with no Liquid at all.

</details>

<details>
<summary>Odd technical entries appear on my paperwork</summary>

Your template is printing every property, including the app's internal ones. The snippet in [Show options on orders](../storefront/show-options-on-orders.md) skips names beginning with an underscore.

</details>

<details>
<summary>Order lines read as "text" or "checkbox"</summary>

Those are the options' **Name** values, left at their defaults. Set them to something readable — it applies to future orders. See [Label vs Name](../concepts/label-vs-name.md).

</details>

<details>
<summary>Uploaded files show as long unreadable addresses</summary>

Use the file handling in the snippet, which renders them as links with readable names.

</details>

<details>
<summary>I cannot find a customer's uploaded file</summary>

It is attached to the order in Shopify admin, with the option details for that line item.

</details>

<details>
<summary>An automation did not run</summary>

Check the workflow is **Active**, the order contained app options, and order data access was approved. Then use the workflow's own test against a recent order. See [Automations](../automations/README.md).

</details>

## Next steps

* [Options are not showing up](troubleshooting-not-showing.md)
* [Pricing and add-on problems](troubleshooting-pricing.md)
* [Show options on orders](../storefront/show-options-on-orders.md)
