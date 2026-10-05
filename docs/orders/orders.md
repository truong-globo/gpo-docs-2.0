---
description: Every order that used your options, with the revenue your add-ons brought in.
icon: receipt
---

# Overview

**Orders** in the app menu lists the orders that came in through your option sets, and totals what your options earned. Shopify's own order list cannot do this — it has no idea which orders used an option set, or how much of a total came from add-ons.

{% hint style="info" %}
Orders are kept for **90 days**. Older ones drop off the list, so export anything you need to keep. See [Export orders and files](export.md).
{% endhint %}

Viewing orders may not be available on all plans. See [Compare plans](../plans-and-billing/compare-plans.md).

<figure><img src="../.gitbook/assets/order 1.png" alt="The Orders list with its metrics along the top"><figcaption><p>Totals for the period, then the orders behind them.</p></figcaption></figure>

## The numbers along the top

<table><thead><tr><th width="250">Metric</th><th>What it counts</th></tr></thead><tbody><tr><td><strong>Orders with options</strong></td><td>Orders placed with at least one option set in this period</td></tr><tr><td><strong>Total sales</strong></td><td>Total value of those orders, including shipping and taxes</td></tr><tr><td><strong>Average order value</strong></td><td>Total sales divided by the number of orders</td></tr><tr><td><strong>Revenue from add-ons</strong></td><td>What customers paid for add-on prices and add-on products</td></tr></tbody></table>

Each one is compared against the previous period of the same length, so a 30-day range is measured against the 30 days before it.

**Revenue from add-ons** is the figure worth watching. It is the money your options brought in that the product price alone would not have.

### Top option sets and Top option values

Two rankings sit below the metrics.

<table><thead><tr><th width="250">Ranking</th><th>Based on</th></tr></thead><tbody><tr><td><strong>Top option sets</strong></td><td>Add-on revenue, counting both add-on prices and add-on products</td></tr><tr><td><strong>Top option values</strong></td><td>Only values that added an <strong>add-on product</strong>, ranked by that product's revenue</td></tr></tbody></table>

{% hint style="warning" %}
The two rankings do not use the same figure. **Top option values** leaves out [Fixed amount](../add-on-pricing/add-price-directly.md) charges, because a fixed amount has no product behind it to attribute revenue to.

If a value earns well through a fixed amount, it will not appear there. Use **Top option sets** for the complete picture.
{% endhint %}

An option set deleted since the order was placed still appears, marked **Deleted option set**.

## The list

<table><thead><tr><th width="230">Column</th><th>Shows</th></tr></thead><tbody><tr><td><strong>Order</strong></td><td>The order number, and the channel it came from</td></tr><tr><td><strong>Date</strong></td><td>When it was placed</td></tr><tr><td><strong>Products</strong></td><td>How many items it contains</td></tr><tr><td><strong>Files</strong></td><td>How many files the customer uploaded</td></tr><tr><td><strong>Add-ons</strong></td><td>What the add-ons on this order came to</td></tr><tr><td><strong>Total</strong></td><td>The order total</td></tr><tr><td><strong>Payment status</strong></td><td>Paid, Partially paid, Payment pending, Refunded, and so on</td></tr><tr><td><strong>Fulfillment status</strong></td><td>Fulfilled, Partially fulfilled, Unfulfilled, Scheduled, On hold</td></tr></tbody></table>

{% hint style="info" %}
**Payment and fulfillment status are only available for orders from the last 60 days.** Those two columns are read from Shopify live rather than stored, and Shopify stops serving them beyond that point. Everything else on the row keeps working for the full 90 days.
{% endhint %}

Orders from **Online Store**, **Point of Sale**, and **draft orders** all appear, labelled by channel.

## Finding an order

<table><thead><tr><th width="200">Control</th><th>Options</th></tr></thead><tbody><tr><td><strong>Search</strong></td><td>By order</td></tr><tr><td><strong>Filter</strong></td><td><strong>With files</strong> or <strong>Without files</strong>, <strong>With add-ons</strong> or <strong>Without add-ons</strong>, by option set, and by channel</td></tr><tr><td><strong>Sort by</strong></td><td>Newest first, Oldest first, Highest total, Lowest total, Highest add-ons</td></tr></tbody></table>

**With files** is the filter to reach for first thing in the morning — it gives you exactly the orders waiting on artwork.

## Next

* [Order details](order-details.md) — the option summary, the uploaded files, and the notes for one order
* [Export orders and files](export.md) — getting the data out as CSV or ZIP

## Notes

* Only orders containing at least one option set appear. An ordinary order never shows up here.
* The list is a record of what was ordered. Editing an option set later does not change orders already placed.
* Nothing here changes an order. Use **View in Shopify** for anything that does.
