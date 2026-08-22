---
description: Publish an option set to POS, add the app to the POS home screen, and fill in options at the counter.
icon: mobile-screen
---

# Set up and use options in POS

## Before you start

* Point of Sale is included in your plan. See [Compare plans](../plans/compare-plans.md).
* You have the Shopify POS app, signed in to your store.
* You have read [POS limitations](limitations.md) — two option types and one add-on mode do not work here.

## Set up

{% stepper %}
{% step %}
### Publish the option set to Point of Sale

Open the option set in the builder and, next to its name, tick **Point of Sale** under **Sales channels**. Save.

An option set published only to **Online Store** does not appear in POS at all.
{% endstep %}

{% step %}
### Check the option set is Active

A **Draft** option set does nothing on any channel.
{% endstep %}

{% step %}
### Review the option types it uses

If it contains [Dimension](../option-types/input-types/dimension.md) or [Product links](../option-types/selection-types/product-links.md), those will not work in POS. Either remove them, or keep a separate option set for POS without them.
{% endstep %}

{% step %}
### Review the add-on modes

Any value using **Add price** will not charge in POS. Change those to **Use existing product** or **Automatically generate product**. See [Add-on pricing](../add-on-pricing/README.md).
{% endstep %}

{% step %}
### Add the app tile to the POS home screen

In the Shopify POS app, customise the home screen and add a tile for the app, so staff can reach it in one tap rather than hunting through a menu.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: pos-sales-channel | App admin → builder → popover Sales channels | Point of Sale đang được bật | Khoanh dòng Point of Sale -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The sales channels control with Point of Sale enabled"><figcaption><p>An option set must be published to Point of Sale to appear there.</p></figcaption></figure>

## Using it at the counter

{% stepper %}
{% step %}
### Add the product to the POS cart

As normal, however your staff usually do it.
{% endstep %}

{% step %}
### Open the app from the POS home screen

It lists the items currently in the cart.
{% endstep %}

{% step %}
### Select the item to personalise

Items that have an option set available can be selected. Add-on items already in the cart cannot — they belong to the item above them.
{% endstep %}

{% step %}
### Fill in the options

The option form appears, using the same option set as your storefront.
{% endstep %}

{% step %}
### Update the cart

The item's options are recorded against it, and any add-on products are added as their own cart lines.
{% endstep %}

{% step %}
### Complete the sale

Check out as normal. The options travel with the order exactly as they do online.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: pos-cart-items | Shopify POS → app | Danh sách line item trong cart, 1 item đang được chọn | Khoanh item đang chọn -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The app open in Shopify POS listing the current cart items"><figcaption><p>The app lists the cart, and staff pick the item to personalise.</p></figcaption></figure>

## Practical advice for the counter

<table><thead><tr><th width="290">Do</th><th>Why</th></tr></thead><tbody><tr><td>Keep POS option sets short</td><td>A customer is standing there. A twenty-field form is not a counter experience</td></tr><tr><td>Use a separate option set for POS where the online one is long</td><td>Publish the long one to Online Store only, and a trimmed one to POS only</td></tr><tr><td>Prefer <a href="../option-types/selection-types/button.md">Button</a> and <a href="../option-types/selection-types/radio-button.md">Radio button</a> over dropdowns</td><td>Fewer taps on a touch screen</td></tr><tr><td>Set sensible <a href="../option-types/shared-settings/required-and-default-value.md#default-value">default values</a></td><td>Staff confirm rather than fill in</td></tr><tr><td>Give options obvious labels</td><td>Staff are reading them aloud to a customer</td></tr><tr><td>Train staff to open the app <em>after</em> adding the product</td><td>The app works from what is already in the cart</td></tr></tbody></table>

{% hint style="info" %}
The separate-option-set pattern is worth the small extra effort: your online form can ask everything, while your counter form asks only what staff need while a customer waits. Split them with **Sales channels** — one published to Online Store, one to Point of Sale.
{% endhint %}

## What reaches the order

The same as online: the options are attached to the line item, and add-on products appear as their own lines. Your production team sees an in-person order exactly as they see a web order.

See [Show options on orders](../storefront/show-options-on-orders.md).

## Notes

* The app must be opened from within POS. It reads the current POS cart.
* Add-on lines already in the cart cannot themselves be personalised — they belong to the item they were added for.
* Option sets published to both channels are shared, so a change affects both. Use separate sets if you want them to differ.
* Country and customer rules are storefront concepts and are not a meaningful filter for an in-person sale.

## Troubleshooting

<details>
<summary>The app is not on the POS home screen</summary>

Customise the POS home screen and add the app's tile.
</details>

<details>
<summary>The app opens but shows no items</summary>

The POS cart is empty. Add the product first, then open the app.
</details>

<details>
<summary>An item has no options</summary>

Its option set is not published to **Point of Sale**, is **Draft**, or its product rule does not match that product.
</details>

<details>
<summary>Some options are missing compared to the storefront</summary>

They are probably [Dimension](../option-types/input-types/dimension.md) or [Product links](../option-types/selection-types/product-links.md), neither of which works in POS.
</details>

<details>
<summary>Add-ons are not charged</summary>

Those values use **Add price**, which POS does not support. Change them to a product-backed mode. See [POS limitations](limitations.md).
</details>

<details>
<summary>I cannot select an add-on line</summary>

Correct — add-on lines cannot be personalised. Select the main item instead.
</details>

<details>
<summary>The cart did not update</summary>

Try again from the app. If it persists, note what you were doing and [contact support](../help/contact-support.md).
</details>

## Next steps

* [POS limitations](limitations.md)
* [Status and sales channels](../concepts/status-and-sales-channels.md)
* [Add-on pricing](../add-on-pricing/README.md)
