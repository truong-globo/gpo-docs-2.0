---
description: >-
  A complete real example — paid engraving, a gift-wrap add-on with stock
  tracking, and a gift message that only appears when it is needed.
icon: list-check
---

# Walkthrough: engraving and gift wrap

The [Quickstart](quickstart.md) built one plain text field. This page builds something you could actually sell with. By the end you will have used four of the app's core features together:

* an option that **charges extra**
* an add-on that **tracks its own stock**
* an option that **only appears under a condition**
* a product rule that **applies the set automatically** as your catalogue grows

The example is a jewellery store selling engravable bracelets. Substitute your own products and wording as you go.

## What we are building

<table><thead><tr><th width="200">Option</th><th width="130">Type</th><th>Behaviour</th></tr></thead><tbody><tr><td>Engraving text</td><td>Text</td><td>Max 20 characters, with a live counter. Adds a flat $5.00.</td></tr><tr><td>Gift wrap</td><td>Checkbox</td><td>One choice. Adds $3.00 through a real product so stock is tracked.</td></tr><tr><td>Gift message</td><td>Textarea</td><td>Hidden until the customer ticks Gift wrap.</td></tr></tbody></table>

Applies to every product tagged `engravable`.

## Before you start

* The app is installed and a plan is chosen — see [Install the app](install-the-app.md).
* The [app embed](enable-the-app-embed.md) is enabled on your live theme.
* At least one product carries the tag `engravable`. Add the tag in Shopify admin under the product's **Tags** field.
* Add-on pricing and conditional logic are plan-gated. If a field is greyed out with an upgrade prompt, see [Compare plans](../plans/compare-plans.md).

## Steps

{% stepper %}
{% step %}
### Create the option set and name the section

Go to **Option Sets** > **Create option set** > **Create from scratch**.

Name the option set `Bracelet personalization` at the top of the builder.

A new option set already contains one empty **Section**. Select it and change its **Label** to `Personalize your bracelet` — sections are containers with a visible heading, so this is what shoppers read above the group of options.

{% hint style="info" %}
Sections also have a **Style** setting: **Default** shows everything open, while **Expand** and **Collapse** turn the section into a collapsible panel. Handy when you have many options. See [Section](../option-types/static-types/section.md).
{% endhint %}

<!-- SCREENSHOT: start-wt-section-label | App admin → builder → chọn Section | Field Label của Section đang là "Personalize your bracelet" + dropdown Style | Khoanh field Label và dropdown Style -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A section's settings with its label set to Personalize your bracelet and the style dropdown visible"><figcaption><p>Rename the default section so it reads as a heading for the group.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add the engraving text field

Select the add button inside the section and choose **Text**.

On **Basic Settings**, set:

<table><thead><tr><th width="220">Field</th><th width="200">Value</th><th>Why</th></tr></thead><tbody><tr><td><strong>Label</strong></td><td><code>Engraving text</code></td><td>What shoppers read on the product page.</td></tr><tr><td><strong>Name</strong></td><td><code>Engraving text</code></td><td>What appears on the cart, at checkout, and on the order.</td></tr><tr><td><strong>Max character</strong></td><td><code>20</code></td><td>The bracelet only fits 20 characters.</td></tr><tr><td><strong>Character counter</strong></td><td><strong>Show</strong></td><td>Shoppers can see how much room is left as they type.</td></tr><tr><td><strong>Placeholder</strong></td><td><code>e.g. Forever yours</code></td><td>Shows an example inside the empty box.</td></tr><tr><td><strong>Help text</strong></td><td><code>Up to 20 characters. Letters and numbers only.</code></td><td>Sets expectations before they type.</td></tr></tbody></table>

Leave **Required field** off — not everyone wants engraving.

<!-- SCREENSHOT: start-wt-text-basic | App admin → builder → option Text | Basic Settings đã điền Label, Name, Max character 20, Character counter = Show | Khoanh nhóm Min/Max character + Character counter -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="Basic Settings of a Text option with a 20-character limit and the character counter set to Show"><figcaption><p>A character limit plus a counter stops engraving requests that will not fit.</p></figcaption></figure>
{% endstep %}

