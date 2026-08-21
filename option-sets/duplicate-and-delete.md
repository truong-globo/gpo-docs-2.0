---
description: >-
  Copy an option set as a starting point, and remove one permanently — including
  what a duplicate inherits that you probably did not expect.
icon: copy
---

# Duplicate and delete

Both actions live on the **Option Sets** list. Duplicating is the fastest way to build a variation; deleting is permanent, so read the warning before you use it.

## Duplicate

### When to duplicate

* You want a second version of a set for a different customer group or country.
* You want to try a big change without risking the working set.
* You want a similar set for a different product family and only the targeting changes.

If you expect to reuse the same structure repeatedly, save it as a template instead — templates are built for reuse and do not clutter your option set list. See [Custom templates](../templates/custom-templates.md).

### Steps

{% stepper %}
{% step %}
### Select the option sets

On the **Option Sets** list, tick one or more rows.
{% endstep %}

{% step %}
### Select Duplicate option sets

The action is in the bulk action bar. Each selected set is copied.
{% endstep %}

{% step %}
### Rename the copies immediately

This is the important step. Read the warning below before you go anywhere else.
{% endstep %}
{% endstepper %}

### What a duplicate inherits

{% hint style="warning" %}
A duplicate is a complete copy — **including its name, its status, its sales channels, and its product rule**.

That means if you duplicate an **Active** option set that applies to all products, you immediately have two active option sets applying to all products, with the same name. Shoppers will see every option twice until you fix it.
{% endhint %}

So the first two things to do after duplicating are:

1. **Rename it**, so you can tell the two apart in the list.
2. **Change its targeting**, or set it to **Draft** while you work on it.

<table><thead><tr><th width="290">Copied</th><th>Not copied</th></tr></thead><tbody><tr><td>Every option and all its settings</td><td>Nothing — a duplicate is a full copy</td></tr><tr><td>Option values, prices, images, help text</td><td></td></tr><tr><td>Conditional logic rules</td><td></td></tr><tr><td>Product, customer, and country rules</td><td></td></tr><tr><td>Status and sales channels</td><td></td></tr><tr><td>Personalizer settings and background</td><td></td></tr><tr><td>The name</td><td></td></tr></tbody></table>

Add-on products are **shared**, not copied. If an option value in the original pointed at a generated add-on product, the duplicate points at the same product. Both option sets sell the same add-on and draw down the same stock. That is usually what you want — but if you intended two separate add-ons with separate inventory, reconfigure the add-on in the copy. See [Add-on pricing](../add-on-pricing/README.md).

<!-- SCREENSHOT: set-duplicate-result | App admin → Option Sets sau khi duplicate | 2 dòng cùng tên, cùng status Active | Khoanh 2 dòng trùng tên (mũi tên nhỏ) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The option sets list showing a duplicated set with the same name and status as the original"><figcaption><p>A duplicate keeps the original's name and status — rename it straight away.</p></figcaption></figure>

### The two-versions pattern

Duplicating is how you build "the same options, but different for some shoppers":

{% stepper %}
{% step %}
### Duplicate your working set

Start from the set that already works.
{% endstep %}

{% step %}
### Set the copy to Draft

So it cannot reach shoppers while you edit it.
{% endstep %}

{% step %}
### Change what differs

Adjust prices, add or remove options, change the wording.
{% endstep %}

{% step %}
### Split the audiences so they cannot overlap

On the **Customers** tab, give the copy a rule such as `Customer tags — is equal to — wholesale`, and give the original the opposite: `Customer tags — is not equal to — wholesale`.

If you skip this step, both sets render for the same shopper.
{% endstep %}

{% step %}
### Activate the copy

Both sets are now live, but only one applies to any given shopper.
{% endstep %}
{% endstepper %}

The same pattern works with the **Countries** tab for market-specific variations. See [Assign to customers](assign-to-customers.md) and [Assign to countries](assign-to-countries.md).

### Limits

If duplicating would push you past your plan's option set limit, the action is disabled with an upgrade prompt. When you select several sets and only some fit, the app tells you that some were created and the rest were not.

## Delete

{% hint style="danger" %}
Deleting an option set is **permanent**. There is no trash, no undo, and no recovery. Everything goes: options, values, prices, conditional logic, and rules.
{% endhint %}

### Prefer drafting

In almost every case where you want a set gone, **Set as draft** is the better action:

<table><thead><tr><th width="200">Draft</th><th>Delete</th></tr></thead><tbody><tr><td>Stops rendering everywhere immediately</td><td>Stops rendering everywhere immediately</td></tr><tr><td>Keeps all your work</td><td>Destroys all your work</td></tr><tr><td>Reversible in one click</td><td>Not reversible</td></tr><tr><td>Leaves a row in your list</td><td>Cleans up your list</td></tr></tbody></table>

Draft it, and delete it in three months if you never went back to it.

### Before you delete

{% stepper %}
{% step %}
### Export it

Select the set and use **Export option sets**. The file is a free backup and can be re-imported later. See [Import and export](import-and-export.md).
{% endstep %}

{% step %}
### Check for add-on products

Add-on products the app generated for this set are **not** deleted with it. They stay in your Shopify catalogue.

Decide whether you want them: if the set is gone for good, delete or archive those products in Shopify admin so they do not linger. See [Stock and inventory](../add-on-pricing/stock-and-inventory.md).
{% endstep %}

{% step %}
### Check for automations that reference it

A workflow using the dynamic order-tag mode points at a specific option in a specific option set. Deleting the set breaks that workflow — update it. See [Update order tags](../automations/update-order-tags.md).
{% endstep %}
{% endstepper %}

### Steps

{% stepper %}
{% step %}
### Select the option sets

Tick the rows on the **Option Sets** list.
{% endstep %}

{% step %}
### Select Delete option sets

It is in the bulk action menu, marked as destructive.
{% endstep %}

{% step %}
### Confirm

The dialog names how many sets you are removing and warns that it cannot be undone. Confirm to delete.
{% endstep %}
{% endstepper %}

### What deleting does not touch

* Orders already placed. Option details on past orders are part of the order record and stay exactly as they were.
* Add-on products, as described above.
* Templates you saved from the set. Those are separate objects and survive.
* Store-wide settings, colours, and translations.

## Troubleshooting

<details>
<summary>I duplicated a set and my product page now shows every option twice</summary>

The duplicate inherited **Active** status and the same product rule. Set the duplicate to **Draft**, or change its targeting.
</details>

<details>
<summary>I cannot tell my duplicates apart</summary>

Duplicates keep the original name. Sort the list by **Created — Newest first**; the copy is the newer row. Rename it, then use the ID column to be certain which is which.
</details>

<details>
<summary>Duplicate is disabled</summary>

The copies would exceed your plan's option set limit. Reduce the selection or upgrade.
</details>

<details>
<summary>I deleted the wrong option set</summary>

It cannot be recovered from within the app. If you exported it before, re-import that file. Otherwise it must be rebuilt — and check whether its add-on products are still in your Shopify catalogue so you can reuse them.
</details>

<details>
<summary>I deleted a set but products created by it are still in my catalogue</summary>

Expected. Generated add-on products are ordinary Shopify products and are not removed with the option set. Delete or archive them in Shopify admin.
</details>

## Next steps

* [Import and export](import-and-export.md) — how to take that backup.
* [Custom templates](../templates/custom-templates.md) — the better tool for reuse.
* [Manage option sets](manage-option-sets.md)
