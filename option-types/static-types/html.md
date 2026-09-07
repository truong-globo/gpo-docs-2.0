---
description: >-
  Your own HTML inside the option widget, for anything the other static types
  cannot produce.
icon: code
---

# HTML

A block where you write your own HTML, for anything the other static types cannot produce.

Use it last. A [Paragraph](paragraph.md), [Pop-up modal](pop-up-modal.md), [Size chart](size-chart.md), or [Tabs](tabs.md) is easier to maintain and more likely to keep working when your theme changes. HTML you write yourself is yours to maintain.

## What customers see

The HTML you wrote, displayed in the form.

## Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Content</strong></td><td>Your HTML, written in a code editor. Starts with a sample block.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide the block.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and width.</td></tr></tbody></table>

## When to use it

<table><thead><tr><th width="290">You want</th><th>Notes</th></tr></thead><tbody><tr><td>A small table the rich-text editor cannot produce</td><td>For size tables use <a href="size-chart.md">Size chart</a> first — it is built for this</td></tr><tr><td>A badge, banner, or icon row in your own markup</td><td>Style it with a class and <a href="../../storefront/custom-css.md">custom CSS</a> rather than inline styles, so it stays maintainable</td></tr><tr><td>A layout the other types cannot express</td><td>Keep it simple; your theme's CSS also applies here</td></tr><tr><td>Content produced by another system</td><td>Paste the markup, but check it renders on mobile</td></tr></tbody></table>

## When not to use it

* **Formatted text.** Use [Paragraph](paragraph.md), which gives the same result with an editor and nothing to maintain.
* **A size table.** Use [Size chart](size-chart.md), which has thirteen presets and a table editor.
* **Several blocks of content.** Use [Tabs](tabs.md).
* **Styling the widget.** Use **Settings > Design**, or [custom CSS](../../storefront/custom-css.md) with an [HTML class](../shared-settings/direction-width-and-css.md#html-class). Do not rebuild parts of the widget in HTML.
* **Collecting an answer.** An HTML block collects nothing. A form field written here is not part of the option set, is not validated, and is not stored in the order. Use an [input type](../input-types/) instead.

{% hint style="warning" %}
Only paste markup you understand and trust. Content in this block is rendered directly on your product pages, so treat it like code added to your theme. Always check the result on a real product page and on a mobile device before going live.
{% endhint %}

## Examples

**A small badge row**

```html
<div class="gpo-badges">
  <span>Handmade</span>
  <span>3–5 day lead time</span>
  <span>Gift wrap available</span>
</div>
```

Styled with a `.gpo-badges` rule in [custom CSS](../../storefront/custom-css.md).

**A short specification table**

A two-column table of materials and measurements, where the content is fixed and is not a size chart.

**A conditional notice**

A styled notice block, displayed by conditional logic only when the customer selects an option with a long lead time.

## Notes

* Available on the Advanced plan.
* Works in Shopify POS.
* The content can be translated for each storefront language, like other option content.
* Your theme’s CSS is applied to the block, so class names that conflict with existing theme classes may cause unexpected styling issues. To avoid conflicts, use a unique prefix for your class names.
* Test your content thoroughly on mobile. Fixed-width elements and wide tables are the most common causes of display issues.
