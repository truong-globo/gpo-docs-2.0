---
description: The five groups on the Design section, and where each one is explained in depth.
icon: palette
---

# Design settings

**Settings** > **Settings** > **Design** contains every setting that controls how the widget looks. All of them are store-wide.

The individual settings are documented under [Storefront display and design](../storefront/README.md). This page lists the groups and links to each one.

## The five groups

<table><thead><tr><th width="230">Group</th><th width="290">Contains</th><th>Explained in</th></tr></thead><tbody><tr><td><strong>Theme style</strong></td><td><strong>Match theme style</strong>, plus a link to the supported themes list</td><td><a href="../storefront/match-your-theme-style.md">Match your theme style</a></td></tr><tr><td><strong>Color</strong></td><td>Around forty color settings in six sub-groups: General, Inputs, Choices, Swatches, Tabs, Group</td><td><a href="../storefront/colors.md">Colors</a></td></tr><tr><td><strong>Border</strong></td><td>Size and radius for Input, Dropdown, and Swatch</td><td><a href="../storefront/borders-and-typography.md">Borders and typography</a></td></tr><tr><td><strong>Typography</strong></td><td>Four text styles, each with font, variant, and size</td><td><a href="../storefront/borders-and-typography.md">Borders and typography</a></td></tr><tr><td><strong>Additional</strong></td><td><strong>Custom CSS for the widget</strong></td><td><a href="../storefront/custom-css.md">Custom CSS</a></td></tr></tbody></table>

## The order to set them in

{% stepper %}
{% step %}
### Turn on Match theme style

If your theme is supported, this sets most of the appearance at once. See [Match your theme style](../storefront/match-your-theme-style.md).
{% endstep %}

{% step %}
### Adjust the remaining colors

Copy the values from your theme's own settings rather than selecting similar colors. Set all three states, rest, hover, and active, on anything interactive.
{% endstep %}

{% step %}
### Match the border radius

This is the setting that most often makes the widget look separate from the page.
{% endstep %}

{% step %}
### Match the fonts

Use your theme's fonts rather than similar ones.
{% endstep %}

{% step %}
### Add custom CSS for anything left

See [Custom CSS](../storefront/custom-css.md).
{% endstep %}

{% step %}
### Check a real product page and a phone

Use **View in Store**. The builder preview always uses the app's own styling, so it does not reflect your theme.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
The builder's preview panel does not reflect these settings. It is a functional preview rather than a visual one, so check the design on a real product page.
{% endhint %}

## Notes

* These settings are store-wide. There is no per-option-set design.
* **Match theme style** and the manual settings work together, so you can turn on the setting and then adjust individual values.
* The Personalizer's own colors and fonts are set per layer, separately from these. See [Text layers](../personalizer/layer-settings/text-layers.md) and [Fonts](../personalizer/layer-settings/fonts.md).
* Custom fonts have to be uploaded in **General** before you can select them here. See [Custom fonts](custom-fonts.md).
