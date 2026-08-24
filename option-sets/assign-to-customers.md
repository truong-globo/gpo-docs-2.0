---
description: >-
  Show an option set only to certain shoppers — by tag, name, email, or whether
  they are logged in at all.
icon: user-check
---

# Assign to customers

By default an option set is shown to everybody. The **Customers** tab narrows that: wholesale-only options, a VIP engraving service, or a field that only makes sense for signed-in shoppers.

## Before you start

* An option set is open in the builder. Select **Customers** in the left rail.
* Customer rules are plan-gated. If the switches are unavailable, see [Compare plans](../plans/compare-plans.md).
* This narrows an option set that already has a product rule. It does not replace it — the product rule still decides which products are in scope.

## The three methods

Like product rules, these are **mutually exclusive**: turning one on turns the other two off.

<table><thead><tr><th width="210">Method</th><th>Shows the option set to</th></tr></thead><tbody><tr><td><strong>Everyone</strong></td><td>All visitors, signed in or not. This is the default.</td></tr><tr><td><strong>Manual Selection</strong></td><td>Only the specific customers you pick from your customer list.</td></tr><tr><td><strong>Automatic Rules</strong></td><td>Anyone matching your conditions — customer tag, name, email, logged-in, or guest.</td></tr></tbody></table>

<!-- SCREENSHOT: set-customers-methods | App admin → builder → tab Customers | 3 khối Everyone / Manual Selection / Automatic Rules, Everyone đang bật | Khoanh 3 khối -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Customers tab with the Everyone, Manual Selection, and Automatic Rules blocks"><figcaption><p>Everyone is the default, so an option set reaches all shoppers until you narrow it.</p></figcaption></figure>

## Everyone

Nothing to configure. The option set is visible to all visitors, including people who are not signed in.

Leave this on unless you have a reason not to. Most option sets should be visible to everybody.

## Manual Selection

Pick individual customers from your Shopify customer list.

{% stepper %}
{% step %}
### Turn on Manual Selection

The block expands with a customer table and a **Select customers** button.
{% endstep %}

{% step %}
### Approve customer data access, once

The first time you use this, the app asks for permission to read your customer data, explaining that the data is used only for this feature and is not distributed.

Select **Update** to approve. This goes through Shopify, exactly like the original install. Until you approve it, you cannot pick customers.
{% endstep %}

{% step %}
### Select customers

**Select customers** opens a picker over your customer list. Search by name or email and select as many as you need.
{% endstep %}

{% step %}
### Review the list

Selected customers appear in a table. Remove one with the remove action on its row, or clear the list with **Deselect all customers** — which asks you to confirm first.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
A manual customer rule with nobody selected is incomplete. The builder shows "Please select customer to apply this option set." and blocks **Save**.
{% endhint %}

Manual selection suits a genuinely fixed list — three trade accounts, say. For anything that grows, tag those customers in Shopify and use an automatic rule instead.

## Automatic Rules

{% stepper %}
{% step %}
### Turn on Automatic Rules

The block expands with a **Customers must match** setting and one empty condition.
{% endstep %}

{% step %}
### Choose all conditions or any condition

**all conditions** requires every condition to be true; **any condition** requires at least one.
{% endstep %}

{% step %}
### Build a condition

<table><thead><tr><th width="270">Field</th><th>Matches against</th></tr></thead><tbody><tr><td><strong>Customer tags</strong></td><td>The tags on the customer's record in Shopify.</td></tr><tr><td><strong>Customer name</strong></td><td>The customer's name.</td></tr><tr><td><strong>Customer email</strong></td><td>The customer's email address.</td></tr><tr><td><strong>Logged-in customer</strong></td><td>Whether the visitor is signed in. No operator or value needed.</td></tr><tr><td><strong>Guest (non-logged in customer)</strong></td><td>Whether the visitor is browsing without signing in. No operator or value needed.</td></tr></tbody></table>

For **Customer tags**, **Customer name**, and **Customer email** the operators are: is equal to, is not equal to, starts with, ends with, contains, does not contain.

**Logged-in customer** and **Guest** are switches rather than comparisons — the app disables the operator and value fields when you pick either, because the field alone is the whole condition.
{% endstep %}

{% step %}
### Add more conditions if you need them

**Add another condition** appends a row; each row has a delete action.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: set-customers-automatic | App admin → builder → tab Customers → Automatic Rules đang bật | Điều kiện "Customer tags is equal to wholesale" + selector all/any conditions | Khoanh dòng điều kiện -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A customer rule matching customers whose tags equal wholesale"><figcaption><p>Customer tags are the most practical field — you control them entirely.</p></figcaption></figure>

### Worked examples

<table><thead><tr><th width="300">You want</th><th>Set up</th></tr></thead><tbody><tr><td>Wholesale-only bulk options</td><td>Customer tags — is equal to — <code>wholesale</code></td></tr><tr><td>Options only for signed-in shoppers</td><td>Logged-in customer</td></tr><tr><td>A "create an account for engraving" prompt for guests</td><td>Guest (non-logged in customer)</td></tr><tr><td>Free personalisation for VIPs</td><td>Customer tags — is equal to — <code>vip</code>, on a duplicate of your normal set with the add-on prices removed</td></tr><tr><td>One corporate client's branded options</td><td>Customer email — contains — <code>@theircompany.com</code></td></tr><tr><td>Trade customers except those on hold</td><td><strong>all conditions</strong>; Customer tags — is equal to — <code>trade</code>; Customer tags — is not equal to — <code>on-hold</code></td></tr></tbody></table>

## A pattern worth knowing: two versions of the same set

Customer rules are what make "different options for different shoppers" possible, and the cleanest way to do it is two option sets rather than one clever one:

1. Build your normal option set. Set **Customers** to **Automatic Rules** with `Customer tags — is not equal to — wholesale`.
2. Duplicate it. In the copy, change the prices or add the extra options, and set **Customers** to `Customer tags — is equal to — wholesale`.

Both target the same products, but only one ever renders for a given shopper. See [Duplicate and delete](duplicate-and-delete.md).

## Notes
* Customer rules narrow an option set; they never widen it. A product outside the product rule stays outside, whoever is looking.
* Rules are evaluated on the storefront using the signed-in customer. A guest matches only **Everyone** or a **Guest** condition — a tag condition cannot match somebody the store does not know.
* Customer tags are managed in Shopify admin on the customer's record, not in this app.
* The live preview in the builder does not apply customer rules. Test by signing in to your storefront as a test customer.
* Manual customer selection needs the customer data permission described above.
