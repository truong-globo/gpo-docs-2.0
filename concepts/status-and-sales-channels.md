---
description: >-
  Active versus Draft, Online Store versus Point of Sale, and the four switches
  that decide whether anyone can see your option set.
icon: toggle-off
---

# Status and sales channels

An option set can be perfectly built and still be invisible. Two settings control that: its **Status**, and its **Sales channels**. Both live next to the option set's name.

## Status

<table><thead><tr><th width="150">Status</th><th>Meaning</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>Saved but switched off. It never renders on any channel. Use it while you are still building, or to retire a set without deleting it.</td></tr><tr><td><strong>Active</strong></td><td>Live. It renders wherever its rules and channels allow.</td></tr></tbody></table>

{% hint style="info" %}
A newly created option set is **Draft**. Remembering to switch it to **Active** is the second most common reason options do not appear — after the app embed.
{% endhint %}

### Where to change it

* **In the builder** — the status control sits next to the option set name in the header.
* **On the Option Sets list** — select one or more rows, then use the bulk action **Set as active** or **Set as draft**.

The list can also be filtered by **All**, **Active**, or **Draft**, which is the quickest way to spot a set you forgot to activate.

<!-- SCREENSHOT: concept-status-header | App admin → builder | Khối Status cạnh tên option set, đang bật Active | Khoanh khối Status -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The status control in the builder header set to Active"><figcaption><p>Status sits next to the option set's name in the builder header.</p></figcaption></figure>

## Sales channels

Separately from status, each option set is published to one or both of Shopify's channels.

<table><thead><tr><th width="200">Channel</th><th>What it covers</th></tr></thead><tbody><tr><td><strong>Online Store</strong></td><td>Your storefront: product pages, quickview popups, and featured-product sections on other pages.</td></tr><tr><td><strong>Point of Sale</strong></td><td>Orders you take in person through the Shopify POS app.</td></tr></tbody></table>

Both are on by default. Turning one off is how you say "these options are for in-store orders only" — or the reverse.

### Where to change it

* **In the builder** — the **Sales channels** control next to the status, with a switch per channel.
* **On the Option Sets list** — each row has its own sales channels control, so you can adjust one set without opening it.

<!-- SCREENSHOT: concept-sales-channels | App admin → builder → mở popover Sales channels | 2 dòng Online Store và Point of Sale với switch | Khoanh popover -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Sales channels popover with switches for Online Store and Point of Sale"><figcaption><p>Publish an option set to your storefront, to POS, or to both.</p></figcaption></figure>

{% hint style="warning" %}
Publishing to **Point of Sale** is not enough on its own. Some option types do not work in POS, and one add-on mode is not supported there. Read [POS limitations](../pos/limitations.md) before you rely on it.
{% endhint %}

## The four switches, in order

When an option set is not appearing, check these in this order. It is almost always one of them.

{% stepper %}
{% step %}
### Is the app embed enabled on the live theme?

This is store-wide, not per option set. Without it, nothing from the app renders anywhere. See [Enable the app embed](../getting-started/enable-the-app-embed.md).
{% endstep %}

{% step %}
### Is the option set Active?

A **Draft** set never renders. See above.
{% endstep %}

{% step %}
### Is the right sales channel ticked?

**Online Store** for your storefront, **Point of Sale** for the POS app.
{% endstep %}

{% step %}
### Does a rule match?

The product rule must match the product you are looking at, and if you set customer or country rules, those must match the visitor too. See [Assign to products](../option-sets/assign-to-products.md), [Assign to customers](../option-sets/assign-to-customers.md), and [Assign to countries](../option-sets/assign-to-countries.md).
{% endstep %}
{% endstepper %}

## The status line in the builder

Above the **Setup flow** panel the builder prints a one-line summary of the option set, so you can see its state without hunting:

* what it is assigned to — "Not assigned yet", "Applies to all products", "Applies to 12 selected products", or a summary of the automatic conditions
* when it was last updated, or that it has unsaved changes
* its status, or a warning if a rule is incomplete

If that line says the set is not assigned, or flags a problem, fix it before wondering why the storefront is empty.

## Limits and notes

* Status and sales channels are per option set. There is no store-wide "switch everything off" — for that, turn off the app embed.
* Setting a set to **Draft** does not delete anything. Options, rules, and prices are kept exactly as they were.
* Add-on products the app generated stay in your Shopify catalogue when an option set goes to draft. They stop being purchasable through the widget because the option set no longer renders.
* Point of Sale requires a plan that includes it. If the switch is unavailable, see [Compare plans](../plans/compare-plans.md).

## Troubleshooting

<details>
<summary>The option set is Active but still not on my storefront</summary>

Work through the four switches above in order. If all four are correct, continue with [Options are not showing up](../help/troubleshooting-not-showing.md).
</details>

<details>
<summary>Options appear on my storefront but not in POS</summary>

Tick **Point of Sale** under **Sales channels**, then check that the option types you used are supported in POS — [POS limitations](../pos/limitations.md) lists the exceptions.
</details>

<details>
<summary>I set it to Active but it flipped back to Draft</summary>

It did not flip back — the change was not saved. Change the status, then select **Save**. Alternatively use the bulk action **Set as active** on the Option Sets list, which saves immediately.
</details>

<details>
<summary>I want to hide options temporarily during a sale</summary>

Set the option set to **Draft**. Everything is preserved, and switching it back to **Active** restores it exactly.
</details>

## Next steps

* [Plans and locked features](plans-and-feature-gating.md)
* [Manage option sets](../option-sets/manage-option-sets.md) — the list page and its bulk actions.
* [Options are not showing up](../help/troubleshooting-not-showing.md)
