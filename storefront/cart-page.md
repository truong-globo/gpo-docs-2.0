---
description: Add-on lines, letting customers edit their options, and how personalised designs are previewed in the cart.
icon: cart-shopping
---

# Cart page

Three settings in **Settings** > **Settings** > **General** > **Cart page**, plus one in the add-on settings. Together they decide how a personalised order behaves once it is in the cart.

## Hide quantity box and remove button for add-on products

<table><thead><tr><th width="180">Default</th><td>On</td></tr></thead></table>

Stops customers changing the quantity of an add-on line, or deleting it, independently of the item it belongs to.

**Leave this on.** Without it a shopper can remove the gift box while keeping the "gift wrapped" option on the main item, and you receive an order describing something that was not paid for. It is the sort of thing you only notice at packing time.

It applies to product-backed add-ons, which are the ones that get their own cart line. An [Add price](../add-on-pricing/add-price-directly.md) charge has no separate line to protect.

## Show "Edit Options" button in cart

<table><thead><tr><th width="180">Default</th><td>Off</td></tr></thead></table>

Adds a control to the cart line that reopens the option form, so customers can change their choices without removing the item and starting again.

<table><thead><tr><th width="290">Turn it on when</th><th>Leave it off when</th></tr></thead><tbody><tr><td>You sell personalised products, where a typo is likely and costly</td><td>Your options are simple and quick to redo</td></tr><tr><td>Forms are long enough that redoing one is a real deterrent</td><td>You would rather the cart stayed as simple as possible</td></tr><tr><td>You want fewer abandoned carts from small mistakes</td><td></td></tr></tbody></table>

For a personalisation shop this is worth having. Somebody who spots a misspelled name in their engraving after adding to cart has two choices without it: start again, or leave. Some of them leave.

It is plan-gated. See [Compare plans](../plans/compare-plans.md).

The button's wording, along with **Cancel** and **Save Changes**, is editable per language in **Settings** > **Translations**. See [Translate widget text](../translations/translate-widget-text.md).

## Personalize preview mode

<table><thead><tr><th width="180">Default</th><td><strong>View in modal</strong></td></tr></thead></table>

How a personalised design is shown from the cart.

<table><thead><tr><th width="230">Mode</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>View in modal</strong></td><td>Opens in a dialog on the cart page</td></tr><tr><td><strong>Download file</strong></td><td>Downloads as a file</td></tr></tbody></table>

**View in modal** is the better default — a shopper who has to download a file to check their own order may not bother. Choose **Download file** only if customers genuinely need to keep or forward a copy, such as approving artwork with somebody else.

Plan-gated, and only relevant if you use the [Personalizer](../personalizer/README.md). See [Designs in cart and orders](../personalizer/cart-and-orders.md).

## Merge main product and add-ons

Not on this page, but it shapes the cart more than anything above. **Settings** > **Settings** > **Add-on price** > **Merge Main product & Add-on products** presents add-on lines as part of the main item instead of separately.

New stores start with it on. See [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).

<!-- SCREENSHOT: store-cart-settings | App admin → Settings → General → Cart page | 3 setting: hide quantity/remove, Edit Options, Personalize preview mode | Khoanh nhóm Cart page -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The cart page settings group with its three switches"><figcaption><p>Three cart settings, all store-wide.</p></figcaption></figure>

## What the cart shows anyway

Regardless of these settings, the cart shows the option details under each item — the text they typed, the values they chose, links to files they uploaded. That is automatic, because option values travel as line item properties.

See [Show options on orders](show-options-on-orders.md).

## A recommended configuration for personalised products

<table><thead><tr><th width="330">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Hide quantity box and remove button for add-on products</td><td><strong>On</strong></td></tr><tr><td>Show "Edit Options" button in cart</td><td><strong>On</strong></td></tr><tr><td>Personalize preview mode</td><td><strong>View in modal</strong></td></tr><tr><td>Merge Main product &amp; Add-on products</td><td><strong>On</strong>, unless you want add-on prices itemised</td></tr></tbody></table>

## Notes

* All store-wide.
* Two of the three are plan-gated.
* Cart appearance also depends on your theme, which builds the cart page. Check the result on your own cart after changing anything here.
* Options are collected before the cart, so there is no way to add an option from the cart page itself — only to edit what is already there.

## Troubleshooting

<details>
<summary>Customers remove add-on lines and break their orders</summary>

Turn on **Hide quantity box and remove button for add-on products**. It is on by default, so check it has not been turned off.
</details>

<details>
<summary>There is no Edit Options button</summary>

Turn on **Show "Edit Options" button in cart**, and check it is included in your plan.
</details>

<details>
<summary>Editing options in the cart does not work on my theme</summary>

Themes build carts differently. Report it with your theme name — see [Contact support](../help/contact-support.md).
</details>

<details>
<summary>The design downloads instead of opening</summary>

**Personalize preview mode** is set to **Download file**.
</details>

<details>
<summary>Add-on lines clutter the cart</summary>

Turn on [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md).
</details>

<details>
<summary>Option details are missing from the cart</summary>

That is not a setting — they travel automatically. Check the item was added through the widget rather than through a dynamic checkout button that bypasses it.
</details>

## Next steps

* [Show options on orders](show-options-on-orders.md)
* [Merge main product and add-ons](../add-on-pricing/merge-as-bundle.md)
* [Ajax cart and redirect to cart](ajax-cart-and-redirect.md)
