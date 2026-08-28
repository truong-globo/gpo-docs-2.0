---
description: >-
  Move option sets between stores using CSV files, create backups, or migrate
  from another product options app.
icon: file-import
---

# Import and export

**Export option sets** creates a CSV file containing your option sets. **Import option sets** lets you upload a CSV file created by this app or exported from another supported product options app.

Use these tools to back up your option sets before making major changes, move a setup from a development store to a live store, or migrate from an app you are replacing.

Both actions are available next to **Create option set** on the **Option Sets** page. Import and export are controlled separately by your plan, so you may have access to one without the other.

## Export

{% stepper %}
{% step %}
### Select the option sets you want to include if you only want to export specific sets.

Skip this to export everything.
{% endstep %}

{% step %}
### Select Export option sets, then choose the scope

<table><thead><tr><th width="260">Choice</th><th>Includes</th></tr></thead><tbody><tr><td><strong>Current page</strong></td><td>Every option set on the page you are looking at</td></tr><tr><td><strong>All option sets</strong></td><td>Every option sets in your store</td></tr><tr><td><strong>Selected: N option sets</strong></td><td>Only selected rows. Unavailable when nothing is chosen.</td></tr></tbody></table>

The format is a **Plain CSV file**.
{% endstep %}

{% step %}
### Select Export option sets again

Your browser downloads `OptionsExport.csv`.
{% endstep %}
{% endstepper %}

<figure><img src="../.gitbook/assets/placeholder.png" alt="The export dialog with scope choices and the CSV format option"><figcaption><p>Export the current page, everything, or just your selection.</p></figcaption></figure>

{% hint style="info" %}
Export before any change you are unsure about. The file costs nothing to produce, and it is the only way to get an option set back after it is deleted.
{% endhint %}

## Import

{% stepper %}
{% step %}
### Select Import option sets and add your file

Drop it into the drop zone or browse for it. Accepted: `.csv`, `.txt`, `.xlsx`, `.xls`, up to 10 MB.

Building a file by hand? The dialog links to a **sample CSV template** — start from that rather than inventing the layout.
{% endstep %}

{% step %}
### Say which app the file came from

**Select app for import** tells the app how to read your columns. It defaults to **Globo Product Options, Variant**, and also reads files from **Easify**, **Avis**, **OPTIS**, **Qikify**, **Hulk**, and **APO**.

Getting this wrong is the most common cause of a failed or scrambled import.
{% endstep %}

{% step %}
### Leave "Set all imported option sets as Active" off

Imports then land as **Draft**, so you can review them before shoppers see them. Tick it only when you are certain.
{% endstep %}

{% step %}
### Select Upload and continue, then review what arrived

Open each imported set and check its options, its **Name** fields, its add-on configuration, and its product rule.
{% endstep %}
{% endstepper %}

<figure><img src="../.gitbook/assets/placeholder.png" alt="The import dialog with the drop zone, the app selector, and the set as active checkbox"><figcaption><p>Telling the app which file format you have is the step people skip.</p></figcaption></figure>

## Migrating from another app

Same import as above, plus two rules that save you trouble:

1. **Import without activating**, review, then activate.
2. **Test one set on a real product before uninstalling the old app.** Uninstalling first makes any gap visible to shoppers.

Expect some tidying, because different apps model options differently. Check these in particular:

<table><thead><tr><th width="220">Check</th><th>Why</th></tr></thead><tbody><tr><td>Add-on pricing</td><td>How the other app charged may not map exactly. Review every price and pick the right mode — see <a href="../add-on-pricing/">Add-on pricing</a></td></tr><tr><td>Conditional logic</td><td>Operators differ between apps, so rules may need rebuilding</td></tr><tr><td>Option <strong>Name</strong> fields</td><td>They must be readable and must not clash — see <a href="../option-types/shared-settings/labels-and-visibility.md">Label and Name</a></td></tr><tr><td>Product rules</td><td>Confirm each set targets what you expect</td></tr><tr><td>Swatch images</td><td>May need re-uploading if the old app hosted them itself</td></tr></tbody></table>

## What travels, and what does not

