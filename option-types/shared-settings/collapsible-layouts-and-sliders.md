---
description: >-
  Enable custom layout, Layout type, scrolling, and the slider settings — how to
  fit a long list of choices into a small space.
icon: layer-group
---

# Collapsible layouts and sliders

A row of six colour swatches is fine. Sixty swatches pushes your **Add to cart** button off the screen. These settings are the answer: collapse the list, give it its own scrollbar, or turn it into a slider.

All of them live on **Advanced Settings** and all of them are hidden until you turn on **Enable custom layout**.

## Enable custom layout

The switch that unlocks everything else on this page.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td>Off — the option renders as a plain list</td></tr><tr><th>Available on</th><td>Checkbox, Radio button, Button, Color swatch, Image swatch</td></tr></thead></table>

With it off, the option lists every value in the normal way. With it on, you choose a **Layout type** and its related settings appear.

## Layout type

How the list is presented.

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Expand</strong></td></tr><tr><th>Available on</th><td>Checkbox and Radio button offer <strong>Expand</strong> and <strong>Collapse</strong>. Button, Color swatch, and Image swatch also offer <strong>Slider</strong></td></tr></thead></table>

<table><thead><tr><th width="180">Choice</th><th>Behaviour</th><th>Use when</th></tr></thead><tbody><tr><td><strong>Expand</strong></td><td>A collapsible group that starts open. The shopper can fold it away.</td><td>The choice matters to most shoppers, but you want them able to tidy it up.</td></tr><tr><td><strong>Collapse</strong></td><td>A collapsible group that starts closed. The shopper opens it if they want it.</td><td>An optional or advanced choice most shoppers skip.</td></tr><tr><td><strong>Slider</strong></td><td>A horizontal carousel showing a few values at a time.</td><td>Many visual choices — colour or image swatches — where scrolling a grid feels clumsy.</td></tr></tbody></table>

{% hint style="warning" %}
**Collapse** hides the choice behind a click. Never use it for a **required** option, or for a choice that changes the price — shoppers do not open things they cannot see the point of, and then they hit a validation error they do not understand.
{% endhint %}

## Scrolling

With **Expand** or **Collapse** selected, you can also give the list its own scroll area so it never grows beyond a set size.

### Scroll type

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Default</strong></td></tr><tr><th>Available on</th><td>Checkbox, Radio button, Button, Color swatch, Image swatch — with <strong>Expand</strong> or <strong>Collapse</strong> selected</td></tr></thead></table>

<table><thead><tr><th width="290">Choice</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>No scroll area. The list is as tall as it needs to be.</td></tr><tr><td><strong>By fixed height</strong></td><td>The list gets a fixed height in pixels and scrolls inside it. Reveals <strong>Scroll height</strong>.</td></tr><tr><td><strong>By number of option values</strong></td><td>The list shows a set number of values and scrolls for the rest. Reveals <strong>Number of option values</strong>.</td></tr></tbody></table>

### Scroll height

A height in pixels, shown only when **Scroll type** is **By fixed height**. Everything past that height scrolls.

Use this when your page design needs a predictable height — for example when the option sits next to something else of a known size.

### Number of option values

How many values to show before scrolling, shown only when **Scroll type** is **By number of option values**.

This is usually the better of the two, because it does not depend on your theme's font size or swatch dimensions. "Show six and scroll the rest" behaves the same on every device; "scroll after 240 pixels" does not.

<table><thead><tr><th width="290">Situation</th><th>Setting</th></tr></thead><tbody><tr><td>Forty colour names in a checkbox list</td><td><strong>By number of option values</strong>, showing 8</td></tr><tr><td>A fixed-height sidebar layout</td><td><strong>By fixed height</strong></td></tr><tr><td>Twelve values that fit fine</td><td><strong>Default</strong> — do not add a scrollbar you do not need</td></tr></tbody></table>

## Slider settings

With **Layout type** set to **Slider**, five more settings appear. Slider layout is available on **Button**, **Color swatch**, and **Image swatch**, and is plan-gated — see [Compare plans](../../plans/compare-plans.md).

