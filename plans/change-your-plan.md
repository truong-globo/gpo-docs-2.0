---
description: Start a trial, upgrade, downgrade, or move between monthly and yearly billing.
icon: arrow-up-right-dots
---

# Change your plan

All of it happens on the **Pricing** page in the app.

## Starting a trial

Paid plans include a 14-day free trial.

{% stepper %}
{% step %}
### Open Pricing

From the app menu.
{% endstep %}

{% step %}
### Choose monthly or yearly

The switch at the top. Features are the same either way; yearly is discounted.
{% endstep %}

{% step %}
### Select Start 14-day trial on the plan you want

Enter a discount code first if you have one.
{% endstep %}

{% step %}
### Approve the charge in Shopify

Shopify shows its own approval screen. Approving authorises the charge; nothing is taken until the trial ends.
{% endstep %}

{% step %}
### Build the real thing during the trial

Not a demo. Use the fourteen days to set up what you actually intend to sell, so you find out whether the plan covers it.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
The most common mistake with a trial is spending it exploring. Set up one real product properly — options, prices, conditional logic, and a test order — and you will know by day three whether the plan is right.
{% endhint %}

## Upgrading

Select the higher plan and approve the charge. It takes effect immediately.

Nothing needs rebuilding. Anything you had configured that was being ignored — a conditional rule on a plan without conditional logic, a Personalizer layer that was not drawing — starts working straight away.

## Downgrading

Select the lower plan. The app warns you first, because features your new plan does not include stop working on your storefront immediately, and that is visible to shoppers.

Your option sets are not deleted. Read [What happens when you downgrade](what-happens-on-downgrade.md) before confirming.

## Moving between monthly and yearly

Switch the toggle and select your plan again. Yearly billing is discounted, and the feature set is identical.

## Discount codes

The discount field on the **Pricing** page accepts a code before you select a plan. A code may be limited to monthly or yearly billing, and to a number of billing periods — the page tells you what it applies to when you enter it.

If a code is refused, check it has not expired and that you are on the billing period it applies to.

## Cancelling

Move to the free plan, or uninstall the app.

<table><thead><tr><th width="290">Action</th><th>Result</th></tr></thead><tbody><tr><td>Move to the free plan</td><td>Billing stops. Your option sets are kept, and features outside the free plan stop working</td></tr><tr><td>Uninstall the app</td><td>Billing stops and the app loses access to your store. Options no longer render</td></tr></tbody></table>

If you might come back, [export your option sets and settings](../option-sets/import-and-export.md) first.

## Notes

* Billing goes through Shopify and appears on your Shopify invoice.
* Any plan change needs Shopify's approval screen to be completed. Abandoning it leaves you on your current plan.
* On a new install the app requires a plan to be chosen before anything else. The free plan counts.
* When a trial ends without a change, you return to your previous plan — which can make a feature stop working without you doing anything. See [Plans and locked features](../concepts/plans-and-feature-gating.md).

## Troubleshooting

<details>
<summary>I selected a plan but nothing changed</summary>

Shopify's charge approval screen was not completed. Go back to **Pricing** and select the plan again.
</details>

<details>
<summary>A feature is still locked after upgrading</summary>

Reload the app so it picks up the new plan. Then check **Pricing** shows the new plan as current.
</details>

<details>
<summary>A feature stopped working and I changed nothing</summary>

A trial probably ended, returning you to your previous plan. Check which plan **Pricing** shows as current.
</details>

<details>
<summary>My discount code is refused</summary>

Check it has not expired, and that you are on the billing period it applies to — some apply to yearly only.
</details>

<details>
<summary>I want to try a feature without committing</summary>

Start the trial on the plan that includes it. There is no charge for fourteen days.
</details>

<details>
<summary>Will downgrading delete my work?</summary>

No. Option sets are kept. Features the lower plan does not include stop working. See [What happens when you downgrade](what-happens-on-downgrade.md).
</details>

## Next steps

* [What happens when you downgrade](what-happens-on-downgrade.md)
* [Compare plans](compare-plans.md)
* [Import and export](../option-sets/import-and-export.md) — take a backup first.