Exported option sets carry their own configuration only. Everything store-wide travels separately:

* Colours, borders, typography, custom CSS, widget position and behaviour — export from **Settings**. See [Import and export settings](../settings/import-export-settings.md).
* Widget text and validation messages — **Settings > Translations**.
* Automations — configured per store.
* **Add-on products themselves.** The file records which product an add-on pointed at, but another store does not have that product. Reconnect add-ons after importing across stores.

## Notes

* Imported sets are added, never merged or overwritten. Importing the same file twice gives you two copies.
* Import respects your plan. A file containing features your plan does not allow is refused outright rather than partly applied.
* Files from older versions of this app are still readable — the app recognises the older column layout by itself.

<details>

<summary>What the exported CSV contains, column by column</summary>

You only need this if you intend to read or edit the file by hand.

The file has one row per option value. Options without values, such as text fields, get a single row. Columns describing the whole option set or the whole option are filled on the **first** row only and left blank on the rest.

<table><thead><tr><th width="230">Column</th><th>Contains</th></tr></thead><tbody><tr><td><code>option_set_id</code></td><td>The option set's ID, repeated on every row of that set</td></tr><tr><td><code>option_set_name</code></td><td>The option set's name. First row only</td></tr><tr><td><code>option_id</code></td><td>The option's internal ID within the set</td></tr><tr><td><code>option_type</code></td><td>The option's type</td></tr><tr><td><code>option_label</code></td><td>The option's <strong>Label</strong>, including any translations</td></tr><tr><td><code>option_name</code></td><td>The option's <strong>Name</strong></td></tr><tr><td><code>required</code></td><td><code>yes</code> when <strong>Required field</strong> is on</td></tr><tr><td><code>allow_multiple</code></td><td><code>yes</code> when multiple selection or multiple file upload is on</td></tr><tr><td><code>min</code>, <code>max</code></td><td>The option's minimum and maximum, whatever they measure for that type</td></tr><tr><td><code>placeholder</code></td><td>The option's <strong>Placeholder</strong></td></tr><tr><td><code>helptext</code></td><td>The option's <strong>Help text</strong> and its position</td></tr><tr><td><code>option_value</code></td><td>The value on this row, with its own help text where it has one</td></tr><tr><td><code>addon</code></td><td>The add-on configuration: which mode, which product and variant, and the price</td></tr><tr><td><code>swatch_name</code></td><td>The swatch's internal name</td></tr><tr><td><code>swatch_value</code></td><td>The colour, the two colours of a split swatch, or the image address</td></tr><tr><td><code>swatch_asset_name</code></td><td>The uploaded image's file name</td></tr><tr><td><code>default_value</code></td><td>The option's default value</td></tr><tr><td><code>rich_text_value</code></td><td>Rich-text content for Paragraph, Pop-up modal, HTML, Size chart, and Tabs</td></tr><tr><td><code>advanced_settings</code></td><td>Everything from the <strong>Advanced Settings</strong> and <strong>Personalizer Settings</strong> tabs, in one cell</td></tr><tr><td><code>columnWidth</code></td><td>The option's <strong>Column width</strong></td></tr><tr><td><code>conditionalField</code></td><td><code>yes</code> when conditional logic is on for this option</td></tr><tr><td><code>condition_logic</code></td><td>The conditional logic rule itself</td></tr><tr><td><code>products</code></td><td>The product rule. First row only</td></tr><tr><td><code>customers</code></td><td>The customer rule. First row only</td></tr><tr><td><code>countries</code></td><td>The country rule. First row only</td></tr><tr><td><code>settings</code></td><td>Option set settings, including the Personalizer background. First row only</td></tr></tbody></table>

{% hint style="warning" %}
`addon`, `condition_logic`, `advanced_settings`, `products`, `customers`, `countries`, and `settings` each hold structured data in one cell. Editing them by hand is easy to get wrong — change the setting in the app and export again instead.

Spreadsheet programs also mangle CSV files: they reformat numbers, strip leading zeros, and change quoting. If you must edit, use a plain text editor, or import the CSV as text rather than opening it directly.
{% endhint %}

</details>
