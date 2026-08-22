---
description: What is kept, what stops working, and what to check before moving to a lower plan.
icon: arrow-down
---

# What happens when you downgrade

The short version: **your work is kept, but features the lower plan does not include stop working on your storefront immediately.**

That combination is the thing to understand. Nothing is deleted, so nothing is lost — but your live product pages change, and shoppers see the difference before you do.

## Kept and lost

<table><thead><tr><th width="290">Kept</th><th>Stops working</th></tr></thead><tbody><tr><td>All your option sets, with every option and value</td><td>Option types the new plan does not include</td></tr><tr><td>Your conditional logic rules, saved as configured</td><td>Conditional logic, if the new plan lacks it — or variant conditions, if it lacks the advanced level</td></tr><tr><td>Your add-on prices and linked products</td><td>Add-on pricing, if the new plan lacks it</td></tr><tr><td>Your Personalizer settings</td><td>The live preview, if the new plan lacks the Personalizer</td></tr><tr><td>Your customer and country rules</td><td>Those rules being applied</td></tr><tr><td>Your translations</td><td>Translated option content being served</td></tr><tr><td>Your store-wide settings</td><td>Custom styling, if the new plan lacks it</td></tr><tr><td>Your templates and automations</td><td>Automations running</td></tr><tr><td>Add-on products in your Shopify catalogue</td><td></td></tr><tr><td>Orders already placed, exactly as recorded</td><td></td></tr></tbody></table>

Upgrade again and everything in the left column resumes working without any rebuilding.

## What shoppers see

This is the part worth thinking about before you confirm.

<table><thead><tr><th width="290">If you lose</th><th>Your live product pages</th></tr></thead><tbody><tr><td>Conditional logic</td><td>Show every option all the time — including ones that only made sense in context</td></tr><tr><td>Add-on pricing</td><td>Stop charging for paid choices. Shoppers get them free</td></tr><tr><td>The Personalizer</td><td>Stop previewing on the product photo. The options still collect the same information</td></tr><tr><td>An option type</td><td>Stop showing options of that type</td></tr><tr><td>Customer or country rules</td><td>Show option sets you had restricted to certain shoppers</td></tr><tr><td>Multi-language option content</td><td>Show your primary language everywhere</td></tr><tr><td>Custom styling</td><td>Revert to the app's default appearance</td></tr><tr><td>Removing the watermark</td><td>Show a "Powered by" line under the widget</td></tr></tbody></table>

{% hint style="danger" %}
The dangerous one is **add-on pricing**. If your paid options stop charging, customers can order personalised extras for nothing, and it may be days before you notice.

If you are downgrading to a plan without add-on pricing, remove the paid options — or set the affected option sets to **Draft** — before the downgrade takes effect.
{% endhint %}

## Before you downgrade

{% stepper %}
{% step %}
### Check what the lower plan includes

On **Pricing**, compare the two columns and note every difference. See [Compare plans](compare-plans.md).
{% endstep %}

{% step %}
### Export your option sets and settings

A free backup. See [Import and export](../option-sets/import-and-export.md) and [Import and export settings](../settings/import-export-settings.md).
{% endstep %}

{% step %}
### Deal with anything that charges money

If you are losing add-on pricing, remove the paid options or draft those option sets.
{% endstep %}

{% step %}
### Check option sets that rely on conditional logic

An option set whose options are mostly hidden by rules becomes a very long form when the rules stop applying. Consider simplifying it, or drafting it.
{% endstep %}

{% step %}
### Check option sets restricted by customer or country

Without those rules they show to everybody. Draft the ones that should not.
{% endstep %}

{% step %}
### Confirm the downgrade
{% endstep %}

{% step %}
### Look at a real product page immediately

Not the builder preview. Check what shoppers are now seeing.
{% endstep %}
{% endstepper %}

## Limits as well as features

Some plans limit counts rather than features — how many option sets, how many files a customer may upload, how large a file may be.

Existing option sets are not removed to fit a lower limit. But you may not be able to create more until you are back under it, and the **Create option set** button shows an upgrade prompt when you are at the limit.

## Notes

* Configuration is never deleted by a plan change. Only what is *applied* changes.
* Upgrading restores everything immediately, with no rebuilding.
* Add-on products the app generated stay in your catalogue whatever plan you are on.
* Orders already placed are untouched. Their option details are part of the order record.
* A trial ending has the same effect as a downgrade, so the checklist above applies then too.

## Troubleshooting

<details>
<summary>My storefront changed and I did not change anything</summary>

A trial ended, returning you to your previous plan. Check which plan **Pricing** shows as current.
</details>

<details>
<summary>Paid options are no longer charging</summary>

Add-on pricing is not in your current plan. Upgrade, or remove the paid options so shoppers are not getting them free.
</details>

<details>
<summary>All my options are showing at once</summary>

Conditional logic is not being applied. The rules are still saved and resume on upgrade.
</details>

<details>
<summary>A "Powered by" line appeared</summary>

The watermark. It is removed on plans that include that feature.
</details>

<details>
<summary>Did I lose my Personalizer setup?</summary>

No. The settings are kept and resume drawing when you upgrade again.
</details>

<details>
<summary>I cannot create a new option set</summary>

You are at the lower plan's limit. Delete one you no longer use, or upgrade.
</details>
