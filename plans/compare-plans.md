---
description: How to read the plan comparison table, and what each feature group covers.
icon: table-list
---

# Compare plans

The comparison table lives on the **Pricing** page in the app, below the plan cards. It is the authoritative list for your store — this page explains how to read it.

{% hint style="info" %}
We do not reproduce the table here on purpose. Feature availability changes as plans evolve, and an out-of-date copy in documentation is worse than no copy. Open **Pricing** in the app for the current picture.
{% endhint %}

## How to read it

The table is grouped, and each row shows what every plan gives you for that feature. A row's value is one of:

<table><thead><tr><th width="230">Value</th><th>Means</th></tr></thead><tbody><tr><td>A tick</td><td>Included</td></tr><tr><td>Blank or a cross</td><td>Not included</td></tr><tr><td>A number</td><td>A limit — files, megabytes, option sets</td></tr><tr><td><strong>Unlimited</strong></td><td>No limit</td></tr><tr><td>A level, such as basic or advanced</td><td>The feature is included, at that level</td></tr></tbody></table>

Rows also carry a link to the documentation for that feature, so you can read what something is before deciding whether you need it.

## The groups

### Option Set

Counts and rules: how many option sets, how many options in each, and which product targeting methods you can use — manual, automatic, or all products. Plus duplicating, importing, and exporting, and the customer and country rules.

See [Assign to products](../option-sets/assign-to-products.md), [Assign to customers](../option-sets/assign-to-customers.md), and [Assign to countries](../option-sets/assign-to-countries.md).

### Option Config

The biggest group, and where most of the difference between plans sits:

<table><thead><tr><th width="290">Feature</th><th>Read about it in</th></tr></thead><tbody><tr><td>Conditional logic, at basic or advanced level</td><td><a href="../conditional-logic/README.md">Conditional logic</a>. Advanced is what adds <a href="../conditional-logic/conditions-on-shopify-variants.md">variant conditions</a></td></tr><tr><td>Price add-ons, and the advanced add-on modes</td><td><a href="../add-on-pricing/README.md">Add-on pricing</a></td></tr><tr><td>Multi-language option content</td><td><a href="../translations/translate-option-content.md">Translate option content</a></td></tr><tr><td>Default values, min and max limits, character limits</td><td><a href="../option-types/shared-settings/limits.md">Limits</a></td></tr><tr><td>Swatch sliders</td><td><a href="../option-types/shared-settings/collapsible-layouts-and-sliders.md">Collapsible layouts and sliders</a></td></tr><tr><td>Product personalize</td><td><a href="../personalizer/README.md">Product Personalizer</a></td></tr><tr><td>Option groups</td><td><a href="../option-types/static-types/section.md">Section</a></td></tr><tr><td>Out of stock options</td><td><a href="../option-types/shared-settings/out-of-stock-options.md">Out of stock options</a></td></tr><tr><td>Multiple file upload, and the file size limit</td><td><a href="../option-types/input-types/file-upload.md">File upload</a></td></tr><tr><td>Custom fonts</td><td><a href="../settings/custom-fonts.md">Custom fonts</a></td></tr><tr><td>Date restrictions, ranges, and calendar language</td><td><a href="../option-types/input-types/date-and-time-picker.md">Date and time picker</a></td></tr><tr><td>International phone validation</td><td><a href="../option-types/input-types/phone.md">Phone</a></td></tr></tbody></table>

### Option Type

One row per option type, so you can see exactly which of the 32 a plan gives you. See [Option types](../option-types/README.md).

### Features

Store-level capabilities: options in quickview, option templates, custom widget styling, editing options in the cart, Point of Sale, and analytics.

### Automations

The three workflow types. See [Automations](../automations/README.md).

### Support

Priority support, and removing the app's watermark from the widget.

## Working out which plan you need

Rather than comparing plans, list what you actually need and find the lowest plan that covers it.

{% stepper %}
{% step %}
### List your must-have option types

Look at what you need to ask customers. See [Choose the right option type](../option-types/choose-the-right-type.md).
{% endstep %}

{% step %}
### Decide whether you need to charge for options

If yes, you need add-on pricing — and if you sell in person, product-backed add-ons. See [Add-on pricing](../add-on-pricing/README.md).
{% endstep %}

{% step %}
### Decide whether you need conditional logic, and at which level

Variant-based conditions need the advanced level. See [Conditional logic](../conditional-logic/README.md).
{% endstep %}

{% step %}
### Decide whether you need the Personalizer

It is the single biggest feature in the app, and the one most likely to determine your plan. See [Product Personalizer](../personalizer/README.md).
{% endstep %}

{% step %}
### Add the operational needs

POS, automations, analytics, multi-language, import and export.
{% endstep %}

{% step %}
### Find the lowest plan that covers the list

Then start its 14-day trial and build the real thing before the trial ends. See [Change your plan](change-your-plan.md).
{% endstep %}
{% endstepper %}

## Notes

* Yearly and monthly billing include the same features. Only the price differs.
* Shopify Plus stores have their own pricing.
* Locked features are visible in the app with an upgrade prompt, so you can always see what you are missing.
* A trial gives you that plan's features in full, which is the best way to find out whether you need them.

## Next steps

* [Change your plan](change-your-plan.md)
* [What happens when you downgrade](what-happens-on-downgrade.md)
* [Plans and locked features](../concepts/plans-and-feature-gating.md)
