---
description: >-
  Create an option set, add one option, assign it to your products, and see it on
  your live product page.
icon: rocket
---

# Quickstart

This is the shortest complete path through the app. Follow it end to end and you will have a working text field on your product page that customers can type into.

Give it about ten minutes. Everything you do here is reversible.

## Before you start

* The app is installed and you have chosen a plan — see [Install the app](install-the-app.md).
* You know which of your themes is live, and you can open the Shopify theme editor.
* You have a product you can open on your storefront to test with.

## Steps

{% stepper %}
{% step %}
### Create an option set

In the app menu select **Option Sets**, then **Create option set** > **Create from scratch**.

The builder opens on the **Setup flow** tab, which has two steps: **Build option** and **Assign products**. You start on **Build option**.

A new option set already contains one empty **Section**. A section is just a container that groups options together — you can ignore it for now and add your option inside it.

<!-- SCREENSHOT: start-qs-create-from-scratch | App admin → Option Sets | Nút Create option set đang mở, thấy 2 lựa chọn Create from scratch và Use a template | Khoanh "Create from scratch" (mũi tên nhỏ vì có 2 mục giống nhau) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Create option set menu open on the Option Sets page, showing Create from scratch and Use a template"><figcaption><p>Start a new option set from scratch on the Option Sets page.</p></figcaption></figure>
{% endstep %}

{% step %}
### Name the option set

At the top of the builder, replace the default name with something you will recognise later, for example `Engraving`.

This name is for you. Customers never see it — it only appears in your admin and in the option set list.

<!-- SCREENSHOT: start-qs-name | App admin → builder, mới tạo | Ô tên option set ở header đang nhập "Engraving" | Khoanh ô tên -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The option set name field in the builder header with the name Engraving typed in"><figcaption><p>The option set name is internal — it never appears on your storefront.</p></figcaption></figure>
{% endstep %}

{% step %}
### Add your first option

In the **Build option** panel, select the add button, then pick **Text** from the **Option Types** list.

The list is grouped into three families — **Input**, **Selection**, and **Static** — with 32 option types in total. **Text** is the simplest: a single-line box the customer types into. See [Option types](../option-types/README.md) for the full list.

<!-- SCREENSHOT: start-qs-add-option | App admin → builder → Build option | Popover chọn option type đang mở, thấy 3 nhóm Input / Selection / Static | Khoanh mục "Text" trong nhóm Input (mũi tên nhỏ vì danh sách dài) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The option type picker open in the builder, showing the Input, Selection, and Static groups"><figcaption><p>Option types are grouped into Input, Selection, and Static.</p></figcaption></figure>
{% endstep %}

{% step %}
### Fill in the two fields that matter

The option's settings open on the **Basic Settings** tab. Two fields decide what customers and you see:

* **Label** — the text shown above the box on your product page. Change it to `Engraving text`.
* **Name** — the internal name used on the cart, at checkout, and on the order. Change it to `Engraving text` as well.

Optionally turn on **Required field** if customers must fill it in before adding to cart.

