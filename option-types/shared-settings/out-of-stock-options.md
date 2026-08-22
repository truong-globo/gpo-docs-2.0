---
description: >-
  How a choice looks when the add-on product behind it has run out — shown,
  hidden, blurred, or struck through.
icon: boxes-stacked
---

# Out of stock options

One setting, four choices. It decides what a shopper sees when a value they might have picked is unavailable.

## Out of stock options

<table><thead><tr><th width="180">Tab</th><td>Advanced Settings</td></tr><tr><th>Default</th><td><strong>Show</strong></td></tr><tr><th>Available on</th><td>9 types: Checkbox, Radio button, Button, Dropdown, Color dropdown, Image dropdown, Color swatch, Image swatch, Product links</td></tr></thead></table>

{% hint style="warning" %}
This setting only does something when a value is linked to an **add-on product** — either an existing product or one the app generated. A value priced with **Add price** has no product and therefore no stock, so there is nothing to be out of. See [Add-on pricing](../../add-on-pricing/README.md).
{% endhint %}

<table><thead><tr><th width="200">Choice</th><th>Appearance</th><th>Can it still be selected?</th></tr></thead><tbody><tr><td><strong>Show</strong></td><td>Normal, with no indication</td><td>Yes</td></tr><tr><td><strong>Hide</strong></td><td>Removed from the list entirely</td><td>No</td></tr><tr><td><strong>Blur</strong></td><td>Faded out</td><td>No</td></tr><tr><td><strong>Strike-through</strong></td><td>Crossed out</td><td>No</td></tr></tbody></table>

## Choosing between them

<table><thead><tr><th width="210">Choice</th><th>Best for</th><th>Downside</th></tr></thead><tbody><tr><td><strong>Show</strong></td><td>Options that are not really stock-limited, or where you make to order and inventory is only a record</td><td>Shoppers can order something you cannot supply</td></tr><tr><td><strong>Hide</strong></td><td>Long lists where a missing entry is not noticeable</td><td>Shoppers cannot tell the choice exists, so they will not ask when it is coming back</td></tr><tr><td><strong>Blur</strong></td><td>Colour and image swatches — the shopper still sees the colour or picture</td><td>Faded can read as "not selected" rather than "unavailable"</td></tr><tr><td><strong>Strike-through</strong></td><td>Text choices — unmistakably "not available"</td><td>Looks cluttered when many values are out at once</td></tr></tbody></table>

For visual swatch lists, **Blur** is usually the best answer. The shopper sees that the colour exists and is currently unavailable, which is more useful than it silently vanishing — and it gives them a reason to come back.

For long text lists, **Hide** keeps the list short. For short text lists, **Strike-through** is clearer.

<!-- SCREENSHOT: type-shared-oos-storefront | Storefront → trang sản phẩm | 1 hàng color swatch trong đó 1 swatch hết hàng đang bị blur | Khoanh swatch bị blur -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A row of colour swatches on the storefront with one blurred to show it is out of stock"><figcaption><p>Blur keeps the colour visible while making its unavailability clear.</p></figcaption></figure>

## How stock is determined

Stock comes from the linked product's inventory in Shopify. There is nothing to manage in this app: open the add-on product in Shopify admin and set its inventory exactly as you would for any other product.

The availability check happens when the product page loads, against live inventory.

If a value points at a specific **variant** rather than a whole product, the check is against that variant. A value linked to a sold-out variant is out of stock even when other variants of the same product still have stock.

See [Stock and inventory](../../add-on-pricing/stock-and-inventory.md).

## A configuration that works

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Option type</td><td><a href="../selection-types/color-swatch.md">Color swatch</a></td></tr><tr><td><strong>Swatch style</strong></td><td><strong>Color</strong></td></tr><tr><td>Each value's <strong>Price</strong></td><td><strong>Automatically generate product</strong>, so each colour has its own inventory</td></tr><tr><td><strong>Out of stock options</strong></td><td><strong>Blur</strong></td></tr><tr><td>Value help text</td><td><code>Back in stock next week</code> on anything you know is returning</td></tr></tbody></table>

## Limits and notes

* Plan-gated. If the setting is greyed out, see [Compare plans](../../plans/compare-plans.md).
* On **Product links** it works the same way, using the linked product's own availability.
* The setting is per option, not per value. All values in one option share the same treatment.
* It affects appearance and selectability only. It does not stop the customer buying the main product.

## Troubleshooting

<details>
<summary>The setting makes no difference</summary>

The values are not linked to add-on products, so there is no stock to read. Check each value's **Price** field — **Add price** carries no inventory. See [Add-on pricing](../../add-on-pricing/README.md).
</details>

<details>
<summary>A value shows as out of stock when the product has stock</summary>

Check the exact variant the value points at rather than the product as a whole.
</details>

<details>
<summary>The setting is greyed out</summary>

The feature is not in your plan. See [Compare plans](../../plans/compare-plans.md).
</details>

<details>
<summary>Out-of-stock values still get ordered</summary>

The setting is on **Show**, which leaves them selectable. Change it to **Hide**, **Blur**, or **Strike-through**.
</details>

<details>
<summary>I want the whole option hidden when everything in it is out of stock</summary>

Not available as a setting. Set the option to **Hide** so the list empties, or set the option set to **Draft** while you restock.
</details>
