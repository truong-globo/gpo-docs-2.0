---
description: Tag orders by what the customer chose, so you can filter, route, and report on them.
icon: tag
---

# Update order tags

Adds a tag to orders containing app options. Tags are how you filter orders in Shopify admin, and how most fulfilment and reporting tools decide what to do with an order — which makes this the automation that connects options to the rest of your operation.

Unlike the other two, you can have **as many order tag workflows as you like**.

## Two modes

<table><thead><tr><th width="290">Mode</th><th>Tags the order with</th></tr></thead><tbody><tr><td><strong>Fixed tag for every orders containing globo options</strong></td><td>A tag you type, on every order that has options</td></tr><tr><td><strong>Dynamic tag based on selected option element</strong></td><td>The value the customer chose in a specific option</td></tr></tbody></table>

<!-- SCREENSHOT: auto-order-tags | App admin → Automations → workflow Order tags update | Dropdown Type với 2 mode, và field Tag name hoặc Option element | Khoanh dropdown Type -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The order tags workflow with its type selector"><figcaption><p>A fixed tag on every order with options, or a tag from what the customer chose.</p></figcaption></figure>

## Fixed tag

Choose the mode, then enter a **Tag name**. Every order containing app options gets it.

Use it to separate personalised orders from ordinary ones:

<table><thead><tr><th width="230">Tag</th><th>Lets you</th></tr></thead><tbody><tr><td><code>personalised</code></td><td>Filter your order list to just the ones needing production work</td></tr><tr><td><code>custom-order</code></td><td>Route them to a different fulfilment flow</td></tr><tr><td><code>needs-proof</code></td><td>Flag them for a proofing step before production</td></tr></tbody></table>

That single tag is often enough to reorganise a whole workflow, because everything downstream can filter on it.

## Dynamic tag

Choose the mode, then select an **Option element** — a specific option, in a specific option set. The tag becomes the value the customer chose in it.

{% stepper %}
{% step %}
### Set Type to dynamic

The option element selector appears.
{% endstep %}

{% step %}
### Select the option element

A picker lists your option sets and their options. Choose the one whose value should become the tag.
{% endstep %}

{% step %}
### Save and set the workflow Active
{% endstep %}

{% step %}
### Test it

Against a real recent order that used that option.
{% endstep %}
{% endstepper %}

**Worked examples**

<table><thead><tr><th width="290">Option</th><th>Resulting tags</th><th>Useful for</th></tr></thead><tbody><tr><td><code>Delivery speed</code></td><td><code>Express</code>, <code>Standard</code></td><td>Filtering the urgent orders each morning</td></tr><tr><td><code>Engraving font</code></td><td>The font name</td><td>Batching orders by machine setup</td></tr><tr><td><code>Workshop</code></td><td>The workshop name</td><td>Routing to the right team</td></tr><tr><td><code>Gift wrap</code></td><td>The gift-wrap value</td><td>Picking wrapping materials in one pass</td></tr></tbody></table>

Batching is where this pays off. Twenty orders all tagged with the same font can be run through one machine setup instead of twenty.

## Using several workflows together

Because order tags are unlimited, the useful pattern is one workflow per thing you want to filter on:

<table><thead><tr><th width="230">Workflow</th><th width="180">Mode</th><th>Tag</th></tr></thead><tbody><tr><td>Flag personalised orders</td><td>Fixed</td><td><code>personalised</code></td></tr><tr><td>Tag by delivery speed</td><td>Dynamic</td><td>From the delivery option</td></tr><tr><td>Tag by font</td><td>Dynamic</td><td>From the font option</td></tr></tbody></table>

An order then arrives already sorted: `personalised`, `Express`, `Roboto`.

## Choosing option values that make good tags

A dynamic tag is the option value verbatim, so the values you wrote become your tags.

<table><thead><tr><th width="290">Good as a tag</th><th>Poor as a tag</th></tr></thead><tbody><tr><td><code>Express</code></td><td><code>Yes please, as fast as you can!</code></td></tr><tr><td><code>Oak</code></td><td><code>Natural oak with a matt finish</code></td></tr><tr><td><code>Gift wrap</code></td><td><code>Yes, wrap it as a gift</code></td></tr></tbody></table>

If your values are long and conversational, that is fine for shoppers but awkward as tags. Either shorten them, or accept long tags — Shopify tolerates them, they are just harder to read in a filter list.

{% hint style="warning" %}
A dynamic workflow points at a **specific option in a specific option set**. Delete that option set, or change the option, and the workflow no longer has anything to read. Revisit your workflows after restructuring option sets. See [Duplicate and delete](../option-sets/duplicate-and-delete.md).
{% endhint %}

## Testing

**Test** opens your fifty most recent orders. Choose one that used the relevant option, and the workflow runs against it so you can see the tag it produces.

## Notes

* Unlimited order tag workflows.
* Tags are added; nothing is removed. Tags Shopify or other apps set are untouched.
* Runs shortly after the order is created, so the tag appears a moment later.
* A workflow set to **Draft** does nothing.
* Requires order data access, approved once when you first open **Automations**.
* A customer who selects several values in a multi-select option produces tags accordingly — test it if you rely on it.

## Troubleshooting

<details>
<summary>No tag is added</summary>

Check the workflow is **Active**, the order had app options, and — for a dynamic tag — that the order actually used the option you selected. Then use **Test** against a known order.
</details>

<details>
<summary>The dynamic tag is empty</summary>

The customer left that option blank, or it was hidden by a conditional rule. A hidden option collects nothing.
</details>

<details>
<summary>The workflow stopped working</summary>

The option set or option it points at was changed or deleted. Edit the workflow and reselect the option.
</details>

<details>
<summary>My tags are long and unwieldy</summary>

They are your option values. Shorten the values, or use a fixed tag instead and read the detail from the order note.
</details>

<details>
<summary>I want a tag based on two options</summary>

Create two workflows, one per option. Each adds its own tag.
</details>

<details>
<summary>I want to tag by something other than an option</summary>

Not supported here — the source is always an app option. Shopify Flow or a similar tool can tag on other conditions.
</details>

## Next steps

* [Update order notes](update-order-notes.md)
* [Email notification](email-notification.md)
* [Label vs Name](../concepts/label-vs-name.md) — the Name identifies the option a workflow points at.
