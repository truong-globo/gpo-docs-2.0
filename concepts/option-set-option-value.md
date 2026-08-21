---
description: >-
  The three levels every configuration in this app is built from, and which
  settings live at each level.
icon: layer-group
---

# Option sets, options, and values

Almost every question about where a setting lives is answered by knowing which of these three levels it belongs to.

## The three levels

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

<table><thead><tr><th width="170">Level</th><th>What it is</th><th>Example</th></tr></thead><tbody><tr><td><strong>Option set</strong></td><td>The container you create, save, and activate. It holds the options and the rules for where they apply.</td><td>"Bracelet personalization"</td></tr><tr><td><strong>Section</strong></td><td>Optional. A visual container that groups options under a heading, and can be collapsible.</td><td>"Personalize your bracelet"</td></tr><tr><td><strong>Option</strong></td><td>One field the customer interacts with. Has a type, which decides which settings it offers.</td><td>"Engraving text", a Text option</td></tr><tr><td><strong>Option value</strong></td><td>One choice inside a selection-style option. Input-style options have none.</td><td>"Yes, wrap it as a gift"</td></tr></tbody></table>

## Which settings live where

This is the useful part. If you are hunting for a setting, this table tells you which level to look at.

<table><thead><tr><th width="200">Level</th><th>Settings that live here</th></tr></thead><tbody><tr><td><strong>Whole store</strong></td><td>Where the widget appears, colours, borders, typography, custom CSS, how add-on prices are displayed, widget text and validation messages, custom fonts. All in <strong>Settings</strong>. These apply to every option set.</td></tr><tr><td><strong>Option set</strong></td><td>Name, status, sales channels, product rule, customer rule, country rule, and the personalizer background.</td></tr><tr><td><strong>Option</strong></td><td>Type, label, name, required, help text, placeholder, limits, layout, column width, conditional logic, add-on settings, personalizer settings.</td></tr><tr><td><strong>Option value</strong></td><td>The value text, its own help text, its own add-on price or add-on product, and its colour or image for swatch-style options.</td></tr></tbody></table>

{% hint style="info" %}
A common mix-up: colours and fonts are **store-wide**, not per option set. If you want two option sets to look different from each other, you do it with [custom CSS](../storefront/custom-css.md) and the **HTML class** setting on an option, not with separate colour settings.
{% endhint %}

## Which option types have option values

<table><thead><tr><th width="230">Family</th><th>Option values?</th><th>Notes</th></tr></thead><tbody><tr><td>Input types</td><td>No</td><td>The customer types, picks, uploads, or slides. The exception is <strong>Dimension</strong>, which has one row per axis rather than a list of choices.</td></tr><tr><td>Selection types</td><td>Yes</td><td>You list the choices. <strong>Font picker</strong> is a special case — its list is fonts you select rather than free text, and <strong>Product links</strong> lists products.</td></tr><tr><td>Static types</td><td>No</td><td>They display content rather than collect it. <strong>Tabs</strong> is the exception — each tab is a value with its own rich-text content.</td></tr></tbody></table>

See [Option types](../option-types/README.md) for the full list.

## How many can I have?

<table><thead><tr><th width="300">Limit</th><th>Current plans</th></tr></thead><tbody><tr><td>Option sets per store</td><td>Unlimited</td></tr><tr><td>Options per option set</td><td>Unlimited</td></tr><tr><td>Option values per option</td><td>Unlimited</td></tr><tr><td>Products per option set</td><td>Unlimited</td></tr></tbody></table>

Some option types and configurations are limited by plan even where the counts are not — for example how many files a customer may upload at once. Check the **Pricing** page in the app for what your plan includes, and see [Compare plans](../plans/compare-plans.md).

{% hint style="warning" %}
Practical advice rather than a hard limit: very long option sets slow the product page down and hurt conversion. If you have more than about fifteen options on one product, use [Sections](../option-types/static-types/section.md) to group them and [conditional logic](../conditional-logic/README.md) to reveal only what is relevant.
{% endhint %}

## Can several option sets apply to the same product?

Yes. If two active option sets both match a product, both render. That is useful — you might have one store-wide set for "delivery notes" and a second set only for engravable products.

It also means a product can end up with duplicated options if two sets overlap by accident. If you see an option twice, check whether a second option set also matches that product. See [Assign to products](../option-sets/assign-to-products.md).

## Next steps

* [Label vs Name](label-vs-name.md) — the two fields every option has.
* [Working with option values](option-values.md)
* [Create an option set](../option-sets/create-an-option-set.md)
