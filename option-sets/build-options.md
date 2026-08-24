---
description: >-
  Adding, changing, duplicating, hiding, reordering, and grouping the options
  inside an option set.
icon: screwdriver-wrench
---

# Build your options

Everything in this page happens in **Setup flow** > **Build option**. It is the panel where your form takes shape.

## Before you start

* An option set is open in the builder — see [Create an option set](create-an-option-set.md).
* If you are unsure which option type to use, see [Choose the right option type](../option-types/choose-the-right-type.md).

## Reading the option list

Each option in the panel shows a short summary so you can scan the form without opening anything.

<table><thead><tr><th width="220">What you see</th><th>What it tells you</th></tr></thead><tbody><tr><td>Icon</td><td>The option's type.</td></tr><tr><td>Title</td><td>The option's <strong>Label</strong>, or the section's label for a section.</td></tr><tr><td>Description line</td><td>A plain-language summary — "Customers enter Engraving text", "Customers choose Gift wrap", "Separates content on the product page".</td></tr><tr><td><strong>Required</strong> badge</td><td>The option has <strong>Required field</strong> turned on.</td></tr><tr><td>Values badge</td><td>How many option values a selection option has.</td></tr><tr><td>Price badge</td><td>The add-on attached. A single price shows as <code>+ price</code>; a range across values shows as <code>From … to …</code>.</td></tr></tbody></table>

<!-- SCREENSHOT: set-build-option-list | App admin → builder → Build option | Danh sách option với icon, title, description, badge Required và badge giá | Khoanh 1 dòng option kèm các badge (mũi tên nhỏ vì nhiều dòng) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The option list in the builder with type icons, descriptions, and required and price badges"><figcaption><p>Badges let you audit a whole form without opening each option.</p></figcaption></figure>

## Adding options

Select the add button inside a section. The picker has two tabs — **Option Types** for all 32 types, grouped into **Input**, **Selection**, and **Static**; and **Option Templates** for a saved group of options inserted in one go. It also offers **Add section** and **Add template** directly.

Two shortcuts worth knowing:

* **Insert between two options.** Hover between them in the list and an insert control appears — quicker than adding at the end and dragging.
* **Add template.** Inserts a ready-made group, so a monogram block you already built can be reused in another option set. Clashing names are renumbered automatically, and conditional logic inside the template is repointed so it keeps working. See [Custom templates](../templates/custom-templates.md).

## Editing an option

Select an option to open its settings. They are split across tabs:

<table><thead><tr><th width="230">Tab</th><th>Contains</th></tr></thead><tbody><tr><td><strong>Basic Settings</strong></td><td>The essentials: label, name, required, values, limits, help text, placeholder, default value, add-on settings, and conditional logic.</td></tr><tr><td><strong>Advanced Settings</strong></td><td>Presentation and edge cases: layout, column width, prefix and suffix, HTML class, out-of-stock handling, tooltip style, scroll and slider behaviour, advanced add-on modes.</td></tr><tr><td><strong>Personalizer Settings</strong></td><td>Only on option types that can appear in the live preview. Fonts, effects, position, clip area, and customer controls. See <a href="../personalizer/README.md">Product Personalizer</a>.</td></tr></tbody></table>

Which settings appear depends on the type. Every shared setting has its own reference page — see [Shared settings](../option-types/shared-settings/README.md).

Use the back control at the top of the settings panel to return to the option list.

{% hint style="info" %}
On the free plan, premium settings are folded into a collapsed group at the bottom of the panel with a count, rather than shown greyed-out inline. Expand it to see what a higher plan would add.
{% endhint %}

## Changing an option's type

The settings panel header shows the current type and lets you switch it.

Changing type keeps the option in place, and keeps settings the new type also has — label, name, required, help text. Settings that do not exist on the new type are dropped.

{% hint style="warning" %}
Switching between an input type and a selection type loses the parts that cannot carry over: option values and their prices when you move to an input type, or limits like **Max character** when you move to a selection type. Check the option afterwards, including its **Name**, and check any conditional logic rule that reads this option — the available operators change with the type.
{% endhint %}

