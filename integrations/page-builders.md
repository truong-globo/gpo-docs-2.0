---
description: Getting options onto product pages and landing pages built with a page builder.
icon: table-layout
---

# Page builders

A page builder replaces your theme's product template with its own layout. That is fine — but it changes where the app has to look, and sometimes the app needs telling.

## Why it needs attention

Automatic placement works by finding your theme's product form and putting the widget in relation to it. A page builder builds its own layout, which may not include the elements the app expects, or may name them differently.

So on a builder-made page, the widget sometimes lands in an odd place, or does not appear at all.

## The three fixes, in order

{% stepper %}
{% step %}
### Try the app block first

Most builders support Shopify app blocks. If yours does, add the **Globo Product Options** block to the builder's layout and drag it where you want.

This is by far the most robust route: no selector to maintain, and the position is visible while you edit. See [Add the app block](../getting-started/add-the-app-block.md).
{% endstep %}

{% step %}
### If the builder has an embed or HTML element, use a CSS selector

Add an element to the builder's layout where the options should appear, give it an id you choose, then in **Settings** > **Settings** > **General** set **Widget placement** to **At the start of an HTML element** with that id as the selector.

That way the anchor is something *you* created, so a builder update cannot rename it. See [Widget placement](../storefront/widget-placement.md).
{% endstep %}

{% step %}
### If neither works, ask us

Builder integration is common support work. Tell us which builder and send the page. See [Contact support](../help/contact-support.md).
{% endstep %}
{% endstepper %}

## Things to test on a builder-made page

A builder page can render the options correctly and still break the purchase, because the add-to-cart flow is the builder's rather than the theme's.

<table><thead><tr><th width="290">Test</th><th>Why</th></tr></thead><tbody><tr><td>The options appear, in the right place</td><td>The obvious one</td></tr><tr><td>Required options actually block add to cart</td><td>Validation has to hook into the builder's button</td></tr><tr><td>Add-ons appear in the cart at the right price</td><td>The builder's add-to-cart may take a different route</td></tr><tr><td>The <a href="../personalizer/README.md">Personalizer</a> preview draws on the right image</td><td>Builders often use their own image gallery</td></tr><tr><td>Everything again on mobile</td><td>Builders frequently use a separate mobile layout</td></tr></tbody></table>

{% hint style="warning" %}
Test the add-to-cart flow, not just the appearance. A page where options render but validation does not fire will take orders with required fields empty — which is worse than options not appearing at all, because nobody notices.
{% endhint %}

## Landing pages with a featured product

A landing page showing one product is a different case, and simpler: it needs the featured-product treatment.

* Add the app block inside the section showing the product
* Turn on **Show widget on regular page** in **Settings** > **Settings** > **General**

See [Quickview and other pages](../storefront/quickview-and-other-pages.md).

## Notes

* The app embed must be enabled on the theme, whatever the page is built with.
* Option sets still need to be **Active**, published to **Online Store**, and matched by their product rule.
* A builder page that does not use a real Shopify product cannot show options — there is nothing to attach them to.

## Troubleshooting

<details>
<summary>Options do not appear on my builder page</summary>

Add the app block if the builder supports it. If not, add your own element and target it with a CSS selector.
</details>

<details>
<summary>Options appear but in the wrong place</summary>

Move the app block, or change which of your own elements the selector targets.
</details>

<details>
<summary>Add to cart ignores my required options</summary>

The builder's button is not going through the app's validation. This needs looking at — contact support with the page and the builder name.
</details>

<details>
<summary>It works on desktop but not on mobile</summary>

Your builder probably has a separate mobile layout that needs its own app block or element.
</details>

<details>
<summary>The Personalizer preview draws on the wrong image</summary>

The builder is using its own gallery. Contact support with the page.
</details>
