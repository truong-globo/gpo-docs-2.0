---
description: One switch that makes the widget inherit your theme's fonts, colours, and control styling — on the themes it supports.
icon: wand-sparkles
---

# Match your theme style

**Match theme style** makes the widget adopt your theme's own appearance instead of the app's default styling. On a supported theme it does in one switch what would otherwise take a long session with the colour and typography settings.

## Where it is

**Settings** > **Settings** > **Design** > **Theme style** > **Match theme style**.

Next to it is a link to the list of supported themes, which is the same list as below.

<!-- SCREENSHOT: store-match-theme | App admin → Settings → Design → Theme style | Switch Match theme style và tip banner có link View supported themes | Khoanh switch -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Match theme style switch with its supported themes link"><figcaption><p>One switch, and a link to check whether your theme is covered.</p></figcaption></figure>

## Supported themes

The app carries styling for these themes. Support is per theme **and per theme version**, and the app picks the closest version it has to the one you are running.

<table><thead><tr><th width="230">Theme</th><th width="230">Theme</th><th>Theme</th></tr></thead><tbody><tr><td>Dawn</td><td>Refresh</td><td>Pitch</td></tr><tr><td>Sense</td><td>Origin</td><td>Atelier</td></tr><tr><td>Crave</td><td>Publisher</td><td>Fabric</td></tr><tr><td>Craft</td><td>Spotlight</td><td>Dwell</td></tr><tr><td>Studio</td><td>Colorblock</td><td>Ritual</td></tr><tr><td>Taste</td><td>Ride</td><td>Savor</td></tr><tr><td>Trade</td><td>Prestige</td><td>Tinker</td></tr><tr><td>Rise</td><td>Impulse</td><td>Vessel</td></tr><tr><td>Concept</td><td>Be Yours</td><td>Hyper</td></tr><tr><td>Horizon</td><td>Eurus</td><td>Wonder</td></tr></tbody></table>

Plus one further theme not named in this list. If yours is not here, see [If your theme is not supported](#if-your-theme-is-not-supported) below.

{% hint style="info" %}
The list grows. The **View supported themes** link beside the setting is always current — check there rather than relying on this page if your theme is missing.
{% endhint %}

## What it does

With the switch on, the widget takes its cues from your theme rather than from the app's defaults: input and button styling, control shapes, typography, and the general feel of form elements.

The result is a widget that reads as part of the page rather than as an app bolted on.

## What it does not do

<table><thead><tr><th width="290">Not covered</th><th>Where to handle it</th></tr></thead><tbody><tr><td>Where the widget sits on the page</td><td><a href="widget-placement.md">Widget placement</a></td></tr><tr><td>Behaviour — tooltips, height limits, selected values</td><td><a href="widget-behavior.md">Widget behavior</a></td></tr><tr><td>Anything specific to your own customisations of the theme</td><td><a href="custom-css.md">Custom CSS</a></td></tr><tr><td>The builder's preview panel</td><td>Nothing — the preview always uses the app's own styling. Compare with <strong>View in Store</strong></td></tr></tbody></table>

## Steps

{% stepper %}
{% step %}
### Turn on Match theme style

**Settings** > **Settings** > **Design** > **Theme style**.
{% endstep %}

{% step %}
### Save
{% endstep %}

{% step %}
### Look at a real product page

Use **View in Store** from the builder. The builder preview will not show the change — it never uses your theme's styling.
{% endstep %}

{% step %}
### Fix what is left

Anything that still looks wrong can be adjusted with the [colour](colors.md), [border, and typography](borders-and-typography.md) settings, which continue to work alongside this.
{% endstep %}

{% step %}
### Check on a phone

And after any theme update.
{% endstep %}
{% endstepper %}

## If your theme is not supported

Turning the switch on does no harm — the widget simply keeps the app's own styling. Style it by hand instead:

{% stepper %}
{% step %}
### Match your fonts

**Settings** > **Design** > **Typography**. Set the four text styles to your theme's fonts and sizes. See [Borders and typography](borders-and-typography.md).
{% endstep %}

{% step %}
### Match your colours

**Settings** > **Design** > **Color**. Take the values from your theme's own settings so they match exactly rather than approximately. See [Colors](colors.md).
{% endstep %}

{% step %}
### Match your border weight and radius

Also in **Design**. Rounded controls in a square theme are the most noticeable mismatch.
{% endstep %}

{% step %}
### Fill any gaps with custom CSS

See [Custom CSS](custom-css.md).
{% endstep %}

{% step %}
### Or ask us

Theme styling is something we do regularly. See [Contact support](../help/contact-support.md).
{% endstep %}
{% endstepper %}

## Notes

* Store-wide, like everything in **Design**.
* Support is per theme version, and the app uses the nearest version it has. A very old or very new version of a supported theme may match less exactly.
* A heavily customised copy of a supported theme may not match, because the customisations are yours rather than the theme's.
* Colour, border, and typography settings still apply, so you can use this as a base and adjust from there.

## Troubleshooting

<details>
<summary>Nothing changed after turning it on</summary>

Three possibilities: your theme is not on the list; you are looking at the builder preview rather than a real product page; or the settings were not saved.
</details>

<details>
<summary>It changed, but not enough</summary>

Expected on a customised theme. Use the colour, border, and typography settings to close the remaining gap.
</details>

<details>
<summary>It looks worse than before</summary>

Turn it off. It is a single switch with no side effects, and the manual settings are a perfectly good route.
</details>

<details>
<summary>My theme is not on the list</summary>

Check the **View supported themes** link, which is more current than this page. Then style manually, or contact us.
</details>

<details>
<summary>It stopped matching after a theme update</summary>

Support is per version. A new theme version may not be covered yet — tell us which theme and version.
</details>

<details>
<summary>The builder preview still looks like the app</summary>

It always will. The preview uses the app's own styling by design.
</details>

## Next steps

* [Colors](colors.md)
* [Borders and typography](borders-and-typography.md)
* [Custom CSS](custom-css.md)
