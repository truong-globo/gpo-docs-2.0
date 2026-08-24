---
description: >-
  The 12 option types where the customer enters something rather than choosing
  from a list.
icon: keyboard
---

# Input types

Input types collect whatever the customer gives you. They have no option values, because there is no list to pick from — the customer types, picks, drags, or uploads.

## The twelve

<table><thead><tr><th width="220">Type</th><th>Collects</th><th>Reach for it when</th></tr></thead><tbody><tr><td><a href="text.md">Text</a></td><td>One line of text</td><td>A name, an engraving, a short message</td></tr><tr><td><a href="textarea.md">Textarea</a></td><td>Several lines of text</td><td>A gift message or special instructions</td></tr><tr><td><a href="number.md">Number</a></td><td>A number</td><td>A quantity or a single measurement</td></tr><tr><td><a href="phone.md">Phone</a></td><td>A phone number</td><td>Delivery contact details, with country validation</td></tr><tr><td><a href="email.md">Email</a></td><td>An email address</td><td>Sending a digital gift or a proof</td></tr><tr><td><a href="hidden-field.md">Hidden field</a></td><td>Nothing from the customer</td><td>Attaching a fixed value to the order silently</td></tr><tr><td><a href="date-and-time-picker.md">Date and time picker</a></td><td>A date, a time, or a range</td><td>Delivery dates, appointments, event dates</td></tr><tr><td><a href="file-upload.md">File upload</a></td><td>One or more files</td><td>Photos to print, logos, artwork</td></tr><tr><td><a href="color-picker.md">Color picker</a></td><td>Any colour</td><td>Custom paint or thread colours</td></tr><tr><td><a href="switch.md">Switch</a></td><td>Yes or no</td><td>A single paid extra such as gift wrap</td></tr><tr><td><a href="range-slider.md">Range slider</a></td><td>A number, dragged</td><td>An approximate value within a range</td></tr><tr><td><a href="dimension.md">Dimension</a></td><td>Two or three measurements</td><td>Made-to-measure products priced by size</td></tr></tbody></table>

## What they have in common

Nearly all of them offer these, all documented in [Shared settings](../shared-settings/README.md):

* [Label](../shared-settings/labels-and-visibility.md#label), [Name](../shared-settings/labels-and-visibility.md#name), [Hidden label](../shared-settings/labels-and-visibility.md#hidden-label)
* [Required field](../shared-settings/required-and-default-value.md#required-field) and [Default value](../shared-settings/required-and-default-value.md#default-value)
* [Placeholder](../shared-settings/placeholder-and-help-text.md#placeholder), [Help text](../shared-settings/placeholder-and-help-text.md#help-text) and its [position](../shared-settings/placeholder-and-help-text.md#help-text-position)
* [Conditional logic](../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic)
* [Column width](../shared-settings/direction-width-and-css.md#column-width) and [HTML class](../shared-settings/direction-width-and-css.md#html-class)

## Where they differ

<table><thead><tr><th width="290">Capability</th><th>Types that have it</th></tr></thead><tbody><tr><td>Can carry an add-on price</td><td>Text, Textarea, Number, Switch, Color picker, Dimension</td></tr><tr><td><strong>Cannot</strong> carry an add-on price</td><td>Phone, Email, Hidden field, Date and time picker, File upload, Range slider</td></tr><tr><td>Personalizer support</td><td>Text, Textarea, Number, File upload</td></tr><tr><td>Character or value limits</td><td>Text and Textarea (characters); Number and Range slider (values); File upload (file count)</td></tr><tr><td>Prefix and suffix</td><td>Text, Textarea, Number, Phone, Email, Date and time picker; Range slider has its own simpler pair</td></tr><tr><td>Not supported on POS</td><td>Dimension</td></tr></tbody></table>

{% hint style="info" %}
Some types cannot carry a price — a delivery-date fee, for example. Put the charge on a separate [Switch](switch.md) or [Checkbox](../selection-types/checkbox.md) beside it, then use [conditional logic](../../conditional-logic/README.md) to reveal it when relevant.
{% endhint %}

## Choosing between them

The close calls are covered in [Choose the right option type](../choose-the-right-type.md): Text against Textarea, Number against Range slider against Dimension, and Switch against a single Checkbox.
