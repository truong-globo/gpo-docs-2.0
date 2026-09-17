---
description: What the synced files look like in your Drive — three levels, from the root folder down to the files themselves.
icon: folder-tree
---

# What it looks like in Drive

Files are never dumped into one folder. The workflow builds three levels, so a file's path tells you which order and which product it belongs to before you open it.

```
Globo order files          ← root folder
└── Order #1112            ← one per order
    └── Personalized Dog Paw Ornament - Rose gold
        ├── 1.png          ← the customer's uploads, in upload order
        ├── 2.jpg
        └── design-1.png   ← the Personalizer design
```

Each level is named by a setting you control. See [Destination](README.md#destination).

## The root folder

Everything the workflow creates lives inside one folder. If you did not choose one when you set the automation up, it is created in **My Drive** and called **Globo order files**.

<!-- SCREENSHOT: drive-tree-root | Google Drive → My Drive → Globo order files | Danh sách folder Order #1107 … #1114 | Khoanh tên folder gốc trên breadcrumb -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="The root folder in Google Drive containing one folder per order"><figcaption><p>One folder per order, newest at the top.</p></figcaption></figure>

Share this one folder with your production team and they see every order as it arrives, without needing access to the rest of your Drive.

## The order folder

Inside the root, each order gets its own folder. The default name is `Order #{order_number}`, which is the number your team sees in Shopify admin.

<!-- SCREENSHOT: drive-tree-order | Google Drive → Globo order files → Order #1112 | Các folder sản phẩm bên trong một order | Khoanh tên order trên breadcrumb -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="An order folder containing one folder per personalized product in that order"><figcaption><p>Inside an order, one folder per personalized product.</p></figcaption></figure>

The product level only exists when **Create a folder for each product** is on. Turn it off and every file in the order lands directly in the order folder — fine for one-product orders, confusing for the rest.

## The product folder

The lowest level holds the actual files. The default name is `{product_title} - {variant_title}`, so a folder tells you the exact variant to produce.

<!-- SCREENSHOT: drive-tree-files | Google Drive → Globo order files → Order #1112 → 1 folder sản phẩm | 3 file: 1.png, 2.jpg, design-1.png | Khoanh danh sách file -->

<figure><img src="../../.gitbook/assets/placeholder.png" alt="A product folder containing the customer's uploads and the personalizer design"><figcaption><p>Uploads are numbered in upload order; the Personalizer design is prefixed so it never takes a number from them.</p></figcaption></figure>

<table><thead><tr><th width="230">File</th><th>What it is</th></tr></thead><tbody><tr><td><code>1.png</code>, <code>2.jpg</code></td><td>What the customer uploaded, numbered in the order they attached them</td></tr><tr><td><code>design-1.png</code></td><td>The image the Personalizer generated. Only present when <strong>Also sync personalizer design images</strong> is on</td></tr></tbody></table>

The customer's original filename is not kept, which is why the numbering exists. See [File names](README.md#file-names).

{% hint style="info" %}
**A product with no variants leaves a trailing dash.** The default name ends with `- {variant_title}`, and a single-variant product has nothing to put there, so the folder reads `The Collection Snowboard Hydrogen -`.

It is only cosmetic. If it bothers you, and none of your personalized products have variants, set **Product folder name** to `{product_title}` on its own.
{% endhint %}

## Changing the shape

<table><thead><tr><th width="290">You want</th><th>Change</th></tr></thead><tbody><tr><td>Everything under a folder you already share</td><td><strong>Root folder</strong> — select <strong>Change</strong> and pick it</td></tr><tr><td>Folders named by customer or date instead of order number</td><td><strong>Order folder name</strong> — use <code>{customer_name}</code> or <code>{order_date}</code></td></tr><tr><td>One folder per order, no product level</td><td>Turn off <strong>Create a folder for each product</strong></td></tr><tr><td>Folders named by SKU, for a production system that matches on it</td><td><strong>Product folder name</strong> — use <code>{sku}</code></td></tr><tr><td>Uploads only, no design images</td><td>Turn off <strong>Also sync personalizer design images</strong></td></tr></tbody></table>

All of these are on the [Google Drive sync](README.md) page, and the preview there shows the result before you save.

## Notes

* Folders are created the first time a file needs them, so an order with no uploads creates nothing.
* Changing a name setting affects new orders only. Folders that already exist are not renamed.
* Renaming or moving a folder in Drive yourself does not break the workflow, but the app creates the expected folder again on the next order.
* A file already in Drive is never copied twice, so a retry only adds what is missing. See [Google Drive sync history](google-drive-sync-history.md).
