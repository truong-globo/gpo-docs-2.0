---
description: Where the widget appears on your storefront, how it looks, and how it behaves.
icon: store
---

# Overview

Your option sets decide *what* you ask. This section decides *where it appears* and *what it looks like* — all of it store-wide, in **Settings**.

## Pages in this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Widget placement</strong></td><td>The eight positions, and the CSS-selector options for anything else.</td><td><a href="widget-placement.md">widget-placement.md</a></td></tr><tr><td><strong>Match your theme style</strong></td><td>Let the widget inherit your theme's look automatically, on supported themes.</td><td><a href="match-your-theme-style.md">match-your-theme-style.md</a></td></tr><tr><td><strong>Colors</strong></td><td>Every colour setting, grouped as the app groups them.</td><td><a href="colors.md">colors.md</a></td></tr><tr><td><strong>Borders and typography</strong></td><td>Border weight and radius, and the four text styles.</td><td><a href="borders-and-typography.md">borders-and-typography.md</a></td></tr><tr><td><strong>Custom CSS</strong></td><td>For anything the settings do not reach.</td><td><a href="custom-css.md">custom-css.md</a></td></tr><tr><td><strong>Widget behavior</strong></td><td>Alignment, tooltips, selected values, and limiting the widget's height.</td><td><a href="widget-behavior.md">widget-behavior.md</a></td></tr><tr><td><strong>Quickview and other pages</strong></td><td>Collection quickviews, home pages, and regular pages.</td><td><a href="quickview-and-other-pages.md">quickview-and-other-pages.md</a></td></tr><tr><td><strong>Cart page</strong></td><td>Add-on lines, editing options, and design previews.</td><td><a href="cart-page.md">cart-page.md</a></td></tr><tr><td><strong>Ajax cart and redirect to cart</strong></td><td>What happens after Add to cart.</td><td><a href="ajax-cart-and-redirect.md">ajax-cart-and-redirect.md</a></td></tr><tr><td><strong>Show options on orders</strong></td><td>Option details on the cart, checkout, orders, invoices, packing slips, and emails.</td><td><a href="show-options-on-orders.md">show-options-on-orders.md</a></td></tr></tbody></table>

## The quickest path to a widget that looks right

{% stepper %}
{% step %}
### Turn on Match theme style

**Settings** > **Design** > **Theme style**. On a supported theme this does most of the work in one switch. See [Match your theme style](match-your-theme-style.md).
{% endstep %}

{% step %}
### Fix anything it did not cover

Colours, borders, and typography, in the same **Design** tab.
{% endstep %}

{% step %}
### Check the placement

**Settings** > **General** > **Widget Settings**. New stores start with the widget above the **Add to cart** button. See [Widget placement](widget-placement.md).
{% endstep %}

{% step %}
### Look at a real product page

With **View in Store** from the builder. The builder preview uses the app's own styling, so it is not a fair comparison.
{% endstep %}

{% step %}
### Check it on a phone

Where most of your shoppers are.
{% endstep %}
{% endstepper %}

## Everything here is store-wide

There is no per-option-set styling or placement. One widget position, one colour scheme, one set of fonts, for every option set in the store.

If you genuinely need one option set to look different, the route is an [HTML class](../option-types/shared-settings/direction-width-and-css.md#html-class) on its options plus [custom CSS](custom-css.md).

## Next steps

* [Widget placement](widget-placement.md)
* [Match your theme style](match-your-theme-style.md)
* [Settings overview](../settings/README.md)