{% step %}
### Charge $5.00 for engraving

Still on the Text option's **Basic Settings**, find **Add-on Settings** and select the **Price** field. A dialog opens with three tabs — three genuinely different ways to charge:

<table><thead><tr><th width="260">Tab</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Use existing product</strong></td><td>Links a product and variant you already sell. The add-on costs whatever that variant costs, and its stock is tracked.</td></tr><tr><td><strong>Automatically generate product</strong></td><td>The app creates a hidden product for you at the price you type. Stock is tracked, and you never have to build the product by hand.</td></tr><tr><td><strong>Add price</strong></td><td>Just adds money to the order. No product, no stock tracking. Not supported on Shopify POS.</td></tr></tbody></table>

Engraving is a service with no stock to track, so open **Add price**, enter `5`, and select **Select**.

The **Advanced settings** dropdown next to it controls how the charge scales with quantity. Leave it on **Default** — one charge per bracelet. See [Advanced add-on modes](../add-on-pricing/advanced-add-on-modes.md) for the other seven modes, including **Per character**, which prices engraving by how much the customer types.

<!-- SCREENSHOT: start-wt-addon-add-price | App admin → builder → option Text → mở dialog Price | Dialog Add-on Configuration với 3 tab, tab "Add price" đang chọn, giá 5 | Khoanh hàng 3 tab (mũi tên nhỏ vào tab Add price) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The add-on configuration dialog with three tabs and the Add price tab selected"><figcaption><p>Every add-on starts with this choice: link a product, generate one, or just add money.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add the gift wrap checkbox

Add another option, this time **Checkbox**.

Set **Label** to `Gift wrap` and **Name** to `Gift wrap`.

In the **Option values** table there is one starter row. Change its **Value** to `Yes, wrap it as a gift`.

Values have their own rules: each must be unique within the option, cannot be empty, and cannot contain `,` `:` `"` `'` or `|`. See [Working with option values](../concepts/option-values.md).

<!-- SCREENSHOT: start-wt-checkbox-values | App admin → builder → option Checkbox | Bảng Option values với các cột Value / Price / Product / Action, 1 dòng "Yes, wrap it as a gift" | Khoanh cả bảng Option values -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The option values table for a checkbox showing the Value, Price, Product, and Action columns"><figcaption><p>Selection options list their choices in a table, one row per choice.</p></figcaption></figure>
{% endstep %}

{% step %}
### Charge $3.00 for gift wrap, and track its stock

Gift wrap is a physical thing — you can run out of boxes and ribbon. So this add-on should be a real product.

In the option values table, select the **Price** cell on the `Yes, wrap it as a gift` row. In the dialog choose **Automatically generate product**, enter `3`, and select **Select**.

Save the option set, then reload the page. The **Product** column on that row now links to the product the app created, so you can open it in Shopify admin and set its inventory, SKU, and weight like any other product.

{% hint style="info" %}
Notice where the price lives in each case. On the Text option the price belonged to the **whole option**. On a Checkbox it belongs to **each option value**, because different choices usually cost different amounts. See [Where you can set add-ons](../add-on-pricing/where-you-can-set-add-ons.md).
{% endhint %}

<!-- SCREENSHOT: start-wt-addon-auto-product | App admin → builder → dialog Price của 1 option value | Tab "Automatically generate product" với giá 3 | Khoanh field giá trong tab -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Automatically generate product tab of the add-on dialog with a price of 3 entered"><figcaption><p>Generating a product gives the add-on real inventory you can manage in Shopify.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add the gift message field, hidden by default

Add a third option: **Textarea**.

Set **Label** to `Gift message`, **Name** to `Gift message`, and **Max character** to `200`.

Now make it conditional. Still on **Basic Settings**, turn on **Conditional logic**. A rule builder appears. Configure it like this:

