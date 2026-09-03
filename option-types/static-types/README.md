---
description: >-
  The 9 option types that collect no customer input. Use them to organize your
  form, explain information, and break up the page.
icon: table-cells-large
---

# Static types

Static types do not ask the customer for anything. They make the rest of the form easier to read by adding headings, spacing, explanations, size tables, and containers that group related options together.

They turn a form from a wall of fields into something shoppers can scan and understand.

## The nine static types

<table><thead><tr><th width="200">Type</th><th>Does</th><th>Reach for it when</th></tr></thead><tbody><tr><td><a href="section.md">Section</a></td><td>Groups options under a heading, optionally collapsible</td><td>You have more than about six options</td></tr><tr><td><a href="heading.md">Heading</a></td><td>A heading in one of six sizes</td><td>You want a divider with words</td></tr><tr><td><a href="divider.md">Divider</a></td><td>A horizontal rule</td><td>Two groups need separating visually</td></tr><tr><td><a href="spacing.md">Spacing</a></td><td>Vertical space, in pixels</td><td>Something needs room around it</td></tr><tr><td><a href="paragraph.md">Paragraph</a></td><td>Formatted text</td><td>A sentence or two of explanation</td></tr><tr><td><a href="pop-up-modal.md">Pop-up modal</a></td><td>A link that opens content in a dialog</td><td>The explanation is long and most shoppers will skip it</td></tr><tr><td><a href="html.md">HTML</a></td><td>Your own HTML</td><td>Nothing else produces what you need</td></tr><tr><td><a href="size-chart.md">Size chart</a></td><td>A size table, from a preset or your own</td><td>You sell clothing, shoes, or other wearable items.</td></tr><tr><td><a href="tabs.md">Tabs</a></td><td>Several panels behind tabs</td><td>Care, delivery, and returns in one place</td></tr></tbody></table>

## What they have in common

Static types have far fewer settings than the others, because most settings describe collecting an answer.

<table><thead><tr><th width="290">They have</th><th>They do not have</th></tr></thead><tbody><tr><td>Their own content field — text, rich text, HTML, or a table</td><td><strong>Label</strong> and <strong>Name</strong> — except <a href="section.md">Section</a>, which has a Label</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a> — on all nine</td><td><strong>Required field</strong>, <strong>Placeholder</strong>, <strong>Help text</strong>, <strong>Default value</strong></td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a></td><td>Add-on pricing</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a> — all except Section</td><td>Personalizer Settings</td></tr></tbody></table>

{% hint style="info" %}
**Conditional logic also works on static types**, which makes them more useful than they might seem. You can show a warning only when a shopper selects a risky option, reveal a size chart only for garments, or hide an entire [Section](section.md) until it becomes relevant. See [Conditional logic](../../conditional-logic/).
{% endhint %}

## Because they collect nothing

Static types never appear on the cart or the order. They are purely part of the product page.

That also means they have no **Name**, so there is nothing to keep unique — you can have five dividers and three headings in one option set without any naming conflict.

## Using them well

A few habits that make a long form readable:

* **Group before you explain.** A [Section](section.md) with a good label often removes the need for a heading and a paragraph.
* **One paragraph, not three.** If you have more to say, use a [Pop-up modal](pop-up-modal.md) or [Tabs](tabs.md) so the page stays short.
* **Prefer Spacing to empty paragraphs.** It is what it says, and it is easier to adjust.
* **Use Divider sparingly.** A rule between every option is noise; a rule between two groups is structure.
* **Reach for HTML last.** If a native type can do it, use the native type — it will keep working when your theme changes.
