---
description: >-
  Collect photos, logos, and artwork — with allowed file types, file counts, an
  image editor, and live preview on the product photo.
icon: paperclip
---

# File upload

A field the customer attaches files to. It is the type that makes print-on-demand, photo gifts, and custom artwork possible.

## What customers see

An upload control with your label above it. After uploading, the file is listed — as a thumbnail if it is an image, or as a link otherwise, depending on your store-wide **File preview** setting.

<!-- SCREENSHOT: type-file-storefront | Storefront → trang sản phẩm | Field File upload đã upload 1 ảnh, hiện thumbnail preview | Khoanh vùng upload và thumbnail -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A file upload field on a storefront product page with an uploaded image shown as a thumbnail"><figcaption><p>Uploaded images can preview as thumbnails, so the shopper can confirm they sent the right file.</p></figcaption></figure>

## Basic Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><a href="../shared-settings/labels-and-visibility.md#label">Label</a> / <a href="../shared-settings/labels-and-visibility.md#name">Name</a></td><td>Customer-facing text, and the name on the order.</td></tr><tr><td><a href="../shared-settings/required-and-default-value.md#required-field">Required field</a></td><td>Blocks add to cart until at least one file is attached.</td></tr><tr><td><a href="../shared-settings/labels-and-visibility.md#hidden-label">Hidden label</a></td><td>Hides the label.</td></tr><tr><td><strong>Allow multiple (up to 20)</strong></td><td>Lets the customer attach more than one file. Off by default. Reveals the two file-count limits.</td></tr><tr><td><a href="../shared-settings/limits.md#min-and-max-number-of-files">Min number of files</a> / <a href="../shared-settings/limits.md#min-and-max-number-of-files">Max number of files</a></td><td>Between 1 and 20 each. Only shown once <strong>Allow multiple</strong> is on.</td></tr><tr><td><strong>Allowed extensions</strong></td><td>Which file types are accepted. Starts as <code>jpg</code>, <code>jpeg</code>, <code>png</code>.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text">Help text</a></td><td>Guidance that stays visible — the right place for your quality requirements.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide based on other choices.</td></tr></tbody></table>

There is no placeholder, no default value, and **no add-on price** on this type.

### Allowed extensions

The picker groups every accepted extension into nine categories, so you can allow a whole family at once:

<table><thead><tr><th width="250">Group</th><th>Contains</th></tr></thead><tbody><tr><td><strong>Image</strong></td><td>jpg, jpeg, png, gif, bmp, webp, tif, heic, dng</td></tr><tr><td><strong>Graphics</strong></td><td>svg, eps, ico, stl, 3mf and other design and 3D formats</td></tr><tr><td><strong>Document</strong></td><td>doc, docx, rtf, txt</td></tr><tr><td><strong>Spreadsheet</strong></td><td>Spreadsheet formats</td></tr><tr><td><strong>Presentation</strong></td><td>Presentation formats</td></tr><tr><td><strong>Audio</strong></td><td>mp3, wav, mpc</td></tr><tr><td><strong>Video</strong></td><td>mp4, mov and others</td></tr><tr><td><strong>Archive &amp; Compressed</strong></td><td>zip, rar, 7z, bin</td></tr><tr><td><strong>Others</strong></td><td>Specialist formats, including machine and font files</td></tr></tbody></table>

There is a search box, so you can find a single extension without opening the group.

{% hint style="warning" %}
Allow only what you can actually use. Accepting `heic` means iPhone photos arrive in a format some design tools cannot open; accepting `zip` means you cannot see what you have been sent until you unpack it. Narrowing the list is the single most effective thing you can do to reduce back-and-forth with customers.
{% endhint %}

## Advanced Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Enable image editor</strong></td><td>Lets customers adjust an image before it is uploaded — cropping, rotating, and similar. Off by default.</td></tr><tr><td><a href="../shared-settings/placeholder-and-help-text.md#help-text-position">Help text position</a></td><td>Where the help text sits.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and field width.</td></tr></tbody></table>

**Enable image editor** is worth turning on for anything printed. A customer who can crop their own photo to the right shape sends you a usable file first time, instead of a landscape snapshot for a portrait frame.

## Personalizer Settings

File upload is one of the four types with live preview support, and the most impressive of them: the customer's uploaded image appears on the product photo immediately.

Its personalizer settings are:

