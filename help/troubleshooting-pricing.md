---
description: Add-on charges that are missing, wrong, doubled, or applied when they should not be.
icon: money-bill-wave
---

# Pricing and add-on problems

Pricing problems fall into two groups: **display** problems, where the number shown is not what you expected, and **charging** problems, where the amount taken is wrong. They have different causes, so establish which you have first.

## Which do you have?

<table><thead><tr><th width="290">Symptom</th><th>Group</th></tr></thead><tbody><tr><td>No price shown beside an option</td><td>Display</td></tr><tr><td>The product price does not change as the shopper chooses</td><td>Display</td></tr><tr><td>The product looks more expensive than advertised</td><td>Display</td></tr><tr><td>The cart total is not what the product page showed</td><td>Could be either — read on</td></tr><tr><td>Nothing is charged at checkout</td><td>Charging</td></tr><tr><td>The charge is multiplied when several are bought</td><td>Charging</td></tr></tbody></table>

Remember that the product page shows a **preview** and checkout applies the real prices. See [How pricing is applied](../add-on-pricing/how-pricing-is-applied.md).

## Display problems

<details>
<summary>No price appears beside an option</summary>

**Settings** > **Settings** > **Add-on price**. Two switches control this:

* **Show add-on for inputs** — Text, Textarea, Number
* **Show add-on for options** — the selection types

One covers input types and the other selection types, so turning off the wrong one looks like a bug. See [Add-on price display settings](../add-on-pricing/price-display-settings.md).

</details>

<details>
<summary>The product price does not change as the customer chooses</summary>

**Add add-on price to the product price** is off, so the add-on is shown separately instead of being folded into the displayed price. That is a valid way to present it — turn the setting on if you want one running total.

</details>

<details>
<summary>The product looks more expensive than my listed price, before anybody chooses anything</summary>

An option has a **Default value** with a price attached, so it is charged from page load.

Either remove the default, or make the default the free choice. This is the single most common pricing complaint. See [Required field and default value](../option-types/shared-settings/required-and-default-value.md#default-value).

</details>

<details>
<summary>The amount format is wrong</summary>

**Add-on money format** switches the currency code on and off, and **Add-on label format** controls the wrapper around the number — `(+ {{addon}})` by default. Keep `{{addon}}` in it, or the number has nowhere to go.

</details>

## Charging problems

<details>
<summary>Nothing is charged at all</summary>

In order:

1. **Is the option hidden?** A hidden option is not charged. Check its conditional logic rules.
2. **Is the price actually set?** Open the option's **Price** field, or the values table's **Price** column, and confirm it holds a value.
3. **Is the option set saved and Active?**
4. **Are you on POS with the Add price mode?** That combination is not supported. See [POS limitations](../pos/limitations.md).

If all four are right, contact support — this one is not something to work around.

</details>

<details>
<summary>The charge multiplies when a customer buys several</summary>

That is **Default** mode, where the add-on follows the product quantity. For anything charged per order — gift wrap, delivery upgrades, setup fees — use **One time charge**.

See [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md).

</details>

<details>
<summary>Only one charge applies when I expected several</summary>

The reverse: you are on **One time charge** where you want **Default**.

</details>

<details>
<summary>A per-character charge is enormous</summary>

There is no **Max character** limit on the option, so the charge is unbounded. Set one, and turn on the character counter so shoppers can see it building.

</details>

<details>
<summary>Every selected value is being charged on a multi-select</summary>

That is correct behaviour. Cap it with **Max selections**. See [Limits](../option-types/shared-settings/limits.md#min-and-max-selections).

</details>

<details>
<summary>The cart total does not match the product page</summary>

First check whether it is a display setting — **Add add-on price to the product price** changes what the page shows without changing what is charged.

If the amounts genuinely differ, check whether an option was hidden by a conditional rule between the shopper choosing and adding to cart. Hidden options are not charged.

</details>

## Stock and product problems

<details>
<summary>Out of stock options does nothing</summary>

Three causes, in order:

1. The values use **Add price**, which has no product and therefore no stock.
2. The add-on product does not have inventory tracking turned on.
3. The variant is still set to continue selling when out of stock.

Generated products arrive needing both 2 and 3 doing by hand. See [Stock and inventory](../add-on-pricing/stock-and-inventory.md).

</details>

<details>
<summary>Customers can buy add-ons I have run out of</summary>

Same cause. The default inventory policy on a generated product is to keep selling.

</details>

<details>
<summary>Generated products appear in my collections and search</summary>

Exclude the tag `globo-product-options` from those collections. Do not unpublish them from the Online Store — an unpublished product cannot be added to the cart. See [Automatically generate a product](../add-on-pricing/auto-generate-a-product.md).

</details>

<details>
<summary>"This product does not exist on your store anymore."</summary>

A linked product or variant was deleted in Shopify. Reopen the price dialog and select a current one.

</details>

<details>
<summary>Two option sets are draining the same stock</summary>

They link to the same add-on product — which is what happens when you duplicate an option set. If you need separate counts, generate a product for one of them.

</details>

<details>
<summary>Add-on prices in the app look out of date</summary>

Run **Sync Add-on data** from the builder's more-actions menu.

</details>

## Dimension formula problems

<details>
<summary>"Formula cannot contain subtraction"</summary>

Remove the `-`. Use multiplication, addition, and division instead.

</details>

<details>
<summary>The calculated price is out by a factor of ten or a hundred</summary>

Your rate is out by an order of magnitude. Work it back from a size you know the price of: for a 60 × 90 piece selling at $54, the rate is 54 ÷ 5400 = 0.01. See [Dimension add-on formula](../add-on-pricing/dimension-formula.md).

</details>

## Next steps

* [Add-on pricing](../add-on-pricing/README.md)
* [How pricing is applied](../add-on-pricing/how-pricing-is-applied.md)
* [Add-on pricing limitations](../add-on-pricing/limitations.md)
