---
description: The option types and add-on mode that do not work in Shopify POS, and what to use instead.
icon: circle-exclamation
---

# POS limitations

Read this before building anything for POS. Everything here fails quietly rather than loudly — an option that simply is not there, or an add-on that simply is not charged.

## The three that matter

<table><thead><tr><th width="290">Not supported in POS</th><th>Use instead</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/dimension.md">Dimension</a></td><td><a href="../option-types/input-types/number.md">Number</a> fields, one per measurement</td></tr><tr><td><a href="../option-types/selection-types/product-links.md">Product links</a></td><td>Nothing needed — staff can find the other product in POS directly</td></tr><tr><td>The <a href="../add-on-pricing/add-price-directly.md">Add price</a> add-on mode</td><td><a href="../add-on-pricing/use-an-existing-product.md">Use existing product</a> or <a href="../add-on-pricing/auto-generate-a-product.md">Automatically generate a product</a></td></tr></tbody></table>

The app warns you about the two option types when you add them: each carries a notice saying it is not supported on the POS channel and recommending you skip it if you use POS.

## Add price is the one that costs money

The two option types are visible problems — staff notice a missing field. **Add price** is not: the option appears, the customer chooses it, the sale completes, and the charge is simply absent.

{% hint style="danger" %}
If an option set is published to **Point of Sale**, check every add-on it contains. Any value using **Add price** is money you will not collect at the counter.

Both product-backed modes work in POS, and switching is quick — open the value's **Price** field and change the tab.
{% endhint %}

### Auditing an option set for POS

{% stepper %}
{% step %}
### List the option sets published to POS

On the **Option Sets** list, check the sales channels on each row.
{% endstep %}

{% step %}
### Open each one and look at every priced option

Input types: the **Price** field under **Add-on Settings**. Selection types: the **Price** column, row by row.
{% endstep %}

{% step %}
### Change any Add price value to a product-backed mode

**Automatically generate product** is the easiest swap — same price, same effort, and it works in POS.
{% endstep %}

{% step %}
### Remove or replace Dimension and Product links options

Or move them into an option set published to Online Store only.
{% endstep %}

{% step %}
### Test a real sale in POS

Add the product, fill in the options, and check the total before completing.
{% endstep %}
{% endstepper %}

## Other differences from the storefront

<table><thead><tr><th width="290">Behaviour</th><th>In POS</th></tr></thead><tbody><tr><td>Country rules</td><td>Not a meaningful filter — an in-person sale has no browsing country</td></tr><tr><td>Customer rules</td><td>Depend on a customer being attached to the sale</td></tr><tr><td>Widget placement, colours, typography</td><td>Not applicable. POS renders its own interface</td></tr><tr><td>Match theme style</td><td>Not applicable</td></tr><tr><td>Quickview and other page settings</td><td>Storefront only</td></tr><tr><td>The Personalizer</td><td>Built for a product page with a photograph. Treat it as a storefront feature and test carefully before relying on it at the counter</td></tr><tr><td>Personalising an add-on line</td><td>Not possible. Add-on lines belong to the item they were added for</td></tr></tbody></table>

## The recommended pattern

Where your online form is long or uses unsupported types, run two option sets:

<table><thead><tr><th width="230">Option set</th><th width="230">Sales channel</th><th>Contents</th></tr></thead><tbody><tr><td>Your full form</td><td><strong>Online Store</strong> only</td><td>Everything, including Dimension and Product links if you need them</td></tr><tr><td>A counter form</td><td><strong>Point of Sale</strong> only</td><td>Only what staff need while a customer waits, with product-backed add-ons throughout</td></tr></tbody></table>

Both target the same products. Because each is published to one channel only, they never collide.

See [Status and sales channels](../concepts/status-and-sales-channels.md).

## Next steps

* [Set up and use options in POS](set-up-and-use.md)
* [Add-on pricing limitations](../add-on-pricing/limitations.md)
* [Status and sales channels](../concepts/status-and-sales-channels.md)
