---
description: Live preview problems — nothing drawn, wrong position, wrong font, or unusable customer designs.
icon: wand-magic-sparkles
---

# Personalizer problems

The Personalizer has its own detailed troubleshooting page, organised by symptom:

**→ [Troubleshooting personalizer](../personalizer/troubleshooting.md)**

## The four-point check

Before reading further, check these:

<table><thead><tr><th width="60">#</th><th width="290">Check</th><th>Where</th></tr></thead><tbody><tr><td>1</td><td>A background is configured for the option set</td><td><strong>Change background</strong> in the builder's preview panel</td></tr><tr><td>2</td><td><strong>Enable personalize</strong> is on for the option</td><td>The option's <strong>Personalizer Settings</strong> tab</td></tr><tr><td>3</td><td>There is something to draw — a default value, or an uploaded file</td><td><strong>Basic Settings</strong></td></tr><tr><td>4</td><td>The Personalizer is in your plan</td><td><a href="../plans/compare-plans.md">Compare plans</a></td></tr></tbody></table>

Those four cover most cases of "nothing is happening".

## The most common causes

<table><thead><tr><th width="290">Symptom</th><th>Usual cause</th></tr></thead><tbody><tr><td>Nothing drawn on the product photo</td><td>No background configured, or a text layer with no default value</td></tr><tr><td>The layer is in the wrong place</td><td>The background was changed after positioning, or your product photographs are framed inconsistently</td></tr><tr><td>Personalisation on the wrong product image</td><td><strong>Apply to</strong> is set to <strong>All product images</strong>. Choose a single image</td></tr><tr><td>Long text runs off the product</td><td><a href="../personalizer/curve-and-auto-fit.md#auto-fit-max-width">Auto-fit max width</a> is off, and no character limit is set</td></tr><tr><td>The wrong font</td><td>A custom font is not uploaded, or custom fonts are not in your plan</td></tr><tr><td>An uploaded image is squashed</td><td><strong>Background mode</strong> is on <strong>Stretch</strong>. Use <strong>Cover</strong></td></tr><tr><td>Customers place designs where you cannot print</td><td>No <a href="../personalizer/clip-area.md">clip area</a>, with customer controls enabled</td></tr><tr><td>Designs arrive rotated and unproducible</td><td><strong>Rotate</strong> is enabled under <strong>Allow customers to</strong>. Turn it off</td></tr></tbody></table>

## Two rules worth remembering

{% hint style="warning" %}
**Set the background first.** Layer positions are relative to it, so changing the background moves everything. Doing it in the wrong order means positioning every layer twice.
{% endhint %}

{% hint style="warning" %}
**Any customer control needs a clip area.** If shoppers can drag, resize, or rotate a layer, a [clip area](../personalizer/clip-area.md) is what stops them placing it somewhere you cannot produce. Without one, the preview will happily show — and they will happily order — something you cannot make.
{% endhint %}

## Next steps

* [Troubleshooting personalizer](../personalizer/troubleshooting.md) — the full list by symptom.
* [Set the preview background](../personalizer/set-the-background.md)
* [Walkthrough: custom printed mug](../personalizer/walkthrough-custom-mug.md)
