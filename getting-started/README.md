---
description: >-
  Everything you need to do once, in order, to get your first custom option live
  on your storefront.
icon: flag-checkered
---

# Overview

This section takes you from an empty store to a working option on a live product page. Read the pages in order the first time — each one assumes the previous one is done.

## What has to be true before options appear

Four things. If options are not showing on your storefront, one of these is the reason.

<table><thead><tr><th width="60">#</th><th width="250">What</th><th>Why</th></tr></thead><tbody><tr><td>1</td><td>The app is installed and you have chosen a plan</td><td>On first open the app takes you to <strong>Pricing</strong> and will not let you past it until you choose. The free plan counts as a choice.</td></tr><tr><td>2</td><td>You have built an option set</td><td>The options themselves — the questions you want to ask the shopper.</td></tr><tr><td>3</td><td>That option set is <strong>Active</strong>, published to <strong>Online Store</strong>, and its product rule matches the product you are looking at</td><td>A new option set starts as <strong>Draft</strong>, and a draft never renders. The product rule is what decides which products it applies to.</td></tr><tr><td>4</td><td>The app embed is enabled on your live theme</td><td>This is what actually puts the widget on the page. Installing the app does not do it for you, and it has to be done again on every theme you publish.</td></tr></tbody></table>

{% hint style="info" %}
Steps 2 and 3 are hard to get wrong, because the builder will not let you save an option set until it has at least one option and a product rule. Step 4 is the one people miss.
{% endhint %}

## Pages in this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Install the app</strong></td><td>Install from the Shopify App Store, review permissions, and choose your plan.</td><td><a href="install-the-app.md">install-the-app.md</a></td></tr><tr><td><strong>Quickstart</strong></td><td>Build one option and get it live on a product page, in five steps.</td><td><a href="quickstart.md">quickstart.md</a></td></tr><tr><td><strong>Enable the app embed</strong></td><td>The switch that makes options appear at all, and how to confirm it worked.</td><td><a href="enable-the-app-embed.md">enable-the-app-embed.md</a></td></tr><tr><td><strong>Add the app block</strong></td><td>Optional. Pin the widget to an exact spot in your product template.</td><td><a href="add-the-app-block.md">add-the-app-block.md</a></td></tr></tbody></table>

## What you need before you begin

* A Shopify store you can install apps on. If you are a staff member, you need the **Apps** permission; if you are a collaborator, the store owner must approve app installation.
* Access to the theme you want the options to appear on. You will open the Shopify theme editor once.
* At least one product to test with. A draft product is fine for testing, as long as you can open its product page.

{% hint style="info" %}
Nothing in this section changes your theme's code. The app renders through Shopify's theme app extension system, which you switch on and off from the theme editor.
{% endhint %}
