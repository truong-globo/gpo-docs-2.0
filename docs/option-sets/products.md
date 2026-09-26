---
description: See which option set each product uses, and why the others were skipped.
icon: bag-shopping
---

# Products

**Products** in the app menu lists your Shopify products and, beside each one, the option set your storefront actually uses for it. It answers the question the option set list cannot: _this product — what do customers see on it, and why?_

<figure><img src="../.gitbook/assets/prod 1.png" alt="The Products list with the option set applied to each product"><figcaption><p>One row per product, with the option set your storefront uses for it.</p></figcaption></figure>

## Only one option set runs

This is the rule the whole page is built on:

{% hint style="info" %}
Several option sets can match the same product, but **only one runs**. Your store checks them **newest first** and uses the first one that can run.
{% endhint %}

So a product with three matching option sets still shows the options from one of them. The others appear under **Also matches**, and the page tells you why each was passed over.

<table><thead><tr><th width="200">State</th><th>Meaning</th></tr></thead><tbody><tr><td><strong>Applied</strong></td><td>The one your storefront uses</td></tr><tr><td><strong>Not applied</strong></td><td>It matches, but a newer option set won</td></tr><tr><td><strong>Can't run</strong></td><td>It matches, but something stops it — see the table below</td></tr><tr><td><strong>No option set</strong></td><td>Nothing matches. Customers see no options on this product</td></tr></tbody></table>

### Why an option set can't run

<table><thead><tr><th width="290">Reason</th><th>Fix</th></tr></thead><tbody><tr><td>This option set is a draft</td><td>Set it to <strong>Active</strong>. See <a href="create-an-option-set.md#publish-the-option-set">Activate and publish</a></td></tr><tr><td>It isn't published to Online Store</td><td>Select <strong>Online Store</strong> under its <strong>Sales channels</strong></td></tr><tr><td>It's over your plan's limit</td><td>Option sets beyond your plan's allowance stop running. See <a href="../plans-and-billing/compare-plans.md">Compare plans</a></td></tr><tr><td>Its rule is incomplete, or your store can't check it</td><td>Open the option set and finish the rule. See <a href="assign-to-products.md">Assign to products</a></td></tr></tbody></table>

{% hint style="warning" %}
**A broken rule stops the check.** When your store reaches an option set whose rule it cannot evaluate, it stops there rather than carrying on to older ones — so the product shows no options at all, even if an older option set would have matched.

This is why one unfinished rule can silently remove options from products you never touched.
{% endhint %}

## Finding a product

<table><thead><tr><th width="180">Control</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Search</strong></td><td>By title, ID, SKU, or handle</td></tr><tr><td><strong>Filter</strong></td><td>By <strong>Status</strong>, <strong>Product type</strong>, <strong>Vendor</strong>, or <strong>Tagged with</strong></td></tr><tr><td><strong>Sort</strong></td><td>Title A–Z or Z–A, newest created, recently updated, product type, or vendor</td></tr></tbody></table>

Products carry their Shopify status — **Active**, **Draft**, **Unlisted**, or **Archived** — so you can tell a product with no options from a product that is not on your store at all.

## The product page

Selecting a product opens everything the app knows about it.

**Option sets that match this product** lists them in the order your store checks them, with the applied one first. Each row says whether it is applied, not applied, or cannot run, and adds a note where a rule narrows it further:

* _Shows only to customers who match its customer rule_
* _Shows only in the countries its country rule allows_

Those two are worth reading carefully. An option set can be **Applied** here and still show nothing to a particular customer, because customer and country rules are evaluated per visitor rather than per product. See [Assign to customers](assign-to-customers.md) and [Assign to countries](assign-to-countries.md).

**Product details** shows the fields your rules actually read — **Price**, **Product ID**, **SKU**, **Handle**, **Tags**, and the **collections in your rules**. If a rule is not matching the way you expect, this is where you check the value it is matching against.

A collection the product belongs to but which is not published to Online Store is marked, because rules skip it.

<figure><img src="../.gitbook/assets/prdu 2.png" alt="A product page listing the option sets that match it and the fields its rules read"><figcaption><p>The option sets that match, in the order your store checks them.</p></figcaption></figure>

**Preview in store** opens the product with its options, which works even for a draft product that is not on your storefront yet. **View in admin** opens it in Shopify.

## Using it to troubleshoot

<table><thead><tr><th width="330">Symptom</th><th>What the page tells you</th></tr></thead><tbody><tr><td>No options on a product</td><td>Whether anything matches at all, and if it does, what is blocking it</td></tr><tr><td>The wrong options on a product</td><td>Which option set won, and which ones were passed over</td></tr><tr><td>Options disappeared from several products at once</td><td>Look for an option set with a broken rule — it stops the check for every product it matches</td></tr><tr><td>A rule that should match but doesn't</td><td><strong>Product details</strong> shows the tag, type, vendor, and collections your rule is being tested against</td></tr><tr><td>Options show for you but not for a customer</td><td>A customer or country rule on the applied option set</td></tr></tbody></table>

## Notes

* The list reads your live Shopify catalog, so a product added a moment ago appears here.
* Product status comes from Shopify. A **Draft** product keeps its option set; it simply is not on your storefront yet.
* The page describes what your storefront does. It does not change anything — fixes are made in the option set itself.
* If Shopify is slow to respond, the page says so and asks you to refresh rather than showing a half-loaded list.
