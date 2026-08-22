---
description: >-
  Which themes Match theme style has ready-made styling for, and what happens when
  yours is not one of them.
icon: paintbrush
---

# Supported themes

The app works on **any** Online Store 2.0 theme. This page is about something narrower: which themes [Match theme style](../storefront/match-your-theme-style.md) carries purpose-built styling for.

{% hint style="success" %}
**Your theme not being listed is not a problem.** It means the widget uses the app's own design settings instead of borrowing your theme's. Set your colours and typography in **Settings** > **Design** and it will still look right. See [If your theme is not listed](#if-your-theme-is-not-listed).
{% endhint %}

## The list

Support is per theme **and per theme version**. The version column shows the versions the app carries styling for.

<table><thead><tr><th width="290">Theme</th><th>Styled for version</th></tr></thead><tbody><tr><td>Atelier</td><td>4.1.3</td></tr><tr><td>Be Yours</td><td>9.2.0</td></tr><tr><td>Colorblock</td><td>15.5.0</td></tr><tr><td>Concept</td><td>6.0.1</td></tr><tr><td>Craft</td><td>15.5.0</td></tr><tr><td>Crave</td><td>15.5.0</td></tr><tr><td>Dawn</td><td>15.5.0, 15.4.1</td></tr><tr><td>Dwell</td><td>4.1.3</td></tr><tr><td>Eurus</td><td>10.2.0</td></tr><tr><td>Fabric</td><td>4.1.3</td></tr><tr><td>Horizon</td><td>4.1.3</td></tr><tr><td>Hyper</td><td>1.4.0</td></tr><tr><td>Impulse</td><td>9.2.0</td></tr><tr><td>Origin</td><td>15.5.0</td></tr><tr><td>Pitch</td><td>4.1.3</td></tr><tr><td>Prestige</td><td>11.4.0</td></tr><tr><td>Publisher</td><td>15.5.0</td></tr><tr><td>Refresh</td><td>15.5.0</td></tr><tr><td>Ride</td><td>15.5.0</td></tr><tr><td>Rise</td><td>15.5.0</td></tr><tr><td>Ritual</td><td>4.1.3</td></tr><tr><td>Savor</td><td>4.1.3</td></tr><tr><td>Sense</td><td>15.5.0</td></tr><tr><td>Spotlight</td><td>15.5.0</td></tr><tr><td>Studio</td><td>15.5.0</td></tr><tr><td>Taste</td><td>15.5.0</td></tr><tr><td>Tinker</td><td>4.1.3</td></tr><tr><td>Trade</td><td>15.5.0</td></tr><tr><td>Vessel</td><td>4.1.3</td></tr><tr><td>Wonder</td><td>2.4.1</td></tr></tbody></table>

Plus one further theme not named in this table.

{% hint style="info" %}
**Check the app, not this page.** The list grows with each release. The **View supported themes** link next to the **Match theme style** switch in **Settings** > **Design** is always current.
{% endhint %}

## How version matching works

You do not need to be on exactly the version listed.

{% stepper %}
{% step %}
### The app identifies your theme

From the theme itself, not from its name — so renaming your theme changes nothing.
{% endstep %}

{% step %}
### It looks for your exact version

If the app has styling for the version you are running, that is what is used.
{% endstep %}

{% step %}
### Otherwise it uses the nearest version it has

Running Dawn 15.3 with 15.4.1 and 15.5.0 available means 15.4.1 is used — the closest match. Theme versions rarely change form styling much between minor releases, so this is usually indistinguishable.
{% endstep %}

{% step %}
### If your theme is not in the list at all, nothing is loaded

The widget uses your **Settings** > **Design** values instead. No error, no broken layout.
{% endstep %}
{% endstepper %}

Finding your theme version: **Online Store** > **Themes** in Shopify admin, on your live theme.

## What "matched" actually covers

<table><thead><tr><th width="290">Matched</th><th>Not matched</th></tr></thead><tbody><tr><td>Input and select field styling</td><td>Where the widget sits — see <a href="../storefront/widget-placement.md">Widget placement</a></td></tr><tr><td>Button appearance</td><td>Behaviour such as tooltips and height limits — see <a href="../storefront/widget-behavior.md">Widget behavior</a></td></tr><tr><td>Control shapes, borders, and corner radius</td><td>Your own customisations of the theme — see <a href="../storefront/custom-css.md">Custom CSS</a></td></tr><tr><td>Typography and general form feel</td><td>The builder's preview panel, which always uses the app's own styling</td></tr></tbody></table>

## If your theme is not listed

In order of effort:

{% stepper %}
{% step %}
### Turn Match theme style on anyway

It costs nothing to try. Some themes are close enough to a listed one that the result is already good.
{% endstep %}

{% step %}
### Set your colours and fonts in Settings > Design

This is the real answer, and enough for most stores. Match your theme's button colour, text colour, border colour, and font family. See [Colors](../storefront/colors.md) and [Borders and typography](../storefront/borders-and-typography.md).
{% endstep %}

{% step %}
### Use Custom CSS for the last details

For anything the design settings do not reach — a specific border radius, a particular spacing. See [Custom CSS](../storefront/custom-css.md).
{% endstep %}

{% step %}
### Tell us which theme you are on

Themes are added on the basis of what merchants are actually using. Send the name and version. See [Contact support](../help/contact-support.md).
{% endstep %}
{% endstepper %}

## Themes that are not Online Store 2.0

The widget is built for Online Store 2.0, which covers every theme currently in Shopify's theme store and most sold elsewhere.

On an older theme:

<table><thead><tr><th width="290">Consequence</th><th>Detail</th></tr></thead><tbody><tr><td>No app block</td><td>The <a href="../getting-started/add-the-app-block.md">app block</a> needs a 2.0 template. Automatic placement is used instead</td></tr><tr><td>Placement may need adjusting</td><td>Older product templates give the app less to anchor to. Try the other <a href="../storefront/widget-placement.md">Widget placement</a> values</td></tr><tr><td>Match theme style will not apply</td><td>No older theme is in the list above</td></tr></tbody></table>

If your theme predates 2.0, upgrading is worth doing for reasons well beyond this app.

## Troubleshooting

<details>
<summary>Match theme style is on but nothing looks different</summary>

Either your theme is not in the list, or your theme is already close to the app's defaults. Check the list, then set your colours in **Settings** > **Design**.
</details>

<details>
<summary>It looks close but not exact</summary>

Your version is not one the app carries styling for, so the nearest is used, or you have customised the theme's own styling. Finish with [Custom CSS](../storefront/custom-css.md).
</details>

<details>
<summary>The builder preview looks different from my storefront</summary>

Expected. The preview always uses the app's own styling. Use **View in Store** to see the real thing.
</details>

<details>
<summary>It worked, then stopped after a theme update</summary>

The update moved you to a version the app does not carry styling for yet. Tell us the theme and the new version.
</details>

<details>
<summary>My theme is a copy of a supported theme with a different name</summary>

Matching is by the theme itself rather than its name, so a renamed copy is still recognised. A theme heavily rebuilt from a supported one may not be.
</details>

## Next steps

* [Match your theme style](../storefront/match-your-theme-style.md) — the setting itself.
* [Colors](../storefront/colors.md) and [Borders and typography](../storefront/borders-and-typography.md) — the manual route.
* [Custom CSS](../storefront/custom-css.md)
