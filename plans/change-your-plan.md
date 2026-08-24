---
description: Start a trial, switch plans, apply a discount code, and what a downgrade does to your work.
icon: arrow-up-right-dots
---

# Change your plan

Open **Pricing** in the app. Every plan is listed side by side, with your current one marked.

## The controls on that page

<table><thead><tr><th width="230">Control</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Monthly</strong> / <strong>Yearly</strong> switch</td><td>Changes the billing period. Yearly is discounted; feature availability is identical either way</td></tr><tr><td>Discount code field</td><td>Enter a code, if you were given one, before switching</td></tr><tr><td>The button on each plan</td><td>Reads <strong>Start 14-day trial</strong>, <strong>Upgrade</strong>, <strong>Downgrade</strong>, or <strong>Current plan</strong>, depending on where that plan sits relative to yours</td></tr></tbody></table>

<!-- SCREENSHOT: plan-choose-your-plan | App admin → Pricing | Các plan card cạnh nhau, switch Monthly/Yearly, ô discount code, plan hiện tại hiện "Current plan" | Khoanh nút hành động trên 1 plan (mũi tên nhỏ vì nhiều card giống nhau) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Pricing page with plan cards side by side, the billing period switch, and a discount code field"><figcaption><p>Compare plans and change billing period from one page.</p></figcaption></figure>

Selecting a plan's button takes you through Shopify's own billing confirmation before anything takes effect. Nothing is charged until you approve it there.

## Trials

Paid plans include a **14-day free trial**. During it you have that plan's features in full and you are not charged. Starting a trial still goes through Shopify's charge approval — the charge is authorised then, not taken.

Two things worth doing during a trial:

* Build the real thing, not a test. If you spend the trial experimenting, you reach the end without knowing whether the plan suits you.
* Note when it ends. Nothing warns you as the trial expires, and when it does you return to your previous plan.

## Upgrading

Takes effect immediately. Locked settings unlock, and anything you configured earlier that was being ignored starts working straight away. There is nothing to rebuild.

If a setting still looks locked, reload the app so it picks up the new plan.

## Downgrading

{% hint style="warning" %}
Downgrading does not delete anything. But features the lower plan does not include **stop working on your storefront immediately**, even though they remain configured in the app.

An option that was hidden until a box was ticked becomes permanently visible. Customer and country rules stop restricting who sees a set. Most seriously, **add-on charges stop being applied** — the option still appears, and you stop being paid for it.
{% endhint %}

Before you downgrade:

{% stepper %}
{% step %}
### Check what the lower plan includes

On **Pricing**, against the features your live option sets actually rely on.
{% endstep %}

{% step %}
### Export your option sets

A CSV export costs seconds and gives you something to restore from. See [Import and export](../option-sets/import-and-export.md).
{% endstep %}

{% step %}
### Deal with anything that charges money first

If add-on pricing will not survive the downgrade, remove or restructure those options rather than leaving them selling for free.
{% endstep %}

{% step %}
### Look at a real product page immediately afterwards

Not the builder preview. Open a product the option set applies to and check it behaves as you now expect.
{% endstep %}
{% endstepper %}

## Cancelling

Uninstalling the app from Shopify admin ends the subscription. Your option sets stop rendering, and add-on products the app generated stay in your Shopify catalogue as ordinary products. See [Permissions and data](../reference/permissions-and-data.md).
