---
description: Collecting options as part of a quote request rather than an immediate sale.
icon: file-invoice-dollar
---

# Request a Quote and hide price

Some businesses do not sell directly. They collect a specification, price it, and come back with a quote — trade suppliers, made-to-measure manufacturers, wholesale.

Product options are a natural fit for that: the option form *is* the specification.

## How the pieces fit together

<table><thead><tr><th width="230">Piece</th><th>Does</th></tr></thead><tbody><tr><td>This app</td><td>Collects the specification — measurements, materials, quantities, uploaded drawings</td></tr><tr><td>A quote or hide-price app</td><td>Replaces the buy button with a quote request, and hides prices where you do not want them shown</td></tr><tr><td>Your process</td><td>Prices the specification and responds</td></tr></tbody></table>

The app supports flows that build a draft order rather than a normal checkout, which is how quote requests are usually handled — the specification becomes a draft order you can price and send.

## What to test

<table><thead><tr><th width="290">Test</th><th>What you are checking</th></tr></thead><tbody><tr><td>Options appear on a hidden-price product</td><td>The widget is not tied to the price being visible</td></tr><tr><td>Required options block the quote request</td><td>You do not receive specifications with gaps</td></tr><tr><td>The option details reach the quote or draft order</td><td>Otherwise you have a request with no specification</td></tr><tr><td>Uploaded files reach you</td><td>Drawings and artwork are usually the point</td></tr><tr><td>Add-on prices behave as you expect</td><td>You may want them recorded but not shown</td></tr></tbody></table>

## Building a good quote form

<table><thead><tr><th width="290">Use</th><th>For</th></tr></thead><tbody><tr><td><a href="../option-types/input-types/dimension.md">Dimension</a></td><td>Measurements with units and limits, so you never receive an impossible size</td></tr><tr><td><a href="../option-types/input-types/file-upload.md">File upload</a></td><td>Drawings, specifications, artwork</td></tr><tr><td><a href="../option-types/input-types/number.md">Number</a></td><td>Quantities, with a minimum that matches your minimum order</td></tr><tr><td><a href="../option-types/selection-types/dropdown.md">Dropdown</a></td><td>Materials and finishes you actually offer</td></tr><tr><td><a href="../option-types/input-types/textarea.md">Textarea</a></td><td>Anything you have not thought of. Always include one</td></tr><tr><td><a href="../option-types/input-types/email.md">Email</a> and <a href="../option-types/input-types/phone.md">Phone</a></td><td>How to reach them, if the quote tool does not already ask</td></tr><tr><td><a href="../option-types/shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Everything you cannot quote without. This is where required earns its keep</td></tr><tr><td><a href="../conditional-logic/README.md">Conditional logic</a></td><td>Asking follow-up questions only when relevant, so the form stays short</td></tr></tbody></table>

{% hint style="info" %}
A quote form is the one place to be generous with **Required field**. On a retail product, required options cost you sales. On a quote request, an incomplete specification costs you a round of emails — so require everything you genuinely need.
{% endhint %}

## Trade prices alongside retail

If you sell both ways, [customer rules](../option-sets/assign-to-customers.md) let one product behave differently for trade customers:

* Your retail option set, with **Customers** set to exclude your trade tag
* A trade option set, with **Customers** set to that tag, with different options or prices

Both target the same products, and only one ever renders for a given shopper. See [Duplicate and delete](../option-sets/duplicate-and-delete.md) for the pattern.

## Notes

* Which quote app you use is your choice; the app's job is the specification.
* Options are collected before the cart, so they are available whatever happens next — a normal checkout or a draft order.
* If the flow does not work end to end on your theme, that is integration work. See [Contact support](../help/contact-support.md).

## Next steps

* [Assign to customers](../option-sets/assign-to-customers.md)
* [Dimension](../option-types/input-types/dimension.md)
* [Automations](../automations/README.md) — get each request emailed to you.
