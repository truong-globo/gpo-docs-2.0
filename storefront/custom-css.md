---
description: Style the widget yourself when the settings do not reach far enough.
icon: code
---

# Custom CSS

**Settings** > **Settings** > **Design** > **Additional** > **Custom CSS for the widget**. A code editor whose contents are applied to the widget on your storefront.

## Try the settings first

Most requests that reach for CSS have a setting, and a setting will keep working when your theme changes.

<table><thead><tr><th width="330">You want</th><th>Setting</th></tr></thead><tbody><tr><td>The widget to look like your theme</td><td><a href="match-your-theme-style.md">Match theme style</a></td></tr><tr><td>Different colours</td><td><a href="colors.md">Colors</a></td></tr><tr><td>Different fonts or sizes</td><td><a href="borders-and-typography.md">Borders and typography</a></td></tr><tr><td>Rounder or squarer controls</td><td>Border radius, same page</td></tr><tr><td>Fields side by side</td><td><a href="../option-types/shared-settings/direction-width-and-css.md#column-width">Column width</a></td></tr><tr><td>A shorter widget</td><td><a href="widget-behavior.md">Limit widget height</a></td></tr><tr><td>Options grouped or collapsible</td><td><a href="../option-types/static-types/section.md">Section</a></td></tr></tbody></table>

Custom CSS is for what is genuinely left after those.

## Targeting one option

Global rules are risky. The safe pattern is a class on the specific option:

{% stepper %}
{% step %}
### Give the option an HTML class

On its **Advanced Settings**, in **HTML class**. Letters, numbers, hyphens, and underscores only, and no leading dot. See [HTML class](../option-types/shared-settings/direction-width-and-css.md#html-class).
{% endstep %}

{% step %}
### Write a rule against it

```css
.engraving-field label {
  font-weight: 600;
  letter-spacing: 0.04em;
}

.engraving-field input {
  text-align: center;
}
```
{% endstep %}

{% step %}
### Check on a real product page

Custom CSS applies to the storefront, not to the builder preview. Use **View in Store**.
{% endstep %}

{% step %}
### Check on a phone

Most CSS problems are layout problems, and most layout problems are mobile problems.
{% endstep %}
{% endstepper %}

## What it is genuinely good for

<table><thead><tr><th width="290">Use</th><th>Notes</th></tr></thead><tbody><tr><td>Emphasising one important option</td><td>A background, a border, more spacing</td></tr><tr><td>Hiding something in a context no setting covers</td><td>Use a class rather than a broad selector</td></tr><tr><td>Fine spacing adjustments</td><td>Where the design settings are too coarse</td></tr><tr><td>Matching a house style the settings cannot reach</td><td>Unusual label placement, custom control shapes</td></tr><tr><td>Excluding something on one page type</td><td>Combine with your theme's own body classes</td></tr></tbody></table>

## Writing it so it keeps working

<table><thead><tr><th width="290">Do</th><th>Avoid</th></tr></thead><tbody><tr><td>Target your own <strong>HTML class</strong> values</td><td>Targeting the app's internal class names, which can change</td></tr><tr><td>Keep rules short and specific</td><td>Broad selectors that catch more than you meant</td></tr><tr><td>Write down why each rule exists, in a comment</td><td>An unexplained block nobody dares delete</td></tr><tr><td>Test after every theme update</td><td>Assuming it still works</td></tr><tr><td>Use relative units and check mobile</td><td>Fixed pixel widths</td></tr></tbody></table>

{% hint style="warning" %}
Custom CSS is yours to maintain. It is not covered by **Match theme style**, it is not adjusted when the app changes, and it is the first thing to check when the widget looks wrong after an update. Keep it as small as you can.
{% endhint %}

## Notes

* Store-wide — one stylesheet for every option set.
* Applied to the widget on the storefront. The builder preview is unaffected.
* Your theme's own CSS also applies, and may be more specific than your rules.
* Nothing here changes what the options collect or how they behave.
* If you would rather not write CSS, styling is something support can help with. See [Contact support](../help/contact-support.md).

## Troubleshooting

<details>
<summary>My CSS has no effect</summary>

Four things: it is saved; you are looking at the storefront rather than the builder preview; the selector matches — check in your browser's inspector; and your theme's rules are not more specific.
</details>

<details>
<summary>It works on desktop but breaks the phone layout</summary>

Fixed widths are the usual cause. Use relative units, and add a media query if a rule should only apply on larger screens.
</details>

<details>
<summary>It stopped working after a theme update</summary>

Your theme's markup changed. Re-inspect and update the selectors. Rules targeting your own **HTML class** values are the most durable.
</details>

<details>
<summary>My rule affects more options than I intended</summary>

The selector is too broad. Add an HTML class to the specific option and target that.
</details>

<details>
<summary>"HTML class only accepts letters, numbers, hyphens and underscore"</summary>

That is the option's HTML class field, not the CSS editor. Remove the offending character — usually a leading dot.
</details>

## Next steps

* [HTML class](../option-types/shared-settings/direction-width-and-css.md#html-class)
* [Colors](colors.md) and [Borders and typography](borders-and-typography.md) — try these first.
* [Match your theme style](match-your-theme-style.md)
