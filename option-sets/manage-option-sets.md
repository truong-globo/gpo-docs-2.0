---
description: >-
  The Option Sets list: searching, filtering, sorting, bulk actions, and the
  per-row controls.
icon: table-list
---

# Manage option sets

**Option Sets** is the list of everything you have built. Once you have more than a handful, this page is where you spend your admin time.

## What each row shows

<table><thead><tr><th width="180">Column</th><th>What it tells you</th></tr></thead><tbody><tr><td>ID</td><td>The option set's internal number. Useful when you talk to support.</td></tr><tr><td><strong>Name</strong></td><td>The name you gave it. Select it to open the builder.</td></tr><tr><td><strong>Status</strong></td><td><strong>Active</strong> or <strong>Draft</strong>, switchable in place.</td></tr><tr><td><strong>Sales channels</strong></td><td>Which channels it is published to, editable in place.</td></tr><tr><td><strong>Date created</strong></td><td>When it was created.</td></tr><tr><td><strong>Actions</strong></td><td>Per-row actions, including <strong>View Analytics</strong>.</td></tr></tbody></table>

<!-- SCREENSHOT: set-list-overview | App admin → Option Sets | Bảng danh sách với các cột, tab filter All/Active/Draft, ô search, nút Create option set | Không khoanh -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Option Sets list page with filter tabs, search, and the create button"><figcaption><p>The Option Sets list, with filters, search, and bulk actions.</p></figcaption></figure>

## Finding an option set

<table><thead><tr><th width="200">Tool</th><th>How it works</th></tr></thead><tbody><tr><td>Search</td><td>Type into the filter field to search option set names.</td></tr><tr><td>Status tabs</td><td><strong>All</strong>, <strong>Active</strong>, <strong>Draft</strong>. The quickest way to catch a set you forgot to activate.</td></tr><tr><td>Sort</td><td><strong>Option set name</strong> A–Z or Z–A, or <strong>Created</strong> oldest or newest first.</td></tr><tr><td>Pagination</td><td>The list is paged. Move through pages at the bottom.</td></tr></tbody></table>

Your search, filter, and sort are kept in the page address, so going into an option set and coming back returns you to the same view.

## Creating from this page

**Create option set** offers two routes:

* **Create from scratch** — an empty option set. See [Create an option set](create-an-option-set.md).
* **Use a template** — opens **Templates** to copy a ready-made set. See [Templates](../templates/README.md).

If your plan limits how many option sets you may have and you are at the limit, **Create from scratch** is disabled and shows an upgrade prompt.

## Bulk actions

Tick one or more rows and a bulk action bar appears.

<table><thead><tr><th width="230">Action</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Set as active</strong></td><td>Publishes the selected sets. You are asked to confirm, with a reminder that this makes them available to their selected sales channels and products.</td></tr><tr><td><strong>Set as draft</strong></td><td>Hides the selected sets from all their sales channels. Also confirmed first.</td></tr><tr><td><strong>Duplicate option sets</strong></td><td>Copies each selected set. See <a href="duplicate-and-delete.md">Duplicate and delete</a>.</td></tr><tr><td><strong>Save as Template</strong></td><td>Turns the selection into reusable templates. See <a href="../templates/custom-templates.md">Custom templates</a>.</td></tr><tr><td><strong>Delete option sets</strong></td><td>Permanently removes them. Confirmed first, and it cannot be undone.</td></tr></tbody></table>

{% hint style="danger" %}
**Delete option sets** cannot be undone. If you might want a set back, use **Set as draft** instead — it hides the set while keeping everything intact. Better still, export first: see [Import and export](import-and-export.md).
{% endhint %}

<!-- SCREENSHOT: set-list-bulk-actions | App admin → Option Sets, đã tick vài dòng | Thanh bulk action với Set as active / Set as draft / Duplicate + menu chứa Save as Template và Delete | Khoanh thanh bulk action -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The bulk action bar with set as active, set as draft, duplicate, and the overflow menu"><figcaption><p>Bulk actions save opening each option set to change one thing.</p></figcaption></figure>

## Changing status and channels without opening a set

Two things are editable directly on the row, which is faster than opening the builder:

* **Status** — flip a set between **Active** and **Draft** in place.
* **Sales channels** — open the row's channels control, switch **Online Store** or **Point of Sale**, then save.

Unlike the builder, both of these save immediately.

{% hint style="info" %}
This is how you take options off your storefront temporarily — for a sale, or while you rework them. Set the option set to **Draft**; everything is preserved, and switching it back to **Active** restores it exactly. See [Create an option set](create-an-option-set.md) for what each status and channel means.
{% endhint %}

## Import and export

The page's secondary actions are **Export option sets** and **Import option sets**.

Export asks what to include — the current page, all option sets, or just your selection. Import accepts a file, including files exported from several other product options apps.

Both are plan-gated. Full detail: [Import and export](import-and-export.md).

## View Analytics

Each row's actions include **View Analytics**, which opens the revenue and usage report for that option set.

This requires a plan that includes advanced analytics. On other plans the action shows an upgrade prompt. See [Option set analytics](analytics.md).

## Keeping the list readable

Some habits that pay off once you pass ten option sets:

* **Name by product family, not by contents.** `Engravable jewellery` beats `Text + checkbox`.
* **Delete or draft the experiments.** A list full of `Test`, `Test 2`, `Copy of Test` makes it hard to see what is actually live.
* **Filter to Active before debugging.** When an option appears twice on a product page, the culprit is almost always a second active set. Filtering to **Active** makes that visible immediately.
* **Draft rather than delete.** Drafting costs nothing and keeps the work.
* **Export before a big change.** An exported file is a free backup.

## Troubleshooting

<details>
<summary>An option set is missing from the list</summary>

Check the status tab you are on — you may be filtered to **Active** while the set is **Draft**. Clear the search field too.
</details>

<details>
<summary>Create from scratch is disabled</summary>

You are at your plan's limit on option sets. Delete one you no longer need, or upgrade. See [Locked features](../plans/compare-plans.md).
</details>

<details>
<summary>Duplicate is disabled</summary>

Duplicating the selected sets would take you past your plan's limit. Reduce the selection or upgrade.
</details>

<details>
<summary>Export or Import shows an upgrade prompt</summary>

Import and export are plan-gated features. See [Compare plans](../plans/compare-plans.md).
</details>

<details>
<summary>I deleted an option set by mistake</summary>

Deletion cannot be undone. If you exported previously, re-import that file. Otherwise the set must be rebuilt — and if it created add-on products, those products still exist in your Shopify catalogue.
</details>

<details>
<summary>An option appears twice on a product page</summary>

Two active option sets both match that product. Filter the list to **Active** and check which sets could apply — particularly any using **Apply to All Products**. See [Assign to products](assign-to-products.md).
</details>
