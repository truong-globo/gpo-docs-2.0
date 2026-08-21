---
description: >-
  Switch the app on in your theme so your options actually render for shoppers —
  three ways to do it, and how to confirm it worked.
icon: toggle-on
---

# Enable the app embed

The **app embed** is the switch that lets the app run on your storefront. Until it is on, your option sets exist in the app but no shopper ever sees them.

You only need to do this once per theme. It does not edit any of your theme's files — Shopify stores the setting with the theme, and turning it off removes the app cleanly.

## Before you start

* Know which theme is your live theme. In Shopify admin that is **Online Store** > **Themes**, the one under **Live**.
* You need permission to edit themes.

{% hint style="warning" %}
The app embed is per theme. Enabling it on one theme does **not** enable it on the others. If you publish a different theme later — including a duplicate of the same theme — you have to enable it again on that theme.
{% endhint %}

## Method 1: From the app dashboard

The fastest route if you have just installed the app.

{% stepper %}
{% step %}
### Open the Setup guide step

On the **Dashboard**, find the **Setup guide** card and select **Step 2: Make options visible on your storefront**.
{% endstep %}

{% step %}
### Select Enable app embed

The button opens the Shopify theme editor in a new tab, already scrolled to the app embed section with our app highlighted.
{% endstep %}

{% step %}
### Turn the toggle on and save

Switch **Globo Product Options** on, then select **Save** in the theme editor.
{% endstep %}

{% step %}
### Return to the app tab

Come back to the tab where the app is open. It checks the theme again automatically and the step ticks itself off — usually within a few seconds. The app keeps checking for about a minute after you leave for the theme editor.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: start-embed-setupguide-step2 | App admin → Dashboard | Setup guide card, step 2 đang mở với nút "Enable app embed" | Khoanh nút Enable app embed -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="Step 2 of the Setup guide expanded with the Enable app embed button"><figcaption><p>Step 2 of the Setup guide opens the theme editor at the right place.</p></figcaption></figure>

## Method 2: From Theme Setup

Use this when you have more than one theme, or when you want to check the status of a specific theme.

{% stepper %}
{% step %}
### Open Theme Setup

In the app menu go to **Settings**, then select the **Theme Setup** tab.
{% endstep %}

{% step %}
### Pick the theme

The dropdown lists every theme in your store. Your published theme is marked **(Live theme)**.

Select the theme you want to work on. The badge next to **App embed** updates to show that theme's status: **Activated** or **Deactivated**.
{% endstep %}

{% step %}
### Select Go to Theme Editor

This appears whenever the selected theme shows **Deactivated**. It opens the Shopify theme editor for that theme, at the app embed.
{% endstep %}

{% step %}
### Turn the toggle on, save, and come back

Switch **Globo Product Options** on, select **Save**, then return to the app tab. The badge changes to **Activated** by itself.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: start-embed-theme-setup | App admin → Settings → Theme Setup | Dropdown chọn theme + badge Deactivated + nút Go to Theme Editor | Khoanh badge và nút Go to Theme Editor -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Theme Setup page with a theme selected, a Deactivated badge, and the Go to Theme Editor button"><figcaption><p>Theme Setup shows the app embed status for whichever theme you select.</p></figcaption></figure>

## Method 3: Directly in Shopify, without the app

Useful if someone else manages your theme, or if you want to do it without opening the app.

{% stepper %}
{% step %}
### Open the theme editor

In Shopify admin go to **Online Store** > **Themes**, find the theme you want, and select **Customize**.
{% endstep %}

{% step %}
### Open App embeds

In the theme editor's left sidebar, select the **App embeds** icon — it is the puzzle-piece icon near the bottom of the sidebar.

This lists every app that offers an embed for your theme.
{% endstep %}

{% step %}
### Turn on Globo Product Options

Find **Globo Product Options** in the list and switch its toggle on.
{% endstep %}

{% step %}
### Save

Select **Save** in the top-right of the theme editor.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: start-embed-theme-editor-toggle | Shopify theme editor → App embeds | Danh sách app embeds, toggle "Globo Product Options" đang bật | Khoanh dòng Globo Product Options (mũi tên nhỏ vì nhiều dòng giống nhau) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The App embeds panel in the Shopify theme editor with the Globo Product Options toggle switched on"><figcaption><p>The app embed lives in the App embeds panel of the Shopify theme editor.</p></figcaption></figure>

## Confirm it worked

Check in two places, then on your storefront.

<table><thead><tr><th width="260">Where</th><th>What you should see</th></tr></thead><tbody><tr><td><strong>Settings &gt; Theme Setup</strong></td><td>The <strong>App embed</strong> badge reads <strong>Activated</strong> for the selected theme.</td></tr><tr><td><strong>Dashboard</strong> → <strong>App embed status</strong></td><td>The badge reads <strong>Activated</strong>, and the Setup guide's step 2 is ticked.</td></tr><tr><td>Your storefront</td><td>Open a product that one of your active option sets applies to. The options render on the page.</td></tr></tbody></table>

{% hint style="success" %}
Once the badge reads **Activated** you never need to come back here — unless you publish a different theme.
{% endhint %}

## Limits and notes

* Enabling the app embed does not create or edit theme files, and does not slow your theme down when no option set applies to the page.
* The app embed only makes the app *available*. Each option set still needs to be **Active**, published to **Online Store**, and matched to the product by its product rule.
* If you work on a duplicate of your theme, enable the embed on the duplicate too before publishing it — otherwise options disappear the moment you publish.
* Turning the toggle off is a clean way to switch the app off storefront-wide without uninstalling it.

## Troubleshooting

<details>
<summary>The badge still says Deactivated after I saved in the theme editor</summary>

Make sure you selected **Save** in the theme editor — the toggle alone does not persist. Then switch back to the app tab; the app re-checks automatically when the tab becomes visible again. If it still shows **Deactivated**, reload the app page.

Also check you enabled it on the same theme the app has selected in **Theme Setup**. Enabling it on a different theme leaves the selected one **Deactivated**.
</details>

<details>
<summary>I enabled it, but options only appear on some pages</summary>

That is normal and is controlled by settings, not by the embed. Quickview, home page, and regular pages each have their own switch in **Settings > Settings > General**. See [Quickview and other pages](../storefront/quickview-and-other-pages.md).
</details>

<details>
<summary>Options disappeared after I changed themes</summary>

The new theme does not have the app embed enabled yet. Enable it on the new theme using any of the three methods above.
</details>

<details>
<summary>I cannot find App embeds in the theme editor</summary>

App embeds require an Online Store 2.0 theme. If your theme is older, the panel may not be there. Contact us and we will tell you what your theme needs — see [Contact support](../help/contact-support.md).
</details>

<details>
<summary>Options render, but in the wrong place on the product page</summary>

The embed decides *whether* the app runs, not *where* the widget goes. Change the position in **Settings > Settings > General**, or pin it exactly with an app block. See [Widget placement](../storefront/widget-placement.md) and [Add the app block](add-the-app-block.md).
</details>

## Next steps

* [Add the app block](add-the-app-block.md) — for exact control over where the widget sits.
* [Widget placement](../storefront/widget-placement.md) — the eight built-in placement options.
* [Options are not showing up](../help/troubleshooting-not-showing.md) — the full diagnostic checklist.
