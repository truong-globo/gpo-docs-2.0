---
description: >-
  Move option sets between stores as CSV, keep backups, and migrate from another
  product options app.
icon: file-import
---

# Import and export

Export writes your option sets to a CSV file. Import reads one back — either a file this app produced, or a file exported from one of several other product options apps.

Three good reasons to use it: backing up before a risky change, copying a setup from a development store to a live one, and migrating from an app you are leaving.

## Before you start

* Both actions are on the **Option Sets** page, as secondary actions next to **Create option set**.
* Import and export are plan-gated separately. If either shows an upgrade prompt, see [Compare plans](../plans/compare-plans.md).

## Export

{% stepper %}
{% step %}
### Optionally select the sets you want

If you only want specific option sets, tick their rows first.
{% endstep %}

{% step %}
### Select Export option sets

The export dialog opens.
{% endstep %}

{% step %}
### Choose what to include

<table><thead><tr><th width="260">Choice</th><th>Includes</th></tr></thead><tbody><tr><td><strong>Current page</strong></td><td>Every option set on the page you are looking at.</td></tr><tr><td><strong>All option sets</strong></td><td>Everything in your store, across all pages.</td></tr><tr><td><strong>Selected: N option sets</strong></td><td>Only your ticked rows. Unavailable when nothing is selected.</td></tr></tbody></table>
{% endstep %}

{% step %}
### Choose the format

**Plain CSV file** is the format.
{% endstep %}

{% step %}
### Select Export option sets

Your browser downloads a CSV file named `OptionsExport.csv`.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: set-export-modal | App admin → Option Sets → modal Export option sets | Nhóm "Export" với 3 lựa chọn và nhóm "Export as" với Plain CSV file | Không khoanh (modal đơn) -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The export dialog with scope choices and the CSV format option"><figcaption><p>Export the current page, everything, or just your selection.</p></figcaption></figure>

{% hint style="info" %}
Export before any change you are not sure about. The file costs nothing to produce and is the only way to get an option set back after it is deleted.
{% endhint %}

## Import

{% stepper %}
{% step %}
### Select Import option sets

The import dialog opens with a drop zone.
{% endstep %}

{% step %}
### Get the sample file, if you are building one by hand

The dialog links to a **sample CSV template** showing the required format. Start from it rather than inventing the layout.
{% endstep %}

{% step %}
### Add your file

Drop the file into the drop zone, or select it. Accepted formats: `.csv`, `.txt`, `.xlsx`, `.xls`, up to 10 MB.
{% endstep %}

{% step %}
### Say which app the file came from

**Select app for import** tells the app how to read your file. The choices are:

<table><thead><tr><th width="330">Choice</th><th>Use for</th></tr></thead><tbody><tr><td><strong>Globo Product Options, Variant</strong></td><td>A file exported from this app. This is the default.</td></tr><tr><td><strong>Easify Custom Product Options</strong></td><td>A file exported from that app.</td></tr><tr><td><strong>Avis Product Options, Variants</strong></td><td>A file exported from that app.</td></tr><tr><td><strong>OPTIS Product Options, Variant</strong></td><td>A file exported from that app.</td></tr><tr><td><strong>Qikify Custom Product Options</strong></td><td>A file exported from that app.</td></tr><tr><td><strong>Hulk Product Options</strong></td><td>A file exported from that app.</td></tr><tr><td><strong>APO Product Options, Variants</strong></td><td>A file exported from that app.</td></tr></tbody></table>

Picking the wrong app here is the most common cause of a failed import — the file is read with the wrong column layout.
{% endstep %}

{% step %}
### Decide whether the imports go live immediately

**Set all imported option sets as Active** publishes everything as it arrives.

Leave it off for the safer path: imports land as **Draft**, you review them, then activate the ones you want.
{% endstep %}

{% step %}
### Select Upload and continue

The app reads the file and creates the option sets. A message confirms the result, or explains what stopped it.
{% endstep %}

