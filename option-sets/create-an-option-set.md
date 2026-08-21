---
description: >-
  From an empty builder to a saved, live option set — including the two rules
  that decide whether Save works.
icon: pen-ruler
---

# Create an option set

This page covers the whole creation flow once. Later pages go deeper on each part.

## Before you start

* The app is installed and a plan is chosen — see [Install the app](../getting-started/install-the-app.md).
* You know roughly what you want to ask customers. If not, browse [Option types](../option-types/README.md) or start from a [template](../templates/README.md) instead.

## Two ways to start

<table><thead><tr><th width="240">Choice</th><th>What you get</th></tr></thead><tbody><tr><td><strong>Create from scratch</strong></td><td>An empty option set with one empty section. Full control, nothing pre-filled.</td></tr><tr><td><strong>Use a template</strong></td><td>A complete option set copied from our library or from your own saved templates. Everything is editable afterwards. See <a href="../templates/README.md">Templates</a>.</td></tr></tbody></table>

Both are behind the **Create option set** button on the **Option Sets** page.

## Steps

{% stepper %}
{% step %}
### Open the builder

Go to **Option Sets** and select **Create option set** > **Create from scratch**.

The builder opens on the **Setup flow** tab. Setup flow has exactly two steps, and they are the two things an option set cannot go without:

1. **Build option** — add fields like text, swatches, dropdowns, uploads, and checkboxes.
2. **Assign products** — choose which products or collections use this option set.

Above them is a status line summarising the set: what it is assigned to, when it was last updated, and whether anything needs attention.

<!-- SCREENSHOT: set-create-setup-flow | App admin → builder mới tạo | Tab Setup flow với 2 step Build option / Assign products + dòng status phía trên | Khoanh 2 thẻ step -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Setup flow tab of a new option set showing the Build option and Assign products steps"><figcaption><p>Setup flow reduces the required work to two steps.</p></figcaption></figure>
{% endstep %}

{% step %}
### Name it

Replace the default name in the header with something descriptive.

Good names describe the products, not the options: `Engravable jewellery` reads better in a list of twenty sets than `Text field + checkbox`.

The name is internal. It is not shown to shoppers, it is not used on the order, and it has no character restrictions.
{% endstep %}

{% step %}
### Rename or configure the starting section

A new option set contains one empty **Section**. Sections group options under a heading and can be made collapsible.

Select it and set its **Label** — that label is shown to shoppers as the group heading. Its **Style** setting offers:

* **Default** — everything inside is always visible
* **Expand** — a collapsible group that starts open
* **Collapse** — a collapsible group that starts closed

If you do not want a visible group at all, you can still add options directly and leave the section label short. See [Section](../option-types/static-types/section.md).
{% endstep %}

{% step %}
### Add your options

Inside the section, select the add button and pick a type. The picker has two tabs:

* **Option Types** — the 32 individual types, grouped into **Input**, **Selection**, and **Static**.
* **Option Templates** — insert a ready-made group of options instead of building one.

Add as many as you need. Full detail on adding, reordering, duplicating, and grouping: [Build your options](build-options.md).

For each option, at minimum set:

<table><thead><tr><th width="200">Field</th><th>Notes</th></tr></thead><tbody><tr><td><strong>Label</strong></td><td>What shoppers read. No restrictions.</td></tr><tr><td><strong>Name</strong></td><td>What appears on the cart and order. Must be unique in this option set and cannot contain <code>.</code> <code>:</code> <code>"</code> <code>'</code> <code>\</code> <code>|</code>. See <a href="../concepts/label-vs-name.md">Label vs Name</a>.</td></tr><tr><td><strong>Required field</strong></td><td>Whether the customer must fill it in before adding to cart.</td></tr></tbody></table>

Selection-style options also need their **Option values** — see [Working with option values](../concepts/option-values.md).
{% endstep %}

{% step %}
### Assign it to products

Switch to **Assign products** and turn on one of the three methods:

<table><thead><tr><th width="220">Method</th><th>Best for</th></tr></thead><tbody><tr><td><strong>Manual Selection</strong></td><td>A fixed, small list of products you pick by hand.</td></tr><tr><td><strong>Automatic Rules</strong></td><td>Anything that matches a condition — tag, type, vendor, price, or collection. Keeps working as your catalogue grows.</td></tr><tr><td><strong>Apply to All Products</strong></td><td>Store-wide options such as a delivery note.</td></tr></tbody></table>

