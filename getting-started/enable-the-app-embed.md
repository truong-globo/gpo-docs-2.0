---
description: Turn on the app embed so your option sets can actually appear on the storefront.
icon: toggle-on
---

# Enable the app embed

The app renders its widget on your storefront through a Shopify **theme app embed**. Until it is turned on for your live theme, none of your option sets appear — even fully built and assigned to products.

It takes about thirty seconds, and it does not touch your theme's code.

## Steps

{% stepper %}
{% step %}
### Open Theme Setup

In the app, go to **Settings**, then the **Theme Setup** tab.

The page shows an **App embed** badge — **Activated** or **Deactivated** — for the theme selected in the dropdown below it. If you publish more than one theme, use the dropdown to check each.

<!-- SCREENSHOT: start-embed-theme-setup | App admin → Settings → Theme Setup | Dropdown chọn theme + badge Deactivated + nút Go to Theme Editor | Khoanh badge và nút Go to Theme Editor -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Theme Setup page with a theme selected, a Deactivated badge, and the Go to Theme Editor button"><figcaption><p>Theme Setup shows whether the embed is on, for the theme you select.</p></figcaption></figure>
{% endstep %}

{% step %}
### Select Go to Theme Editor

This opens Shopify's theme editor for that theme, already scoped to the app embeds section.

{% hint style="info" %}
If app embeds are new to you, **How to enabled app embed?** on the same page opens a short walkthrough.
{% endhint %}
{% endstep %}

{% step %}
### Turn on Globo Product Options

Find **Globo Product Options** in the **App embeds** list, turn its toggle on, and select **Save** in the theme editor.

The toggle alone does not persist — the save is what matters.

<!-- SCREENSHOT: start-embed-theme-editor-toggle | Shopify theme editor → App embeds | Danh sách app embeds, toggle "Globo Product Options" đang bật | Khoanh dòng Globo Product Options (mũi tên nhỏ vì nhiều dòng giống nhau) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Shopify theme editor App embeds list with Globo Product Options toggled on"><figcaption><p>Turn the toggle on, then save in the theme editor.</p></figcaption></figure>
{% endstep %}

{% step %}
### Confirm it is activated

Go back to the app tab. The **App embed** badge changes to **Activated** on its own once the app detects the change — no reload needed in most cases.

Then open a product page that one of your active option sets applies to, and check the options render.
{% endstep %}
{% endstepper %}

{% hint style="success" %}
Once the badge reads **Activated** you never need to come back here — unless you publish a different theme.
{% endhint %}

## Two things worth knowing

{% hint style="warning" %}
**The embed is per theme.** Publishing a different theme — including a duplicate of the same one — leaves the new theme without it, and your options disappear the moment you publish. If you work on a duplicate, enable the embed on the duplicate before publishing it.

This is the single most common reason options stop appearing.
{% endhint %}

{% hint style="info" %}
**Enabling the embed makes the app available; it does not display anything by itself.** Each option set still needs to be **Active**, published to **Online Store**, and matched to the product by its product rule. See [Assign to products](../option-sets/assign-to-products.md).

The reverse is also useful: turning the toggle off is a clean way to switch the app off storefront-wide, without deleting option sets or uninstalling.
{% endhint %}

## Other ways to reach the same switch

The Theme Setup route above is the one to use, because it tells you whether it worked. Two shortcuts do the same thing:

* **The Setup guide** on the app's Dashboard has an **Enable app embed** button in step 2.
* **Shopify directly**, without the app: **Online Store** > **Themes** > **Customize** > the app embeds icon in the left sidebar.

## Troubleshooting

<details>
<summary>The badge still says Deactivated after I saved</summary>

Two causes. Either **Save** was not selected in the theme editor — the toggle alone does not persist — or the embed was enabled on a different theme from the one selected in **Theme Setup**. Check the dropdown, then reload the app page.
</details>

<details>
<summary>Options disappeared after I changed themes</summary>

The new theme does not have the embed enabled. Enable it on that theme.
</details>

<details>
<summary>I cannot find App embeds in the theme editor</summary>

App embeds need an Online Store 2.0 theme. On an older theme the panel may not exist — see [Contact support](../help/contact-support.md).
</details>

<details>
<summary>It is activated, but options appear only on some pages</summary>

That is controlled by settings, not by the embed. Quickview, the home page, and regular pages each have their own switch in **Settings** > **Settings** > **General**. See [Quickview and other pages](../storefront/quickview-and-other-pages.md).
</details>
