---
description: Get your orders out as a CSV, or the customers' uploaded files as a ZIP.
icon: file-export
---

# Export orders and files

Two exports, for two different jobs: a **CSV of the orders** for your spreadsheet or production system, and a **ZIP of the files** customers uploaded.

Both work on what you have selected. Select orders on the page, or export everything matching your current search and filters.

<table><thead><tr><th width="290">Scope</th><th>What it covers</th></tr></thead><tbody><tr><td><strong>Selected</strong></td><td>Just the orders you ticked</td></tr><tr><td><strong>Current page</strong></td><td>Every order on the page you are looking at</td></tr><tr><td><strong>All orders matching your search and filters</strong></td><td>The whole filtered set, however many pages it spans</td></tr></tbody></table>

## Exporting orders

**Export orders** produces a CSV. The choice that matters is the row format.

<table><thead><tr><th width="250">Format</th><th>Shape</th><th>Best for</th></tr></thead><tbody><tr><td><strong>One row per product</strong></td><td>All options of a product in one cell</td><td>Processing orders — one line per thing you have to make</td></tr><tr><td><strong>One row per option</strong></td><td>Each option value on its own row</td><td>Analysing options in a spreadsheet — you can pivot and count values</td></tr></tbody></table>

Pick by what you are going to do with it. A production list reads better as one row per product; counting how often customers choose each font needs one row per option.

The file opens in Excel, Numbers, or Google Sheets.

## Exporting files

**Export files** produces a ZIP of what customers uploaded.

<table><thead><tr><th width="250">Setting</th><th>Options</th></tr></thead><tbody><tr><td><strong>File organization</strong></td><td><strong>Each order in its own folder</strong>, or <strong>All files in one folder</strong></td></tr><tr><td><strong>File name</strong></td><td>A template you build from the order and option details</td></tr><tr><td>What to include</td><td>Customer uploaded files, personalization previews, or both</td></tr></tbody></table>

At least one type has to be selected, or the export has nothing to produce.

{% hint style="warning" %}
**Put `{OptionName}` in the file name.** Without it, two files from different options on the same order end up with the same name, and one overwrites the other as soon as they land in one folder.

This matters most with **All files in one folder**, where every file from every order shares a single namespace.
{% endhint %}

If you already run [Google Drive sync](../automations/google-drive-sync/README.md), you may not need this at all — files from new orders are copied there automatically, already sorted into a folder per order.

## Large exports

Small exports download immediately. Larger ones are prepared in the background and emailed to you as a download link.

<table><thead><tr><th width="250">Export</th><th>Downloads right away</th></tr></thead><tbody><tr><td>Orders</td><td>Up to <strong>500</strong> orders</td></tr><tr><td>Files</td><td>Up to <strong>20</strong> files</td></tr></tbody></table>

Beyond that, the app says it is preparing them and names the address the link will go to. You can leave the page.

<table><thead><tr><th width="330">Message</th><th>What to do</th></tr></thead><tbody><tr><td>The files are too large to download together</td><td>Select fewer orders, or split the export into batches</td></tr><tr><td>These orders have no files to export</td><td>Nothing was uploaded on the orders you selected</td></tr><tr><td>Too many exports. Try again in a minute</td><td>Exporting is rate-limited. Wait, then retry</td></tr></tbody></table>

## Notes

* Exports cover orders still in the app. Anything past the 90-day window is gone, so export before you need it rather than after.
* The CSV reflects the order as placed, including option sets you have since changed or deleted.
* A file the customer uploaded that has since been removed cannot be exported.
