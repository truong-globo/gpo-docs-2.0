---
description: Where the widget appears on your storefront, how it looks, and how it behaves.
icon: store
---

# Overview

Your option sets define _what_ you ask. The settings in this section define _where the widget appears_ and _what it looks like_. All of them are store-wide, in **Settings**.

## Pages in this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Widget placement</strong></td><td>The eight positions, and the CSS-selector options for anything else.</td><td><a href="widget-placement.md">widget-placement.md</a></td></tr><tr><td><strong>Match your theme style</strong></td><td>Let the widget inherit your theme's look automatically, on supported themes.</td><td><a href="match-your-theme-style.md">match-your-theme-style.md</a></td></tr><tr><td><strong>Colors</strong></td><td>Every color setting, grouped as the app groups them.</td><td><a href="colors.md">colors.md</a></td></tr><tr><td><strong>Borders and typography</strong></td><td>Border weight and radius, and the four text styles.</td><td><a href="borders-and-typography.md">borders-and-typography.md</a></td></tr><tr><td><strong>Custom CSS</strong></td><td>Style the parts the design settings do not cover.</td><td><a href="custom-css.md">custom-css.md</a></td></tr><tr><td><strong>Widget behavior</strong></td><td>Alignment, tooltips, selected values, and limiting the widget's height.</td><td><a href="widget-behavior.md">widget-behavior.md</a></td></tr><tr><td><strong>Quickview and other pages</strong></td><td>Collection quickviews, home pages, and regular pages.</td><td><a href="/broken/pages/z3MOr9S1i9k8wdOYumws">Broken link</a></td></tr><tr><td><strong>Cart page</strong></td><td>Add-on lines, editing options, and design previews.</td><td><a href="cart-page.md">cart-page.md</a></td></tr><tr><td><strong>Ajax cart and redirect to cart</strong></td><td>What happens after Add to cart.</td><td><a href="ajax-cart-and-redirect.md">ajax-cart-and-redirect.md</a></td></tr><tr><td><strong>Show options on orders</strong></td><td>Option details on the cart, checkout, orders, invoices, packing slips, and emails.</td><td><a href="show-options-on-orders.md">show-options-on-orders.md</a></td></tr></tbody></table>

## Setting up the widget's appearance

{% stepper %}
{% step %}
### Turn on Match theme style

**Settings** > **Design** > **Theme style**. On a supported theme, this sets most of the appearance at once. See [Match your theme style](match-your-theme-style.md).
{% endstep %}

{% step %}
### Adjust anything it did not cover

Set colors, borders, and typography in the same **Design** tab.
{% endstep %}

{% step %}
### Check the placement

**Settings** > **General** > **Widget Settings**. By default, the widget is above the **Add to cart** button. See [Widget placement](widget-placement.md).
{% endstep %}

{% step %}
### Check a real product page

Use **View in Store** from the builder. The builder preview uses the app's own styling, so it does not reflect your theme.
{% endstep %}

{% step %}
### Check it on a phone

Most customers shop on a phone, so check the widget there as well.
{% endstep %}
{% endstepper %}

## Everything here is store-wide

There is no per-option-set styling or placement. Every option set in the store uses the same position, color scheme, and fonts.

To make one option set look different, add an [HTML class](../option-types/shared-settings/direction-width-and-css.md#html-class) to its options and target that class with [custom CSS](custom-css.md).
