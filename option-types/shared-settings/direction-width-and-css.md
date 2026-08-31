---
description: >-
  Set the direction of option values, control how much width an option uses, and
  add a CSS class for custom styling.
icon: table-columns
---

# Direction, width, and CSS

These three settings control the layout of an option. All of them are available under **Advanced Settings**.

## Direction style

Sets whether option values are listed vertically or horizontally.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>Vertical</strong>. On Tabs, the default is <strong>Horizontal</strong></td></tr><tr><td>Available on</td><td>Checkbox, Radio button, Button, Color swatch, Image swatch, Tabs</td></tr></tbody></table>

**Vertical**

Each option value is displayed on its own line.

Use **Vertical** when option values have long names or their own help text. This layout is also the safest on mobile.

**Horizontal**

Option values are displayed across the page and wrap to the next line when there is no more space.

Use **Horizontal** for short values such as sizes, small color chips, or a small number of buttons. This layout reduces the height of the option.

{% hint style="info" %}
Check the mobile preview after selecting **Horizontal**. Values that fit on one row on desktop can wrap into several rows on a phone, and long value names can break mid-word.
{% endhint %}

**On Tabs**

For the Tabs option type, **Direction style** controls the position of the tab titles.

* **Horizontal** displays the tab titles in a row above the content.
* **Vertical** displays the tab titles in a column beside the content.

See [Tabs](../static-types/tabs.md).

## Column width

Sets how much of the widget width the option uses.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td><strong>100%</strong></td></tr><tr><td>Available on</td><td>30 option types. Not available on Section or Hidden field</td></tr></tbody></table>

The available values are **25%**, **33%**, **50%**, **66%**, **75%**, and **100%**.

Options set to less than 100% are displayed side by side on the same row. They are placed in the order they appear in the option list, until the row is full.

The percentage is a share of the widget width, not of the page width. On narrow screens, options are displayed at full width.

The [inspector](../../option-sets/live-preview-and-inspector.md) includes **Half width** and **Full width** shortcuts for 50% and 100%.

<table><thead><tr><th width="290">Layout</th><th>Configuration</th></tr></thead><tbody><tr><td>First name and last name on one row</td><td>Two text options at <strong>50%</strong></td></tr><tr><td>Width, height, and depth on one row</td><td>Three number options at <strong>33%</strong></td></tr><tr><td>A wide field with a small selector beside it</td><td><strong>75%</strong>, then <strong>25%</strong></td></tr><tr><td>A date and a time slot on one row</td><td>Two options at <strong>50%</strong></td></tr><tr><td>An option with long help text</td><td><strong>100%</strong></td></tr></tbody></table>

{% hint style="warning" %}
The percentages are not validated. Two options set to 75% cannot share a row, so the second option moves to the next row and leaves empty space. Check that the widths on each row add up to 100% or less.
{% endhint %}

For three measurements in a single option, use the [Dimension](../input-types/dimension.md) option type instead. It includes its own units and pricing formula.

## HTML class

Adds a CSS class to the option so you can apply your own styles.

<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Empty</td></tr><tr><td>Available on</td><td>31 option types. Not available on Hidden field. Section has its own field</td></tr></tbody></table>

Enter one class name, for example `engraving-field`. Do not include a leading dot.

Only letters, numbers, hyphens, and underscores are accepted. Other characters are rejected with the message "HTML class only accepts letters, numbers, hyphens and underscore."

**Using the class**

Add your rules to **Custom CSS for the widget** under **Settings > Settings > Design > Additional**:

```css
.engraving-field label {
  font-weight: 600;
  letter-spacing: 0.04em;
}

.engraving-field input {
  text-align: center;
}
```

Custom CSS applies to the widget on your storefront, not to the builder preview. Use **View in Store** to check the result.

**When to use it**

Use **HTML class** when you need to:

* Change the appearance of one option only.
* Hide an element in a specific context that no setting covers.
* Match a style that the design settings do not cover.
* Give a developer or support agent a way to target one option.

Before using custom CSS, check whether a setting already covers your requirement:

<table><thead><tr><th width="290">Requirement</th><th>Setting</th></tr></thead><tbody><tr><td>Change the width of an option</td><td><a href="#column-width">Column width</a></td></tr><tr><td>Change colors, borders, or fonts</td><td><a href="../../storefront/colors.md">Design settings</a></td></tr><tr><td>Match the widget to your theme</td><td><a href="../../storefront/match-your-theme-style.md">Match your theme style</a></td></tr></tbody></table>

Custom CSS is not maintained by the app. A theme update can change the elements your selectors apply to.

For more information, see:

* [Custom CSS](../../storefront/custom-css.md)
* [Live preview and inspector](../../option-sets/live-preview-and-inspector.md)
* [Dimension](../input-types/dimension.md)

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Direction style, Column width, and HTML class settings"><figcaption><p>Direction style, Column width, and HTML class under Advanced Settings.</p></figcaption></figure>
