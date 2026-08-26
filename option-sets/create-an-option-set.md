---
description: From an empty builder to a live option set on your storefront, in a few steps.
icon: pen-ruler
---

# Create an option set

The whole creation flow, once. Later pages go deeper on each part.

**Before you start:** the app is installed and a plan is chosen ([Install the app](../getting-started/install-the-app.md)). If you are not sure what to ask customers yet, browse [Option types](../option-types/) or start from a [template](../templates/).

## Steps

{% stepper %}
{% step %}
### Create from scratch

**Option Sets** > **Create option set** > **Create from scratch**. (The other choice, **Use a template**, copies a complete option set you can then edit — see [Templates](../templates/).)

The builder opens on **Setup flow**, which has exactly two steps, because they are the two things an option set cannot go without:

1. **Build option** — the fields you want to show
2. **Assign products** — which products use them

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Setup flow tab of a new option set showing the Build option and Assign products steps"><figcaption><p>Setup flow reduces the required work to two steps.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add your options

Select the add button inside the section and pick a type. The picker has two tabs: **Option Types** for the 32 individual types, and **Option Templates** to insert a ready-made group.

For each option, set at least these three:

<table><thead><tr><th width="200">Field</th><th>Notes</th></tr></thead><tbody><tr><td><strong>Label</strong></td><td>What shoppers read. No restrictions</td></tr><tr><td><strong>Name</strong></td><td>What appears on the cart and order. Must be unique in this set, and cannot contain <code>.</code> <code>:</code> <code>"</code> <code>'</code> <code>\</code> <code>|</code> — see <a href="../option-types/shared-settings/labels-and-visibility.md">Label and Name</a></td></tr><tr><td><strong>Required field</strong></td><td>Whether the customer must fill it in before adding to cart</td></tr></tbody></table>

Selection-style options also need their values — see [Working with option values](option-values.md). For reordering, duplicating, and grouping, see [Build your options](build-options.md).
{% endstep %}

{% step %}
### Assign it to products

Switch to **Assign products** and turn on one of three methods:

<table><thead><tr><th width="220">Method</th><th>Best for</th></tr></thead><tbody><tr><td><strong>Manual Selection</strong></td><td>A fixed, small list you pick by hand</td></tr><tr><td><strong>Automatic Rules</strong></td><td>Anything matching a tag, type, vendor, price, or collection. Keeps working as your catalogue grows</td></tr><tr><td><strong>Apply to All Products</strong></td><td>Store-wide options such as a delivery note</td></tr></tbody></table>

Full detail: [Assign to products](assign-to-products.md).
{% endstep %}

{% step %}
### Optionally narrow by customer or country

Two more tabs on the left rail, both optional and both plan-gated: **Customers** limits the set to certain shoppers, **Countries** includes or excludes countries. Skip them to show the set to everyone, everywhere.

See [Assign to customers](assign-to-customers.md) and [Assign to countries](assign-to-countries.md).
{% endstep %}

{% step %}
### Check the preview, then Save

The live preview on the right renders the real widget, runs your conditional logic, and previews add-on prices. See [Live preview and inspector](live-preview-and-inspector.md).

Then select **Save** in the top-right.

{% hint style="warning" %}
Save is blocked unless there is **at least one option** and **a complete product rule**. The builder switches you to whichever step is missing something and says why.
{% endhint %}
{% endstep %}

{% step %}
### Activate and publish

A new option set is **Draft**, which renders nowhere. Set the status to **Active** — the control is beside the option set's name — then check **Sales channels**:

<table><thead><tr><th width="200">Channel</th><th>What it covers</th></tr></thead><tbody><tr><td><strong>Online Store</strong></td><td>Your storefront: product pages, quickview popups, and featured-product sections</td></tr><tr><td><strong>Point of Sale</strong></td><td>Orders you take in person through the Shopify POS app</td></tr></tbody></table>

Both are on by default. Turn one off to say "these options are for in-store orders only", or the reverse.

<figure><img src="../.gitbook/assets/placeholder.png" alt="The status control and Sales channels popover in the builder header"><figcaption><p>Status and Sales channels sit next to the option set's name.</p></figcaption></figure>

{% hint style="warning" %}
Ticking **Point of Sale** is not enough on its own — some option types and one add-on mode do not work there. See [POS limitations](../pos/limitations.md).
{% endhint %}
{% endstep %}

{% step %}
### View it on your storefront

**View in Store** in the builder header opens a product this set applies to. If the set is active and the [app embed](../getting-started/enable-the-app-embed.md) is on, your options are there.
{% endstep %}
{% endstepper %}

<details>

<summary>What Save stores, and what lives elsewhere</summary>

<table><thead><tr><th width="240">Saved with the option set</th><th>Store-wide, saved elsewhere</th></tr></thead><tbody><tr><td>Options and all their settings</td><td>Colours, borders, typography — <strong>Settings > Design</strong></td></tr><tr><td>Option values, prices, and images</td><td>Widget position — <strong>Settings > General</strong></td></tr><tr><td>Conditional logic rules</td><td>Widget text and validation messages — <strong>Settings > Translations</strong></td></tr><tr><td>Product, customer, and country rules</td><td>Automations — <strong>Automations</strong></td></tr><tr><td>Status and sales channels</td><td></td></tr><tr><td>The Personalizer background for this set</td><td></td></tr></tbody></table>

This is why copying an option set to another store does not copy its look. See [Import and export](import-and-export.md).

</details>
