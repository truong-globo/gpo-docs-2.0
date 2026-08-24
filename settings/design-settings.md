---
description: The five groups on the Design section, and where each one is explained in depth.
icon: palette
---

# Design settings

**Settings** > **Settings** > **Design**. Everything about how the widget looks, store-wide.

The individual settings are documented under [Storefront display and design](../storefront/README.md), organised by what you are trying to achieve. This page is the map.

## The five groups

<table><thead><tr><th width="230">Group</th><th width="290">Contains</th><th>Explained in</th></tr></thead><tbody><tr><td><strong>Theme style</strong></td><td><strong>Match theme style</strong>, plus a link to the supported themes list</td><td><a href="../storefront/match-your-theme-style.md">Match your theme style</a></td></tr><tr><td><strong>Color</strong></td><td>Around forty colour settings in six sub-groups: General, Inputs, Choices, Swatches, Tabs, Group</td><td><a href="../storefront/colors.md">Colors</a></td></tr><tr><td><strong>Border</strong></td><td>Size and radius for Input, Dropdown, and Swatch</td><td><a href="../storefront/borders-and-typography.md">Borders and typography</a></td></tr><tr><td><strong>Typography</strong></td><td>Four text styles, each with font, variant, and size</td><td><a href="../storefront/borders-and-typography.md">Borders and typography</a></td></tr><tr><td><strong>Additional</strong></td><td><strong>Custom CSS for the widget</strong></td><td><a href="../storefront/custom-css.md">Custom CSS</a></td></tr></tbody></table>

## The order to work in

{% stepper %}
{% step %}
### Turn on Match theme style

If your theme is supported, this does most of the work at once. See [Match your theme style](../storefront/match-your-theme-style.md).
{% endstep %}

{% step %}
### Fix the colours that are still wrong

Copy exact values from your theme's own settings rather than estimating. Set all three states — rest, hover, active — on anything interactive.
{% endstep %}

{% step %}
### Match the border radius

The setting that most often gives a widget away as an add-on.
{% endstep %}

{% step %}
### Match the fonts

Your theme's fonts, not similar ones.
{% endstep %}

{% step %}
### Add custom CSS only for what is left

See [Custom CSS](../storefront/custom-css.md).
{% endstep %}

{% step %}
### Check on a real product page and on a phone

Use **View in Store**. The builder preview always uses the app's own styling, so it is not a fair comparison.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
The builder's preview panel never reflects these settings. That is by design — it is a functional preview, not a visual one. Always judge the design on a real product page.
{% endhint %}

## Notes

* Store-wide. There is no per-option-set design.
* **Match theme style** and the manual settings work together: use the switch as a base and adjust individual values from there.
* The Personalizer's own colours and fonts are set per layer, separately from these. See [Text layers](../personalizer/layer-settings/text-layers.md) and [Fonts](../personalizer/layer-settings/fonts.md).
* Custom fonts must be uploaded in **General** before they can be selected here. See [Custom fonts](custom-fonts.md).
