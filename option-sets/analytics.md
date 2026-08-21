---
description: >-
  See what an option set earned, which choices customers actually pick, and how
  much of your revenue comes from add-ons.
icon: chart-line
---

# Option set analytics

Analytics answers three questions about a specific option set: how much money it brought in, how much of that was add-ons, and which option values customers actually choose.

That last one is the most useful in practice. It tells you which choices to keep, which to price differently, and which to drop.

## Before you start

* Advanced analytics is plan-gated. On plans without it, **View Analytics** shows an upgrade prompt. See [Compare plans](../plans/compare-plans.md).
* Analytics is built from orders, so a new option set shows nothing until it has sold something.

## Opening it

Go to **Option Sets**, find the set, and choose **View Analytics** from its row actions. Use the back action to return to the list.

<!-- SCREENSHOT: set-analytics-open | App admin → Option Sets | Menu action của 1 dòng đang mở với mục View Analytics | Khoanh mục View Analytics -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The row actions menu on the option sets list with View Analytics"><figcaption><p>Analytics is per option set, opened from its row on the list.</p></figcaption></figure>

## Choosing a period

The date range selector sits at the top and applies to everything on the page.

<table><thead><tr><th width="220">Range</th><th width="220">Range</th><th>Range</th></tr></thead><tbody><tr><td>Today</td><td>Last 60 days</td><td>Week to date</td></tr><tr><td>Yesterday</td><td>Last 90 days</td><td>Month to date</td></tr><tr><td>Last 7 days</td><td>Last week</td><td>Custom range</td></tr><tr><td>Last 30 days</td><td>Last month</td><td></td></tr></tbody></table>

**Last 7 days** is the default. **Custom range** lets you pick your own start and end dates.

The app also loads the equivalent previous period so the summary figures can show whether you are up or down. Choosing **Last 30 days** compares against the 30 days before that.

## The summary figures

<table><thead><tr><th width="240">Figure</th><th>What it counts</th></tr></thead><tbody><tr><td><strong>Total revenue</strong></td><td>All revenue from orders containing this option set — the products themselves plus their add-ons.</td></tr><tr><td><strong>Revenue from add-ons</strong></td><td>Just the add-on portion. Compare it with total revenue to see what your options are worth on their own.</td></tr><tr><td><strong>Total products</strong></td><td>How many products were sold through this option set.</td></tr><tr><td><strong>Total orders</strong></td><td>How many orders included it.</td></tr><tr><td><strong>Average order value</strong></td><td>Average value of those orders.</td></tr></tbody></table>

Each figure shows its movement against the previous period, so you can see direction as well as size.

<!-- SCREENSHOT: set-analytics-summary | App admin → Analytics của 1 option set | 5 ô số liệu Total revenue / Revenue from add-ons / Total products / Total orders / Average order value kèm chỉ số so sánh | Khoanh hàng 5 ô -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The analytics summary row with five figures and their trends against the previous period"><figcaption><p>Revenue from add-ons against total revenue is the number to watch.</p></figcaption></figure>

## The charts

<table><thead><tr><th width="270">Chart</th><th>Shows</th></tr></thead><tbody><tr><td><strong>Total sales</strong></td><td>Sales over time across the period, so you can see trend and spikes rather than one total.</td></tr><tr><td><strong>Most valued options</strong></td><td>Your option values ranked by what they earned, with a purchase count for each. This is the list that tells you which choices matter.</td></tr><tr><td><strong>Total products quantity</strong></td><td>Quantities split into <strong>Main Products</strong> and <strong>Add-on Products</strong>.</td></tr><tr><td><strong>Orders revenue distribution</strong></td><td>Revenue split between orders <strong>With Add-ons</strong> and <strong>Without Add-ons</strong> — the share of business where customers pay for an option.</td></tr><tr><td><strong>Average order value</strong></td><td>Average order value over time, so you can see whether a pricing change moved it.</td></tr></tbody></table>

A chart with no data for the chosen period says so rather than showing an empty grid. Widen the period if that happens.

<!-- SCREENSHOT: set-analytics-charts | App admin → Analytics của 1 option set | Các chart: Total sales, Most valued options, Total products quantity, Orders revenue distribution, Average order value | Không khoanh -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The analytics charts including most valued options and the add-on revenue split"><figcaption><p>Five views of the same period, from trend over time to a ranking of individual choices.</p></figcaption></figure>

## How to read it

**Revenue from add-ons against Total revenue.** If add-ons are a small fraction, the option set is helping customers buy rather than adding revenue — which may be fine, but it means pricing is not where the value is.

**Most valued options.** Look at both ends. The top entries are candidates for a price rise or for being made more prominent — move them higher in the option, or set one as the default value. The bottom entries, especially those with almost no purchases, are candidates for removal: every unused choice is one more decision for every shopper.

**Orders revenue distribution.** A low **With Add-ons** share usually means the paid option is not visible or not persuasive enough. Try clearer help text, a better label, or moving the option above the **Add to cart** button.

**Total products quantity.** A high add-on product count relative to main products means customers are buying several add-ons per order — worth checking your inventory can keep up. See [Stock and inventory](../add-on-pricing/stock-and-inventory.md).

## The store-wide chart

The **Dashboard** carries a smaller chart covering your whole store rather than one option set: **Total sales**, **Total orders**, and **Total products** over the last 7 or 30 days, with revenue plotted against add-on revenue and main products against add-on products.

Use the dashboard for the overall picture and this page when you want to know about one option set.

## Limits and notes

* Figures are built from orders, so they only cover completed orders — not carts, and not views of the product page. The app does not measure how many shoppers saw an option and skipped it.
* An order containing two option sets contributes to both sets' analytics.
* Money is shown in your store's currency format.
* Refunds and cancellations are reflected through the order data the app reads; expect figures for a recent period to settle over a day or two.
* Basic and advanced analytics differ by plan. The per-option-set page requires advanced.

## Troubleshooting

<details>
<summary>View Analytics shows an upgrade prompt</summary>

Advanced analytics is not in your plan. See [Compare plans](../plans/compare-plans.md).
</details>

<details>
<summary>Everything reads zero</summary>

Either the option set has not sold in the chosen period, or it is newer than the period. Widen the range to **Last 90 days**. Confirm the set is **Active** and has actually been ordered.
</details>

<details>
<summary>Revenue from add-ons is zero, but I charge for options</summary>

Check that your add-ons are configured on the options themselves rather than being baked into the product price. Open an option and confirm its **Price** field is set. See [Where you can set add-ons](../add-on-pricing/where-you-can-set-add-ons.md).
</details>

<details>
<summary>Most valued options is empty but I have sales</summary>

The set may consist only of input-type options — text, numbers, uploads — which have no option values to rank. This chart ranks values from selection options.
</details>

<details>
<summary>The numbers do not match my Shopify reports</summary>

They measure different things. Shopify reports cover all orders; this page covers only orders containing this option set, and splits out the add-on portion. Use Shopify for accounting and this page for comparing options.
</details>

## Next steps

* [Add-on pricing](../add-on-pricing/README.md) — act on what the numbers tell you.
* [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md) — change how a charge scales.
* [Manage option sets](manage-option-sets.md)
