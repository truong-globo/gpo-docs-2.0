---
description: Your own HTML inside the option widget, for anything the other static types cannot produce.
icon: code
---

# HTML

A block where you write your own HTML. It is the escape hatch: everything the other static types cannot do, you can do here.

Reach for it last. A [Paragraph](paragraph.md), [Pop-up modal](pop-up-modal.md), [Size chart](size-chart.md), or [Tabs](tabs.md) will keep working when your theme changes; hand-written HTML is yours to maintain.

## What customers see

Whatever you wrote, rendered in the flow of the form.

<!-- SCREENSHOT: type-html-storefront | Storefront → trang sản phẩm | 1 block HTML tuỳ chỉnh (ví dụ bảng nhỏ hoặc badge) trong widget | Khoanh riêng block HTML -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A custom HTML block rendered inside the option widget on a storefront product page"><figcaption><p>The HTML block renders inline with your options.</p></figcaption></figure>

## Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Content</strong></td><td>Your HTML, written in a code editor. Starts with a sample block.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide the block.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and width.</td></tr></tbody></table>

## When it is the right answer

<table><thead><tr><th width="290">You want</th><th>Notes</th></tr></thead><tbody><tr><td>A small table the rich-text editor cannot produce</td><td>For size tables use <a href="size-chart.md">Size chart</a> first — it is built for this</td></tr><tr><td>A badge, banner, or icon row in your own markup</td><td>Style it with a class and <a href="../../storefront/custom-css.md">custom CSS</a> rather than inline styles, so it stays maintainable</td></tr><tr><td>A layout the other types cannot express</td><td>Keep it simple; your theme's CSS also applies here</td></tr><tr><td>Content produced by another system</td><td>Paste the markup, but check it renders on mobile</td></tr></tbody></table>

## When it is not

* **Formatted text.** Use [Paragraph](paragraph.md) — you get the same result with an editor and no maintenance.
* **A size table.** Use [Size chart](size-chart.md), which has thirteen presets and a table editor.
* **Several blocks of content.** Use [Tabs](tabs.md).
* **Styling the widget.** Use **Settings > Design**, or [custom CSS](../../storefront/custom-css.md) with an [HTML class](../shared-settings/direction-width-and-css.md#html-class). Do not rebuild parts of the widget in HTML.
* **Collecting anything.** An HTML block collects nothing. A form field written here is not part of the option set, is not validated, and does not reach the order — use a real [input type](../input-types/README.md).

{% hint style="warning" %}
Only paste markup you understand and trust. Content in this block renders on your product pages, so treat it like anything else you put into your theme — and check the result on a real product page and on a phone before going live.
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

A two-column table of materials and measurements, where the content is fixed and does not belong in a size chart.

**A conditional notice**

A styled notice block, shown by conditional logic only when the shopper chooses an option with a long lead time.

## Limits and notes

* Available on the Advanced plan.
* Works in Shopify POS.
* Collects nothing, so it never reaches the cart or order.
* Content is translatable per storefront language, like other option content.
* Your theme's CSS applies to the block, so a class name that collides with a theme class can produce surprising results. Prefix your class names.
* Test on mobile. Fixed widths and wide tables are the usual problems.

## Troubleshooting

<details>
<summary>My HTML does not render as expected</summary>

Check the markup is complete and well formed. Your theme's own styles also apply — inspect the element on the storefront to see what is overriding what.
</details>

<details>
<summary>It looks broken on mobile</summary>

Avoid fixed widths and wide tables. Test at mobile width in the builder preview and on a real phone.
</details>

<details>
<summary>My styling is ignored</summary>

Theme rules may be more specific. Move your styles into [custom CSS](../../storefront/custom-css.md) with a distinctive class name.
</details>

<details>
<summary>I added a form field and nothing arrives on the order</summary>

Expected. HTML blocks collect nothing. Use a real [input type](../input-types/README.md).
</details>

<details>
<summary>HTML is greyed out</summary>

It is on the Advanced plan. See [Compare plans](../../plans/compare-plans.md).
</details>

## Next steps

* [Paragraph](paragraph.md) — formatted text without the maintenance.
* [Size chart](size-chart.md) — for size tables.
* [Custom CSS](../../storefront/custom-css.md) — the right place for styling.
