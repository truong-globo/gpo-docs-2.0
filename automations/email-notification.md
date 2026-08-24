---
description: Email yourself every order containing options, with your own subject, layout, and sending service.
icon: envelope
---

# Email notification

Sends you an email when a customer orders a product with options, listing what they chose.

For a personalisation business this is often the first automation worth setting up: it puts the production detail in your inbox without anybody opening Shopify admin.

You can have one email notification workflow.

## The three tabs

The workflow editor has three tabs.

<table><thead><tr><th width="230">Tab</th><th>What it holds</th></tr></thead><tbody><tr><td><strong>Preview</strong></td><td>The email as it will arrive, with the subject line above it</td></tr><tr><td><strong>Edit code</strong></td><td><strong>Email subject</strong> and <strong>Email body (HTML)</strong>, plus the Liquid variable reference</td></tr><tr><td><strong>Configure</strong></td><td>Which service sends the email, and what it is sent from</td></tr></tbody></table>

<!-- SCREENSHOT: auto-email-tabs | App admin → Automations → workflow Email notification | 3 tab Preview / Edit code / Configure, tab Preview đang mở | Khoanh hàng 3 tab -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="The email notification workflow with its Preview, Edit code, and Configure tabs"><figcaption><p>Preview what will arrive, edit the template, and choose how it is sent.</p></figcaption></figure>

## Editing the email

**Edit code** gives you the subject and the body as HTML. Both accept Liquid variables, so the email can include the order number, the customer's details, and every line item with its options.

The full list of variables is available from the page itself, and documented in [Liquid variables reference](liquid-variables-reference.md).

A useful subject line puts the important information where you can see it in a list:

```liquid
New personalised order {{ order_name }} — {{ customer_name }}
```

If you break the template, **Revert to default** restores the original. It asks you to confirm, because anything you wrote is lost.

## Choosing how it is sent

**Configure** decides which service delivers the email.

<table><thead><tr><th width="230">Provider</th><th width="180">Type</th><th>You need</th></tr></thead><tbody><tr><td><strong>Default</strong></td><td>Ours</td><td>Nothing. Works immediately</td></tr><tr><td>Google</td><td>SMTP</td><td>Server, port, encryption, username, password</td></tr><tr><td>Outlook</td><td>SMTP</td><td>The same</td></tr><tr><td>SendGrid</td><td>API</td><td>An API key</td></tr><tr><td>Sendinblue</td><td>API</td><td>An API key</td></tr><tr><td>Pepipost</td><td>API</td><td>An API key</td></tr><tr><td>Amazon SES</td><td>API</td><td>Key id, secret key, region</td></tr><tr><td>Elastic Email</td><td>API</td><td>An API key</td></tr><tr><td>Mailgun</td><td>API</td><td>An API key and a domain</td></tr><tr><td>Zoho</td><td>API</td><td>An API key, a from address, and a bounce address</td></tr></tbody></table>

The SMTP providers pre-fill their usual server and port, so you normally only supply your username and password.

### Custom sender information

Whichever provider you use, you can set:

<table><thead><tr><th width="230">Field</th><th>What it does</th></tr></thead><tbody><tr><td><strong>From email</strong></td><td>The address the email appears to come from</td></tr><tr><td><strong>From name</strong></td><td>The name shown alongside it</td></tr><tr><td><strong>Reply to</strong></td><td>Where replies go</td></tr></tbody></table>

### Which provider to choose

<table><thead><tr><th width="290">Situation</th><th>Choice</th></tr></thead><tbody><tr><td>You just want the emails, today</td><td><strong>Default</strong></td></tr><tr><td>You already use a sending service</td><td>That one, so all your mail is in one place</td></tr><tr><td>Emails must come from your own domain</td><td>Your own provider, with the sender fields set</td></tr><tr><td>Emails are going to spam</td><td>Your own provider, on a domain you have authenticated</td></tr><tr><td>You need delivery reporting</td><td>An API provider, which gives you its own dashboard</td></tr></tbody></table>

{% hint style="info" %}
Start with **Default**. It works with no configuration, and you can move to your own provider later without changing the template.
{% endhint %}

## Testing

**Send test email** sends the current template to the address shown, and **Send test to another email** sends it somewhere else — useful for checking it arrives for a colleague, or for testing spam handling.

Send a test after every change to the template or the provider. It is the only way to know an SMTP password or API key is right.

Test sending is rate-limited, so wait a moment between attempts rather than retrying immediately.

## Notes

* One email notification workflow per store.
* It runs on orders containing app options, shortly after the order is created.
* A workflow set to **Draft** sends nothing.
* Requires order data access, approved once when you first open **Automations**.
* Provider credentials are stored so the workflow can send. Use an application password or an API key rather than your main account password where the provider offers one.
