---
description: >-
  Every setting that appears on more than one option type, explained once and
  linked from everywhere.
icon: sliders
---

# Shared settings

Most settings are not unique to one option type. **Required field** works the same way on a text box and on a dropdown; **Column width** works the same way on all thirty types that have it.

Rather than repeat those explanations on thirty pages, they live here. The option type pages tell you *which* settings a type has; these pages tell you *what each one does*.

## How to find a setting

<table><thead><tr><th width="330">Setting</th><th>Page</th></tr></thead><tbody><tr><td><strong>Label</strong>, <strong>Name</strong>, <strong>Hidden label</strong></td><td><a href="labels-and-visibility.md">Labels and visibility</a></td></tr><tr><td><strong>Placeholder</strong>, <strong>Help text</strong>, <strong>Help text position</strong></td><td><a href="placeholder-and-help-text.md">Placeholder and help text</a></td></tr><tr><td><strong>Required field</strong>, <strong>Default value</strong></td><td><a href="required-and-default-value.md">Required field and default value</a></td></tr><tr><td><strong>Min character</strong>, <strong>Max character</strong>, <strong>Character counter</strong>, <strong>Min value</strong>, <strong>Max value</strong>, <strong>Min selections</strong>, <strong>Max selections</strong>, <strong>Min number of files</strong>, <strong>Max number of files</strong></td><td><a href="limits.md">Limits</a></td></tr><tr><td><strong>Allowed value</strong>, <strong>Text transform</strong></td><td><a href="text-input-rules.md">Text input rules</a></td></tr><tr><td><strong>Allow multiple</strong>, <strong>Not allow deselect</strong>, <strong>Search suggestion</strong></td><td><a href="selection-behaviour.md">Selection behaviour</a></td></tr><tr><td><strong>Swatch style</strong>, <strong>Swatch image width</strong>, <strong>Swatch image height</strong>, <strong>Tooltip style</strong>, <strong>Tooltip image width</strong>, <strong>Tooltip image height</strong>, <strong>Color preview</strong>, <strong>Select text box</strong>, <strong>Font preview</strong></td><td><a href="swatch-style-and-previews.md">Swatch style and previews</a></td></tr><tr><td><strong>Enable custom layout</strong>, <strong>Layout type</strong>, <strong>Scroll type</strong>, <strong>Scroll height</strong>, <strong>Number of option values</strong>, <strong>Number of rows</strong>, <strong>Swatches per row</strong>, <strong>Show navigation arrows</strong>, <strong>Show indicators</strong>, <strong>Slider style</strong></td><td><a href="collapsible-layouts-and-sliders.md">Collapsible layouts and sliders</a></td></tr><tr><td><strong>Direction style</strong>, <strong>Column width</strong>, <strong>HTML class</strong></td><td><a href="direction-width-and-css.md">Direction, width, and CSS</a></td></tr><tr><td><strong>Prefix</strong>, <strong>Prefix icon</strong>, <strong>Prefix text</strong>, <strong>Suffix</strong>, element icons</td><td><a href="prefix-suffix-and-icons.md">Prefix, suffix, and icons</a></td></tr><tr><td><strong>Out of stock options</strong></td><td><a href="out-of-stock-options.md">Out of stock options</a></td></tr><tr><td><strong>Conditional logic</strong>, <strong>Price</strong>, <strong>Advanced settings</strong>, <strong>Set quantity</strong></td><td><a href="conditional-logic-and-add-on-fields.md">Conditional logic and add-on fields</a></td></tr></tbody></table>

## Which tab a setting is on

Every option's settings are split across tabs. Knowing which tab a setting lives on saves hunting for it.

<table><thead><tr><th width="230">Tab</th><th>Holds</th></tr></thead><tbody><tr><td><strong>Basic Settings</strong></td><td>Label, Name, Required field, Hidden label, option values, Placeholder, Help text, Default value, all the min and max limits, Character counter, Allow multiple, Swatch style, the <strong>Price</strong> add-on field, and the Conditional logic switch.</td></tr><tr><td><strong>Advanced Settings</strong></td><td>Help text position, Allowed value, Text transform, Prefix and Suffix, Column width, HTML class, Direction style, Out of stock options, Search suggestion, Not allow deselect, all the collapsible and slider settings, swatch and tooltip image sizes, Color preview, Select text box, Font preview, and the add-on <strong>Advanced settings</strong> dropdown.</td></tr><tr><td><strong>Personalizer Settings</strong></td><td>Everything about the live preview. Covered in <a href="../../personalizer/README.md">Product Personalizer</a> rather than here.</td></tr></tbody></table>

{% hint style="info" %}
Many settings only appear once something else is turned on. **Scroll height** appears only after you choose a scroll type; **Set quantity** appears only for two of the advanced add-on modes; **Prefix icon** appears only when **Prefix** is set to **Icon**. If a setting is described here but you cannot see it, check what it depends on.
{% endhint %}

## Notation used on these pages

Each setting is documented with the same three facts before the explanation:

* **Tab** — Basic Settings or Advanced Settings.
* **Default** — what a new option starts with.
* **Available on** — which option types offer it. Where a setting is on nearly everything, the list says which types *lack* it instead, because that is shorter and more useful.

## Next steps

* [Option types](../README.md) — which settings each type has.
* [Labels and visibility](labels-and-visibility.md) — the two fields every option has.
* [Conditional logic](../../conditional-logic/README.md) and [Add-on pricing](../../add-on-pricing/README.md) — the two big features these fields lead into.
