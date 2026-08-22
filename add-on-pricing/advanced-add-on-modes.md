---
description: >-
  All eight modes that decide how an add-on charge scales with quantity, each with
  a worked calculation.
icon: calculator
---

# Advanced add-on modes

Setting a price answers "how much". The **Advanced settings** dropdown answers "how many" — and it is the setting most often left at its default when it should not be.

A $5.00 gift-wrap charge on an order of three items is $15.00 or $5.00 depending entirely on this dropdown.

## Where it is

**Advanced Settings** tab, labelled **Advanced settings**. It sits at **option** level even when the prices are on the individual values, and it applies to the whole option.

It does nothing on an option with no price attached.

<!-- SCREENSHOT: addon-advanced-modes | App admin → builder → option có Price → Advanced Settings | Dropdown "Advanced settings" đang mở với đủ các mode và help text | Khoanh dropdown -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Advanced settings dropdown open, listing the add-on quantity modes with their help text"><figcaption><p>Each mode carries a one-line explanation in the app itself.</p></figcaption></figure>

## The eight modes

<table><thead><tr><th width="290">Mode</th><th width="180">Quantity comes from</th><th>Available on</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>The main product's quantity</td><td>Everything with a price</td></tr><tr><td><strong>One time charge</strong></td><td>Always 1</td><td>Everything with a price</td></tr><tr><td><strong>Fixed quantity</strong></td><td>A number you set</td><td>Everything with a price</td></tr><tr><td><strong>Dynamic quantity</strong></td><td>A number you set × main quantity</td><td>Everything with a price</td></tr><tr><td><strong>Fixed quantity (by customer)</strong></td><td>A number the customer enters</td><td>Everything with a price</td></tr><tr><td><strong>Dynamic quantity (by customer)</strong></td><td>The customer's number × main quantity</td><td>Everything with a price</td></tr><tr><td><strong>Mixed quantity</strong></td><td>A number per option value, entered by the customer</td><td>Multi-select options only</td></tr><tr><td><strong>Per character</strong></td><td>How many characters were typed</td><td><a href="../option-types/input-types/text.md">Text</a> and <a href="../option-types/input-types/textarea.md">Textarea</a> only</td></tr></tbody></table>

## Worked calculations

Throughout: the add-on price is **$4.00** and the customer is buying **3** of the main product.

### Default

The add-on follows the main product's quantity.

> 3 × $4.00 = **$12.00**

Correct for anything consumed per item: an engraved plate per bracelet, a fabric per cushion.

### One time charge

Charged once, whatever the main quantity.

> 1 × $4.00 = **$4.00**

Correct for anything per order: gift wrapping one parcel, one delivery upgrade, one setup fee. This is the mode most often needed and least often chosen.

### Fixed quantity

Always the number you set in **Set quantity**, regardless of the main quantity. With **Set quantity** = `2`:

> 2 × $4.00 = **$8.00**

Correct when the add-on always comes in a set amount: a gift box that always includes two ribbons.

### Dynamic quantity

Your **Set quantity** multiplied by the main quantity. With **Set quantity** = `2`:

> 2 × 3 × $4.00 = **$24.00**

Correct when each main item needs a fixed number of the add-on: two batteries per torch.

### Fixed quantity (by customer)

A quantity box appears below the option. The customer's number is used as-is. If they enter `5`:

> 5 × $4.00 = **$20.00**

Correct when the customer decides how many they want, independently of how many products they are buying: extra embroidered names, spare buttons.

### Dynamic quantity (by customer)

The customer's number multiplied by the main quantity. If they enter `5`:

> 5 × 3 × $4.00 = **$60.00**

Correct when the customer's number is "per item": five extra names on each of three jerseys.

{% hint style="warning" %}
This mode multiplies twice, so totals climb fast. Make sure the option's label makes clear the figure is per item, and set a **Max value** on the quantity so nobody produces a total by accident.
{% endhint %}

### Mixed quantity

Each option value gets its own quantity box. Multi-select options only — [Checkbox](../option-types/selection-types/checkbox.md), or any selection type with **Allow multiple** on.

A shopper picking two of `Chocolate` and one of `Vanilla`, both at $4.00:

> (2 × $4.00) + (1 × $4.00) = **$12.00**

Correct for pick-and-mix: toppings, flavours, components in a hamper.

### Per character

Charged by how many characters the customer typed. Text and Textarea only. For `Forever yours` — 13 characters — at $0.50:

> 13 × $0.50 = **$6.50**

Correct for engraving and embroidery priced by length.

{% hint style="info" %}
Always pair **Per character** with a [Max character](../option-types/shared-settings/limits.md#min-and-max-character) limit, so the charge has a ceiling, and turn on the [Character counter](../option-types/shared-settings/limits.md#character-counter) so the shopper can see it building.
{% endhint %}

## Set quantity

The number field used by **Fixed quantity** and **Dynamic quantity**. It appears only when one of those two is selected — the other modes take the quantity from the customer or do not need one.

## Choosing the right mode

<table><thead><tr><th width="330">The add-on is…</th><th>Mode</th></tr></thead><tbody><tr><td>Consumed once per item bought</td><td><strong>Default</strong></td></tr><tr><td>Per order — wrapping, delivery, a setup fee</td><td><strong>One time charge</strong></td></tr><tr><td>A set amount that comes with the product</td><td><strong>Fixed quantity</strong></td></tr><tr><td>A set amount per item</td><td><strong>Dynamic quantity</strong></td></tr><tr><td>However many the customer wants, in total</td><td><strong>Fixed quantity (by customer)</strong></td></tr><tr><td>However many the customer wants, per item</td><td><strong>Dynamic quantity (by customer)</strong></td></tr><tr><td>Pick-and-mix across several values</td><td><strong>Mixed quantity</strong></td></tr><tr><td>Priced by the length of the text</td><td><strong>Per character</strong></td></tr></tbody></table>

## The mistake to avoid

Leaving gift wrap on **Default**.

A customer buys five bracelets and asks for gift wrapping. On **Default** they are charged for five wraps. They either complain, or they do not notice and you have overcharged them.

Anything that happens once per parcel belongs on **One time charge**. Delivery upgrades, gift wrapping, handling fees, artwork setup, rush production — all of them.

## Notes

* The mode is per option. If different values in one option need different scaling, you need two options with conditional logic, or **Mixed quantity**.
* **Mixed quantity** only appears once the option is multi-select.
* **Per character** only appears on Text and Textarea.
* Hidden options are not charged at all, whatever the mode.
* An add-on on a **default value** is charged from page load. Combined with **Default** mode on a multi-buy, that surprises people.

## Troubleshooting

<details>
<summary>The dropdown makes no difference</summary>

The option has no price attached. Set the **Price** first.
</details>

<details>
<summary>Customers are charged too much when they buy several</summary>

You are on **Default**. For per-order charges, use **One time charge**.
</details>

<details>
<summary>Set quantity is not visible</summary>

It only appears for **Fixed quantity** and **Dynamic quantity**.
</details>

<details>
<summary>Mixed quantity is missing from the list</summary>

The option is single-select. Turn on [Allow multiple](../option-types/shared-settings/selection-behaviour.md#allow-multiple), or use a Checkbox.
</details>

<details>
<summary>Per character is missing from the list</summary>

It exists on Text and Textarea only.
</details>

<details>
<summary>The quantity box does not appear for the customer</summary>

Only the two "by customer" modes and **Mixed quantity** show one. The others take the quantity from you or from the product.
</details>

<details>
<summary>Per-character charges are enormous</summary>

There is no **Max character** limit. Set one, and show the counter.
</details>