Full detail: [Assign to products](assign-to-products.md).
{% endstep %}

{% step %}
### Optionally narrow by customer or country

Two more tabs on the left rail refine who sees the set:

* **Customers** — show it only to specific customers, or by tag, name, email, logged-in status, or guest status. Default is everyone. See [Assign to customers](assign-to-customers.md).
* **Countries** — include or exclude specific countries. Off by default. See [Assign to countries](assign-to-countries.md).

Both are optional, and both are plan-gated. Skip them if you want the set to apply to all shoppers everywhere.
{% endstep %}

{% step %}
### Test it in the preview

Before saving, use the live preview on the right. It renders the real widget, runs your conditional logic, and previews add-on prices.

Switch between desktop and mobile width, and use the inspector to jump from a rendered element to its settings. See [Live preview and inspector](live-preview-and-inspector.md).
{% endstep %}

{% step %}
### Save

Select **Save** in the top-right.

{% hint style="warning" %}
Save is blocked unless **both** of these are true:

* at least one option exists inside a section
* a product rule is turned on, and complete

If something is missing, the builder switches you to the step that needs attention and shows the reason — for example that no options have been added, or that a manual rule has no products selected.
{% endhint %}
{% endstep %}

{% step %}
### Activate and publish

A new option set is created as **Draft** and does not render on any channel.

Set the status to **Active**, then check **Sales channels**: **Online Store** for your storefront, **Point of Sale** if you also sell in person.

See [Status and sales channels](../concepts/status-and-sales-channels.md).
{% endstep %}

{% step %}
### View it on your storefront

Use **View in Store** in the builder header to open a product that this option set applies to.

If the option set is active and the [app embed](../getting-started/enable-the-app-embed.md) is enabled, your options render there.
{% endstep %}
{% endstepper %}

## What Save actually stores

<table><thead><tr><th width="240">Saved with the option set</th><th>Not saved with the option set</th></tr></thead><tbody><tr><td>Options and all their settings</td><td>Colours, borders, and typography — those are store-wide in <strong>Settings &gt; Design</strong></td></tr><tr><td>Option values, prices, and images</td><td>Widget position — store-wide in <strong>Settings &gt; General</strong></td></tr><tr><td>Conditional logic rules</td><td>Widget text and validation messages — store-wide in <strong>Settings &gt; Translations</strong></td></tr><tr><td>Product, customer, and country rules</td><td>Automations — those live in <strong>Automations</strong></td></tr><tr><td>Status and sales channels</td><td></td></tr><tr><td>The Personalizer background for this set</td><td></td></tr></tbody></table>

## Unsaved changes

The builder tracks unsaved changes and warns you before you navigate away. If you get the discard prompt, **Discard changes** throws away everything since your last save, and **Continue editing** takes you back.

## Limits and notes

* There is no limit on how many option sets you can have on current plans, nor on how many options each contains.
* Creating an option set does not create products. Products are only created if you use the **Automatically generate product** add-on mode — see [Automatically generate a product](../add-on-pricing/auto-generate-a-product.md).
* Several option sets may apply to the same product. They all render, in the order the app loads them. If you see duplicates, look for a second overlapping set.

## Troubleshooting

<details>
<summary>Save does nothing, or the builder jumps to another step</summary>

The set is incomplete. It needs at least one option and a product rule. The step it jumps to is the one missing something.
</details>

<details>
<summary>"Name must be unique" on an option</summary>

Two options in this set share a **Name**, ignoring capitalisation and spaces. Duplicated options are the usual cause — rename the copy.
</details>

<details>
<summary>I saved it, but nothing shows on my storefront</summary>

Work through the four switches: app embed enabled, status **Active**, **Online Store** ticked, and a matching product rule. See [Options are not showing up](../help/troubleshooting-not-showing.md).
</details>

<details>
<summary>The preview looks nothing like my theme</summary>

The preview uses the app's own styling. To make the widget inherit your theme's look on the storefront, turn on **Match theme style** in **Settings > Design**. See [Match your theme style](../storefront/match-your-theme-style.md).
</details>

## Next steps

* [Build your options](build-options.md) — the builder in depth.
* [Assign to products](assign-to-products.md) — targeting in depth.
* [Walkthrough: engraving and gift wrap](../getting-started/first-option-set-walkthrough.md) — a full worked example.