<table><thead><tr><th width="200">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Action</td><td><strong>Show</strong></td></tr><tr><td>Match</td><td><strong>all conditions</strong></td></tr><tr><td>When</td><td><strong>Gift wrap</strong></td></tr><tr><td>Operator</td><td><strong>contains</strong></td></tr><tr><td>Value</td><td><code>Yes, wrap it as a gift</code></td></tr></tbody></table>

The **Gift message** box now stays hidden until the shopper ticks **Gift wrap**.

{% hint style="info" %}
Conditions can also read the **Shopify variant** the customer picked, not just other app options — so you can show an option only for the Large size, for example. See [Conditions based on Shopify variants](../conditional-logic/conditions-on-shopify-variants.md).
{% endhint %}

<!-- SCREENSHOT: start-wt-clo-rule | App admin → builder → option Textarea | Khối Conditional logic đã bật, rule Show / all conditions / Gift wrap / contains / "Yes, wrap it as a gift" | Khoanh khối rule -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A conditional logic rule set to show the option when Gift wrap contains the gift-wrap value"><figcaption><p>Conditional logic keeps the form short until the shopper asks for more.</p></figcaption></figure>
{% endstep %}

{% step %}
### Check the order and the live preview

Drag the three options in the panel so they read top to bottom: **Engraving text**, **Gift wrap**, **Gift message**. That is the order shoppers see them in.

Use the preview on the right to test the logic without leaving the app: tick **Gift wrap** and the message box appears; untick it and it hides again. Switch the preview between desktop and mobile width to check both.

<!-- SCREENSHOT: start-wt-preview-logic | App admin → builder | Preview bên phải: Gift wrap đã tick và Gift message hiện ra | Khoanh vùng Gift message vừa xuất hiện trong preview -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The builder's live preview with Gift wrap ticked and the Gift message field revealed"><figcaption><p>The live preview runs your conditional logic, so you can test rules before saving.</p></figcaption></figure>
{% endstep %}

{% step %}
### Apply it to every engravable product

Switch to the **Assign products** step and turn on **Automatic Rules**.

Set **Products must match: all conditions**, then build one condition:

* **Product tag** — **is equal to** — `engravable`

From now on, any product you tag `engravable` picks this option set up automatically. You never come back here to add products by hand.

<!-- SCREENSHOT: start-wt-automatic-rule | App admin → builder → Assign products | Automatic Rules đang bật với điều kiện Product tag is equal to engravable | Khoanh dòng điều kiện -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="An automatic rule matching products whose tag equals engravable"><figcaption><p>Automatic rules keep the option set in sync with your catalogue as it grows.</p></figcaption></figure>
{% endstep %}

{% step %}
### Save, activate, publish

Select **Save**.

Then set the status next to the option set name to **Active**, and confirm **Online Store** is ticked under **Sales channels**.

{% hint style="warning" %}
If you also sell in person, tick **Point of Sale** too — but note that the **Add price** add-on you used for engraving is not supported on POS. For POS orders, use **Use existing product** or **Automatically generate product** instead. See [POS limitations](../pos/limitations.md).
{% endhint %}
{% endstep %}

{% step %}
### Test the whole thing on your storefront

Open a product tagged `engravable`.

1. Type `Forever yours` into **Engraving text**. The counter shows how many characters are left, and the price shown for the product goes up by $5.00.
2. Tick **Gift wrap**. Another $3.00 is added, and **Gift message** appears.
3. Type a message and add the product to your cart.

On the cart page you now see the bracelet with **Engraving text** and **Gift message** listed under it, plus a separate line for the gift-wrap product.

<!-- SCREENSHOT: start-wt-storefront-filled | Storefront → trang sản phẩm | Cả 3 option hiện ra, Gift wrap đã tick, Gift message hiện, giá đã tăng | Khoanh riêng widget do app tạo -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A storefront product page with engraving text filled in, gift wrap ticked, and the gift message field showing"><figcaption><p>The finished form on the storefront, with the conditional field revealed.</p></figcaption></figure>

