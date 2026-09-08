---
description: Copy the files customers upload into your own Google Drive, organized into a folder per order.
icon: google-drive
---

# Google Drive sync

Files a customer uploads are stored with the order, but they stay inside the app. This workflow copies them into your own Google Drive and sorts them into folders, so your production team can work from Drive instead of opening orders one at a time.

**Automations** in the app menu, then **Add workflow** > **Google Drive sync**. It has its own configuration page rather than the standard workflow form, and you can create one per store.

It copies every file attached through a [File upload](../option-types/input-types/file-upload.md) option, and optionally the [Personalizer](../personalizer/README.md) design image. Only line items created by the app are read, so ordinary products in the same order are skipped.

<!-- SCREENSHOT: drive-config-page | App admin → Automations → Google Drive sync | Trang cấu hình với card Connected, Destination và File names | Không khoanh -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The Google Drive sync page with its connection, destination, and file name sections"><figcaption><p>The whole automation is configured on one page.</p></figcaption></figure>

## Before you start

* Automations may not be available on all plans. See [Compare plans](../plans/compare-plans.md).
* Only the store owner can connect an account or change these settings. Staff accounts see the page read-only.
* Google Drive has to be enabled for your store first. If it is not, the page says **Google Drive is not set up for this app yet. Contact support to enable it.** See [Contact support](../help/contact-support.md).

## Connect a Google account

{% stepper %}
{% step %}
### Select **Connect Google Drive**

A Google window opens and asks for permission to create folders in the destination you select, upload files that customers attach to their orders, and read the storage quota of the account. The app never reads or deletes files outside the folder you select.
{% endstep %}

{% step %}
### Choose the Google account

Use the account whose Drive the files should live in. Copied files count against that account's storage, not against your Shopify plan.
{% endstep %}

{% step %}
### Save the automation

Until you save, the page shows **Save this automation to start copying files to Google Drive.** Nothing is copied before that.
{% endstep %}
{% endstepper %}

<!-- SCREENSHOT: drive-connect-panel | App admin → Automations → Google Drive sync (chưa kết nối) | Panel Connect a Google account với danh sách 3 quyền và nút Connect Google Drive | Khoanh nút Connect Google Drive -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The connect panel listing the three permissions the app asks for"><figcaption><p>The app asks for the narrowest access that lets it write into one folder.</p></figcaption></figure>

{% hint style="warning" %}
Three messages can appear instead of a connected account:

* **Your browser blocked the Google window.** Allow pop-ups for the page and try again.
* **The permission request was declined.** Connect again and approve the request.
* **Google did not grant long-lived access.** Remove the app from your Google account's permissions, then connect again.
{% endhint %}

Once connected, the page shows the account's email, the date it was connected, and how much of its storage is in use. If the app later loses access, the account is badged **Reconnect required** and syncing stops until you reconnect. Files already in Drive are not affected.

## Destination

<table><thead><tr><th width="290">Setting</th><th width="170">Default</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Root folder</strong></td><td>Created automatically</td><td>Where everything else is created. <strong>Change</strong> opens Google's own folder picker</td></tr><tr><td><strong>Order folder name</strong></td><td><code>Order #{order_number}</code></td><td>One folder per order, inside the root folder</td></tr><tr><td><strong>Create a folder for each product</strong></td><td>On</td><td>A folder per product inside the order folder</td></tr><tr><td><strong>Product folder name</strong></td><td><code>{product_title} - {variant_title}</code></td><td>The name of each product folder. Only displayed when the setting above is on</td></tr><tr><td><strong>Also sync personalizer design images</strong></td><td>On</td><td>Saves the Personalizer's generated image as <code>design-1.png</code> beside that product's files</td></tr></tbody></table>

If you do not choose a root folder, the app creates one called **Globo order files** in My Drive the first time it syncs.

Keep **Create a folder for each product** on. An order with three personalized products otherwise puts every photo in one folder, and nothing tells you which photo belongs to which item.

### Folder name tokens

Select a token chip to insert it, rather than typing it.

<table><thead><tr><th width="230">Order folder</th><th>Product folder</th></tr></thead><tbody><tr><td><code>{order_number}</code></td><td><code>{product_title}</code></td></tr><tr><td><code>{order_id}</code></td><td><code>{variant_title}</code></td></tr><tr><td><code>{customer_name}</code> — <code>Guest</code> with no account</td><td><code>{sku}</code></td></tr><tr><td><code>{order_date}</code> — as <code>2026-09-04</code></td><td><code>{line_item_index}</code> — position in the order, from 1</td></tr></tbody></table>

A token that does not exist is removed rather than printed, so a typo leaves a gap instead of `{prodct_title}`. Characters Drive cannot use — `/` `\` `:` `*` `?` `"` `<` `>` `|` — become spaces, and names longer than 100 characters are shortened.

The page previews the folder tree as you type, using a sample order, so you can check the structure before saving.

<!-- SCREENSHOT: drive-destination | App admin → Automations → Google Drive sync | Card Destination với Root folder, 2 ô tên folder, token chips và preview cây folder | Khoanh khối preview cây folder -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The destination settings with the folder tree preview underneath"><figcaption><p>The preview shows the folders your current names would produce.</p></figcaption></figure>

## File names

Files are numbered in upload order inside each folder: `1.jpg`, `2.jpg`, `3.jpg`. Personalizer images are numbered separately as `design-1.png`, so they never take a number from a customer's upload. The name the file had on the customer's own computer is not kept, which is why numbering is used.

## Running it

**Automation active** controls whether the workflow runs. On, it is **Running** and files from new orders are copied automatically. Off, it is **Paused** and no new files are copied. Pausing removes nothing from Drive.

**Test** opens a list of your recent orders. Select one that has uploads, and the workflow runs against it, so you can check the folder structure and file names in your Drive before real orders arrive.

**Sync history** records every file the workflow has handled, and is where you retry anything that did not arrive. See [Google Drive sync history](google-drive-sync-history.md).

## Disconnecting

**Disconnect** removes the Google account from the app. It asks you to confirm first, because it also pauses the automation.

Files already in Drive stay there. New order files stop syncing until you connect an account again.

## Notes

* One Google Drive sync workflow per store.
* The workflow runs shortly after an order is created, so files appear in Drive a short time later rather than immediately.
* Files are copied, not moved. They remain available from the order in Shopify admin. See [Show options on orders](../storefront/show-options-on-orders.md).
* Changing the folder name settings affects new orders only. Folders that already exist are not renamed.
* Staff accounts can open the page and read the sync history, but cannot connect, change settings, disconnect, or retry.
