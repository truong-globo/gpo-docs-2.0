---
description: Choose which theme to work with, and turn the app embed on or off for it.
icon: brush
---

# Theme setup

**Settings** > **Theme Setup**. One job: making sure the app is switched on in the right theme.

## What is on the page

<table><thead><tr><th width="230">Element</th><th>What it does</th></tr></thead><tbody><tr><td>Theme selector</td><td>Lists every theme in your store. Your published theme is marked <strong>(Live theme)</strong></td></tr><tr><td><strong>App embed</strong> badge</td><td><strong>Activated</strong> or <strong>Deactivated</strong> for the selected theme</td></tr><tr><td><strong>Go to Theme Editor</strong></td><td>Appears when the selected theme shows <strong>Deactivated</strong>. Opens the Shopify theme editor at the app embed</td></tr></tbody></table>

<!-- SCREENSHOT: settings-theme-setup | App admin → Settings → Theme Setup | Dropdown theme, badge App embed, nút Go to Theme Editor | Khoanh badge và nút -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Theme Setup page with a theme selected and its app embed status"><figcaption><p>Select a theme, and the badge tells you whether the app is running on it.</p></figcaption></figure>

## The app embed

The app embed is what lets the app run on your storefront. Nothing you build appears to shoppers until it is on.

It is **per theme**, which is the important part: enabling it on one theme does nothing for the others. Publish a new theme — including a duplicate of the same theme — and you must enable it again there.

Full instructions, including two other ways to do it: [Enable the app embed](../getting-started/enable-the-app-embed.md).

## Checking a theme before you publish it

The theme selector's real value is checking a theme you are **about to** publish.

{% stepper %}
{% step %}
### Select the draft theme

From the theme selector.
{% endstep %}

{% step %}
### Read the badge

If it says **Deactivated**, your options will disappear the moment you publish that theme.
{% endstep %}

{% step %}
### Enable it now

**Go to Theme Editor**, turn the app embed on, save.
{% endstep %}

{% step %}
### Preview the draft theme

Check a product page on it before publishing.
{% endstep %}
{% endstepper %}

Doing this before a theme launch avoids the most alarming version of this problem: options vanishing from a live store immediately after a redesign.

## Notes

* Enabling the embed does not edit theme files. Shopify stores it with the theme.
* Turning it off is a clean way to switch the app off storefront-wide without uninstalling.
* The badge updates by itself when you come back from the theme editor — the app re-checks when the tab becomes visible again.
* The **Dashboard** shows the same status, plus a count of any [app blocks](../getting-started/add-the-app-block.md) you have placed.

## Troubleshooting

<details>
<summary>The badge says Deactivated after I enabled it</summary>

Make sure you saved in the theme editor, and that you enabled it on the same theme the selector has chosen. Then return to the app tab, or reload it.
</details>

<details>
<summary>Options disappeared after a theme change</summary>

The new theme does not have the app embed enabled. Select it here and turn it on.
</details>

<details>
<summary>Go to Theme Editor is not shown</summary>

It only appears when the selected theme shows **Deactivated**. If it already says **Activated**, there is nothing to do.
</details>

<details>
<summary>My theme is not in the list</summary>

The list comes from your Shopify themes. If it is missing, reload the page.
</details>
