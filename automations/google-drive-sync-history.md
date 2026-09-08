---
description: >-
  Check which uploaded files reached your Google Drive, and retry the ones that
  did not.
icon: clock-rotate-left
---

# Google Drive sync history

The **Sync history** link on the [Google Drive sync](google-drive-sync.md) page opens a record of every file the workflow has handled. Use it to confirm an order's files arrived, and to retry the ones that did not.

<table><thead><tr><th width="230">Column</th><th>Shows</th></tr></thead><tbody><tr><td><strong>Order</strong></td><td>The order the file came from</td></tr><tr><td><strong>File</strong></td><td>The name the file was given in Drive</td></tr><tr><td><strong>Size</strong></td><td>The file size</td></tr><tr><td><strong>Status</strong></td><td><strong>Synced</strong>, <strong>Failed</strong>, or <strong>Pending</strong></td></tr><tr><td><strong>Last attempt</strong></td><td>When the app last tried to copy the file</td></tr></tbody></table>

Filter by **All**, **Synced**, **Failed**, or **Pending**. A failed row shows the reason when you hover its status, and **Retry** re-runs anything that is not yet synced.

A file already in Drive is never copied twice, so retrying an order only picks up what is missing.

<figure><img src="../.gitbook/assets/drive 5.png" alt="The sync history table with a failed row and its retry action"><figcaption><p>Every file the workflow has handled, with a retry for the ones that did not arrive.</p></figcaption></figure>

## What the failure messages mean

<table><thead><tr><th width="330">Message</th><th>What to do</th></tr></thead><tbody><tr><td>The app lost access to your Google account</td><td>Reconnect the account. Syncing resumes from where it stopped</td></tr><tr><td>Your Google Drive is full</td><td>Free up space in that account, or upgrade its Google storage, then retry</td></tr><tr><td>The destination folder no longer exists in Google Drive</td><td>The folder was deleted or moved. Choose a root folder again</td></tr><tr><td>The uploaded file is no longer available</td><td>The original file has been removed and cannot be recovered</td></tr><tr><td>The connection to Google Drive dropped</td><td>Retry. This is usually temporary</td></tr><tr><td>Syncing was paused to stay within Google Drive limits</td><td>Nothing. It resumes on its own</td></tr></tbody></table>

The app retries temporary problems by itself — a dropped connection, Google being busy, or a Drive rate limit — spacing the attempts out over about an hour. A lost account, a full Drive, and a missing original file are not retried automatically, because the result would be the same until you fix the cause.

{% hint style="info" %}
The page is empty until a customer places an order with uploads. If it stays empty after one, check that the automation is saved and set to **Running**, and that the products in that order actually use a [File upload](../option-types/input-types/file-upload.md) option.
{% endhint %}

## Notes

* The history covers files, not orders. One order with four uploads is four rows.
* **Pending** means the file is queued or waiting on a retry, not that it failed.
* Staff accounts can read the history but cannot retry.
