---
description: Save your own setups as reusable templates, and manage, duplicate, import, and export them.
icon: bookmark
---

# Custom templates

A custom template is a template you own. Once you have built a setup that works, saving it means the next product family starts from your version rather than from an empty option set.

## Two ways to create one

<table><thead><tr><th width="290">Route</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Save as Template</strong> from an existing option set</td><td>You have already built something that works. This is the usual route</td></tr><tr><td><strong>Create template</strong> from scratch</td><td>You want a reusable block that was never a live option set — a standard gift-options group, say</td></tr></tbody></table>

### Save an option set as a template

{% stepper %}
{% step %}
### Select the option sets

On the **Option Sets** list, tick one or more rows. You can also do this from inside the builder, from its more-actions menu.
{% endstep %}

{% step %}
### Choose Save as Template

From the bulk action menu on the list, or the builder's more-actions menu.
{% endstep %}

{% step %}
### Find it under Custom Templates

**Templates** > **Custom Templates**.
{% endstep %}
{% endstepper %}

### Create one from scratch

**Templates** > **Create template**. The builder opens in template mode.

Template mode differs from an option set in one important way: there is no **Setup flow** and no product, customer, or country rules. A template has no targeting, because it never goes live — it only has options. The left rail shows **Elements** instead.

<!-- SCREENSHOT: tpl-custom-list | App admin → Templates → tab Custom Templates | Bảng danh sách template với cột ID, Name, Option elements, Date created, Actions | Không khoanh -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Custom Templates tab listing saved templates with their option elements"><figcaption><p>Your own templates, listed with the option types each contains.</p></figcaption></figure>

## Using a custom template

Two ways, and they do different things.

<table><thead><tr><th width="290">Route</th><th>Result</th></tr></thead><tbody><tr><td><strong>Use template</strong> from the Templates page</td><td>Creates a whole new option set from it</td></tr><tr><td><strong>Add template</strong> in the builder's add picker</td><td>Inserts its options into the option set you are already building</td></tr></tbody></table>

The second is the more useful of the two once you have a library. A standard "gift options" template inserted into five different option sets keeps five product families consistent, and you only wrote it once.

When inserting, names that clash with existing options are renumbered automatically, and conditional logic inside the template is repointed so it keeps working. Check the names afterwards and give them readable values.

## Managing them

The **Custom Templates** tab is a list like the option sets list.

<table><thead><tr><th width="230">Action</th><th>What it does</th></tr></thead><tbody><tr><td>Search and sort</td><td>By name, or by date created</td></tr><tr><td>Open</td><td>Edit the template's options</td></tr><tr><td><strong>Duplicate templates</strong></td><td>Copy one or more</td></tr><tr><td><strong>Delete templates</strong></td><td>Permanently remove them. Confirmed first</td></tr><tr><td>Import and export</td><td>Move templates between stores</td></tr></tbody></table>

Each row shows which option types the template contains, which is quicker than opening it to remember what is inside.

{% hint style="info" %}
Deleting a template does **not** affect option sets created from it. Once used, the option set is independent — it does not stay linked to the template.
{% endhint %}

## A library worth building

Three templates cover most of what a personalisation shop repeats:

<table><thead><tr><th width="290">Template</th><th>Contains</th></tr></thead><tbody><tr><td><code>Gift options</code></td><td>A gift-wrap switch, a gift message textarea with a conditional rule, and a recipient email</td></tr><tr><td><code>Engraving block</code></td><td>An engraving text field with your limits and input rules, a font picker with your fonts, and a position choice</td></tr><tr><td><code>Delivery preferences</code></td><td>A date picker with your lead time and blocked days, plus a delivery notes field</td></tr></tbody></table>

Insert whichever you need into each new option set. Your wording, limits, and fonts stay consistent across the store without anybody having to remember them.

## Notes

* Custom templates are plan-gated. See [Compare plans](../plans/compare-plans.md).
* A template has no product, customer, or country rules — only options.
* Add-on products referenced by a template's options behave as they do anywhere else: an existing-product link points at the same product, and a generated product is shared. See [Add-on pricing](../add-on-pricing/README.md).
* Templates import and export separately from option sets. See [Import and export](../option-sets/import-and-export.md) for the option set equivalent.

## Troubleshooting

<details>
<summary>Save as Template did nothing visible</summary>

Look under **Templates** > **Custom Templates** rather than in the option sets list.
</details>

<details>
<summary>The template has no Setup flow or product rules</summary>

Correct — templates have no targeting. Assign products on the option set you create from it.
</details>

<details>
<summary>Inserting a template renamed my options</summary>

Names must stay unique within an option set, so clashes are renumbered. Rename the copies to something readable.
</details>

<details>
<summary>I deleted a template and want to know what happened to my option sets</summary>

Nothing. Option sets created from a template are independent of it.
</details>

<details>
<summary>Create template is unavailable</summary>

Option templates are not in your plan. See [Compare plans](../plans/compare-plans.md).
</details>
