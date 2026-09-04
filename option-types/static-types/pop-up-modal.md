---
description: >-
  A link that opens formatted content in a dialog, so long explanations do not
  lengthen the page.
icon: window-restore
---

# Pop-up modal

A link on the product page that opens a dialog with your content. The information is available to shoppers who want it without taking up space for everyone else.

Use it for care instructions, personalization policies, return terms, delivery details, or anything important that not every shopper needs to read.

## What customers see

A link with your title. Selecting it opens a dialog with your content, at the width you set.

<figure><img src="../../.gitbook/assets/2026-09-03_15-39-47.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/2026-09-03_15-38-02.png" alt="A pop-up modal opened from a link on a storefront product page"><figcaption><p>A modal keeps long content off the page until it is asked for.</p></figcaption></figure>

## Settings

<table><thead><tr><th width="250">Setting</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Modal title</strong></td><td>The link text on the product page, and the dialog's heading. Starts as <code>Open modal</code>.</td></tr><tr><td><strong>Modal width</strong></td><td>The dialog width in pixels. Starts at <code>600</code>.</td></tr><tr><td><strong>Modal content</strong></td><td>The content, written in a rich-text editor.</td></tr><tr><td><a href="../shared-settings/conditional-logic-and-add-on-fields.md#conditional-logic">Conditional logic</a></td><td>Show or hide the link.</td></tr><tr><td><a href="../shared-settings/direction-width-and-css.md#html-class">HTML class</a> / <a href="../shared-settings/direction-width-and-css.md#column-width">Column width</a></td><td>Styling hook and width of the link, not the dialog.</td></tr></tbody></table>

{% hint style="info" %}
**Modal title** serves two purposes, so write it as a link that clearly tells shoppers what they will find. `Read our personalization policy` works as both a link and a dialog title; `Open modal` does neither.
{% endhint %}

### Modal width

<table><thead><tr><th width="180">Width</th><th>Suits</th></tr></thead><tbody><tr><td><code>400</code>–<code>500</code></td><td>A few short paragraphs</td></tr><tr><td><code>600</code></td><td>The default. Comfortable for most text</td></tr><tr><td><code>800</code>+</td><td>Content with a table or images</td></tr></tbody></table>

Dialogs shrink to fit narrow screens, so a wide value does not break mobile — but a table inside a dialog still becomes cramped on a phone. For a size table specifically, use [Size chart](size-chart.md), which is built for it.

## Modal or Tabs?

<table><thead><tr><th width="230">Pop-up modal</th><th>Tabs</th></tr></thead><tbody><tr><td>One block of content</td><td>Several blocks</td></tr><tr><td>Hidden until opened</td><td>Always on the page, one panel at a time</td></tr><tr><td>Takes one line on the page</td><td>Takes the height of a panel</td></tr><tr><td>Best when most shoppers skip it</td><td>Best when most shoppers read at least one panel</td></tr></tbody></table>

If you have several topics to present, such as care, delivery, and returns, [Tabs](tabs.md) is usually the better choice. If you have a single policy that only some shoppers need to read, use a **Popup modal**.

## Examples

**A personalisation policy**

<table><thead><tr><th width="290">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Modal title</td><td><code>How personalisation works</code></td></tr><tr><td>Modal width</td><td><code>600</code></td></tr><tr><td>Modal content</td><td>Lead times, what can and cannot be engraved, the returns position</td></tr></tbody></table>

**Care instructions**

Title `Care instructions`, content: a short formatted list, placed at the bottom of the form.

**A conditional warning**

Title `Important: engraved items cannot be returned`, shown by conditional logic only when the shopper has entered engraving text.

## Notes

* Available on all plans.
* Works in Shopify POS.
* Content is translatable per storefront language. See [Translate option content](../../translations/translate-option-content.md).
* The rich-text editor covers most formatting needs. Use [HTML](html.md) only when you need formatting that the editor does not support.
* A modal is not suitable for information shoppers must read before making a choice, because they may never open it. Use a [Paragraph](paragraph.md) instead.
