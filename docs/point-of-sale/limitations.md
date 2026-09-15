---
description: The option types and add-on mode that do not work in Shopify POS, and what to use instead.
icon: circle-exclamation
---

# POS limitations

Read this before you build anything for POS. None of these limitations produces an error message. An option is missing, or an add-on is not charged.

## The three limitations

<table><thead><tr><th width="290">Not supported in POS</th><th>Use instead</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/dimension.md">Dimension</a></td><td><a href="../option-types/input-types/number.md">Number</a> fields, one per measurement</td></tr><tr><td><a href="../option-types/selection-types/product-links.md">Product links</a></td><td>Nothing needed — staff can find the other product in POS directly</td></tr><tr><td>The <a href="../add-on-pricing/add-price-directly.md">Add price</a> add-on mode</td><td><a href="../add-on-pricing/use-an-existing-product.md">Use existing product</a> or <a href="../add-on-pricing/auto-generate-a-product.md">Automatically generate a product</a></td></tr></tbody></table>

The app warns you about the two option types when you add them. Each one displays a notice saying it is not supported on the POS channel.

## Add price is the one to check

Staff notice a missing field, so the two option types are visible problems. **Add price** is not. The option appears, the customer selects it, the sale completes, and the charge is not applied.

{% hint style="danger" %}
If an option set is published to **Point of Sale**, check every add-on it contains. Any value using **Add price** is not charged at the counter.

Both product-backed modes work in POS. To switch, open the value's **Price** field and change the tab.
{% endhint %}

### Auditing an option set for POS

{% stepper %}
{% step %}
### List the option sets published to POS

On the **Option Sets** list, check the sales channels shown on each row.
{% endstep %}

{% step %}
### Open each one and check every priced option

For input types, check the **Price** field under **Add-on Settings**. For selection types, check the **Price** column for each value.
{% endstep %}

{% step %}
### Change any Add price value to a product-backed mode

**Automatically generate product** is the simplest replacement. It charges the same price and works in POS.
{% endstep %}

{% step %}
### Remove or replace Dimension and Product links options

Alternatively, move them into an option set published to Online Store only.
{% endstep %}

{% step %}
### Test a real sale in POS

Add the product, complete the options, and check the total before finishing the sale.
{% endstep %}
{% endstepper %}

## Other differences from the storefront

<table><thead><tr><th width="290">Behavior</th><th>In POS</th></tr></thead><tbody><tr><td>Country rules</td><td>Not a meaningful filter — an in-person sale has no browsing country</td></tr><tr><td>Customer rules</td><td>Depend on a customer being attached to the sale</td></tr><tr><td>Widget placement, colors, typography</td><td>Not applicable. POS renders its own interface</td></tr><tr><td>Match theme style</td><td>Not applicable</td></tr><tr><td>Quickview and other page settings</td><td>Storefront only</td></tr><tr><td>The Personalizer</td><td>Built for a product page with a photograph. Treat it as a storefront feature and test carefully before relying on it at the counter</td></tr><tr><td>Personalizing an add-on line</td><td>Not possible. Add-on lines belong to the item they were added for</td></tr></tbody></table>

## Recommended setup

If your online form is long or uses unsupported types, create two option sets:

<table><thead><tr><th width="230">Option set</th><th width="230">Sales channel</th><th>Contents</th></tr></thead><tbody><tr><td>Your full form</td><td><strong>Online Store</strong> only</td><td>Everything, including Dimension and Product links if you need them</td></tr><tr><td>A counter form</td><td><strong>Point of Sale</strong> only</td><td>Only what staff need while a customer waits, with product-backed add-ons throughout</td></tr></tbody></table>

Both target the same products. Because each is published to one channel only, they do not overlap.

See [Activate and publish](../option-sets/create-an-option-set.md#publish-the-option-set).