* **Image shape** — a preset shape the image is masked into, or your own uploaded shape
* **Background mode** — how the image fits the shape: **Stretch**, **Cover**, **Contain**, **Full width**, **Full height**
* **Width**, **Height**, **X-Axis**, **Y-Axis**, **Opacity**, **Rotation**
* **Clip area** — a region the image cannot escape
* **Allow customers to** — change position, resize, rotate

That combination is how "upload your photo and see it in the frame" works. See [Image layers](../../personalizer/image-layers.md) and [Customer controls](../../personalizer/customer-controls.md).

## Add-on pricing

File upload cannot carry a price.

To charge for an upload — an artwork setup fee, say — put the charge on a [Switch](switch.md) or [Checkbox](../selection-types/checkbox.md) next to it, and reveal the upload field with [conditional logic](../../conditional-logic/README.md) when they opt in.

## Store-wide settings that affect it

<table><thead><tr><th width="290">Setting</th><th>Where</th><th>Effect</th></tr></thead><tbody><tr><td><strong>File preview</strong></td><td>Settings &gt; Settings &gt; General &gt; Product page</td><td><strong>Show image if the uploaded file is a photo, otherwise show link</strong>, or <strong>Show link</strong> for everything.</td></tr><tr><td>Maximum file size</td><td>Your plan</td><td>Each plan allows a different size per file. See <a href="../../plans/compare-plans.md">Compare plans</a>.</td></tr><tr><td><strong>Choose file</strong>, <strong>File uploading</strong>, <strong>Uploaded file:</strong> and similar wording</td><td>Settings &gt; Translations</td><td>All editable per language.</td></tr></tbody></table>

## Examples

**One photo to print in a frame**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Label / Name</td><td><code>Your photo</code></td></tr><tr><td>Required field</td><td>On</td></tr><tr><td>Allow multiple</td><td>Off</td></tr><tr><td>Allowed extensions</td><td><code>jpg</code>, <code>jpeg</code>, <code>png</code></td></tr><tr><td>Enable image editor</td><td>On</td></tr><tr><td>Help text</td><td><code>JPG or PNG, at least 1500 × 1500 pixels for a sharp print.</code></td></tr><tr><td>Personalizer</td><td>On, masked into the frame shape, customer may reposition</td></tr></tbody></table>

**A four-photo collage**

**Allow multiple** on, **Min number of files** `4`, **Max number of files** `4`, image editor on.

**Print-ready artwork from a designer**

**Allowed extensions** `pdf`-style document and graphics formats plus `svg` and `eps`, not required, help text stating your bleed and colour requirements.

**Reference images for a repair quote**

**Allow multiple** on, min `2`, max `6`, help text asking for one photo per angle.

## Limits and notes

* Available on paid plans. Multiple file upload and the per-file size limit are separately plan-gated.
* Works in Shopify POS.
* Cannot carry an add-on price.
* Up to 20 files per option.
* Uploaded files are attached to the order, so your team can download them from the order in Shopify admin.
* Large uploads take time on a slow connection. Keep the allowed list tight and say what you need in help text.

## Troubleshooting

<details>
<summary>The customer's file is rejected</summary>

Its extension is not in **Allowed extensions**, or it is over your plan's size limit. Add the extension, or ask for a smaller file. `heic` from iPhones is the usual surprise.
</details>

<details>
<summary>I cannot find Min or Max number of files</summary>

Turn on **Allow multiple** first.
</details>

<details>
<summary>Uploads show as links rather than images</summary>

That is the store-wide **File preview** setting. Change it to show images where possible in **Settings > Settings > General**.
</details>

<details>
<summary>I cannot find a Price field</summary>

File upload has none. Put the fee on a Switch or Checkbox beside it.
</details>

<details>
<summary>The uploaded image does not appear on the product photo</summary>

Turn on **Personalizer Settings** for this option, and make sure the option set has a background image configured. See [Set the preview background](../../personalizer/set-the-background.md).
</details>

<details>
<summary>Customers send low-resolution photos</summary>

State the minimum in help text with a real number, and turn on **Enable image editor** so they can crop rather than resize badly.
</details>

## Next steps

* [Image layers](../../personalizer/image-layers.md) — put the upload on the product photo.
* [Limits](../shared-settings/limits.md#min-and-max-number-of-files) — file count rules.
* [Conditional logic](../../conditional-logic/README.md) — ask for a file only when needed.
