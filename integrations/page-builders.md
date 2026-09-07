---
description: >-
  Getting options onto product pages and landing pages built with a page
  builder.
icon: table-layout
---

# Page builders

A page builder replaces your theme's product template with its own layout. This changes where the app looks for the product form, so it sometimes needs to be told where to place the widget.

## Why this needs attention

Automatic placement works by finding your theme's product form and placing the widget relative to it. A page builder creates its own layout, which may not contain the elements the app expects, or may name them differently.

On a page built with a page builder, the widget can appear in the wrong place, or not appear at all.

## Three ways to fix it

{% stepper %}
{% step %}
### Try the app block first

Most builders support Shopify app blocks. If yours does, add the **Globo Product Options** block to the builder's layout and drag it where you want.

This is the most reliable method. There is no selector to maintain, and you can see the position while you edit. See [Add the app block](../getting-started/add-the-app-block.md).
{% endstep %}

{% step %}
### If the builder has an embed or HTML element, use a CSS selector

Add an element to the builder's layout where the options should appear, and give it an id. Then in **Settings** > **Settings** > **General**, set **Widget placement** to **At the start of an HTML element** and use that id as the selector.

Because you created the element, a builder update cannot rename it. See [Widget placement](../storefront/widget-placement.md).
{% endstep %}

{% step %}
### If neither works, contact support

Page builder integration is common support work. Include the name of the builder and a link to the page. See [Contact support](../help/contact-support.md).
{% endstep %}
{% endstepper %}

## What to test on a builder page

A builder page can display the options correctly and still fail at checkout, because the add-to-cart flow belongs to the builder rather than to your theme.

<table><thead><tr><th width="290">Test</th><th>Why</th></tr></thead><tbody><tr><td>The options appear, in the right place</td><td>The obvious one</td></tr><tr><td>Required options actually block add to cart</td><td>Validation has to hook into the builder's button</td></tr><tr><td>Add-ons appear in the cart at the right price</td><td>The builder's add-to-cart may take a different route</td></tr><tr><td>The <a href="../personalizer/">Personalizer</a> preview draws on the right image</td><td>Builders often use their own image gallery</td></tr><tr><td>Everything again on mobile</td><td>Builders frequently use a separate mobile layout</td></tr></tbody></table>

{% hint style="warning" %}
Test the add-to-cart flow, not just the appearance. A page where the options appear but validation does not run accepts orders with required fields empty, and nothing indicates that this has happened.
{% endhint %}

## Landing pages with a featured product

A landing page that shows one product is a simpler case. Set it up as a featured product:

* Add the app block inside the section showing the product
* Test again - if it doesn't work, contact support for further troubleshooting.

## Notes

* The app embed must be enabled on the theme, whatever the page is built with.
* Option sets still need to be **Active**, published to the **Online Store**, and matched by their product rule.
* A builder page that does not use a real Shopify product cannot display options, because there is no product to attach them to.
