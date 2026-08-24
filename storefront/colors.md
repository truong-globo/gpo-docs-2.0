---
description: Every colour setting in the widget, grouped as the app groups them.
icon: palette
---

# Colors

**Settings** > **Settings** > **Design** > **Color**. Store-wide, applying to every option set.

Before working through these by hand, try [Match your theme style](match-your-theme-style.md) — on a supported theme it does most of this for you.

## General

<table><thead><tr><th width="290">Setting</th><th>Colours</th></tr></thead><tbody><tr><td><strong>App background</strong></td><td>The widget's own background. Usually left matching your page background</td></tr><tr><td><strong>Label text</strong></td><td>Option labels</td></tr><tr><td><strong>Required character</strong></td><td>The marker on required options. Traditionally red — make sure it is visible against your background</td></tr><tr><td><strong>Help text</strong></td><td>Help text under and around options</td></tr><tr><td><strong>Total text</strong></td><td>The add-on total's label</td></tr><tr><td><strong>Total text money</strong></td><td>The amount itself. Often a green or your brand colour</td></tr></tbody></table>

## Inputs

Covers text fields, number fields, switches, and range sliders.

<table><thead><tr><th width="290">Setting</th><th>Colours</th></tr></thead><tbody><tr><td><strong>Input text</strong></td><td>What the customer types</td></tr><tr><td><strong>Input border</strong></td><td>The field's outline</td></tr><tr><td><strong>Input background</strong></td><td>Inside the field</td></tr><tr><td><strong>Switch background</strong></td><td>A switch when off</td></tr><tr><td><strong>Switch active background</strong></td><td>A switch when on</td></tr><tr><td><strong>Range slider thumb</strong></td><td>The slider handle</td></tr><tr><td><strong>Range slider background</strong></td><td>The unfilled track</td></tr><tr><td><strong>Range slider active background</strong></td><td>The filled part of the track</td></tr></tbody></table>

## Choices

Covers dropdowns, checkboxes, and radio buttons.

<table><thead><tr><th width="290">Setting</th><th>Colours</th></tr></thead><tbody><tr><td><strong>Dropdown text</strong></td><td>Text in a dropdown</td></tr><tr><td><strong>Dropdown border</strong></td><td>Its outline</td></tr><tr><td><strong>Dropdown background</strong></td><td>Inside it</td></tr><tr><td><strong>Dropdown selected</strong></td><td>The highlight on the chosen entry</td></tr><tr><td><strong>Checkbox &amp; Radio text</strong></td><td>Their labels at rest</td></tr><tr><td><strong>Checkbox &amp; Radio text hover</strong></td><td>On hover</td></tr><tr><td><strong>Checkbox &amp; Radio text active</strong></td><td>When selected</td></tr><tr><td><strong>Checkbox &amp; Radio hover</strong></td><td>The control on hover</td></tr><tr><td><strong>Checkbox &amp; Radio active</strong></td><td>The control when selected</td></tr></tbody></table>

## Swatches

Covers buttons, colour swatches, and image swatches.

<table><thead><tr><th width="290">Setting</th><th>Colours</th></tr></thead><tbody><tr><td><strong>Button text</strong> / <strong>hover</strong> / <strong>active</strong></td><td>Button labels in each state</td></tr><tr><td><strong>Button background</strong> / <strong>hover</strong> / <strong>active</strong></td><td>Button fills in each state</td></tr><tr><td><strong>Swatch border</strong></td><td>A swatch at rest</td></tr><tr><td><strong>Swatch border hover</strong></td><td>On hover</td></tr><tr><td><strong>Swatch border active</strong></td><td>When selected</td></tr></tbody></table>

{% hint style="info" %}
**Swatch border active** is the most important colour in this group. It is how a shopper knows which swatch they picked. Make it clearly different from the resting state — a subtle change reads as no change at all, especially on a phone.
{% endhint %}

## Tabs

For the [Tabs](../option-types/static-types/tabs.md) option type.

<table><thead><tr><th width="290">Setting</th><th>Colours</th></tr></thead><tbody><tr><td><strong>Tab title</strong></td><td>Inactive tab titles</td></tr><tr><td><strong>Tab title active</strong></td><td>The open tab's title</td></tr><tr><td><strong>Tab title hover</strong></td><td>On hover</td></tr><tr><td><strong>Tab content</strong></td><td>The text inside a panel</td></tr><tr><td><strong>Tab border</strong></td><td>The lines around and between tabs</td></tr></tbody></table>

## Group

For [Section](../option-types/static-types/section.md) headings.

<table><thead><tr><th width="290">Setting</th><th>Colours</th></tr></thead><tbody><tr><td><strong>Group label</strong></td><td>The section heading text</td></tr><tr><td><strong>Group icon</strong></td><td>The section's prefix icon</td></tr><tr><td><strong>Group chevron</strong></td><td>The open and close arrow on a collapsible section</td></tr></tbody></table>

## Getting a widget that matches

{% stepper %}
{% step %}
### Try Match theme style first

It sets most of this at once on a supported theme. See [Match your theme style](match-your-theme-style.md).
{% endstep %}

{% step %}
### Copy exact values from your theme's settings

Do not eyeball colours. Open your theme's own colour settings and copy the values, so they match precisely rather than nearly.
{% endstep %}

{% step %}
### Set the three states for anything interactive

Buttons and swatches have rest, hover, and active states. Leaving one at its default is the most common cause of a widget that looks almost right.
{% endstep %}

{% step %}
### Check contrast

Especially label text against the app background, and the required marker against everything. A required marker nobody can see is worse than none.
{% endstep %}

{% step %}
### Check on a real product page and on a phone

Use **View in Store**. The builder preview does not use your theme's styling.
{% endstep %}
{% endstepper %}

## Notes

* Store-wide. There is no per-option-set colour scheme — use an [HTML class](../option-types/shared-settings/direction-width-and-css.md#html-class) and [custom CSS](custom-css.md) for that.
* These settings work alongside **Match theme style**, so you can use the switch as a base and adjust individual colours from there.
* Colours apply to the storefront widget. The builder preview uses the app's own styling.
