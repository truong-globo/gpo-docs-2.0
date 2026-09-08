---
description: Add option details to the New order email your store owner and staff receive.
icon: bell
---

# Display option in staff order notification

This is the email the **store owner or staff** receives when a customer places a new order. To include product option details, you can customize the notification template by following these steps:

{% stepper %}
{% step %}
### From your **Shopify admin**, click **Settings**, Select **Notifications**

Scroll down to the **Staff Order Notifications** section

<figure><img src="../.gitbook/assets/screenshot-staff-order-notification-settings.png" alt="Shopify notification settings scrolled to the Staff notifications section"><figcaption><p>Settings, Notifications, then Staff order notifications.</p></figcaption></figure>
{% endstep %}

{% step %}
### Click **New order**

<figure><img src="../.gitbook/assets/screenshot-staff-order-notification-new-order.png" alt="The Staff notifications list with New order highlighted"><figcaption><p>Open the New order notification.</p></figcaption></figure>
{% endstep %}

{% step %}
### **Download the New Order template** ([click this button to download](https://github.com/globo-software/display-cart-line-item-in-notification/blob/main/gpo-new-order-notification.liquid))
{% endstep %}

{% step %}
### Open the downloaded file and **copy the code**

```liquid
 <div class="order-list__item-properties">
	{% assign property_size = line.properties | size %} 
	{% if property_size > 0 %} 
	{% for p in line.properties %} 
	<div class="order-list__item-property">
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

**and Paste to Email body (HTML) box**

<figure><img src="../.gitbook/assets/screenshot-staff-order-notification-email-body.png" alt="The New order template editor with the snippet pasted into the Email body HTML box"><figcaption><p>Paste the snippet into the Email body (HTML) box.</p></figcaption></figure>
{% endstep %}

{% step %}
### **Save**
{% endstep %}
{% endstepper %}

{% hint style="info" %}
📧 **Need Help?**

If you run into any issues while setting up your option set, feel free to reach out to us at **Chat** or email [**contact@globo.io**](mailto:contact@globo.io).

See [Contact support](../help/contact-support.md).
{% endhint %}
