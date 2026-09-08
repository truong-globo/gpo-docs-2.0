---
description: Add option details to the order confirmation email your customer receives.
icon: envelope-open-text
---

# Display options in confirmation email

This is the email your customer receives right after placing an order. By default, Shopify's order confirmation email doesn't include custom option details — but you can change that!

{% hint style="warning" %}
🔔 **Note:** If you've already customized your email templates, **do not** copy and paste the full code below. Instead, review and merge it carefully.
{% endhint %}

## 📌 Follow these steps

{% stepper %}
{% step %}
### From your **Shopify admin**, click on **Settings**, Select **Notifications**

<figure><img src="../.gitbook/assets/screenshot-order-confirmation-email-notifications.png" alt="Shopify settings with the Notifications section open"><figcaption><p>Settings, then Notifications.</p></figcaption></figure>
{% endstep %}

{% step %}
### Under **Customer Notifications**, click **Order confirmation**

<figure><img src="../.gitbook/assets/screenshot-order-confirmation-email-customer-notifications.png" alt="The Customer notifications list with Order confirmation highlighted"><figcaption><p>Customer notifications, then Order confirmation.</p></figcaption></figure>
{% endstep %}

{% step %}
### **Download the Order Confirmation template**

[Click this button to download](https://github.com/globo-software/display-cart-line-item-in-notification/blob/main/gpo-order-confirmation.liquid)
{% endstep %}

{% step %}
### **Copy the code** and Paste to Email body (HTML) box

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

<figure><img src="../.gitbook/assets/screenshot-order-confirmation-email-body.png" alt="The order confirmation template editor with the snippet pasted into the Email body HTML box"><figcaption><p>Paste the snippet into the Email body (HTML) box.</p></figcaption></figure>
{% endstep %}

{% step %}
### **Save**
{% endstep %}
{% endstepper %}

{% hint style="info" %}
📧 **Need Help?**

If you run into any issues while setting up your option set, feel free to reach out at **Chat** or email [contact@globo.io](mailto:contact@globo.io).

See [Contact support](../help/contact-support.md).
{% endhint %}
