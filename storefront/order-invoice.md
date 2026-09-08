---
description: Add option details to printed invoices produced by Shopify's Order Printer app.
icon: file-invoice
---

# Display option on order invoice

## Order invoice with Shopify Order Printer

The Product Options app integrates with Shopify's Order Printer, enabling option details to appear on printed invoices.

### Steps to configure

{% stepper %}
{% step %}
### Access **Apps** from your Shopify admin dashboard
{% endstep %}

{% step %}
### Locate and select **Order Printer** from your installed apps

<figure><img src="../.gitbook/assets/screenshot-order-invoice-open-order-printer.png" alt="The Apps list in Shopify admin with Order Printer highlighted"><figcaption><p>Open Order Printer from your list of installed apps.</p></figcaption></figure>
{% endstep %}

{% step %}
### Navigate to **Manage Templates** and choose **Invoice**

<figure><img src="../.gitbook/assets/screenshot-order-invoice-manage-templates.png" alt="The Order Printer templates screen with Manage templates and the Invoice template highlighted"><figcaption><p>Manage templates, then open the Invoice template.</p></figcaption></figure>
{% endstep %}

{% step %}
### Download the invoice template from the provided GitHub repository

[Click this button to download](https://github.com/globo-software/display-cart-line-item-in-notification/blob/main/gpo-order-invoice.liquid)
{% endstep %}

{% step %}
### Copy this code snippet into the Template Details section

```liquid
<div class="gpo-properties">
	{% assign property_size = line_item.properties | size %} 
	{% if property_size > 0 %} 
	{% for p in line_item.properties %} 
	<div class="gpo-property">
		{% assign first_character_in_key = p.first | truncate: 1, '' %}
		{% unless p.last == blank or first_character_in_key == '_' %} 
		<span>{{ p.first }}: </span>
		{%- if p.last contains '/uploads/' -%} 
		<a href="{{ p.last }}">{{ p.last | split: '/' | last }}</a> 
		{%- else -%} 
		{{ p.last }} 
		{%- endif -%} 
		{% endunless %} 
	</div> 
	{% endfor %}
{% endif %} 
</div>
```

<figure><img src="../.gitbook/assets/screenshot-order-invoice-template-details.png" alt="The invoice template editor with the snippet pasted into the Template Details field"><figcaption><p>Paste the snippet into the Template Details section.</p></figcaption></figure>
{% endstep %}

{% step %}
### Click **Save** to finalize changes
{% endstep %}
{% endstepper %}

### Support

{% hint style="info" %}
📩 **Need help?** If you run into any issues creating a new option set, don't hesitate to reach out! Email us anytime at [**contact@globo.io**](mailto:contact@globo.io) — we're here to help with sincere support.

See [Contact support](../help/contact-support.md).
{% endhint %}