<table><thead><tr><th width="250">Setting</th><th width="130">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Number of rows</strong></td><td><code>1</code></td><td>How many rows of swatches are visible at once. Two rows suit a grid of small colour chips; one row suits larger images.</td></tr><tr><td><strong>Swatches per row</strong></td><td><code>3</code></td><td>How many swatches fit in a row. Whole numbers show whole swatches; a decimal deliberately shows a partial swatch at the edge, which hints that there is more to scroll.</td></tr><tr><td><strong>Show navigation arrows</strong></td><td><strong>Hide</strong></td><td>Previous and next arrows on the sides of the slider.</td></tr><tr><td><strong>Show indicators</strong></td><td><strong>Hide</strong></td><td>Small dots under the slider showing how many swatches there are; selecting one jumps to it.</td></tr><tr><td><strong>Slider style</strong></td><td><strong>Style 1</strong></td><td>One of five arrow designs. Only appears once <strong>Show navigation arrows</strong> is set to <strong>Show</strong>.</td></tr></tbody></table>

{% hint style="info" %}
Turn on at least one of **Show navigation arrows** or **Show indicators**. With both hidden, a desktop shopper has no visual cue that the list scrolls and may never see the other swatches. On touch devices swiping is discoverable; with a mouse it is not.
{% endhint %}

**A configuration that works**

<table><thead><tr><th width="270">Setting</th><th>Value</th></tr></thead><tbody><tr><td><strong>Enable custom layout</strong></td><td>On</td></tr><tr><td><strong>Layout type</strong></td><td><strong>Slider</strong></td></tr><tr><td><strong>Number of rows</strong></td><td><code>2</code></td></tr><tr><td><strong>Swatches per row</strong></td><td><code>4.5</code></td></tr><tr><td><strong>Show navigation arrows</strong></td><td><strong>Show</strong></td></tr><tr><td><strong>Show indicators</strong></td><td><strong>Hide</strong></td></tr><tr><td><strong>Swatch image width / height</strong></td><td><code>60</code> / <code>60</code></td></tr></tbody></table>

Two rows of about four and a half swatches shows sixteen or so choices in the space of one, and the half swatch at the edge tells the shopper there is more.

<!-- SCREENSHOT: type-shared-slider-settings | App admin → builder → option Image swatch → Advanced Settings | Enable custom layout bật, Layout type = Slider, các setting Number of rows / Swatches per row / arrows / indicators / Slider style | Khoanh nhóm slider -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The slider settings on an Image swatch option with rows, swatches per row, arrows, and style"><figcaption><p>Slider settings only appear once Layout type is set to Slider.</p></figcaption></figure>

<!-- SCREENSHOT: type-shared-slider-storefront | Storefront → trang sản phẩm | Image swatch dạng slider 2 hàng, có arrow, thấy 1 swatch bị cắt ở mép | Khoanh vùng slider -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An image swatch slider on the storefront with two rows, navigation arrows, and a partially visible swatch at the edge"><figcaption><p>A partial swatch at the edge is the clearest signal that the list continues.</p></figcaption></figure>

## Which approach for which problem

<table><thead><tr><th width="290">Problem</th><th>Answer</th></tr></thead><tbody><tr><td>Too many text choices, page too long</td><td><strong>Collapse</strong>, or <strong>Expand</strong> with <strong>By number of option values</strong></td></tr><tr><td>Too many visual swatches</td><td><strong>Slider</strong> with two rows</td></tr><tr><td>An advanced option most shoppers skip</td><td><strong>Collapse</strong></td></tr><tr><td>Shoppers need to search rather than scroll</td><td>A <a href="../selection-types/dropdown.md">Dropdown</a> with <a href="selection-behaviour.md#search-suggestion">Search suggestion</a></td></tr><tr><td>Several groups of options crowding each other</td><td>A collapsible <a href="../static-types/section.md">Section</a> around each group</td></tr><tr><td>The whole widget is too tall</td><td><strong>Limit widget height</strong> in <strong>Settings &gt; Settings &gt; General</strong> — see <a href="../../storefront/widget-behavior.md">Widget behavior</a></td></tr></tbody></table>
