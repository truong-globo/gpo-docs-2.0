---
description: >-
  Pin the option widget to an exact spot in your product template using the
  theme app block, instead of letting the app place itself.
icon: thumbtack
---

# Add the app block

The **app block** is an optional second piece of theme integration. Where the [app embed](enable-the-app-embed.md) decides *whether* the app runs, the app block decides *exactly where* the widget sits — you drag it into your product template like any other theme block.

## App embed vs app block

<table><thead><tr><th width="180">Piece</th><th width="120">Required?</th><th>What it does</th></tr></thead><tbody><tr><td><strong>App embed</strong></td><td>Yes</td><td>Loads the app on your storefront. Without it nothing works. It also places the widget automatically, using the position you choose in <strong>Settings &gt; Settings &gt; General</strong>.</td></tr><tr><td><strong>App block</strong></td><td>No</td><td>A block you place in a section. The widget renders exactly where the block sits, so you control the position by dragging rather than by CSS selector.</td></tr></tbody></table>

{% hint style="warning" %}
The app block does not replace the app embed. If the embed is off, an app block renders nothing. Enable the embed first.
{% endhint %}

## When to use it

Use the app block when:

* Automatic placement lands the widget somewhere unhelpful in your theme and none of the built-in positions fix it.
* You want the widget between two specific blocks — for example under the variant picker but above a trust-badge block.
* You want options on a **Featured product** section on your home page or another page.
* You would rather not maintain a CSS selector in the app's settings.

Stick with automatic placement when one of the built-in positions already puts the widget where you want it. See [Widget placement](../storefront/widget-placement.md).

## Add it to your product template

{% stepper %}
{% step %}
### Open the theme editor at the product template

You have three ways in. All three land in the same place.

* **From the dashboard** — on the **Active app blocks** card, select **Add app block**.
* **From settings** — go to **Settings** > **Settings** > **General**. Under **Widget placement** there is a tip that says the app block is the easier and more reliable option. Select **Open theme editor**.
* **Manually in Shopify** — **Online Store** > **Themes** > **Customize**, then switch the template dropdown at the top of the theme editor to **Products** > **Default product**.

The first two routes open the product template with the block ready to insert.

<!-- SCREENSHOT: start-block-add-button | App admin → Dashboard | Card "Active app blocks" với số lượng và nút Add app block | Khoanh nút Add app block -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Active app blocks card on the dashboard with the Add app block button"><figcaption><p>The dashboard tracks how many app blocks you have placed and links straight to adding one.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add the block

In the theme editor's left sidebar, find the product information section (its name varies by theme — often **Product information** or **Product**), and select **Add block**.

Under the **Apps** group, choose **Globo Product Options**.
{% endstep %}

{% step %}
### Drag it into position

The block appears in the section's block list. Drag it up or down until it sits where you want the widget.

The preview on the right redraws as you move it, so you can judge the position directly.

<!-- SCREENSHOT: start-block-drag-position | Shopify theme editor → product template | Block "Globo Product Options" trong danh sách block của section, đang được đặt trên nút Add to cart | Khoanh dòng block Globo Product Options (mũi tên nhỏ vì nhiều block trong list) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Globo Product Options block in a product section's block list, positioned above the buy buttons"><figcaption><p>Drag the block to set the widget's position — no CSS selector needed.</p></figcaption></figure>
{% endstep %}

{% step %}
### Save

Select **Save** in the theme editor.
{% endstep %}

{% step %}
### Check the count

Back in the app, the **Active app blocks** card on the dashboard now counts your block. Open a product page on your storefront to confirm the widget renders in its new position.
{% endstep %}
{% endstepper %}

## Add it to a home page or regular page

Options can also render inside a **Featured product** section outside the product template.

{% stepper %}
{% step %}
### Add a Featured product section

In the theme editor, open the page you want — your home page, or any page template — and add a **Featured product** section if there is not one already.
{% endstep %}

{% step %}
### Add the app block inside it

Select **Add block** inside that section, then choose **Globo Product Options** from the **Apps** group.
{% endstep %}

{% step %}
### Check the product setting

The block has a **Product** setting. It fills itself in from the section's product automatically, but confirm it points at the product you expect.
{% endstep %}

{% step %}
### Save, then check the page setting in the app

Save in the theme editor. Then in the app, go to **Settings** > **Settings** > **General** > **Other pages** and make sure the switch for that page type is on:

* **Show widget on home page (featured product section only)**
* **Show widget on regular page (featured product section only)**

If the relevant switch is off, the widget will not render even with the block in place.
{% endstep %}
{% endstepper %}

## Limits and notes

* Only the product template and **Featured product** sections make sense for the block — it needs a product in context to know which option sets apply.
* Placing an app block does **not** disable automatic placement. If you see the widget twice, either remove the block, or set **Widget placement** so the automatic position no longer applies. See [Widget placement](../storefront/widget-placement.md).
* App blocks are stored with the theme, like the embed. A new theme starts with none.
* Blocks are supported on Online Store 2.0 themes. On older themes, use automatic placement with a custom CSS selector instead.

## Troubleshooting

<details>
<summary>Globo Product Options is not in the Add block list</summary>

Check that you are adding the block inside a section that supports app blocks — usually the product information section on a product template, or a Featured product section. Some theme sections do not accept app blocks at all. Also confirm the app is still installed.
</details>

<details>
<summary>I added the block but nothing renders there</summary>

Three things to check:

1. Is the [app embed](enable-the-app-embed.md) enabled on this theme?
2. Does an **Active** option set match this product?
3. For a home page or regular page, is the matching **Other pages** switch on in **Settings > Settings > General**?
</details>

<details>
<summary>The widget shows up twice</summary>

Automatic placement and the app block are both placing it. Remove one of them.
</details>

<details>
<summary>The widget disappeared after a theme update</summary>

Theme updates can reset a section's blocks. Re-add the app block, or switch to automatic placement, which survives theme updates.
</details>

## Next steps

* [Widget placement](../storefront/widget-placement.md) — the eight automatic positions and the CSS-selector options.
* [Quickview and other pages](../storefront/quickview-and-other-pages.md) — where else the widget can appear.
* [Walkthrough: engraving and gift wrap](first-option-set-walkthrough.md) — build something real.
