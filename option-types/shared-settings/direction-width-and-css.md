---
description: >-
  Direction style, Column width, and HTML class — how much of the page an option
  takes up, and how to style it yourself.
icon: table-columns
---

# Direction, width, and CSS

Three layout settings. Two are for everybody; the third is for whoever writes your CSS.

## Direction style

Whether a list of values runs down the page or across it.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Vertical</strong>, except on <strong>Tabs</strong>, where it is <strong>Horizontal</strong></td></tr><tr><th>Available on</th><td>Checkbox, Radio button, Button, Color swatch, Image swatch, Tabs</td></tr></thead></table>

<table><thead><tr><th width="180">Choice</th><th>Behaviour</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Vertical</strong></td><td>One value per line, stacked</td><td>Values have long names, or per-value help text. Easiest to scan and safest on mobile.</td></tr><tr><td><strong>Horizontal</strong></td><td>Values run across the page and wrap</td><td>Short values — sizes, small colour chips, two or three buttons. Saves vertical space.</td></tr></tbody></table>

**On Tabs** it means something slightly different: **Horizontal** puts the tab titles in a row above the content, **Vertical** puts them in a column beside it. See [Tabs](../static-types/tabs.md).

{% hint style="info" %}
Horizontal saves space, but check the mobile preview. Six buttons that fit one desktop row become three cramped rows on a phone, and long value names wrap mid-word. When in doubt, vertical.
{% endhint %}

## Column width

How much of the widget's width the option occupies.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>100%</strong></td></tr><tr><th>Available on</th><td>30 types — everything except <strong>Section</strong> and <strong>Hidden field</strong></td></tr></thead></table>

Six choices: **25%**, **33%**, **50%**, **66%**, **75%**, **100%**.

**How it behaves**

* Options narrower than 100% sit side by side on the same row, in panel order, until the row is full.
* The width is a share of the widget's width, not of the page.
* On narrow screens options fall back to full width so they stay usable on a phone.
* The [inspector](../../option-sets/live-preview-and-inspector.md) offers **Half width** and **Full width** as one-click shortcuts for 50% and 100%.

**Combinations that work**

<table><thead><tr><th width="290">Layout</th><th>Set</th></tr></thead><tbody><tr><td>First name and last name on one line</td><td>Two text options at <strong>50%</strong></td></tr><tr><td>Width, height, and depth on one line</td><td>Three number options at <strong>33%</strong></td></tr><tr><td>A wide field with a small unit selector beside it</td><td><strong>75%</strong> then <strong>25%</strong></td></tr><tr><td>A date and a time slot</td><td>Two options at <strong>50%</strong></td></tr><tr><td>Anything with long help text</td><td><strong>100%</strong> — narrow columns make help text wrap awkwardly</td></tr></tbody></table>

{% hint style="warning" %}
The percentages do not have to add up. Two options at 75% will not share a row — the second wraps to the next line, leaving a gap. If your layout has unexpected gaps, add up the widths on each row.
{% endhint %}

For three fields of the same kind, consider [Dimension](../input-types/dimension.md) instead: it gives you width, height, and depth in one option, with its own units and its own pricing formula.

## HTML class

Adds a CSS class to the option so you can style it yourself.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td>Empty</td></tr><tr><th>Available on</th><td>30 types — everything except <strong>Hidden field</strong>. <strong>Section</strong> has it too</td></tr></thead></table>

{% hint style="warning" %}
**HTML class only accepts letters, numbers, hyphens, and underscores.** Anything else is rejected with "HTML class only accepts letters, numbers, hyphens and underscore." Do not include a leading dot — enter `engraving-field`, not `.engraving-field`.
{% endhint %}

**How to use it**

{% stepper %}
{% step %}
### Give the option a class

Enter a name that describes the option, for example `engraving-field`.
{% endstep %}

{% step %}
### Write the CSS

Go to **Settings** > **Settings** > **Design** > **Additional** and add your rules to **Custom CSS for the widget**:

```css
.engraving-field label {
  font-weight: 600;
  letter-spacing: 0.04em;
}

.engraving-field input {
  text-align: center;
}
```
{% endstep %}

{% step %}
### Check it on the storefront

Custom CSS applies to the live widget, not the builder preview. Use **View in Store** to check it.
{% endstep %}
{% endstepper %}

**What it is good for**

* Emphasising one important option among many.
* Hiding something in a specific context that no setting covers.
* Matching a house style the [design settings](../../storefront/colors.md) do not reach.
* Giving support or a developer a reliable handle on one option.

**What to try first instead**

Most requests that reach for CSS have a setting: [Column width](#column-width) for layout, [Design settings](../../storefront/colors.md) for colours and fonts, [Match your theme style](../../storefront/match-your-theme-style.md) for making the widget look like your theme. Custom CSS is a fine tool, but it is yours to maintain — a theme update can change what your selectors match.

See [Custom CSS](../../storefront/custom-css.md).

<!-- SCREENSHOT: type-shared-width-css | App admin → builder → 1 option → Advanced Settings | Direction style, Column width (6 lựa chọn), HTML class | Khoanh Column width -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Direction style, Column width, and HTML class on an option's Advanced Settings"><figcaption><p>All three sit together near the bottom of Advanced Settings.</p></figcaption></figure>

## Troubleshooting

<details>
<summary>Two options at 50% are not sharing a row</summary>

Check their order in the panel — they must be adjacent — and that nothing between them is 100%. A [Section](../static-types/section.md) boundary also starts a new row.
</details>

<details>
<summary>There is an empty gap next to an option</summary>

The widths on that row do not fill it. Either widen the option, or give the next option a width that fits the remaining space.
</details>

<details>
<summary>Column width has no effect on mobile</summary>

Expected. Narrow screens fall back to full width so fields stay usable.
</details>

<details>
<summary>"HTML class only accepts letters, numbers, hyphens and underscore"</summary>

Remove the offending character — most often a leading dot or a comma. One class name per option.
</details>

<details>
<summary>My custom CSS is not applying</summary>

Three things: the class is on the option and saved; the CSS is in **Settings > Design > Additional**; and you are looking at the storefront rather than the builder preview. If it still does not apply, your theme's own rules may be more specific.
</details>

<details>
<summary>Horizontal values are wrapping badly</summary>

The value names are too long for the width available. Shorten them, switch to **Vertical**, or give the option a wider column.
</details>

## Next steps

* [Collapsible layouts and sliders](collapsible-layouts-and-sliders.md) — for long lists.
* [Custom CSS](../../storefront/custom-css.md)
* [Colors](../../storefront/colors.md) — before reaching for CSS.
