---
description: >-
  Why a setting is greyed out, what the upgrade prompts mean, and the watermark on
  the free plan.
icon: lock
---

# Locked features

The app shows you everything it can do, whatever plan you are on. Features your plan does not include are visible but locked, so you can see what is available before deciding to pay for it.

That is deliberate, and it means a greyed-out field is not a fault.

## What a locked feature looks like

<table><thead><tr><th width="250">You see</th><th>It means</th></tr></thead><tbody><tr><td>A greyed-out field with an upgrade link underneath it</td><td>That individual setting needs a higher plan. The rest of the option works normally</td></tr><tr><td>An option type you cannot add, or that shows an upgrade prompt when selected</td><td>That option type is not in your plan</td></tr><tr><td>A button labelled with an upgrade prompt instead of its normal action</td><td>The action exists, but not on this plan</td></tr><tr><td>A collapsed group of settings with a count of hidden premium features</td><td>On the free plan, premium settings are folded away so the panel stays short. Expand it to see what they are</td></tr><tr><td>A banner saying you have reached a limit</td><td>You are at a plan ceiling — for example how many files a customer may upload</td></tr></tbody></table>

Selecting any of those upgrade links opens the **Pricing** page with the relevant feature in view.

<!-- SCREENSHOT: concept-locked-setting | App admin → builder → 1 setting bị khoá (ví dụ Personalizer Settings trên plan thấp) | Field mờ + link upgrade | Khoanh field bị khoá và link upgrade -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A greyed-out setting in the builder with an upgrade link beneath it"><figcaption><p>Locked settings stay visible so you can see what a higher plan would add.</p></figcaption></figure>

## A locked setting is still saved

Configuring something and then losing access to it does not erase it. The setting stays on the option; it simply stops being applied on your storefront.

That cuts both ways:

* **Upgrading** makes anything you already configured start working immediately. There is nothing to rebuild.
* **Downgrading** silently stops it working while leaving it in place, which is why [What happens when you downgrade](what-happens-on-downgrade.md) is worth reading first.

## The watermark

On plans that do not include **Remove watermarks**, a small "Powered by" credit appears beneath the widget on your storefront.

There is nothing to switch on or off: it disappears by itself on a plan that includes the feature.

## What is gated

Which features sit on which plan is on the **Pricing** page in the app, grouped exactly as [Compare plans](compare-plans.md) describes. Check there rather than assuming — the split changes as plans evolve.

## Troubleshooting

<details>
<summary>I upgraded but a setting is still greyed out</summary>

Reload the app so it picks up the new plan. If it is still locked, confirm the upgrade actually completed — a paid plan needs Shopify's charge approval screen to be finished. The **Pricing** page marks your current plan.
</details>

<details>
<summary>A feature stopped working and I changed nothing</summary>

Check whether your plan changed. A trial ending returns you to your previous plan, which switches features off without warning you at the moment it happens.
</details>

<details>
<summary>I cannot add another option set</summary>

You are at your plan's limit. Delete one you no longer use, or upgrade — the **Create option set** button shows an upgrade prompt when you are at the ceiling.
</details>

<details>
<summary>A "Powered by" line appears under my options</summary>

That is the watermark. It is removed automatically on a plan that includes <strong>Remove watermarks</strong>.
</details>
