---
description: The store-wide settings, and which page each one lives on.
icon: gear
---

# Overview

**Settings** in the app menu holds everything that applies to your whole store rather than to one option set. It has three tabs across the top.

<table><thead><tr><th width="230">Tab</th><th>Contains</th></tr></thead><tbody><tr><td><strong>Settings</strong></td><td>Three sections: <strong>General</strong>, <strong>Design</strong>, and <strong>Add-on price</strong></td></tr><tr><td><strong>Translations</strong></td><td>The widget's fixed text and every validation message, per language</td></tr><tr><td><strong>Theme Setup</strong></td><td>Choosing a theme and turning the app embed on or off</td></tr></tbody></table>

<!-- SCREENSHOT: settings-tabs | App admin → Settings | 3 tab Settings / Translations / Theme Setup và 3 section trong tab Settings | Khoanh hàng 3 tab -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The settings page with its three tabs and the three sections inside Settings"><figcaption><p>Three tabs, and three sections inside the first one.</p></figcaption></figure>

## Finding a setting

<table><thead><tr><th width="330">Setting</th><th>Page</th></tr></thead><tbody><tr><td>Where the widget appears, tooltips, height limits, quickview, cart behaviour, custom fonts</td><td><a href="general-settings.md">General settings</a></td></tr><tr><td>Colours, borders, typography, custom CSS, match theme style</td><td><a href="design-settings.md">Design settings</a></td></tr><tr><td>How add-on prices are displayed, and cart merging</td><td><a href="add-on-price-settings.md">Add-on price settings</a></td></tr><tr><td>Widget text and validation messages</td><td><a href="../translations/translate-widget-text.md">Translate widget text</a></td></tr><tr><td>The app embed and which theme it applies to</td><td><a href="theme-setup.md">Theme setup</a></td></tr><tr><td>Uploading your own fonts</td><td><a href="custom-fonts.md">Custom fonts</a></td></tr><tr><td>Backing up or copying your settings</td><td><a href="import-export-settings.md">Import and export settings</a></td></tr></tbody></table>

## Everything here is store-wide

There is no per-option-set version of any of it. One widget position, one colour scheme, one set of messages, for every option set.

That is deliberate — a shop where different products had differently styled option forms would look broken. When you genuinely need a difference, the route is an [HTML class](../option-types/shared-settings/direction-width-and-css.md#html-class) on the option plus [custom CSS](../storefront/custom-css.md).

## Saving

Changes are saved explicitly. The app warns you if you try to leave with unsaved changes, and offers to discard them.
