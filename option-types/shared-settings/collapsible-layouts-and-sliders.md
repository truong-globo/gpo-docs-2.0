---
description: >-
  Configure custom layouts, scrolling, and sliders to display long lists of
  option values in a smaller space.
icon: layer-group
---

# Collapsible layouts and sliders

Use custom layouts to control how option values are displayed. You can collapse long lists, add scrolling, or display values in a slider.

These settings are available under **Advanced Settings**. Turn on **Enable custom layout** to access them.

## Enable custom layout

**Enable custom layout** lets you change how the option values are displayed.

<table><thead><tr><th width="290">Setting</th><th>Details</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>Off</td></tr><tr><td><strong>Available on</strong></td><td>Checkbox, Radio button, Button, Color swatch, Image swatch</td></tr></tbody></table>

When disabled, all option values are displayed in the default layout.

When enabled, you can select a **Layout type**.

## Layout type

Select how the option values should be displayed.

<table><thead><tr><th width="290">Option type</th><th>Available layouts</th></tr></thead><tbody><tr><td>Checkbox</td><td>Expand, Collapse</td></tr><tr><td>Radio button</td><td>Expand, Collapse</td></tr><tr><td>Button</td><td>Expand, Collapse, Slider</td></tr><tr><td>Color swatch</td><td>Expand, Collapse, Slider</td></tr><tr><td>Image swatch</td><td>Expand, Collapse, Slider</td></tr></tbody></table>

**Expand**

The option values are displayed in an expanded list by default. Customers can collapse the list.

Use **Expand** when customers are likely to use the option but you still want to let them hide the list.

**Collapse**

The option values are hidden by default. Customers can click to expand the list.

Use **Collapse** for optional or less frequently used options.

{% hint style="warning" %}
Avoid using **Collapse** for required options. Customers may not open the collapsed option and can miss a required selection.
{% endhint %}

**Slider**

The option values are displayed in a horizontal slider. Customers can use the navigation controls or swipe to view additional values.

**Slider** is available for Button, Color swatch, and Image swatch options.

Use it when an option contains many visual values and displaying all of them would make the page too long.

## Scrolling

When using **Expand** or **Collapse**, you can add a scroll area to limit the height of the option values.

<table><thead><tr><th width="290">Setting</th><th>Details</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>Displays all values without scrolling</td></tr><tr><td><strong>By fixed height</strong></td><td>Sets a fixed height in pixels</td></tr><tr><td><strong>By number of option values</strong></td><td>Displays a specified number of values before scrolling</td></tr></tbody></table>

**By fixed height**

Sets a fixed height for the option list. Customers can scroll inside the list when there are more values than can fit in the specified height.

Selecting this option displays the **Scroll height** setting.

Use this when you need the option list to fit within a specific area of your page.

**By number of option values**

Limits the number of visible option values instead of using a fixed height.

Selecting this option displays the **Number of option values** setting.

For example, setting it to **8** displays eight values at a time. Customers can scroll to see the remaining values.

This option is useful when the size of your option values can vary between devices or themes.

**Default**

Displays all option values without a scroll area.

Use **Default** when the option contains only a small number of values and does not need scrolling.

## Slider settings

When **Layout type** is set to **Slider**, additional settings are available.

<table><thead><tr><th width="230">Setting</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><strong>Number of rows</strong></td><td><code>1</code></td><td>Number of rows displayed in the slider</td></tr><tr><td><strong>Swatches per row</strong></td><td><code>3</code></td><td>Number of swatches displayed in each row</td></tr><tr><td><strong>Show navigation arrows</strong></td><td><strong>Hide</strong></td><td>Displays previous and next arrows</td></tr><tr><td><strong>Show indicators</strong></td><td><strong>Hide</strong></td><td>Displays indicators below the slider</td></tr><tr><td><strong>Slider style</strong></td><td><strong>Style 1</strong></td><td>Selects the navigation arrow style</td></tr></tbody></table>

Slider settings are available for **Button**, **Color swatch**, and **Image swatch** options. Availability may depend on your plan.

**Number of rows**

Sets the number of rows displayed in the slider.

For example:

* `1` displays one row.
* `2` displays two rows.

**Swatches per row**

Sets how many swatches are displayed in each row.

You can use a decimal value to display part of the next swatch. For example, `4.5` displays four full swatches and part of the next one.

A partial swatch can help indicate that more values are available.

**Show navigation arrows**

Displays previous and next arrows on the slider.

Set this to **Show** if you want customers to navigate through the slider using the arrows.

**Show indicators**

Displays indicators below the slider.

Customers can select an indicator to move to the corresponding position in the slider.

**Slider style**

Selects the style of the navigation arrows.

This setting is available only when **Show navigation arrows** is set to **Show**.

{% hint style="info" %}
We recommend enabling **Show navigation arrows** or **Show indicators** so customers can see that more option values are available.
{% endhint %}

## Example configuration

The following configuration works well for an image swatch with many values:

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td><strong>Enable custom layout</strong></td><td>On</td></tr><tr><td><strong>Layout type</strong></td><td>Slider</td></tr><tr><td><strong>Number of rows</strong></td><td><code>2</code></td></tr><tr><td><strong>Swatches per row</strong></td><td><code>4.5</code></td></tr><tr><td><strong>Show navigation arrows</strong></td><td>Show</td></tr><tr><td><strong>Show indicators</strong></td><td>Hide</td></tr><tr><td><strong>Swatch image width</strong></td><td><code>60</code></td></tr><tr><td><strong>Swatch image height</strong></td><td><code>60</code></td></tr></tbody></table>

This displays two rows of swatches while keeping the option compact. The partially visible swatch also indicates that more values are available.

## Which layout should I use?

<table><thead><tr><th width="290">Situation</th><th>Recommended setting</th></tr></thead><tbody><tr><td>Many text choices make the page too long</td><td><strong>Collapse</strong> or <strong>Expand</strong> with scrolling</td></tr><tr><td>Many visual swatches</td><td><strong>Slider</strong></td></tr><tr><td>An optional or less frequently used option</td><td><strong>Collapse</strong></td></tr><tr><td>Customers need to search through many values</td><td><strong>Dropdown</strong> with <strong>Search suggestion</strong></td></tr><tr><td>Several groups of options need to be organized</td><td>Use a <strong>Section</strong> around each group</td></tr><tr><td>The entire widget is too tall</td><td>Enable <strong>Limit widget height</strong> under <strong>Settings > Settings > General</strong></td></tr></tbody></table>

For more information, see:

* [Dropdown](../selection-types/dropdown.md)
* [Search suggestion](selection-behaviour.md#search-suggestion)
* [Section](../static-types/section.md)
* [Widget behavior](../../storefront/widget-behavior.md)

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Slider settings for an Image swatch option"><figcaption><p>Slider settings are displayed when Layout type is set to Slider.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/placeholder.png" alt="Image swatch slider with two rows and navigation arrows"><figcaption><p>An image swatch slider with two rows and navigation arrows.</p></figcaption></figure>
