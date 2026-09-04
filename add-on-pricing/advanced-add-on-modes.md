---
description: >-
  All eight modes that decide how an add-on charge scales with quantity, each with
  a worked calculation.
icon: calculator
---

# Advanced add-on modes

The price sets how much an add-on costs. The **Advanced settings** dropdown sets how the quantity is calculated.

For example, a $5.00 gift wrap charge on an order of three items is either $15.00 or $5.00, depending on the mode you select.

## Where it is

The setting is on the **Advanced Settings** tab, labeled **Advanced settings**. It is set at **option** level, even when the prices are set on individual values, and it applies to the whole option.

It has no effect on an option with no price.

<!-- SCREENSHOT: addon-advanced-modes | App admin → builder → option có Price → Advanced Settings | Dropdown "Advanced settings" đang mở với đủ các mode và help text | Khoanh dropdown -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Advanced settings dropdown open, listing the add-on quantity modes with their help text"><figcaption><p>Each mode carries a one-line explanation in the app itself.</p></figcaption></figure>

## The eight modes

<table><thead><tr><th width="290">Mode</th><th width="180">Quantity comes from</th><th>Available on</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>The main product's quantity</td><td>Everything with a price</td></tr><tr><td><strong>One time charge</strong></td><td>Always 1</td><td>Everything with a price</td></tr><tr><td><strong>Fixed quantity</strong></td><td>A number you set</td><td>Everything with a price</td></tr><tr><td><strong>Dynamic quantity</strong></td><td>A number you set × main quantity</td><td>Everything with a price</td></tr><tr><td><strong>Fixed quantity (by customer)</strong></td><td>A number the customer enters</td><td>Everything with a price</td></tr><tr><td><strong>Dynamic quantity (by customer)</strong></td><td>The customer's number × main quantity</td><td>Everything with a price</td></tr><tr><td><strong>Mixed quantity</strong></td><td>A number per option value, entered by the customer</td><td>Multi-select options only</td></tr><tr><td><strong>Per character</strong></td><td>How many characters were typed</td><td><a href="../option-types/input-types/text.md">Text</a> and <a href="../option-types/input-types/textarea.md">Textarea</a> only</td></tr></tbody></table>

## Worked calculations

In all of the following examples, the add-on price is **$4.00** and the customer is buying **3** of the main product.

### Default

The add-on quantity follows the main product's quantity.

> 3 × $4.00 = **$12.00**

Use this for an add-on used once per item, such as an engraved plate per bracelet or fabric per cushion.

### One time charge

The add-on is charged once, regardless of the main product quantity.

> 1 × $4.00 = **$4.00**

Use this for a charge applied once per order, such as gift wrapping a parcel, a delivery upgrade, or a setup fee.

### Fixed quantity

The quantity is always the number you enter in **Set quantity**, regardless of the main product quantity. With **Set quantity** set to `2`:

> 2 × $4.00 = **$8.00**

Use this when the add-on always includes a fixed amount, such as a gift box with two ribbons.

### Dynamic quantity

The **Set quantity** value multiplied by the main product quantity. With **Set quantity** set to `2`:

> 2 × 3 × $4.00 = **$24.00**

Use this when each main item needs a fixed number of the add-on, such as two batteries per flashlight.

### Fixed quantity (by customer)

A quantity field is displayed below the option. The customer's value is used as entered. If the customer enters `5`:

> 5 × $4.00 = **$20.00**

Use this when the customer chooses the quantity independently of how many products they are buying, such as extra embroidered names or spare buttons.

### Dynamic quantity (by customer)

The customer's value multiplied by the main product quantity. If the customer enters `5`:

> 5 × 3 × $4.00 = **$60.00**

Use this when the customer's value applies to each item, for example five extra names on each of three jerseys.

{% hint style="warning" %}
This mode multiplies twice, so the total increases quickly. State in the option's label that the value applies per item, and set a **Max value** on the quantity.
{% endhint %}

### Mixed quantity

Each option value has its own quantity field. This mode is available on multi-select options only: [Checkbox](../option-types/selection-types/checkbox.md), or any selection type with **Allow multiple** enabled.

If a customer selects two of `Chocolate` and one of `Vanilla`, both priced at $4.00:

> (2 × $4.00) + (1 × $4.00) = **$12.00**

Use this for mix-and-match add-ons such as toppings, flavors, or items in a hamper.

### Per character

The charge is based on the number of characters the customer enters. This mode is available on Text and Textarea only. For `Forever yours`, which is 13 characters, at $0.50:

> 13 × $0.50 = **$6.50**

Use this for engraving and embroidery priced by length.

{% hint style="info" %}
Always use **Per character** together with a [Max character](../option-types/shared-settings/limits.md#min-and-max-character) limit, so the charge has a maximum. Enable the [Character counter](../option-types/shared-settings/limits.md#character-counter) so the customer can see how many characters they have entered.
{% endhint %}

## Set quantity

This field is used by **Fixed quantity** and **Dynamic quantity**. It is displayed only when one of those modes is selected. The other modes take the quantity from the customer or do not need one.

## Choosing the right mode

<table><thead><tr><th width="330">The add-on is…</th><th>Mode</th></tr></thead><tbody><tr><td>Consumed once per item bought</td><td><strong>Default</strong></td></tr><tr><td>Per order — wrapping, delivery, a setup fee</td><td><strong>One time charge</strong></td></tr><tr><td>A set amount that comes with the product</td><td><strong>Fixed quantity</strong></td></tr><tr><td>A set amount per item</td><td><strong>Dynamic quantity</strong></td></tr><tr><td>However many the customer wants, in total</td><td><strong>Fixed quantity (by customer)</strong></td></tr><tr><td>However many the customer wants, per item</td><td><strong>Dynamic quantity (by customer)</strong></td></tr><tr><td>Pick-and-mix across several values</td><td><strong>Mixed quantity</strong></td></tr><tr><td>Priced by the length of the text</td><td><strong>Per character</strong></td></tr></tbody></table>

## Common mistake

Leaving a per-order charge such as gift wrap on **Default**.

If a customer buys five bracelets and selects gift wrapping, the **Default** mode charges for five wraps.

Use **One time charge** for anything applied once per order, including delivery upgrades, gift wrapping, handling fees, artwork setup, and rush production.

## Notes

* The mode is set per option. If values in one option need different quantities, use two options with conditional logic, or use **Mixed quantity**.
* **Mixed quantity** is displayed only when the option is multi-select.
* **Per character** is available on Text and Textarea only.
* Hidden options are not charged, regardless of the mode.
* An add-on on a **default value** is charged as soon as the page loads. With the **Default** mode, the charge also multiplies by the product quantity.
