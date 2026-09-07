---
description: Collecting options as part of a quote request rather than an immediate sale.
icon: file-invoice-dollar
---

# Request a Quote and hide price

Some businesses do not sell directly. Trade suppliers, made-to-measure manufacturers, and wholesalers collect a specification, price it, and then send a quote.

Product options suit this well, because the option form is the specification.

## How the parts fit together

<table><thead><tr><th width="230">Piece</th><th>Does</th></tr></thead><tbody><tr><td>This app</td><td>Collects the specification — measurements, materials, quantities, uploaded drawings</td></tr><tr><td>A quote or hide-price app</td><td>Replaces the buy button with a quote request, and hides prices where you do not want them shown</td></tr><tr><td>Your process</td><td>Prices the specification and responds</td></tr></tbody></table>

The app supports flows that create a draft order rather than a normal checkout, which is how quote requests are usually handled. The specification becomes a draft order you can price and send.

## What to test

<table><thead><tr><th width="290">Test</th><th>What you are checking</th></tr></thead><tbody><tr><td>Options appear on a hidden-price product</td><td>The widget is not tied to the price being visible</td></tr><tr><td>Required options block the quote request</td><td>You do not receive specifications with gaps</td></tr><tr><td>The option details reach the quote or draft order</td><td>Otherwise you have a request with no specification</td></tr><tr><td>Uploaded files reach you</td><td>Drawings and artwork are usually the point</td></tr><tr><td>Add-on prices behave as you expect</td><td>You may want them recorded but not shown</td></tr></tbody></table>

## Building a quote form

<table><thead><tr><th width="290">Use</th><th>For</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/dimension.md">Dimension</a></td><td>Measurements with units and limits, so you never receive an impossible size</td></tr><tr><td><a href="../option-types/input-types/file-upload.md">File upload</a></td><td>Drawings, specifications, artwork</td></tr><tr><td><a href="../option-types/input-types/number.md">Number</a></td><td>Quantities, with a minimum that matches your minimum order</td></tr><tr><td><a href="../option-types/selection-types/dropdown.md">Dropdown</a></td><td>Materials and finishes you actually offer</td></tr><tr><td><a href="../option-types/input-types/textarea.md">Textarea</a></td><td>Anything you have not thought of. Always include one</td></tr><tr><td><a href="../option-types/input-types/email.md">Email</a> and <a href="../option-types/input-types/phone.md">Phone</a></td><td>How to reach them, if the quote tool does not already ask</td></tr><tr><td><a href="../option-types/shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Everything you cannot quote without. This is where required earns its keep</td></tr><tr><td><a href="../conditional-logic/">Conditional logic</a></td><td>Asking follow-up questions only when relevant, so the form stays short</td></tr></tbody></table>

{% hint style="info" %}
A quote form is the one place to use **required fields** freely. On a retail product, required options reduce conversions. On a quote request, an incomplete specification means another round of emails, so require everything you need.
{% endhint %}

## Trade prices alongside retail

If you sell both ways, use [customer rules](../option-sets/assign-to-customers.md) so one product behaves differently for trade customers:

* Your retail option set, with **Customers** set to exclude your trade tag
* A trade option set, with **Customers** set to that tag, with different options or prices

Both option sets target the same products, and only one is displayed to any given customer. See [Duplicate and delete](../option-sets/duplicate-and-delete.md).

## Notes

* You can use any quote app. This app collects the product specifications.
* Options are collected before the cart, so they are available for both regular checkouts and draft orders.
* If the flow does not work from start to finish on your theme, the issue requires integration work. See [Contact support](../help/contact-support.md).
