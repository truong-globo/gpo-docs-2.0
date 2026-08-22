---
description: Options missing from your storefront — the full checklist, in the order worth working through.
icon: eye-slash
---

# Options are not showing up

The most common problem, and almost always one of six things. Work through this in order.

## The six-step checklist

{% stepper %}
{% step %}
### Is the app embed enabled on your live theme?

**Settings** > **Theme Setup**. Select your live theme and check the **App embed** badge says **Activated**.

This is the number one cause. It is per theme, so publishing a new theme — even a duplicate of the same one — turns it off again.

See [Enable the app embed](../getting-started/enable-the-app-embed.md).
{% endstep %}

{% step %}
### Is the option set Active?

A **Draft** option set never renders. On the **Option Sets** list, filter to **Draft** to catch anything you forgot to activate.

See [Status and sales channels](../concepts/status-and-sales-channels.md).
{% endstep %}

{% step %}
### Is it published to Online Store?

Check **Sales channels** on the option set. An option set published only to **Point of Sale** does not appear on your storefront.
{% endstep %}

{% step %}
### Does its product rule match this product?

Open the option set, go to **Assign products**, and check the rule against the product you are looking at.

For an automatic rule, use **Preview matching products** to see exactly what it catches. See [Assign to products](../option-sets/assign-to-products.md).
{% endstep %}

{% step %}
### Do the customer and country rules match you?

Both default to everybody, but if you set them:

* A **Customers** rule using tags, name, or email can never match a visitor who is not signed in
* A **Countries** rule set to **Include** with the wrong countries excludes you

Set both back to their defaults temporarily. If the options appear, you have found it. See [Assign to customers](../option-sets/assign-to-customers.md) and [Assign to countries](../option-sets/assign-to-countries.md).
{% endstep %}

{% step %}
### Does the option set actually contain options?

An option set with sections but nothing inside them cannot be saved — but one whose only options are **hidden** saves fine and renders nothing.

Check for options with the **Hide** action applied. See [Build your options](../option-sets/build-options.md).
{% endstep %}
{% endstepper %}

{% hint style="success" %}
If all six are correct and options still do not appear, it is worth reporting rather than working around. Include your theme name, the option set name, and a link to the product page. See [Contact support](contact-support.md).
{% endhint %}

## Partly missing rather than entirely missing

<details>
<summary>Some options appear and others do not</summary>

Three causes, in order of likelihood:

1. **Conditional logic** is hiding them. Check the rules on the missing options — see [Troubleshooting conditional logic](../conditional-logic/troubleshooting.md).
2. **The Hide action** is applied to them.
3. **Your plan** does not include those option types, so they are configured but not rendered. See [Plans and locked features](../concepts/plans-and-feature-gating.md).

</details>

<details>
<summary>Options appear on product pages but not in quickview</summary>

Turn on **Show options on Quickview popups** in **Settings** > **Settings** > **General**. If it is already on, your theme's quickview may not be one the app recognises — report it with your theme name.

See [Quickview and other pages](../storefront/quickview-and-other-pages.md).

</details>

<details>
<summary>Options appear on product pages but not on my home page</summary>

Featured product sections need two things: the [app block](../getting-started/add-the-app-block.md) placed in that section, and **Show widget on home page** on in **Settings** > **Settings** > **General**.

</details>

<details>
<summary>Options do not appear in POS</summary>

Tick **Point of Sale** under the option set's **Sales channels**, and check the option types you used are supported there — [Dimension](../option-types/input-types/dimension.md) and [Product links](../option-types/selection-types/product-links.md) are not. See [POS limitations](../pos/limitations.md).

</details>

<details>
<summary>Options appear twice</summary>

Two causes:

1. **Two active option sets** both match the product. Filter the list to **Active** and check which could apply — especially any using **Apply to All Products**.
2. **Automatic placement and an app block** are both placing the widget. Remove one.

</details>

## Appearing, but wrong

<details>
<summary>The widget is in an odd place on the page</summary>

Change **Widget placement** in **Settings** > **Settings** > **General**, or pin it with an [app block](../getting-started/add-the-app-block.md). See [Widget placement](../storefront/widget-placement.md).

</details>

<details>
<summary>The widget appears late, after the page has loaded</summary>

Usually a speed or script optimisation app deferring the app's scripts. Add the app to its exclusion list. See [Theme and third-party notes](../integrations/theme-and-third-party-notes.md).

</details>

<details>
<summary>It looks nothing like my theme</summary>

Turn on **Match theme style** in **Settings** > **Design**, then adjust colours and typography. See [Match your theme style](../storefront/match-your-theme-style.md).

</details>

<details>
<summary>Options disappeared after a theme change</summary>

The new theme does not have the app embed enabled. That is step one above.

</details>

<details>
<summary>Options disappeared and I changed nothing</summary>

Two possibilities: a trial ended, returning you to a plan without those features — check **Pricing**; or somebody published a different theme.

</details>

## What to send if you contact us

<table><thead><tr><th width="290">Include</th><th>Why</th></tr></thead><tbody><tr><td>Your theme's name</td><td>Most rendering problems are theme-specific</td></tr><tr><td>The option set's name</td><td>So we can look at the right one</td></tr><tr><td>A link to the product page</td><td>So we can see what you see</td></tr><tr><td>Your storefront password, if the store is protected</td><td>Otherwise we cannot open the page</td></tr><tr><td>Which of the six steps above you have checked</td><td>Saves a round trip</td></tr></tbody></table>

## Next steps

* [Pricing and add-on problems](troubleshooting-pricing.md)
* [Cart and checkout problems](troubleshooting-cart-checkout.md)
* [Contact support](contact-support.md)
