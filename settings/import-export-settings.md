---
description: Back up your store-wide settings, or copy them to another store.
icon: file-export
---

# Import and export settings

The **Settings** page can export your store-wide settings to a file and import them back. This is separate from [importing and exporting option sets](../option-sets/import-and-export.md).

## Where it is

Use the **Export settings** and **Import settings** actions on the **Settings** page.

## What is included

<table><thead><tr><th width="290">Included</th><th>Not included</th></tr></thead><tbody><tr><td>Everything in <strong>General</strong> — placement, alignment, tooltips, page switches, cart settings</td><td>Your option sets. Export those separately</td></tr><tr><td>Everything in <strong>Design</strong> — colors, borders, typography, custom CSS, match theme style</td><td>Your templates</td></tr><tr><td>Everything in <strong>Add-on price</strong></td><td>Your automations</td></tr><tr><td></td><td>Uploaded custom fonts and images — those are files in your store</td></tr><tr><td></td><td>The app embed, which lives with your theme</td></tr></tbody></table>

## When to use it

<table><thead><tr><th width="330">Situation</th><th>Why it helps</th></tr></thead><tbody><tr><td>Before a big styling change</td><td>A free undo. Export first, and you can put everything back</td></tr><tr><td>Setting up a second store</td><td>Copy the whole look and behavior in one step instead of forty</td></tr><tr><td>Moving from a development store to live</td><td>The settings you tuned come with you</td></tr><tr><td>Handing the store to somebody else</td><td>A record of how it was configured</td></tr></tbody></table>

## Steps

### Export

{% stepper %}
{% step %}
### Open Settings
{% endstep %}

{% step %}
### Select Export settings

A file is downloaded to your computer.
{% endstep %}

{% step %}
### Store the file somewhere you can find it

Name it with the store and the date, for example `store-settings-2026-08.json` rather than `download.json`.
{% endstep %}
{% endstepper %}

### Import

{% stepper %}
{% step %}
### Select Import settings
{% endstep %}

{% step %}
### Choose your file
{% endstep %}

{% step %}
### Confirm

{% hint style="danger" %}
Importing **replaces** your current store-wide settings rather than merging them. Export your existing settings first if you may want them back.
{% endhint %}
{% endstep %}

{% step %}
### Check the result on a real product page

Check the widget placement in particular, because a selector that worked on one store's theme may not match on another.
{% endstep %}
{% endstepper %}

## Copying a whole setup to another store

Settings are one of several things to move. Do them in this order:

{% stepper %}
{% step %}
### Import the settings

This gives the new store the same appearance and behavior.
{% endstep %}

{% step %}
### Import the option sets

Import them separately, from the **Option Sets** page. See [Import and export](../option-sets/import-and-export.md).
{% endstep %}

{% step %}
### Reconnect the add-ons

Add-on products are per store, so options that linked to a product on the old store have nothing to link to on the new one. Reconfigure each one. See [Add-on pricing](../add-on-pricing/README.md).
{% endstep %}

{% step %}
### Re-upload fonts and images

Custom fonts and swatch images are files, and files are not included in either export.
{% endstep %}

{% step %}
### Enable the app embed on the new store's theme

See [Enable the app embed](../getting-started/enable-the-app-embed.md).
{% endstep %}

{% step %}
### Rebuild the automations

Workflows are configured per store. See [Automations](../automations/README.md).
{% endstep %}
{% endstepper %}

## Notes

* Importing replaces your settings rather than merging them.
* A custom **Widget placement** selector refers to a theme's markup, so it may need to be changed on a different store.
* Custom CSS is included, but it refers to your theme's classes, so check it on the new store.
* Importing and exporting settings may not be available on all plans. See [Compare plans](../plans/compare-plans.md).
