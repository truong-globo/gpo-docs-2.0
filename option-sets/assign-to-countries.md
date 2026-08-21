---
description: >-
  Show or hide an option set depending on the country a shopper is browsing
  from.
icon: earth-americas
---

# Assign to countries

Some options only make sense in some markets: a delivery-date picker where you deliver yourself, engraving in a language your local workshop can produce, a customs declaration field for exports only.

The **Countries** tab handles that with a single include-or-exclude list.

## Before you start

* An option set is open in the builder. Select **Countries** in the left rail.
* Country rules are plan-gated. If **Country restrictions** is unavailable, see [Compare plans](../plans/compare-plans.md).
* Country restrictions are **off** by default, meaning the option set appears in every country.

## Steps

{% stepper %}
{% step %}
### Turn on Country restrictions

The block expands with two choices and a country selector.
{% endstep %}

{% step %}
### Choose Include or Exclude

<table><thead><tr><th width="180">Choice</th><th>Behaviour</th></tr></thead><tbody><tr><td><strong>Include</strong></td><td>Show the option set <strong>only</strong> in the countries you select. Everywhere else, it does not render.</td></tr><tr><td><strong>Exclude</strong></td><td>Show the option set <strong>everywhere except</strong> the countries you select.</td></tr></tbody></table>

Pick whichever gives you the shorter list. Two countries in, or two countries out — same result, less typing.
{% endstep %}

{% step %}
### Select countries

Use the country field to search and select. Search by name and select as many as you need; selected countries appear as removable entries.
{% endstep %}

{% step %}
### Save

Select **Save**. The rule takes effect on the next storefront page load.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: set-countries-panel | App admin → builder → tab Countries | Country restrictions đang bật, chọn Include, đã chọn vài quốc gia | Khoanh 2 radio Include/Exclude và ô chọn quốc gia -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Countries tab with country restrictions enabled, Include selected, and several countries chosen"><figcaption><p>One switch, one choice, one list — country targeting is deliberately simple.</p></figcaption></figure>

## Worked examples

<table><thead><tr><th width="330">You want</th><th>Set up</th></tr></thead><tbody><tr><td>A delivery-date picker only where you deliver</td><td><strong>Include</strong> — your delivery countries</td></tr><tr><td>No engraving on exports, because of lead times</td><td><strong>Include</strong> — your home country only</td></tr><tr><td>Everything except two countries you cannot ship personalised goods to</td><td><strong>Exclude</strong> — those two countries</td></tr><tr><td>Local pickup options for one country</td><td><strong>Include</strong> — that country</td></tr><tr><td>A customs declaration field for international orders only</td><td><strong>Exclude</strong> — your home country</td></tr></tbody></table>

## How the country is determined

The country comes from the storefront's localisation — the country or market the visitor is currently browsing in, which Shopify decides from their location and from any country selector your theme offers.

That has two consequences worth knowing:

* It is the **browsing** country, not a shipping address. The shopper has not reached checkout yet, so there is no address to read.
* A shopper who switches country in your theme's country selector switches which option sets they see, on the next page load.

{% hint style="info" %}
If your store uses Shopify Markets, this rule works alongside it. Markets controls pricing and availability; this rule controls whether your option set renders. They are independent — a country can be in an active market and still be excluded here.
{% endhint %}

## Limits and notes

* Country restrictions narrow an option set; they never widen it. The product rule still decides which products are in scope.
* With **Include** selected and no countries chosen, the option set has nowhere to appear. Either select countries or turn the restriction off.
* The builder's live preview does not apply country rules. Test on your storefront, switching country with your theme's country selector.
* Country rules apply to the Online Store. POS orders are taken in person, so a country restriction is not a meaningful filter there.

## Troubleshooting

<details>
<summary>My option set disappeared everywhere</summary>

You likely have **Include** on with no countries selected, or with only countries you are not browsing from. Turn **Country restrictions** off to confirm the set reappears, then rebuild the list.
</details>

<details>
<summary>The rule does not seem to apply when I test it</summary>

You are probably still browsing as your own country. Use your theme's country selector to switch, then reload the product page. Testing in the builder preview will not work — country rules are only evaluated on the storefront.
</details>

<details>
<summary>I want to target by currency or language instead</summary>

Not supported — the rule is by country. For language, translate the option content instead so the same set reads correctly everywhere. See [Translate option content](../translations/translate-option-content.md).
</details>

<details>
<summary>Country restrictions is greyed out</summary>

The feature is not included in your plan. See [Compare plans](../plans/compare-plans.md).
</details>

## Next steps

* [Manage option sets](manage-option-sets.md)
* [Assign to customers](assign-to-customers.md)
* [Translate option content](../translations/translate-option-content.md) — often the better answer for a multi-country store.
