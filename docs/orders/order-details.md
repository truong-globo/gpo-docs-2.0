---
description: >-
  One order's option summary, uploaded files, customer details, and your team's
  notes.
icon: file-invoice
---

# Order details

Selecting an order opens everything the app recorded about it — what the customer chose, what they uploaded, and what the options added to the total.

<figure><img src="../.gitbook/assets/order 2.png" alt="An order page showing the option summary for each product"><figcaption><p>Each product with the options chosen for it.</p></figcaption></figure>

## Option summary

Each product in the order is listed with the options chosen for it. **Show options** and **Hide options** collapse a product you are not working on, which helps on an order with many items.

A product the customer bought without any options says **No options for this product**.

Add-on products appear as their own entries, marked **Add-on product**, exactly as they do in the cart.

## Files

Files the customer uploaded are listed under the product they belong to, each with its own **Download**. **Download all** takes the whole order as a ZIP.

<table><thead><tr><th width="330">Message</th><th>Meaning</th></tr></thead><tbody><tr><td>This file could not be downloaded</td><td>A temporary problem. Try again in a moment</td></tr><tr><td>The file is no longer available</td><td>The file has been removed and cannot be recovered</td></tr><tr><td>This order has no files</td><td>Nothing was uploaded on this order</td></tr></tbody></table>

### Opening them in Google Drive

If you run [Google Drive sync](../automations/google-drive-sync/), **Open in Drive** takes you to this order's folder instead of downloading anything.

<table><thead><tr><th width="290">What you see</th><th>Why</th></tr></thead><tbody><tr><td><strong>Connect Google Drive</strong></td><td>No account connected yet. Once connected, files from new orders are copied automatically, one folder per order</td></tr><tr><td>Files aren't in Google Drive</td><td>The order was placed while the sync was off. Only orders placed while it is running are copied</td></tr><tr><td>Files are still being copied</td><td>The copy is in progress. Try again in a few minutes</td></tr><tr><td>Files couldn't be copied</td><td>Something failed. <strong>View sync logs</strong> gives the reason. See <a href="../automations/google-drive-sync/google-drive-sync-history.md">Google Drive sync history</a></td></tr><tr><td><strong>Reconnect Google Drive</strong></td><td>The connection expired, so files can no longer be copied or opened</td></tr></tbody></table>

## What the options added

**Summary** breaks the order total down, so you can see the options' share of it.

<table><thead><tr><th width="250">Line</th><th>What it is</th></tr></thead><tbody><tr><td><strong>Option add-ons</strong></td><td>Charges added by a fixed amount on an option</td></tr><tr><td><strong>Add-on products</strong></td><td>Charges from add-ons backed by a real product</td></tr><tr><td><strong>Shipping</strong>, <strong>Tax</strong>, <strong>Discount</strong>, <strong>Tip</strong></td><td>The rest of the order, from Shopify</td></tr></tbody></table>

The two add-on lines are separate because they reach the order differently. See [How pricing is applied](../add-on-pricing/how-pricing-is-applied.md).

## Customer and addresses

Contact information, shipping address, and billing address are shown as Shopify has them, with **Copy** on each so you can paste into a label or a courier form. A billing address identical to the shipping one says **Same as shipping address** rather than repeating it.

Fields Shopify has no value for are stated plainly — **No email**, **No phone number**, **No shipping address** — rather than left blank, so you can tell missing data from a display problem.

## Internal notes

**Add a note for your team** stores a note against the order inside the app. It saves as you type, and **Only your team can see this** is literal: it is not Shopify's order note, the customer never sees it, and it does not appear on any paperwork.

Use it for production notes that should not reach the customer — a colour the customer confirmed by email, a reprint, a decision about a blurry upload.

{% hint style="warning" %}
The note lives in the app, so it goes when the order drops off after 90 days. Anything that has to outlast that belongs in Shopify's own order notes. See [Order notes update](../automations/update-order-notes.md).
{% endhint %}

## Sync from Shopify

**Sync from Shopify** refetches the order. You need it rarely — mainly for orders recorded before this tab existed, which can be missing details.

<table><thead><tr><th width="330">Message</th><th>Meaning</th></tr></thead><tbody><tr><td>Order synced</td><td>Done. The page shows the refreshed details</td></tr><tr><td>This order was placed before the Orders tab</td><td>Its details can no longer be loaded from Shopify</td></tr><tr><td>This order can no longer be loaded from Shopify</td><td>Shopify only serves order details for the last 60 days</td></tr><tr><td>Too many syncs. Try again in a minute</td><td>Syncing is rate-limited. Wait, then retry</td></tr></tbody></table>

## Notes

* **View in Shopify** opens the order in Shopify admin, which is where you refund, fulfill, or edit it.
* The page is a record of the order as placed. Renaming an option later does not change it.
* An order older than 90 days says **This order isn't available**.
