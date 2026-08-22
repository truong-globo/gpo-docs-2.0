---
description: >-
  Install Globo Product Options, Variant from the Shopify App Store, approve the
  permissions it needs, and choose your plan.
icon: download
---

# Install the app

Installing takes about two minutes. At the end of it the app is in your Shopify admin, you have chosen a plan, and you are looking at the app dashboard.

## Before you start

* You need permission to install apps on the store. Staff members need the **Apps** permission; collaborators need the store owner to approve the install.
* Nothing on your storefront changes during install. Options appear later, after you [enable the app embed](enable-the-app-embed.md).

## Steps

{% stepper %}
{% step %}
### Find the app in the Shopify App Store

Either open the listing directly at [apps.shopify.com/product-options-pro](https://apps.shopify.com/product-options-pro), or from your Shopify admin go to **Apps** > **Shopify App Store** and search for **Globo Product Options**.

Make sure you are signed in to the correct store before installing — the App Store installs into whichever store you are currently signed in to.

<!-- SCREENSHOT: start-appstore-listing | Shopify App Store, trang listing "Globo Product Options, Variant" | Tiêu đề app + nút Install | Khoanh nút Install -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Globo Product Options, Variant listing in the Shopify App Store with the Install button"><figcaption><p>Install the app from its Shopify App Store listing.</p></figcaption></figure>
{% endstep %}

{% step %}
### Install and approve the permissions

Select **Install**. Shopify shows you a summary of what the app will be able to access and asks you to confirm.

This screen comes from Shopify, not from the app. Read it, then select **Install** again to confirm. See [What the app can access](#what-the-app-can-access) below for what each item is used for.
{% endstep %}

{% step %}
### Choose your plan

The app opens on the **Pricing** page. On a brand-new install you must choose a plan before you can use anything else — the app sends you back to this page until you do.

* Use the **Monthly** / **Yearly** switch at the top to compare billing periods. Yearly billing is discounted.
* On the free plan the button reads **Continue as Free**. Select it to carry on without a charge.
* On a paid plan the button reads **Start 14-day trial**. Select it to begin the trial. Shopify shows you its own approval screen for the recurring charge — you are not billed until the trial ends.
* If you were given a discount code, enter it in the discount field before choosing a paid plan.

<!-- SCREENSHOT: start-pricing-first-run | App admin → Pricing, lần đầu cài | 4 plan card + switch Monthly/Yearly + nút "Continue as Free" và "Start 14-day trial" | Khoanh switch Monthly/Yearly và 1 nút Start 14-day trial (có mũi tên nhỏ vì nhiều card giống nhau) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Pricing page shown on first install, with plan cards and the monthly and yearly switch"><figcaption><p>On a new install the app opens on Pricing and asks you to choose a plan before anything else.</p></figcaption></figure>

{% hint style="info" %}
Choosing the free plan now does not lock you in. You can start a trial or upgrade at any time from **Pricing** — see [Change your plan](../plans/change-your-plan.md).
{% endhint %}
{% endstep %}

{% step %}
### Land on the dashboard

After you pick a plan the app opens the **Dashboard**. At the top is the **Setup guide** card with three steps and a progress bar:

1. **Create your first option set**
2. **Make options visible on your storefront** (this is the app embed)
3. **Customize the widget**

The card ticks each step off as you complete it. You can collapse it, and close it once you are done with it.

<!-- SCREENSHOT: start-dashboard-setup-guide | App admin → Dashboard | Setup guide card mở, thấy 3 step + progress "0 / 3 completed" | Khoanh riêng card Setup guide -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Setup guide card on the dashboard showing three steps and a progress bar"><figcaption><p>The Setup guide tracks the three things you need to do after installing.</p></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="success" %}
The app is installed when you can see the Dashboard. Nothing is visible to shoppers yet — continue with the [Quickstart](quickstart.md).
{% endhint %}

## What the app can access

Shopify asks you to approve this access during install. Here is what each item is for.

<table><thead><tr><th width="250">Access</th><th>What the app uses it for</th></tr></thead><tbody><tr><td>Products</td><td>Showing your products and variants in the pickers when you assign an option set or link an add-on product, and creating add-on products when you ask the app to generate one for you.</td></tr><tr><td>Themes</td><td>Checking whether the app embed is enabled on a theme, and listing your themes on the <strong>Theme Setup</strong> page.</td></tr><tr><td>Files</td><td>Storing the images you upload for image swatches, custom preview backgrounds, and personalization shapes, and the fonts you upload.</td></tr><tr><td>Draft orders</td><td>Supporting flows that build a draft order instead of a normal checkout, such as quote requests.</td></tr><tr><td>Orders</td><td>Reading order details so the app can show option data and power analytics.</td></tr><tr><td>Store languages</td><td>Listing your storefront languages so you can translate option content per language.</td></tr><tr><td>Sales channels</td><td>Publishing an option set to the Online Store and Point of Sale channels, and publishing add-on products it generates.</td></tr><tr><td>Storefront product data</td><td>Reading up-to-date variant and inventory data on the storefront so out-of-stock handling and pricing previews are correct.</td></tr><tr><td>Cart pricing</td><td>Applying add-on prices to the cart at checkout so the customer is charged the correct total. See <a href="../add-on-pricing/how-pricing-is-applied.md">How pricing is applied</a>.</td></tr></tbody></table>

Some access is requested later, only if you use the feature that needs it:

* **Order permissions** are requested the first time you open **Automations**, because workflows read order details in order to run.
* **Customer permissions** are requested the first time you pick specific customers in a customer rule.

In both cases the app shows you what it is asking for and you approve it in Shopify, exactly like the original install.

## Limits and notes

* Installing does not add, remove, or edit any of your theme files.
* Installing does not create products. Products are only created if you later choose the **Automatically generate product** add-on mode — see [Automatically generate a product](../add-on-pricing/auto-generate-a-product.md).
* The plan you choose controls which option types and features are available. Locked items still appear in the app, greyed out, with an upgrade prompt — see [Locked features](../plans/locked-features.md).

## Troubleshooting

<details>
<summary>The app keeps sending me back to the Pricing page</summary>

That is expected until a plan is selected. Choose **Continue as Free** or start a trial on a paid plan. If you selected a paid plan but did not finish Shopify's charge approval screen, the selection did not complete — go back to **Pricing** and select the plan again.
</details>

<details>
<summary>I cannot install the app — Shopify says I do not have permission</summary>

You are signed in as a staff member or collaborator without app installation rights. Ask the store owner to install the app, or to grant you the **Apps** permission in **Settings > Users and permissions**.
</details>

<details>
<summary>I installed it but I do not see it in my admin</summary>

Go to **Apps** in your Shopify admin — installed apps are listed there. If you use the search bar at the top of Shopify admin, search for the app name and open it from the results.
</details>

<details>
<summary>I installed it on the wrong store</summary>

Uninstall it from that store's **Apps** page, sign in to the correct store, then install again. Uninstalling removes the app's access to that store.
</details>
