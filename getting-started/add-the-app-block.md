---
description: >-
  Use the App Block to place the option widget exactly where you want it in your
  product template, instead of letting the app position it automatically.
icon: thumbtack
---

# Add the app block

The **App Block** is an optional second part of the theme integration:

* **App Embed** controls **whether the app runs** on your storefront.
* **App Block** controls **where the widget appears**.

You can simply drag the App Block to your preferred position in the product template, just like any other theme block.

## App embed vs app block

<table><thead><tr><th width="180">Piece</th><th width="120">Required?</th><th>What it does</th></tr></thead><tbody><tr><td><strong>App embed</strong></td><td>Yes</td><td>Loads the app on your storefront. Without it, the app won’t work. It also places the widget automatically based on the position selected in <strong>Settings → General</strong>.</td></tr><tr><td><strong>App block</strong></td><td>No</td><td>Lets you place the widget inside a specific section of your theme. The widget appears exactly where the block is placed, giving you direct control over its position without using a CSS selector.</td></tr></tbody></table>

{% hint style="warning" %}
The App Block does not replace the App Embed. If the App Embed is disabled, the App Block will not render anything. **Always enable the App Embed first.**
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

<figure><img src="../.gitbook/assets/app block.png" alt="The Active app blocks card on the dashboard with the Add app block button"><figcaption><p>The dashboard counts your app blocks and links straight to adding one.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add the block

In the left sidebar, find the product information section — its name varies by theme, often **Product information** or **Product** — and select **Add block**. Under the **Apps** group, choose **Globo Product Options**.

<figure><img src="../.gitbook/assets/app block 2.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Drag it into position

The block appears in the section's block list. Drag it up or down until it sits where you want the widget. The preview redraws as you move it, so you can judge the position directly.

<figure><img src="../.gitbook/assets/app block 3.png" alt="The Globo Product Options block in a product section&#x27;s block list, positioned above the buy buttons"><figcaption></figcaption></figure>
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

## Notes

* Only the product template and **Featured product** sections make sense for the block — it needs a product in context to know which option sets apply.
* Placing a block does **not** disable automatic placement. If the widget appears twice, remove the block or change **Widget placement** so the automatic position no longer applies.
* App blocks are stored with the theme, like the embed. A new theme starts with none.
* Blocks need an Online Store 2.0 theme. On an older theme, use automatic placement with a custom CSS selector instead.