<!-- SCREENSHOT: start-wt-cart | Storefront → trang cart | Line item chính có option properties + line item add-on gift wrap riêng | Khoanh phần properties dưới line item và dòng add-on -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The cart page showing the bracelet with its option details and a separate gift wrap line"><figcaption><p>Options travel with the line item; add-on products become their own cart lines.</p></figcaption></figure>
{% endstep %}

{% step %}
### Check the order in your admin

Place the test order, then open it in Shopify admin under **Orders**.

The bracelet line item lists **Engraving text** and **Gift message** with the values the customer entered, and the gift-wrap product appears as its own line item. Your production team gets everything without you copying anything by hand.

If you want that information pushed somewhere else — emailed to you, written into the order notes, or turned into an order tag — see [Automations](../automations/README.md).
{% endstep %}
{% endstepper %}

{% hint style="success" %}
You have now used the four features that most stores need: pricing, stock-tracked add-ons, conditional logic, and automatic product rules.
{% endhint %}

## What to change for your own store

<table><thead><tr><th width="280">If you want…</th><th>Do this instead</th></tr></thead><tbody><tr><td>Engraving priced per character</td><td>Set <strong>Advanced settings</strong> on the Text option to <strong>Per character</strong> — see <a href="../add-on-pricing/advanced-add-on-modes.md">Advanced add-on modes</a>.</td></tr><tr><td>Several gift-wrap designs with pictures</td><td>Use <strong>Image swatch</strong> instead of Checkbox, one value per design — see <a href="../option-types/selection-types/image-swatch.md">Image swatch</a>.</td></tr><tr><td>The customer to see their engraving on the bracelet photo</td><td>Turn on <strong>Personalizer Settings</strong> on the Text option — see <a href="../personalizer/README.md">Product Personalizer</a>.</td></tr><tr><td>A delivery date instead of a message</td><td>Use <strong>Date and time picker</strong>, and restrict which dates can be chosen — see <a href="../option-types/input-types/date-and-time-picker.md">Date and time picker</a>.</td></tr><tr><td>This form on only five specific products</td><td>Use <strong>Manual Selection</strong> instead of <strong>Automatic Rules</strong> — see <a href="../option-sets/assign-to-products.md">Assign to products</a>.</td></tr><tr><td>To reuse this whole setup on another store or option set</td><td>Save it as a template — see <a href="../templates/custom-templates.md">Custom templates</a>.</td></tr></tbody></table>

## Troubleshooting

<details>
<summary>The price on the product page did not change when I filled in the engraving</summary>

Check **Settings** > **Settings** > **Add-on price**. **Show add-on for inputs** must be on for text-style options, and **Add add-on price to the product price** controls whether the displayed product price updates or the add-on is shown separately. See [Add-on price display settings](../add-on-pricing/price-display-settings.md).
</details>

<details>
<summary>The Gift message field is always visible, or never visible</summary>

Open the Textarea's conditional rule and compare the condition value with the option value character for character — the match is exact. `Yes, wrap it as a gift` and `Yes, wrap it as a gift.` are different values. See [Troubleshooting conditional logic](../conditional-logic/troubleshooting.md).
</details>

<details>
<summary>The generated gift-wrap product shows up in my storefront search or collections</summary>

Add-on products the app generates are meant to be invisible to browsing. Open the product in Shopify admin and check its sales channel publishing and any collection rules that might be catching it. See [Stock and inventory](../add-on-pricing/stock-and-inventory.md).
</details>

<details>
<summary>The option set does not appear on a product I just tagged</summary>

Confirm the tag is spelled exactly as in the rule, including case, and that the product is saved. Automatic rules are evaluated against the product's current tags.
</details>

## Next steps

* [Option types](../option-types/README.md) — all 32 types, with every setting explained.
* [Add-on pricing](../add-on-pricing/README.md) — the three modes compared in depth.
* [Conditional logic](../conditional-logic/README.md) — including variant-based conditions.
* [Product Personalizer](../personalizer/README.md) — show the customer's text on the product photo.
