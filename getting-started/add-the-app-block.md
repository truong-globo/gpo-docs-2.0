---
description: >-
  Pin the option widget to an exact spot in your product template using the theme
  app block, instead of letting the app place itself.
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

* Automatic placement lands the widget somewhere unhelpful and none of the built-in positions fix it.
* You want the widget between two specific blocks — under the variant picker but above a trust badge, say.
* You want options on a **Featured product** section on your home page or another page.
* You would rather not maintain a CSS selector in the app's settings.

Stick with automatic placement when one of the built-in positions already puts the widget where you want it. See [Widget placement](../storefront/widget-placement.md).

## Add it to your product template

{% stepper %}
{% step %}
### Open the theme editor at the product template

On the app's dashboard, select **Add app block** on the **Active app blocks** card. That opens the product template with the block ready to insert.

The same tip appears under **Widget placement** in **Settings** > **Settings** > **General**. Or open it yourself: **Online Store** > **Themes** > **Customize**, then switch the template dropdown to **Products** > **Default product**.

<!-- SCREENSHOT: start-block-add-button | App admin → Dashboard | Card "Active app blocks" với số lượng và nút Add app block | Khoanh nút Add app block -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Active app blocks card on the dashboard with the Add app block button"><figcaption><p>The dashboard counts your app blocks and links straight to adding one.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add the block

In the left sidebar, find the product information section — its name varies by theme, often **Product information** or **Product** — and select **Add block**. Under the **Apps** group, choose **Globo Product Options**.
{% endstep %}

{% step %}
### Drag it into position

The block appears in the section's block list. Drag it up or down until it sits where you want the widget. The preview redraws as you move it, so you can judge the position directly.

<!-- SCREENSHOT: start-block-drag-position | Shopify theme editor → product template | Block "Globo Product Options" trong danh sách block của section, đang được đặt trên nút Add to cart | Khoanh dòng block Globo Product Options (mũi tên nhỏ vì nhiều block trong list) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Globo Product Options block in a product section's block list, positioned above the buy buttons"><figcaption><p>Drag the block to set the widget's position — no CSS selector needed.</p></figcaption></figure>
{% endstep %}

{% step %}
### Save, then check

Select **Save** in the theme editor. Back in the app, the **Active app blocks** card counts your block — and a product page on your storefront shows the widget in its new position.
{% endstep %}
{% endstepper %}

## Options on a home page or a regular page

Options can also render inside a **Featured product** section outside the product template.

In the theme editor, open the page you want, add a **Featured product** section if there is not one, then **Add block** > **Globo Product Options** inside it. The block's **Product** setting fills itself in from the section, but confirm it points at the product you expect. Save.

{% hint style="warning" %}
The block alone is not enough here. In the app, go to **Settings** > **Settings** > **General** > **Other pages** and turn on the matching switch — **Show widget on home page (featured product section only)** or **Show widget on regular page (featured product section only)**. With the switch off, the widget does not render even with the block in place.
{% endhint %}

## Limits and notes

* Only the product template and **Featured product** sections make sense for the block — it needs a product in context to know which option sets apply.
* Placing a block does **not** disable automatic placement. If the widget appears twice, remove the block or change **Widget placement** so the automatic position no longer applies.
* App blocks are stored with the theme, like the embed. A new theme starts with none.
* Blocks need an Online Store 2.0 theme. On an older theme, use automatic placement with a custom CSS selector instead.

## Troubleshooting

<details>
<summary>Globo Product Options is not in the Add block list</summary>

Check you are adding the block inside a section that accepts app blocks — usually the product information section on a product template, or a Featured product section. Some theme sections do not accept them at all. Also confirm the app is still installed.
</details>

<details>
<summary>I added the block but nothing renders there</summary>

Three things: is the [app embed](enable-the-app-embed.md) enabled on this theme; does an **Active** option set match this product; and for a home or regular page, is the matching **Other pages** switch on?
</details>

<details>
<summary>The widget shows up twice</summary>

Automatic placement and the app block are both placing it. Remove one.
</details>

<details>
<summary>The widget disappeared after a theme update</summary>

Theme updates can reset a section's blocks. Re-add the block, or switch to automatic placement, which survives theme updates.
</details>
