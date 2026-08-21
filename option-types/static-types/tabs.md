---
description: Several panels of content behind tabs — care, delivery, and returns in one place without lengthening the page.
icon: folder-open
---

# Tabs

Several blocks of content, one visible at a time. The shopper selects a tab to switch panels.

Use it when you have three or four things to say and no room to say them all at once: care instructions, delivery information, returns, materials.

## What customers see

A row or column of tab titles with one panel open. Selecting another title switches panels.

<!-- SCREENSHOT: type-tabs-storefront | Storefront → trang sản phẩm | Tabs ngang với 3 tab, tab đầu đang mở với nội dung | Khoanh hàng tab và panel -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A horizontal set of tabs on a storefront product page with the first panel open"><figcaption><p>Three panels in the height of one.</p></figcaption></figure>

## Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Tabs</strong></td><td>The tabs themselves. Each has a title and its own rich-text content.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#direction-style">Direction style</a></td><td><strong>Horizontal</strong> — titles in a row above the content. <strong>Vertical</strong> — titles in a column beside it. Starts on <strong>Horizontal</strong>.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide the whole tab set.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and width.</td></tr></tbody></table>

### Building the tabs

Tabs are managed in a values table, like a selection type's option values — but each entry is a panel rather than a choice.

<table><thead><tr><th width="230">Action</th><th>How</th></tr></thead><tbody><tr><td>Add a tab</td><td><strong>Add another tab</strong> below the table.</td></tr><tr><td>Set a tab's title</td><td>The value field on its row.</td></tr><tr><td>Write a tab's content</td><td>Open the content editor on that row. Rich text, like a <a href="paragraph.md">Paragraph</a>.</td></tr><tr><td>Reorder tabs</td><td>Drag the rows. The first tab is the one open by default.</td></tr><tr><td>Delete a tab</td><td>The remove action on its row.</td></tr><tr><td>Start over</td><td><strong>Delete all tabs</strong>, which asks you to confirm.</td></tr></tbody></table>

Tab titles follow the same character rules as option values — no `,` `:` `"` `'` or `|`. See [Working with option values](../../concepts/option-values.md).

### Horizontal or vertical

<table><thead><tr><th width="200">Direction</th><th>Suits</th><th>Watch out for</th></tr></thead><tbody><tr><td><strong>Horizontal</strong></td><td>Two to four tabs with short titles</td><td>Long titles wrap and the row gets messy on mobile</td></tr><tr><td><strong>Vertical</strong></td><td>Longer titles, or five or more tabs</td><td>Takes horizontal space, so it needs a wide column</td></tr></tbody></table>

Keep titles to one or two words. `Care`, `Delivery`, `Returns` reads far better than `How to care for your item`.

## Order matters

The first tab is open when the page loads, so put your most-read content there. A shopper who sees "Delivery" first will not necessarily notice there is a "Care" tab.

## Tabs, modal, or paragraph?

<table><thead><tr><th width="200">Use</th><th>When you have</th></tr></thead><tbody><tr><td><a href="paragraph.md">Paragraph</a></td><td>One short piece of text everybody should read</td></tr><tr><td><a href="pop-up-modal.md">Pop-up modal</a></td><td>One longer piece most shoppers will skip</td></tr><tr><td><strong>Tabs</strong></td><td>Several pieces, at least one of which most shoppers will read</td></tr></tbody></table>

## Examples

**Care, delivery, returns**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Tabs</td><td><code>Care</code>, <code>Delivery</code>, <code>Returns</code></td></tr><tr><td>Direction style</td><td><strong>Horizontal</strong></td></tr><tr><td>First tab</td><td><code>Care</code> — the one customers ask about most</td></tr></tbody></table>

**Materials and specification**

Two tabs, `Materials` and `Specification`, each with a short formatted list. **Vertical** if the titles are longer.

**Personalisation guidance**

Tabs `How it works`, `Lead times`, `What we cannot engrave`, shown by conditional logic only when the shopper has chosen to personalise.

## Limits and notes

* Available on the Advanced plan.
* Works in Shopify POS.
* Collects nothing, so it never reaches the cart or order.
* Titles and content are translatable per storefront language. See [Translate option content](../../translations/translate-option-content.md).
* Tab colours are store-wide: **Tab title**, **Tab title active**, **Tab title hover**, **Tab content**, and **Tab border** in **Settings > Design**. See [Colors](../../storefront/colors.md).
* No practical limit on the number of tabs, but past about five the row becomes unusable — switch to **Vertical** or split the content.

## Troubleshooting

<details>
<summary>Tab titles wrap onto two lines</summary>

Shorten them, or switch **Direction style** to **Vertical**.
</details>

<details>
<summary>The wrong tab is open by default</summary>

The first tab in the table opens first. Drag the one you want to the top.
</details>

<details>
<summary>"Value can't contain any of the following characters , : " ' |"</summary>

A tab title has a blocked character. Titles follow the option value rules.
</details>

<details>
<summary>Tabs do not match my theme</summary>

Their five colours are in **Settings > Design**. See [Colors](../../storefront/colors.md).
</details>

<details>
<summary>Tabs is greyed out</summary>

It is on the Advanced plan. See [Compare plans](../../plans/compare-plans.md).
</details>

## Next steps

* [Pop-up modal](pop-up-modal.md) — for one block of content.
* [Size chart](size-chart.md) — often one of the things you would put in a tab.
* [Colors](../../storefront/colors.md) — the tab colour settings.
