---
description: >-
  Why a setting is greyed out, what the upgrade prompts mean, and what happens to
  your work if you change plan.
icon: lock
---

# Plans and locked features

The app shows you everything it can do, whatever plan you are on. Features your plan does not include are visible but locked, so you can see what is available before deciding to pay for it.

This page explains what the locks look like and what changing plan does to work you have already done.

## What a locked feature looks like

<table><thead><tr><th width="250">You see</th><th>It means</th></tr></thead><tbody><tr><td>A greyed-out field with an upgrade link underneath it</td><td>That individual setting needs a higher plan. The rest of the option works normally.</td></tr><tr><td>An option type you cannot add, or that shows an upgrade prompt when selected</td><td>That option type is not in your plan.</td></tr><tr><td>A button labelled with an upgrade prompt instead of its normal action</td><td>The action is available, but not on this plan.</td></tr><tr><td>A collapsed group of settings with a count of hidden premium features</td><td>On the free plan, premium settings are folded away so the panel stays short. Expand it to see what they are.</td></tr><tr><td>A banner saying you have reached a limit</td><td>You are at a plan ceiling — for example the number of files a customer may upload.</td></tr></tbody></table>

Selecting any of those upgrade links takes you to the **Pricing** page with the relevant feature in view.

<!-- SCREENSHOT: concept-locked-setting | App admin → builder → 1 setting bị khoá (ví dụ Personalizer Settings trên plan thấp) | Field mờ + link upgrade | Khoanh field bị khoá và link upgrade -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A greyed-out setting in the builder with an upgrade link beneath it"><figcaption><p>Locked settings stay visible so you can see what a higher plan would add.</p></figcaption></figure>

## What is gated

Gating falls into four groups. The exact split per plan is on the **Pricing** page in the app and in [Compare plans](../plans/compare-plans.md) — check there rather than assuming, because it changes as plans evolve.

<table><thead><tr><th width="220">Group</th><th>Examples of what can be gated</th></tr></thead><tbody><tr><td><strong>Option types</strong></td><td>Date and time picker, file upload, colour picker, hidden field, range slider, dimension, size chart, HTML, tabs, image and colour dropdowns, font picker, product links, sections.</td></tr><tr><td><strong>Option configuration</strong></td><td>Conditional logic (basic versus advanced), add-on pricing, advanced add-on modes, default values, min and max limits, character limits, date restrictions, international phone validation, swatch sliders, multi-language option content, out-of-stock handling, multiple file uploads, custom fonts, Personalizer.</td></tr><tr><td><strong>Option set rules and features</strong></td><td>Customer rules, country rules, import and export, option templates, custom widget styling, showing options in quickview, editing options in the cart, Point of Sale, analytics.</td></tr><tr><td><strong>Automations and support</strong></td><td>Email notification, order notes, and order tag workflows; priority support; removing the app's watermark from the widget.</td></tr></tbody></table>

## Changing plan

### Upgrading

Take effect immediately. Locked settings unlock, and anything you configured earlier that was being ignored starts working straight away — you do not need to rebuild anything.

### Downgrading

{% hint style="warning" %}
Downgrading does not delete your option sets. But features the lower plan does not include **stop working on your storefront**, even though they remain configured in the app.
{% endhint %}

For example, if you downgrade to a plan without conditional logic, an option that was previously hidden until a box was ticked becomes permanently visible. The rule is still saved — it simply stops being applied.

The app warns you before a downgrade goes through, because the effect on a live storefront can be immediate and visible to shoppers.

Full detail: [What happens when you downgrade](../plans/what-happens-on-downgrade.md).

## Trials

Paid plans include a 14-day free trial. During the trial you have that plan's features in full, and you are not charged until it ends. Starting a trial goes through Shopify's own charge approval screen — the charge is authorised then, not taken.

See [Change your plan](../plans/change-your-plan.md).

## The watermark

On plans that do not include **Remove watermarks**, a small "Powered by" credit appears beneath the widget on your storefront. It is removed automatically on plans that include the feature — there is nothing to switch on.

## How to check what your plan includes

{% stepper %}
{% step %}
### Open Pricing

Select **Pricing** in the app menu. Your current plan is marked and its button is disabled.
{% endstep %}

{% step %}
### Read the comparison table

Below the plan cards is a feature-by-feature table grouped into **Option Set**, **Option Config**, **Option Type**, **Features**, **Automations**, and **Support**. Each row shows what every plan gives you — a tick, a number, or a level such as basic versus advanced.
{% endstep %}

{% step %}
### Switch between Monthly and Yearly

The switch at the top changes the billing period. Feature availability does not change between monthly and yearly — only the price does.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: concept-pricing-compare | App admin → Pricing | Bảng so sánh feature theo nhóm, plan hiện tại được đánh dấu | Khoanh cột plan hiện tại -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The plan comparison table on the Pricing page with the current plan highlighted"><figcaption><p>The Pricing page is the authoritative list of what each plan includes.</p></figcaption></figure>

## Troubleshooting

<details>
<summary>I upgraded but a setting is still greyed out</summary>

Reload the app page so it picks up your new plan. If it is still locked, confirm the upgrade completed — a paid plan needs Shopify's charge approval screen to be finished. Check the **Pricing** page: your new plan should be marked as current.
</details>

<details>
<summary>A feature stopped working on my storefront and I did not change anything</summary>

Check whether your plan changed — a trial ending returns you to your previous plan, which can silently switch a feature off. Open **Pricing** to see which plan you are on now.
</details>

<details>
<summary>I cannot add another option set</summary>

You have reached your plan's limit on option sets. Either delete one you no longer use, or upgrade. The **Create option set** button shows an upgrade prompt when you are at the limit.
</details>

<details>
<summary>A "Powered by" line appears under my options</summary>

That is the watermark, shown on plans without **Remove watermarks**. Upgrading to a plan that includes it removes the line automatically.
</details>

## Next steps

* [Compare plans](../plans/compare-plans.md)
* [Change your plan](../plans/change-your-plan.md)
* [Option sets](../option-sets/README.md) — start building.
