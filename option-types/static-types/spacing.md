---
description: Vertical space between options, set in pixels.
icon: arrows-up-down
---

# Spacing

A gap that adds empty space between elements. Nothing is displayed; it simply creates room.

## What customers see

Nothing, which is the point. The options above and below it have more space between them.

## Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Height</strong></td><td>The gap in pixels. Starts at <code>10</code>.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide the space.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and width.</td></tr></tbody></table>

### How much

<table><thead><tr><th width="180">Height</th><th>Reads as</th></tr></thead><tbody><tr><td><code>8</code>–<code>12</code></td><td>A small breath between related fields</td></tr><tr><td><code>20</code>–<code>30</code></td><td>A clear break between groups</td></tr><tr><td><code>40</code>+</td><td>A deliberate pause — before a final confirmation, or above the add-to-cart area</td></tr></tbody></table>

## When to use it

* **Give an important field more room.** This helps it stand out instead of reading as just another item in the list.
* **Before a confirmation checkbox.** Extra space makes it less likely to be overlooked.
* **Balance spacing where a** [Divider](divider.md) **feels too heavy.**
* **Separate a group after a long list.** This keeps the groups from running together.

## When not to use it

* Instead of a [Section](section.md). If the fields belong together, group them properly.
* **As a stack of Spacing options.** Use one Spacing option with a larger height instead.
* To fix general widget spacing. Use [custom CSS](../../storefront/custom-css.md) so the spacing is applied consistently across the widget.

## Examples

**Room before a confirmation**

`30`px of spacing between the last engraving field and an "I confirm the spelling" switch.

**Separating two groups without a line**

`24`px between the personalisation fields and the delivery fields, where a divider would feel heavy.

**Space that only appears when needed**

Conditional logic matching the group below it, so you do not get an unexplained gap when that group is hidden.

## Notes

* Available on all plans.
* Works in Shopify POS.
* Collects nothing, so it never reaches the cart or order.
* Vertical only.
* Renders the same on desktop and mobile, so a large value that looks right on desktop can look like a mistake on a phone. Check the mobile preview.
