---
description: Start a trial, switch plans, apply a discount code, and understand what a downgrade changes.
icon: arrow-up-right-dots
---

# Change your plan

Open **Pricing** in the app. Every plan is listed side by side, with your current one marked.

## The controls on the Pricing page

<table><thead><tr><th width="230">Control</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Monthly</strong> / <strong>Yearly</strong> switch</td><td>Changes the billing period. Yearly is discounted; feature availability is identical either way</td></tr><tr><td>Discount code field</td><td>Enter a code, if you were given one, before switching</td></tr><tr><td>The button on each plan</td><td>Reads <strong>Start 14-day trial</strong>, <strong>Upgrade</strong>, <strong>Downgrade</strong>, or <strong>Current plan</strong>, depending on where that plan sits relative to yours</td></tr></tbody></table>

<!-- SCREENSHOT: plan-choose-your-plan | App admin → Pricing | Các plan card cạnh nhau, switch Monthly/Yearly, ô discount code, plan hiện tại hiện "Current plan" | Khoanh nút hành động trên 1 plan (mũi tên nhỏ vì nhiều card giống nhau) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Pricing page with plan cards side by side, the billing period switch, and a discount code field"><figcaption><p>Compare plans and change billing period from one page.</p></figcaption></figure>

Selecting a plan opens Shopify's own billing confirmation before the change takes effect. Nothing is charged until you approve it there.

## Trials

Paid plans include a **14-day free trial**. During the trial you have all of that plan's features and you are not charged. Starting a trial still goes through Shopify's charge approval, where the charge is authorized but not taken.

Two things to do during a trial:

* Build your real option sets rather than test ones. If you only experiment, you reach the end of the trial without knowing whether the plan suits you.
* Note the end date. There is no warning as the trial expires, and when it does you return to your previous plan.

## Upgrading

An upgrade takes effect immediately. Locked settings are unlocked, and anything you configured earlier that was not being applied starts working. There is nothing to rebuild.

If a setting still appears locked, reload the app so it reads the new plan.

## Downgrading

{% hint style="warning" %}
Downgrading does not delete anything, but features the lower plan does not include **stop working on your storefront immediately**, even though they are still configured in the app.

An option that was hidden until a box was selected becomes permanently visible. Customer and country rules stop restricting who sees an option set. Most importantly, **add-on charges stop being applied**, so the option still appears but is no longer charged.
{% endhint %}

Before you downgrade:

{% stepper %}
{% step %}
### Check what the lower plan includes

On **Pricing**, compare the lower plan against the features your live option sets use.
{% endstep %}

{% step %}
### Export your option sets

A CSV export takes a few seconds and gives you a file to restore from. See [Import and export](../option-sets/import-and-export.md).
{% endstep %}

{% step %}
### Handle priced options first

If add-on pricing is not included in the lower plan, remove or restructure those options rather than leaving them uncharged.
{% endstep %}

{% step %}
### Check a real product page immediately afterwards

Do not use the builder preview. Open a product the option set applies to and check that it behaves as you expect.
{% endstep %}
{% endstepper %}

## Cancelling

Uninstalling the app from Shopify admin ends the subscription. Your option sets stop appearing on your storefront, and add-on products the app generated remain in your Shopify catalog as normal products. See [Permissions and data](../reference/permissions-and-data.md).
