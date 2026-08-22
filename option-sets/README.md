---
description: >-
  Everything about building, targeting, and managing the option sets that power
  your product forms.
icon: layer-group
---

# Overview

An **option set** is the unit of work in this app. It holds your options, and it holds the rules that decide which products, customers, and countries they appear for. You will spend most of your time in this section.

## The anatomy of an option set

<table><thead><tr><th width="220">Part</th><th>What it decides</th><th width="200">Where it lives</th></tr></thead><tbody><tr><td>Name</td><td>How you recognise it in your admin. Customers never see it.</td><td>Builder header</td></tr><tr><td>Options</td><td>What you ask the customer for.</td><td><strong>Setup flow</strong> → <strong>Build option</strong></td></tr><tr><td>Product rule</td><td>Which products it appears on. Required.</td><td><strong>Setup flow</strong> → <strong>Assign products</strong></td></tr><tr><td>Customer rule</td><td>Which shoppers see it. Optional.</td><td><strong>Customers</strong> tab</td></tr><tr><td>Country rule</td><td>Which countries it appears in. Optional.</td><td><strong>Countries</strong> tab</td></tr><tr><td>Status</td><td>Whether it is live at all.</td><td>Builder header</td></tr><tr><td>Sales channels</td><td>Storefront, POS, or both.</td><td>Builder header</td></tr></tbody></table>

{% hint style="warning" %}
Two of those are mandatory: an option set needs **at least one option** and **a product rule that is turned on** before it can be saved.
{% endhint %}

## The four levels

Almost every question about where a setting lives is answered by knowing which level it belongs to.

```text
Option set  ──  "Bracelet personalization"
│               applies to: products tagged "engravable"
│               status: Active · Online Store, Point of Sale
│
├── Section  ──  "Personalize your bracelet"
│   │
│   ├── Option  ──  "Engraving text"  (Text)
│   │                required: no · max 20 characters · +$5.00
│   │
│   └── Option  ──  "Gift wrap"  (Checkbox)
│       │
│       └── Option value  ──  "Yes, wrap it as a gift"   +$3.00
│
└── Option  ──  "Gift message"  (Textarea)
                 shown only when Gift wrap is ticked
```

<table><thead><tr><th width="200">Level</th><th>Settings that live here</th></tr></thead><tbody><tr><td><strong>Whole store</strong></td><td>Where the widget appears, colours, borders, typography, custom CSS, how add-on prices are displayed, widget text and validation messages, custom fonts. All in <strong>Settings</strong>, and they apply to every option set</td></tr><tr><td><strong>Option set</strong></td><td>Name, status, sales channels, product rule, customer rule, country rule, and the personalizer background</td></tr><tr><td><strong>Option</strong></td><td>Type, label, name, required, help text, placeholder, limits, layout, column width, conditional logic, add-on settings, personalizer settings</td></tr><tr><td><strong>Option value</strong></td><td>The value text, its own help text, its own add-on price or add-on product, and its colour or image on swatch-style options</td></tr></tbody></table>

{% hint style="info" %}
A common mix-up: colours and fonts are **store-wide**, not per option set. To make two option sets look different from each other, use [custom CSS](../storefront/custom-css.md) with the **HTML class** setting on an option — not separate colour settings, because there are none.
{% endhint %}

## Pages in this section

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Create an option set</strong></td><td>From an empty builder to a saved, live option set.</td><td><a href="create-an-option-set.md">create-an-option-set.md</a></td></tr><tr><td><strong>Build your options</strong></td><td>Adding, changing, duplicating, hiding, reordering, and grouping options.</td><td><a href="build-options.md">build-options.md</a></td></tr><tr><td><strong>Working with option values</strong></td><td>Adding, bulk-adding, reordering, and the characters you cannot use.</td><td><a href="option-values.md">option-values.md</a></td></tr><tr><td><strong>Live preview and inspector</strong></td><td>Test your form without leaving the app, and edit by clicking the preview.</td><td><a href="live-preview-and-inspector.md">live-preview-and-inspector.md</a></td></tr><tr><td><strong>Assign to products</strong></td><td>The three targeting methods, and how automatic rules work.</td><td><a href="assign-to-products.md">assign-to-products.md</a></td></tr><tr><td><strong>Assign to customers</strong></td><td>Show options only to certain shoppers, or only to logged-in ones.</td><td><a href="assign-to-customers.md">assign-to-customers.md</a></td></tr><tr><td><strong>Assign to countries</strong></td><td>Include or exclude countries.</td><td><a href="assign-to-countries.md">assign-to-countries.md</a></td></tr><tr><td><strong>Status and sales channels</strong></td><td>Active vs Draft, Online Store vs Point of Sale, and why a set can be invisible.</td><td><a href="status-and-sales-channels.md">status-and-sales-channels.md</a></td></tr><tr><td><strong>Manage option sets</strong></td><td>The list page: search, filter, sort, and bulk actions.</td><td><a href="manage-option-sets.md">manage-option-sets.md</a></td></tr><tr><td><strong>Duplicate and delete</strong></td><td>Copy a set as a starting point, or remove one for good.</td><td><a href="duplicate-and-delete.md">duplicate-and-delete.md</a></td></tr><tr><td><strong>Import and export</strong></td><td>Move option sets between stores, and migrate from another options app.</td><td><a href="import-and-export.md">import-and-export.md</a></td></tr><tr><td><strong>Option set analytics</strong></td><td>What an option set earned you, and which choices customers actually pick.</td><td><a href="analytics.md">analytics.md</a></td></tr></tbody></table>

## How many option sets should I have?

There is no limit, so the answer is whatever keeps your admin readable. Two patterns work well:

**One set per product family.** A set for engravable jewellery, a set for printed t-shirts, a set for framed prints. Each targeted with an automatic rule on a product tag. This is the usual choice.

**One store-wide set, plus specific ones.** A small set applying to all products for things like delivery notes, plus focused sets for the products that need more. Remember that several option sets can apply to the same product at once — they all render.

What to avoid is one giant set with conditional logic doing all the work. It is harder to reason about, harder to hand over to a colleague, and slower on the product page.
