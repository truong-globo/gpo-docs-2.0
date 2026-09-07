---
description: Fixes for the most common reasons options are not showing up or not working as expected.
icon: wrench
---

# Troubleshooting

Most reports have one of the causes below. Check the first one first, because it is the most common.

## Options are not showing up

<details>
<summary>Nothing from the app appears on the storefront at all</summary>

Check these four items in order:

1. **The app embed is not enabled on your live theme.** This is the most common cause. The app embed is per theme, so publishing a new theme turns it off. See [Enable the app embed](../getting-started/enable-the-app-embed.md).
2. **The option set is Draft.** A draft option set is never displayed. See [Activate and publish](../option-sets/create-an-option-set.md#publish-the-option-set).
3. **Online Store is not selected** under the option set's **Sales channels**.
4. **The product rule does not match** the product you are viewing. Use **Preview matching products** to check. See [Assign to products](../option-sets/assign-to-products.md).

If all four are correct, report it rather than working around it. See [Contact support](contact-support.md).
</details>

<details>
<summary>Some options appear and others do not</summary>

There are three likely causes: [conditional logic](../conditional-logic/README.md) is hiding them, the **Hide** action is applied to them, or your plan does not include those option types, so they are configured but not displayed.
</details>

<details>
<summary>Options appear on product pages but not in a quickview</summary>

Turn on **Show options on Quickview popups** in **Settings** > **Settings** > **General**. See [Quickview and other pages](../storefront/quickview-and-other-pages.md).
</details>

<details>
<summary>Options appear twice on one product</summary>

Either two active option sets match the product, or automatic placement and an [app block](../getting-started/add-the-app-block.md) are both placing the widget. For the first cause, filter the list to **Active** and look for an option set using **Apply to All Products**. For the second, remove one of the two.
</details>

<details>
<summary>Options disappeared after I published a theme</summary>

The app embed is not enabled on the new theme. The app embed is per theme, including a duplicate of the same theme.
</details>

<details>
<summary>Options show on the storefront but not in POS, or the reverse</summary>

Check the option set's **Sales channels**. It has to be published to the channel you expect it on. Then confirm that the option types you used are supported in POS. [Dimension](../option-types/input-types/dimension.md) and [Product links](../option-types/selection-types/product-links.md) are not supported, and **Add price** add-ons are not charged there. See [POS limitations](../pos/limitations.md).
</details>

## Pricing and add-ons

<details>
<summary>An add-on charge is missing, wrong, or doubled</summary>

* **Nothing is charged.** Check that the option is not hidden by a conditional rule, because hidden options are not charged, that the price is set, and that the option set is saved and active.
* **The charge multiplies when a customer buys several.** The option is set to **Default** mode, which follows the product quantity. Use **One time charge** for anything charged once per order, such as gift wrap. See [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md).
* **Every selected value is charged on a multi-select.** This is correct. Limit it with **Max selections**.
</details>

<details>
<summary>The product price is higher than my listed price before anything is selected</summary>

An option has a **default value** with a price attached, so it is charged as soon as the page loads. Either remove the default value, or set the default to a value with no price. See [Required field and default value](../option-types/shared-settings/required-and-default-value.md#default-value).
</details>

<details>
<summary>No price appears beside an option</summary>

**Settings** > **Settings** > **Add-on price** has two settings. **Show add-on for inputs** covers Text, Textarea, and Number, and **Show add-on for options** covers the selection types. Check that the one covering your option type is on. See [Add-on price display settings](../add-on-pricing/price-display-settings.md).
</details>

<details>
<summary>Out of stock options does nothing</summary>

There are three causes. The values use **Add price**, which has no product and therefore no inventory. The add-on product does not have inventory tracking turned on. Or the variant is still set to continue selling when out of stock. On generated products, the last two have to be set manually. See [Stock and inventory](../add-on-pricing/stock-and-inventory.md).
</details>

<details>
<summary>Generated add-on products appear in my collections and search</summary>

Exclude the tag `globo-product-options` from those collections. Do not unpublish the products from the Online Store, because an unpublished product cannot be added to the cart. See [Automatically generate a product](../add-on-pricing/auto-generate-a-product.md).
</details>

## Cart and checkout

<details>
<summary>Add to cart does nothing</summary>

This is usually a validation failure rather than a broken button: a required option is empty, or an entry exceeds a limit. Turn on **Auto-scroll to first error message** in **Settings** > **Settings** > **General** so customers are taken to the field with the error. It is on by default, and with it off customers see no feedback.
</details>

<details>
<summary>Customers can add to cart without seeing the options</summary>

Two things bypass the form: a quickview without **Show options on Quickview popups** enabled, and a sticky add-to-cart bar whose button does not go through the app. Both produce orders you cannot fulfill. If the setting is already correct, report it. See [Theme and third-party notes](../integrations/theme-and-third-party-notes.md).
</details>

<details>
<summary>The accelerated payment buttons disappeared</summary>

This is expected on products with options. Those buttons skip the cart, which would skip the option form, so the app hides them where options are present.
</details>

<details>
<summary>Customers delete add-on lines and break their orders</summary>

Turn on **Hide quantity box and remove button for add-on products** in **Settings** > **Settings** > **General**. It is on by default. Without it, a customer can remove the gift box while keeping the "gift wrapped" option.
</details>

<details>
<summary>Option details are missing from my packing slip</summary>

The template does not print line item properties. Add the snippet from [Show options on orders](../storefront/show-options-on-orders.md) inside the line item loop, or use an [Update order notes](../automations/update-order-notes.md) workflow, because most templates already print the order note.
</details>

<details>
<summary>Odd technical entries appear on my paperwork</summary>

Your template is printing every property, including the app's internal ones. The snippet in [Show options on orders](../storefront/show-options-on-orders.md) skips property names beginning with an underscore.
</details>

<details>
<summary>Order lines read as "text" or "checkbox"</summary>

Those are the options' **Name** values, left at their defaults. Set them to readable values. The change applies to future orders. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).
</details>

## Appearance and behavior

<details>
<summary>The widget looks nothing like my theme</summary>

Turn on **Match theme style** in **Settings** > **Design**, and check whether your theme is listed under the **View supported themes** link beside it. If it is not listed, set the colors, borders, and fonts manually. See [Match your theme style](../storefront/match-your-theme-style.md).
</details>

<details>
<summary>The widget is in an odd place on the page</summary>

Change **Widget placement** in **Settings** > **Settings** > **General**, or set the position exactly with an [app block](../getting-started/add-the-app-block.md). See [Widget placement](../storefront/widget-placement.md).
</details>

<details>
<summary>The widget appears late, after the page has loaded</summary>

This is usually a speed or script optimization app deferring the app's scripts. Add this app to its exclusion list. See [Theme and third-party notes](../integrations/theme-and-third-party-notes.md).
</details>

<details>
<summary>A feature or option type is grayed out, or displays an upgrade prompt</summary>

The feature is not included on your current plan. See [Compare plans](../plans/compare-plans.md).
</details>

## Messages the app shows you

These messages appear in the builder while you configure an option, and prevent you from saving something that would not work. `:field` is replaced with the name of the setting.

<table><thead><tr><th width="330">Message</th><th>What it means</th></tr></thead><tbody><tr><td><code>"Name must be unique. Please enter a different value."</code></td><td>Two options in the set share a <strong>Name</strong>, ignoring capitalisation and spaces. A duplicated option is the usual cause — rename the copy. See <a href="../option-types/shared-settings/labels-and-visibility.md">Label and Name</a></td></tr><tr><td><code>"Name cannot contain any of the following characters . : ' \ |"</code></td><td>Remove the character. Apostrophes are the most frequent offender: use <code>Customers note</code> as the Name and put <code>Customer's note</code> in the Label</td></tr><tr><td><code>"Value must be unique"</code></td><td>Two option values match once capitalisation and spaces are ignored. Look for a trailing space, or <code>Red</code> and <code>RED</code> in the same table</td></tr><tr><td><code>"Value can't contain any of the following characters , : ' |"</code></td><td>An option value or tab title contains a blocked character. See <a href="../option-sets/option-values.md">Working with option values</a></td></tr><tr><td><code>"The value must be between min and max"</code></td><td>A default value falls outside its own limits. Change the default, or widen the range. See <a href="../option-types/shared-settings/limits.md">Limits</a></td></tr><tr><td><code>"The value must be greater than min" / "less than max"</code></td><td>Min and max are the wrong way round</td></tr><tr><td><code>"The value must be between 1 and the number of option values"</code></td><td>Your min or max selections is higher than the number of values the option has. Add values, or lower the limit</td></tr><tr><td><code>"The value must be between 1 and 20 (or max)"</code></td><td>A file count outside the permitted 1–20 range</td></tr><tr><td><code>"Formula cannot contain subtraction"</code></td><td>Remove the <code>-</code> from a dimension formula. Rewrite it using multiplication, addition, and division. See <a href="../add-on-pricing/dimension-formula.md">Dimension add-on formula</a></td></tr><tr><td><code>"This product does not exist on your store anymore."</code></td><td>A linked add-on product was deleted in Shopify. Select a different product, or recreate it</td></tr><tr><td><code>"This variant does not exist on your store anymore. Please select another."</code></td><td>The linked variant was deleted or changed. Reopen the price dialog and pick a current one</td></tr><tr><td><code>"Please select product to apply this option set."</code></td><td><strong>Manual Selection</strong> is on with nothing selected. Select products, or switch method. See <a href="../option-sets/assign-to-products.md">Assign to products</a></td></tr><tr><td><code>"Please select customer to apply this option set."</code></td><td>The same for the customer rule — select customers, or switch to <strong>Everyone</strong></td></tr><tr><td><code>"HTML class only accepts letters, numbers, hyphens and underscore"</code></td><td>That is the option's <strong>HTML class</strong> field, not the CSS editor. Remove the offending character — usually a leading dot. One class name per option</td></tr><tr><td><code>"This element has reached the maximum number of font options (30)"</code></td><td>Thirty is the ceiling per <a href="../option-types/selection-types/font-picker.md">Font picker</a>. Remove some fonts</td></tr><tr><td><code>"File type must be .woff2, .woff, .ttf or .otf"</code></td><td>A custom font upload in an unsupported format. Convert it, or ask your supplier for a web format. See <a href="../settings/custom-fonts.md">Custom fonts</a></td></tr><tr><td><code>"Invalid email" on an address that looks correct</code></td><td>Check for a trailing space, a comma instead of a full stop, or two addresses in one field. Only one address per field is accepted</td></tr><tr><td><code>"Upgrade required", or a grayed-out setting</code></td><td>The feature is not on your plan. See <a href="../plans/compare-plans.md">Compare plans</a></td></tr></tbody></table>

## Conditional logic and the Personalizer

Both have their own troubleshooting page, organized by symptom:

* [Troubleshooting conditional logic](../conditional-logic/troubleshooting.md) covers rules running at the wrong time, options that will not hide, and variant conditions.
* [Troubleshooting personalizer](../personalizer/troubleshooting.md) covers nothing being drawn, an incorrect position, the wrong font, and unusable customer designs.

## Still stuck?

See the [FAQ](faq.md) for quick answers, or [Contact support](contact-support.md) with your theme name, the option set name, and a link to the product page.