{% step %}
### Review what arrived

Open each imported set and check its options, its **Name** fields, its add-on configuration, and its product rule.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: set-import-modal | App admin → Option Sets → modal Import | Drop zone + link sample CSV template + danh sách "Select app for import" 7 lựa chọn + checkbox Set all imported option sets as Active | Khoanh khối "Select app for import" -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The import dialog with the drop zone, the app selector, and the set as active checkbox"><figcaption><p>Telling the app which file format you have is the step people skip.</p></figcaption></figure>

## Migrating from another product options app

{% stepper %}
{% step %}
### Export from your old app

Use that app's own export feature to produce its CSV.
{% endstep %}

{% step %}
### Import here, without activating

Import the file with **Set all imported option sets as Active** left **off**. Everything lands as draft.
{% endstep %}

{% step %}
### Review each imported set

Expect to do some tidying. Different apps model options differently, so check in particular:

* **Add-on pricing** — how the other app charged may not map exactly. Review every price and pick the right mode. See [Add-on pricing](../add-on-pricing/README.md).
* **Conditional logic** — rules may need rebuilding, since operators differ between apps.
* **Names** — check every option's **Name**, and that none clash. See [Label vs Name](../concepts/label-vs-name.md).
* **Product rules** — confirm each set targets what you expect.
* **Images** — swatch images may need re-uploading if the old app hosted them itself.
{% endstep %}

{% step %}
### Test on a product, then switch over

Activate one imported set, test it on a real product with **View in Store**, and only then uninstall the old app and activate the rest.

Uninstalling the old app first means any gap in coverage is visible to shoppers.
{% endstep %}
{% endstepper %}

## What the exported CSV contains

The file has one row per option value. Options without values — text fields, for example — get a single row. Columns that describe the whole option set or the whole option are filled on the **first** row only and left blank on the rest, which keeps the file readable.

<table><thead><tr><th width="230">Column</th><th>Contains</th></tr></thead><tbody><tr><td><code>option_set_id</code></td><td>The option set's ID, repeated on every row of that set.</td></tr><tr><td><code>option_set_name</code></td><td>The option set's name. First row of the set only.</td></tr><tr><td><code>option_id</code></td><td>The option's internal ID within the set.</td></tr><tr><td><code>option_type</code></td><td>The option's type.</td></tr><tr><td><code>option_label</code></td><td>The option's <strong>Label</strong>, including any translations.</td></tr><tr><td><code>option_name</code></td><td>The option's <strong>Name</strong>.</td></tr><tr><td><code>required</code></td><td><code>yes</code> when <strong>Required field</strong> is on, otherwise blank.</td></tr><tr><td><code>allow_multiple</code></td><td><code>yes</code> when multiple selection or multiple file upload is on.</td></tr><tr><td><code>min</code>, <code>max</code></td><td>The option's minimum and maximum, whatever they measure for that type.</td></tr><tr><td><code>placeholder</code></td><td>The option's <strong>Placeholder</strong>.</td></tr><tr><td><code>helptext</code></td><td>The option's <strong>Help text</strong> and its position.</td></tr><tr><td><code>option_value</code></td><td>The value on this row, with its own help text where it has one.</td></tr><tr><td><code>addon</code></td><td>The add-on configuration for this value or option: which mode, which product and variant, and the price.</td></tr><tr><td><code>swatch_name</code></td><td>The swatch's internal name.</td></tr><tr><td><code>swatch_value</code></td><td>The colour, the two colours of a split swatch, or the image address.</td></tr><tr><td><code>swatch_asset_name</code></td><td>The uploaded image's file name.</td></tr><tr><td><code>default_value</code></td><td>The option's default value.</td></tr><tr><td><code>rich_text_value</code></td><td>Rich-text content for static options such as Paragraph, Pop-up modal, HTML, Size chart, and Tabs.</td></tr><tr><td><code>advanced_settings</code></td><td>Everything from the <strong>Advanced Settings</strong> and <strong>Personalizer Settings</strong> tabs, packed into one cell.</td></tr><tr><td><code>columnWidth</code></td><td>The option's <strong>Column width</strong>.</td></tr><tr><td><code>conditionalField</code></td><td><code>yes</code> when conditional logic is on for this option.</td></tr><tr><td><code>condition_logic</code></td><td>The conditional logic rule itself.</td></tr><tr><td><code>products</code></td><td>The option set's product rule. First row of the set only.</td></tr><tr><td><code>customers</code></td><td>The customer rule. First row of the set only.</td></tr><tr><td><code>countries</code></td><td>The country rule. First row of the set only.</td></tr><tr><td><code>settings</code></td><td>Option set settings, including the Personalizer background. First row of the set only.</td></tr></tbody></table>

