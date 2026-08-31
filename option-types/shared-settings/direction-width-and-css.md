---
description: >-
  Direction style, Column width, and HTML class — how much of the page an option
  takes up, and how to style it yourself.
icon: table-columns
---

# Direction, width, and CSS

Three layout settings, all on **Advanced Settings**. The first two are for everybody. The third is only useful if you or someone on your team writes CSS.

## Direction style

Whether a list of values runs down the page or across it.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>Vertical</strong>, except on <strong>Tabs</strong>, where it is <strong>Horizontal</strong></td></tr><tr><td>Available on</td><td>Checkbox, Radio button, Button, Color swatch, Image swatch, Tabs</td></tr></tbody></table>

<table><thead><tr><th width="180">Choice</th><th>Behavior</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Vertical</strong></td><td>One value per line, stacked</td><td>Values have long names, or their own help text. Easiest to scan, and safest on mobile</td></tr><tr><td><strong>Horizontal</strong></td><td>Values run across the page and wrap</td><td>Short values such as sizes, small color chips, or two or three buttons. Saves vertical space</td></tr></tbody></table>

**On Tabs it means something different**

**Horizontal** puts the tab titles in a row above the content. **Vertical** puts them in a column beside it. See [Tabs](../static-types/tabs.md).

{% hint style="info" %}
Horizontal saves space, but check the mobile preview before you commit to it. Six buttons that fit one desktop row become three cramped rows on a phone, and long value names wrap mid-word. When in doubt, vertical.
{% endhint %}

## Column width

How much of the widget's width the option occupies.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>100%</strong></td></tr><tr><td>Available on</td><td>30 types — everything except <strong>Section</strong> and <strong>Hidden field</strong></td></tr></tbody></table>

Six choices: **25%**, **33%**, **50%**, **66%**, **75%**, **100%**.

**How it behaves**

* Options narrower than 100% sit side by side on the same row, in panel order, until the row is full.
* The width is a share of the widget's width, not of the page.
* On narrow screens, options fall back to full width so they stay usable on a phone.
* The [inspector](../../option-sets/live-preview-and-inspector.md) offers **Half width** and **Full width** as one-click shortcuts for 50% and 100%.

**Combinations that work**

<table><thead><tr><th width="290">Layout</th><th>Set</th></tr></thead><tbody><tr><td>First name and last name on one line</td><td>Two text options at <strong>50%</strong></td></tr><tr><td>Width, height, and depth on one line</td><td>Three number options at <strong>33%</strong></td></tr><tr><td>A wide field with a small unit selector beside it</td><td><strong>75%</strong> then <strong>25%</strong></td></tr><tr><td>A date and a time slot</td><td>Two options at <strong>50%</strong></td></tr><tr><td>Anything with long help text</td><td><strong>100%</strong> — narrow columns make help text wrap awkwardly</td></tr></tbody></table>

{% hint style="warning" %}
The percentages do not have to add up, and the app does not stop you. Two options at 75% will not share a row: the second wraps to the next line and leaves a gap. If your layout has gaps you did not expect, add up the widths on each row.
{% endhint %}

For three measurements of the same kind, consider [Dimension](../input-types/dimension.md) instead. It gives you width, height, and depth in one option, with its own units and its own pricing formula.

## HTML class

Adds a CSS class to the option so you can style it yourself.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Empty</td></tr><tr><td>Available on</td><td>31 types — everything except <strong>Hidden field</strong>. <strong>Section</strong> has its own version of the field</td></tr></tbody></table>

**How it behaves**

* Enter a name that describes the option, such as `engraving-field`. No leading dot: `engraving-field`, not `.engraving-field`.
* One class name per option.
* Only letters, numbers, hyphens, and underscores are accepted. Anything else is rejected with "HTML class only accepts letters, numbers, hyphens and underscore."

**Using it**

Give the option a class, then add your rules to **Custom CSS for the widget** in **Settings > Settings > Design > Additional**:

```css
.engraving-field label {
  font-weight: 600;
  letter-spacing: 0.04em;
}

.engraving-field input {
  text-align: center;
}
```

Custom CSS applies to the live widget, not to the builder preview, so check the result with **View in Store**.

**Good uses**

* Emphasizing one important option among many.
* Hiding something in a specific context that no setting covers.
* Matching a house style the [design settings](../../storefront/colors.md) do not reach.
* Giving support or a developer a reliable handle on one option.

**What to try first**

Most requests that reach for CSS have a setting instead: [Column width](#column-width) for layout, [design settings](../../storefront/colors.md) for colors and fonts, and [Match your theme style](../../storefront/match-your-theme-style.md) for making the widget look like your theme.

Custom CSS is a fine tool, but it is yours to maintain — a theme update can change what your selectors match. See [Custom CSS](../../storefront/custom-css.md).

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Direction style, Column width, and HTML class on an option's Advanced Settings"><figcaption><p>All three sit together near the bottom of Advanced Settings.</p></figcaption></figure>