{% hint style="info" %}
**Label** and **Name** look similar but do different jobs, and **Name** has rules — it must be unique within the option set and cannot contain `.` `:` `"` `'` `\` or `|`. See [Label and Name](../option-types/shared-settings/labels-and-visibility.md).
{% endhint %}

<!-- SCREENSHOT: start-qs-basic-settings | App admin → builder → chọn option Text | Tab Basic Settings với Label và Name đã điền "Engraving text" | Khoanh 2 field Label và Name -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="Basic Settings for a Text option with Label and Name both set to Engraving text"><figcaption><p>Label is what shoppers read; Name is what appears on the cart and the order.</p></figcaption></figure>

Look at the preview on the right — it updates as you type, so you can see exactly what shoppers will get.
{% endstep %}

{% step %}
### Choose which products it applies to

Switch to the **Assign products** step. You have three ways to decide where this option set appears:

<table><thead><tr><th width="220">Method</th><th>Use it when</th></tr></thead><tbody><tr><td><strong>Manual Selection</strong></td><td>You want it on a handful of specific products you pick by hand.</td></tr><tr><td><strong>Automatic Rules</strong></td><td>You want it on every product that matches a condition — a tag, a type, a vendor, a price, or a collection.</td></tr><tr><td><strong>Apply to All Products</strong></td><td>You want it on your whole catalogue.</td></tr></tbody></table>

For this first test, turn on **Apply to All Products**. You can narrow it down later — see [Assign to products](../option-sets/assign-to-products.md).

<!-- SCREENSHOT: start-qs-assign-products | App admin → builder → Assign products | 3 khối Manual Selection / Automatic Rules / Apply to All Products, khối Apply to All Products đang bật | Khoanh khối Apply to All Products -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Assign products step with Apply to All Products turned on"><figcaption><p>Apply to All Products is the fastest way to test; narrow it down afterwards.</p></figcaption></figure>

{% hint style="warning" %}
An option set cannot be saved unless it has **at least one option** and **a product rule turned on**. If you try, the builder jumps you back to whichever step is incomplete.
{% endhint %}
{% endstep %}

{% step %}
### Save and activate

Select **Save** in the top-right corner.

Then check the status next to the option set name. A new option set is created as **Draft**, and a draft option set does not appear on your storefront. Set it to **Active**, and make sure **Online Store** is ticked under **Sales channels**.

<!-- SCREENSHOT: start-qs-status-active | App admin → builder → menu Status | Status đặt Active, Sales channels tick Online Store | Khoanh khối Status và Sales channels -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The status menu in the builder with Active selected and Online Store ticked"><figcaption><p>An option set must be Active and published to Online Store to reach shoppers.</p></figcaption></figure>
{% endstep %}

{% step %}
### Enable the app embed

This is the step people miss. Until the app embed is switched on in your theme, nothing you built appears on the storefront — no matter how the option set is configured.

Go to **Settings** > **Theme Setup**, check that the theme shown is your live theme, and select **Go to Theme Editor**. In the theme editor, turn on the **Globo Product Options** app embed and select **Save**.

Come back to the app tab. The badge changes to **Activated** on its own within a few seconds.

Full instructions, including two other ways to do it: [Enable the app embed](enable-the-app-embed.md).
{% endstep %}

{% step %}
### Look at your storefront

Open any product page on your store. Your **Engraving text** field now appears above the **Add to cart** button.

Type something into it and add the product to your cart — the text you typed travels with the item and shows up under it on the cart page.

<!-- SCREENSHOT: start-qs-storefront | Storefront → trang sản phẩm | Field "Engraving text" hiện phía trên nút Add to cart | Khoanh riêng field do app tạo, không khoanh cả form -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="A storefront product page with the Engraving text field above the Add to cart button"><figcaption><p>The option appears above Add to cart, which is the app's default position.</p></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="success" %}
That is the whole loop: build, assign, activate, embed, verify. Everything else in these docs is a variation on it.
{% endhint %}

## What customers see

A single-line text box with your label above it, placed above the **Add to cart** button. What they type is attached to the cart line, and appears on the cart page, at checkout, and on the order in your admin.

You can move the widget somewhere else on the product page, and restyle it to match your theme — see [Widget placement](../storefront/widget-placement.md) and [Match your theme style](../storefront/match-your-theme-style.md).

## Troubleshooting

<details>
<summary>Save is not working, or the builder keeps switching tabs on me</summary>

The option set is missing something required. It needs at least one option in **Build option** and a product rule turned on in **Assign products**. The builder switches you to whichever one is missing.
</details>

<details>
<summary>I saved it but nothing appears on my product page</summary>

Check these in order:

1. Is the app embed enabled on the theme that is actually live? See [Enable the app embed](enable-the-app-embed.md).
2. Is the option set **Active**, not **Draft**?
3. Is **Online Store** ticked under **Sales channels**?
4. Does the product rule match the product you are looking at?

The full checklist is in [Options are not showing up](../help/troubleshooting-not-showing.md).
</details>

<details>
<summary>The field appears, but in an odd place on the page</summary>

The app places itself above the **Add to cart** button by default, which most themes handle well. If your theme puts it somewhere unhelpful, change the placement in **Settings > Settings > General**, or pin it exactly with an [app block](add-the-app-block.md).
</details>

<details>
<summary>I see the field twice</summary>

You most likely have both the app embed placing the widget automatically and an app block placed in your template. Pick one — see [Add the app block](add-the-app-block.md).
</details>