{% hint style="warning" %}
Several columns hold structured data in a single cell — `addon`, `condition_logic`, `advanced_settings`, `products`, `customers`, `countries`, `settings`. Editing those by hand is easy to get wrong. Prefer changing the setting in the app and exporting again.

Spreadsheet programs are also prone to mangling CSV files: they reformat numbers, strip leading zeros, and change quoting. If you must edit the file, use a plain text editor, or import the CSV into your spreadsheet as text rather than opening it directly.
{% endhint %}

## What is not included

Exported option sets carry their own configuration only. These are store-wide and travel separately:

* Colours, borders, typography, and custom CSS — export them from **Settings**. See [Import and export settings](../settings/import-export-settings.md).
* Widget position and behaviour — also in **Settings**.
* Widget text and validation messages — in **Settings > Translations**.
* Automations — configured per store in **Automations**.
* Add-on products themselves. The file records which product an add-on pointed at, but importing into a different store cannot recreate that store's products. Reconnect add-ons after importing across stores.

## Limits and notes

* Import respects your plan. If a file contains features or counts your plan does not allow, the import is refused with an upgrade message rather than partially applied.
* Imported sets are added; nothing is overwritten or merged. Importing the same file twice gives you two copies.
* Import accepts `.csv`, `.txt`, `.xlsx`, and `.xls` up to 10 MB.
* Files exported by older versions of this app are still readable — the app recognises the older column layout automatically.

## Troubleshooting

<details>
<summary>The import failed with an invalid file message</summary>

Check three things: the extension is one of `.csv`, `.txt`, `.xlsx`, `.xls`; the file is under 10 MB; and **Select app for import** matches where the file came from. A file from another app read as a Globo file will fail.
</details>

<details>
<summary>The import says my plan does not allow it</summary>

The file contains option types or configurations your plan does not include. Either upgrade, or remove those options from the file before importing.
</details>

<details>
<summary>The import worked but the option sets look wrong</summary>

Most likely the wrong app was selected, so columns were read in the wrong order. Delete the imported sets and import again with the correct app selected.
</details>

<details>
<summary>Imported add-ons have no product attached</summary>

Add-on products are per store. When you import into a different store the referenced products do not exist there. Open each option and reconfigure its add-on — see [Add-on pricing](../add-on-pricing/README.md).
</details>

<details>
<summary>Swatch images are missing after import</summary>

Images referenced by address may not be reachable from the new store. Re-upload them on the affected option values.
</details>

<details>
<summary>Everything imported as Draft</summary>

Expected unless you ticked **Set all imported option sets as Active**. Activate them from the list with the **Set as active** bulk action.
</details>

<details>
<summary>Export or Import is greyed out</summary>

Your plan does not include that action. They are gated separately, so you may have one and not the other. See [Compare plans](../plans/compare-plans.md).
</details>

## Next steps

* [Option set analytics](analytics.md)
* [Import and export settings](../settings/import-export-settings.md) — for the store-wide settings.
* [Custom templates](../templates/custom-templates.md) — reuse within one store, without files.
