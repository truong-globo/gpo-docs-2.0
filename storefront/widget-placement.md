---
description: The eight positions the widget can take on a product page, and how to put it anywhere else.
icon: crosshairs
---

# Widget placement

Where the option widget sits on your product page. **Settings** > **Settings** > **General** > **Widget Settings** > **Widget placement**.

## The eight positions

Four are relative to things every theme has. Four are relative to an HTML element you name.

<table><thead><tr><th width="330">Position</th><th>Puts the widget</th></tr></thead><tbody><tr><td><strong>Above product variants</strong></td><td>Before the variant pickers</td></tr><tr><td><strong>Below product variants</strong></td><td>After the variant pickers, before the buy buttons</td></tr><tr><td><strong>Above add to cart button</strong></td><td>Directly above the buy buttons. New stores start here</td></tr><tr><td><strong>Below add to cart button</strong></td><td>Directly below the buy buttons</td></tr><tr><td><strong>Above an HTML element</strong></td><td>Immediately before an element you specify</td></tr><tr><td><strong>Below an HTML element</strong></td><td>Immediately after it</td></tr><tr><td><strong>At the start of an HTML element</strong></td><td>Inside it, as its first content</td></tr><tr><td><strong>At the end of an HTML element</strong></td><td>Inside it, as its last content</td></tr></tbody></table>

The four custom positions reveal a **Selector of the HTML element** field, where you enter a CSS selector such as `#addToCart`.

<!-- SCREENSHOT: store-widget-placement | App admin → Settings → General → Widget Settings | Dropdown Widget placement đang mở với 8 lựa chọn chia nhóm Default và Custom | Khoanh dropdown -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The widget placement dropdown showing the default and custom position groups"><figcaption><p>Four positions every theme understands, and four you define yourself.</p></figcaption></figure>

## Which to choose

<table><thead><tr><th width="330">You want</th><th>Choose</th></tr></thead><tbody><tr><td>The most reliable default</td><td><strong>Above add to cart button</strong> — options are read before the shopper commits</td></tr><tr><td>Options grouped with the variant pickers</td><td><strong>Below product variants</strong></td></tr><tr><td>Options before the shopper picks a variant</td><td><strong>Above product variants</strong> — rarely right, since variant choice usually comes first</td></tr><tr><td>Options after the buy buttons</td><td><strong>Below add to cart button</strong> — only if your theme puts something useful there. Shoppers may miss them</td></tr><tr><td>An exact position none of the above gives</td><td>An <a href="../getting-started/add-the-app-block.md">app block</a> first, and a custom selector only if the block will not do</td></tr></tbody></table>

{% hint style="info" %}
**Try the app block before a CSS selector.** An [app block](../getting-started/add-the-app-block.md) is dragged into position in the theme editor and needs no selector to maintain. A selector is a piece of your theme's internal structure, and a theme update can change it.

The app itself suggests the block: the placement setting carries a tip pointing at the theme editor.
{% endhint %}

## Using a custom selector

{% stepper %}
{% step %}
### Find the element

On your product page, use your browser's inspector to find the element you want the widget placed against. Look for a stable `id` or a distinctive class.
{% endstep %}

{% step %}
### Choose the relationship

**Above** and **Below** place the widget outside the element. **At the start of** and **At the end of** place it inside.
{% endstep %}

{% step %}
### Enter the selector

In **Selector of the HTML element** — for example `#addToCart` or `.product-form__buttons`.
{% endstep %}

{% step %}
### Save and check on a real product page

If nothing appears, the selector does not match. Check it in your browser's inspector.
{% endstep %}

{% step %}
### Write down what you used

A theme update can change the markup. Knowing which selector you relied on turns a mystery into a five-minute fix.
{% endstep %}
{% endstepper %}

## Placement on other page types

The setting above covers product pages. Other pages have their own switches:

<table><thead><tr><th width="330">Page</th><th>Controlled by</th></tr></thead><tbody><tr><td>Collection quickview popups</td><td><strong>Show options on Quickview popups</strong>. See <a href="quickview-and-other-pages.md">Quickview and other pages</a></td></tr><tr><td>Home page, featured product section</td><td><strong>Show widget on home page</strong>, plus an <a href="../getting-started/add-the-app-block.md">app block</a> in that section</td></tr><tr><td>Regular pages, featured product section</td><td><strong>Show widget on regular page</strong>, plus an app block</td></tr><tr><td>Cart page</td><td>Its own settings. See <a href="cart-page.md">Cart page</a></td></tr></tbody></table>

## Notes

* Placement is store-wide. Every option set uses the same position.
* Placing an [app block](../getting-started/add-the-app-block.md) does not disable automatic placement. If the widget appears twice, remove one of the two.
* A selector that matches several elements places the widget against the first.
* Changing placement does not affect what the options are or how they behave.

## Troubleshooting

<details>
<summary>The widget appears in an odd place</summary>

Try a different default position first. **Above add to cart button** works on the widest range of themes.
</details>

<details>
<summary>Nothing appears with a custom selector</summary>

The selector does not match anything on the page. Check it in your browser's inspector. Also confirm you have not included the wrong prefix — `#` for an id, `.` for a class.
</details>

<details>
<summary>The widget appears twice</summary>

Automatic placement and an app block are both running. Remove the block, or change the placement so it no longer applies.
</details>

<details>
<summary>It moved after a theme update</summary>

Your theme's markup changed. If you used a custom selector, find the new one. If this keeps happening, switch to an app block.
</details>

<details>
<summary>Options appear on the product page but not in quickview</summary>

That is a separate switch. See [Quickview and other pages](quickview-and-other-pages.md).
</details>

<details>
<summary>I want a different position for different products</summary>

Not possible — the setting is store-wide. Use an app block in a product template that only those products use.
</details>
