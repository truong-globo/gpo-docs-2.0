---
description: >-
  Five steps from an empty app to a working option on your live product page,
  in under ten minutes.
icon: rocket
---

# Quickstart

The shortest complete path through the app. At the end you will have a text field on your product page that customers can type into, and what they type will reach your orders.

Everything here is reversible.

## Before you start

* The app is installed and you have chosen a plan — see [Install the app](install-the-app.md).
* You know which of your themes is live, and you can open the Shopify theme editor.
* You have a product you can open on your storefront to test with.

## Steps

{% stepper %}
{% step %}
### Create an option set and name it

**Option Sets** > **Create option set** > **Create from scratch**.

Replace the default name in the builder header with something you will recognise — `Engraving` will do. The name is internal; customers never see it.

The builder opens on **Build option**, with one empty **Section** already in place. A section is just a container — add your option inside it.

<!-- SCREENSHOT: start-qs-create-from-scratch | App admin → Option Sets | Nút Create option set đang mở, thấy 2 lựa chọn Create from scratch và Use a template | Khoanh "Create from scratch" (mũi tên nhỏ vì có 2 mục giống nhau) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Create option set menu open on the Option Sets page, showing Create from scratch and Use a template"><figcaption><p>Start a new option set from scratch on the Option Sets page.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add a Text option and label it

Select the add button and pick **Text** — the simplest of the 32 [option types](../option-types/README.md): a single-line box.

On **Basic Settings**, two fields matter:

* **Label** — what shoppers read above the box. Set it to `Engraving text`.
* **Name** — what appears on the cart, at checkout, and on the order. Set it to `Engraving text` too.

The preview on the right updates as you type.

<!-- SCREENSHOT: start-qs-add-option | App admin → builder → Build option | Popover chọn option type đang mở, thấy 3 nhóm Input / Selection / Static | Khoanh mục "Text" trong nhóm Input (mũi tên nhỏ vì danh sách dài) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The option type picker open in the builder, showing the Input, Selection, and Static groups"><figcaption><p>Option types are grouped into Input, Selection, and Static.</p></figcaption></figure>

{% hint style="info" %}
**Name** has rules that **Label** does not: it must be unique within the option set, and it cannot contain `.` `:` `"` `'` `\` or `|`. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).
{% endhint %}

<!-- SCREENSHOT: start-qs-basic-settings | App admin → builder → chọn option Text | Tab Basic Settings với Label và Name đã điền "Engraving text" | Khoanh 2 field Label và Name -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="Basic Settings for a Text option with Label and Name both set to Engraving text"><figcaption><p>Label is what shoppers read; Name is what appears on the cart and the order.</p></figcaption></figure>
{% endstep %}

{% step %}
### Assign it to your products

Switch to **Assign products** and turn on **Apply to All Products**.

That is the fastest way to test. The other two methods — picking products by hand, or matching a tag, type, vendor, price, or collection — are what you will actually use in production. See [Assign to products](../option-sets/assign-to-products.md).

<!-- SCREENSHOT: start-qs-assign-products | App admin → builder → Assign products | 3 khối Manual Selection / Automatic Rules / Apply to All Products, khối Apply to All Products đang bật | Khoanh khối Apply to All Products -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Assign products step with Apply to All Products turned on"><figcaption><p>Apply to All Products is the fastest way to test; narrow it down afterwards.</p></figcaption></figure>

{% hint style="warning" %}
An option set will not save without **at least one option** and **a product rule turned on**. If either is missing, the builder jumps you back to that step.
{% endhint %}
{% endstep %}

{% step %}
### Save it as Active

Select **Save**, then set the status beside the option set name to **Active** and tick **Online Store** under **Sales channels**.

A new option set is created as **Draft**, and a draft never appears on your storefront.

<!-- SCREENSHOT: start-qs-status-active | App admin → builder → menu Status | Status đặt Active, Sales channels tick Online Store | Khoanh khối Status và Sales channels -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The status menu in the builder with Active selected and Online Store ticked"><figcaption><p>An option set must be Active and published to Online Store to reach shoppers.</p></figcaption></figure>
{% endstep %}

{% step %}
### Enable the app embed

**This is the step people miss.** Until the app embed is on in your theme, nothing you built appears on the storefront — however the option set is configured.

Go to **Settings** > **Theme Setup**, confirm the theme shown is your live one, and select **Go to Theme Editor**. Turn on the **Globo Product Options** app embed and select **Save**.

Back in the app tab, the badge changes to **Activated** by itself within a few seconds.

Two other ways to do this, and how to confirm it worked: [Enable the app embed](enable-the-app-embed.md).
{% endstep %}
{% endstepper %}

## See it on your storefront

Open any product page. Your **Engraving text** field is there, above the **Add to cart** button — the app's default position.

Type something in and add the product to your cart. The text travels with the item and appears under it on the cart page, at checkout, and on the order in your Shopify admin.

<!-- SCREENSHOT: start-qs-storefront | Storefront → trang sản phẩm | Field "Engraving text" hiện phía trên nút Add to cart | Khoanh riêng field do app tạo, không khoanh cả form -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A storefront product page with the Engraving text field above the Add to cart button"><figcaption><p>The option appears above Add to cart, which is the app's default position.</p></figcaption></figure>

{% hint style="success" %}
That is the whole loop: **build → assign → activate → embed → verify**. Everything else in these docs is a variation on it.
{% endhint %}

You can move the widget elsewhere on the page and restyle it to match your theme — see [Widget placement](../storefront/widget-placement.md) and [Match your theme style](../storefront/match-your-theme-style.md).

## Troubleshooting

<details>
<summary>Save is not working, or the builder keeps switching tabs on me</summary>

The option set is missing something required: at least one option in **Build option**, and a product rule turned on in **Assign products**. The builder switches you to whichever is missing.
</details>

<details>
<summary>I saved it but nothing appears on my product page</summary>

Check these in order:

1. Is the app embed enabled on the theme that is actually live? See [Enable the app embed](enable-the-app-embed.md).
2. Is the option set **Active**, not **Draft**?
3. Is **Online Store** ticked under **Sales channels**?
4. Does the product rule match the product you are looking at?

The full checklist is in [Options are not showing up](../help/troubleshooting.md).
</details>

<details>
<summary>The field appears, but in an odd place on the page</summary>

Change the placement in **Settings > Settings > General**, or pin it exactly with an [app block](add-the-app-block.md).
</details>

<details>
<summary>I see the field twice</summary>

You most likely have both automatic placement and an app block placing the widget. Pick one — see [Add the app block](add-the-app-block.md).
</details>
