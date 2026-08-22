---
description: Every setting on the General section, field by field.
icon: sliders
---

# General settings

**Settings** > **Settings** > **General**. Six groups. Each setting below links to the page that explains it in depth.

## Widget Settings

<table><thead><tr><th width="290">Setting</th><th width="150">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Widget placement</strong></td><td><strong>Above add to cart button</strong></td><td>Where the widget sits on the product page. Eight choices — four relative to theme elements, four relative to a CSS selector. See <a href="../storefront/widget-placement.md">Widget placement</a></td></tr><tr><td><strong>Selector of the HTML element</strong></td><td>Empty</td><td>Only shown for the four custom placements. The CSS selector to position against</td></tr><tr><td><strong>Alignment</strong></td><td><strong>Left</strong></td><td><strong>Left</strong>, <strong>Center</strong>, <strong>Right</strong>, or <strong>Right to left</strong>. See <a href="../storefront/widget-behavior.md">Widget behavior</a></td></tr><tr><td><strong>Show tooltip when hovering over options</strong></td><td>On</td><td>Shows the value's name when hovering a swatch</td></tr><tr><td><strong>Display selected value next to label</strong></td><td>On</td><td>Shows the chosen value beside the option's label</td></tr><tr><td><strong>Limit widget height (scroll if too long)</strong></td><td>Off</td><td>Caps the widget's height and scrolls inside it</td></tr><tr><td><strong>Fixed height</strong></td><td>Empty</td><td>The height in pixels. Only shown when the limit is on</td></tr></tbody></table>

The group also carries a tip pointing at the theme editor, because an [app block](../getting-started/add-the-app-block.md) is usually a more reliable way to place the widget than a CSS selector.

## Collection page

<table><thead><tr><th width="290">Setting</th><th width="150">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Show options on Quickview popups</strong></td><td>On</td><td>Renders options inside collection-page quickviews. Without it, shoppers can add to cart from a quickview without seeing your options. See <a href="../storefront/quickview-and-other-pages.md">Quickview and other pages</a></td></tr></tbody></table>

## Product page

<table><thead><tr><th width="290">Setting</th><th width="150">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Go to cart immediately after adding to cart</strong></td><td>On</td><td>Sends shoppers to the cart page after adding a product with add-ons. See <a href="../storefront/ajax-cart-and-redirect.md">Ajax cart and redirect to cart</a></td></tr><tr><td><strong>Auto-scroll to first error message</strong></td><td>On</td><td>Scrolls to the first problem when add to cart is blocked. Keep it on</td></tr><tr><td><strong>File preview</strong></td><td><strong>Show image if the uploaded file is a photo, otherwise show link</strong></td><td>How uploaded files are shown. The alternative is <strong>Show link</strong> for everything. See <a href="../option-types/input-types/file-upload.md">File upload</a></td></tr></tbody></table>

## Cart page

<table><thead><tr><th width="290">Setting</th><th width="150">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Hide quantity box and remove button for add-on products</strong></td><td>On</td><td>Stops customers changing or deleting add-on lines independently. Keep it on</td></tr><tr><td><strong>Show "Edit Options" button in cart</strong></td><td>Off</td><td>Lets customers reopen the option form from the cart. Plan-gated</td></tr><tr><td><strong>Personalize preview mode</strong></td><td><strong>View in modal</strong></td><td><strong>View in modal</strong> or <strong>Download file</strong> for personalised designs. Plan-gated</td></tr></tbody></table>

See [Cart page](../storefront/cart-page.md).

## Other pages

<table><thead><tr><th width="290">Setting</th><th width="150">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Show widget on home page (featured product section only)</strong></td><td>On</td><td>Options in a featured product section on your home page</td></tr><tr><td><strong>Show widget on regular page (featured product section only)</strong></td><td>On</td><td>The same on other pages</td></tr></tbody></table>

Both also need the [app block](../getting-started/add-the-app-block.md) placed in that section. See [Quickview and other pages](../storefront/quickview-and-other-pages.md).

## Custom fonts

<table><thead><tr><th width="290">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Custom fonts</strong></td><td>Upload your own font files, then use them in the widget's typography and in the Personalizer. See <a href="custom-fonts.md">Custom fonts</a></td></tr></tbody></table>

## The five worth checking on a new store

<table><thead><tr><th width="330">Setting</th><th>Why</th></tr></thead><tbody><tr><td><strong>Widget placement</strong></td><td>The default suits most themes, but check it looks right on yours</td></tr><tr><td><strong>Show options on Quickview popups</strong></td><td>If your theme has quickviews, this prevents orders with no options</td></tr><tr><td><strong>Auto-scroll to first error message</strong></td><td>Leave it on. Shoppers otherwise think the button is broken</td></tr><tr><td><strong>Hide quantity box and remove button for add-on products</strong></td><td>Leave it on. Protects the integrity of add-on orders</td></tr><tr><td><strong>Show "Edit Options" button in cart</strong></td><td>Worth turning on if you sell personalised products</td></tr></tbody></table>

## Notes

* All store-wide.
* Several are plan-gated and show an upgrade prompt rather than being hidden.
* Changes need saving, and the app warns you before you navigate away with unsaved work.
