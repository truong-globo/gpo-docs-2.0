---
description: >-
  Copy an option set as a starting point, and remove one permanently — including
  what a duplicate inherits that you probably did not expect.
icon: copy
---

# Duplicate and delete

Both actions are bulk actions on the **Option Sets** list: tick the rows, then choose the action.

## Duplicate

Duplicating is the fastest way to build a variation — a version for a different customer group or country, or a safe copy before a big change.

{% hint style="warning" %}
**A duplicate is a complete copy — including its name, status, sales channels, and product rule.**

Duplicate an **Active** set that applies to all products and you instantly have two active sets applying to all products, with the same name. Shoppers see every option twice until you fix it.

So do these two things immediately: **rename the copy**, and either **change its targeting** or **set it to Draft**.
{% endhint %}

<!-- SCREENSHOT: set-duplicate-result | App admin → Option Sets sau khi duplicate | 2 dòng cùng tên, cùng status Active | Khoanh 2 dòng trùng tên (mũi tên nhỏ) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The option sets list showing a duplicated set with the same name and status as the original"><figcaption><p>A duplicate keeps the original's name and status — rename it straight away.</p></figcaption></figure>

Everything else copies too: every option and its settings, values, prices, images, help text, conditional logic, all three targeting rules, and the Personalizer background.

One thing does **not** copy — **add-on products are shared**. If a value in the original pointed at a generated add-on product, the copy points at the same product. Both sets sell it and draw down the same stock. Usually that is what you want; if you need separate inventory, reconfigure the add-on in the copy. See [Add-on pricing](../add-on-pricing/README.md).

{% hint style="info" %}
Reusing the same structure repeatedly? Save it as a [custom template](../templates/custom-templates.md) instead. Templates are built for reuse and do not clutter your option set list.
{% endhint %}

<details>
<summary>Pattern: the same options, different for some shoppers</summary>

This is what duplicating is really for — wholesale pricing, market-specific wording, a members-only version.

1. **Duplicate the set that already works.**
2. **Set the copy to Draft**, so it cannot reach shoppers while you edit.
3. **Change what differs** — prices, wording, extra or fewer options.
4. **Split the audiences so they cannot overlap.** On the **Customers** tab give the copy `Customer tags — is equal to — wholesale`, and give the original the opposite, `Customer tags — is not equal to — wholesale`. **Skip this and both sets render for the same shopper.**
5. **Activate the copy.** Both are live, but only one applies to any given shopper.

The same pattern works with the **Countries** tab for market variations. See [Assign to customers](assign-to-customers.md) and [Assign to countries](assign-to-countries.md).

</details>

## Delete

{% hint style="danger" %}
Deleting is **permanent**. No trash, no undo, no recovery — options, values, prices, conditional logic, and rules all go.
{% endhint %}

### Draft it instead, usually

For almost every reason you might delete a set, **Set as draft** is the better action:

<table><thead><tr><th width="200">Draft</th><th>Delete</th></tr></thead><tbody><tr><td>Stops rendering everywhere immediately</td><td>Stops rendering everywhere immediately</td></tr><tr><td>Keeps all your work</td><td>Destroys all your work</td></tr><tr><td>Reversible in one click</td><td>Not reversible</td></tr><tr><td>Leaves a row in your list</td><td>Cleans up your list</td></tr></tbody></table>

Draft it now, and delete it in three months if you never went back.

### If you are deleting anyway

Three things to do first:

1. **Export it.** Select the set and use **Export option sets** — a free backup you can re-import. See [Import and export](import-and-export.md).
2. **Deal with its add-on products.** Products the app generated are **not** deleted with the set; they stay in your catalogue. Delete or archive them in Shopify admin if the set is gone for good.
3. **Check your automations.** A workflow using the dynamic order-tag mode points at a specific option in a specific set, and deleting the set breaks it. See [Update order tags](../automations/update-order-tags.md).

Then tick the rows, choose **Delete option sets** from the bulk action menu, and confirm.

### What deleting does not touch

Orders already placed — option details on past orders are part of the order record. Also add-on products, as above; templates you saved from the set; and store-wide settings, colours, and translations.