<!-- SCREENSHOT: set-build-change-type | App admin → builder → panel setting của 1 option | Control đổi option type ở header panel đang mở | Khoanh control đổi type -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The option type control at the top of an option's settings panel"><figcaption><p>An option's type can be changed after the fact, from its settings header.</p></figcaption></figure>

## Duplicate, hide, remove

Each option has an actions menu with three entries.

<table><thead><tr><th width="180">Action</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Duplicate</strong></td><td>Copies the option with all its settings, values, prices, and rules, and places the copy directly below. The copy's <strong>Name</strong> is renumbered so it stays unique — rename it to something readable.</td></tr><tr><td><strong>Hide</strong> / <strong>Show</strong></td><td>Keeps the option in the set but stops it rendering on the storefront. Use it to park an option you might want back, or to test a form without one field.</td></tr><tr><td><strong>Remove</strong></td><td>Deletes the option from the set. You are asked to confirm.</td></tr></tbody></table>

{% hint style="danger" %}
Removing an option also removes its add-on configuration and its values. Any conditional logic rule on another option that referenced it stops matching — review your rules after deleting. See [Troubleshooting conditional logic](../conditional-logic/troubleshooting.md).
{% endhint %}

**Hide** versus **Draft**: hiding affects one option, setting the option set to draft affects the whole set. Hiding is the right tool for retiring a single field.

## Reordering

Drag an option by its handle to move it. The order in the panel is exactly the order shoppers see, top to bottom.

You can drag options within a section and between sections. Dragging a section moves it and everything inside it.

Some ordering advice:

* Put required options before optional ones, so a customer who abandons the form has filled the important parts.
* Put the option that a conditional rule depends on **above** the option it reveals. Technically it works either way, but a field appearing above where the customer is looking is confusing.
* Group related options into sections rather than relying on one long list.

## Sections

A **Section** is a container with a visible heading, optionally collapsible. Add one with **Add section** from the add picker, then drag options into it. You can have any number of sections, holding any number of options.

Two settings matter:

* **Label** — the heading shoppers read.
* **Style** — **Default** (always open), **Expand** (collapsible, starts open), or **Collapse** (collapsible, starts closed).

Sections also take a **Prefix icon** and an **HTML class** for custom CSS.

{% hint style="info" %}
Sections support conditional logic, and a rule on the section shows or hides everything inside it at once. That is far less work than putting the same rule on eight options.
{% endhint %}

Full reference: [Section](../option-types/static-types/section.md).

<details>
<summary>What the builder blocks while you work</summary>

The builder validates as you type and blocks **Save** until the problems are fixed.

<table><thead><tr><th width="300">Message</th><th>Cause</th></tr></thead><tbody><tr><td>Field is required</td><td><strong>Label</strong> or <strong>Name</strong> is empty.</td></tr><tr><td>Name must be unique</td><td>Another option in the set uses that <strong>Name</strong>, ignoring capitalisation and spaces.</td></tr><tr><td>Name cannot contain <code>.</code> <code>:</code> <code>"</code> <code>'</code> <code>\</code> <code>|</code></td><td>A blocked character in <strong>Name</strong>.</td></tr><tr><td>Value must be unique / Value can't be empty / Value can't contain <code>,</code> <code>:</code> <code>"</code> <code>'</code> <code>|</code></td><td>An option value breaks one of its three rules. See <a href="option-values.md">Working with option values</a>.</td></tr><tr><td>The value must be between min and max</td><td>A default value falls outside the limits you set.</td></tr><tr><td>The value must be less than max / greater than min</td><td><strong>Min</strong> and <strong>Max</strong> are the wrong way round.</td></tr><tr><td>HTML class only accepts letters, numbers, hyphens and underscore</td><td>A blocked character in <strong>HTML class</strong>.</td></tr><tr><td>Formula cannot contain subtraction</td><td>A <code>-</code> in a Dimension add-on formula. See <a href="../add-on-pricing/dimension-formula.md">Dimension add-on formula</a>.</td></tr><tr><td>You haven't added any options yet</td><td>The set has sections but no options inside them.</td></tr></tbody></table>

</details>

## Working in another language

If your storefront has more than one language, the language switcher in the builder header lets you enter translated labels, values, and help text per language. Switch language, edit the text, switch back.

**Name** is deliberately not translatable, so your orders stay consistent. See [Translate option content](../translations/translate-option-content.md).
