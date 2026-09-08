---
description: Add option details to your packing slips, through Order Printer or Shopify's own packing slip template.
icon: box-open
---

# Display options in packing slip

There are two ways to do this. Use whichever matches how you print your packing slips.

## Using Shopify Order Printer

Our **Product Options** app works with Shopify's **Order Printer** app, so you can include custom option details right on your packing slips.

{% stepper %}
{% step %}
### From your **Shopify admin**, click on **Apps**
{% endstep %}

{% step %}
### Select **Order Printer** from your app list

<figure><img src="../.gitbook/assets/screenshot-packing-slip-open-order-printer.png" alt="The Apps list in Shopify admin with Order Printer highlighted"><figcaption><p>Open Order Printer from your app list.</p></figcaption></figure>
{% endstep %}

{% step %}
### Click **Manage Templates** > **Packing slip**

<figure><img src="../.gitbook/assets/screenshot-packing-slip-manage-templates.png" alt="The Order Printer templates screen with Manage templates and the Packing slip template highlighted"><figcaption><p>Manage templates, then open the Packing slip template.</p></figcaption></figure>
{% endstep %}

{% step %}
### **Download the packing slip template**

[Click this button to download](https://github.com/globo-software/display-cart-line-item-in-notification/blob/main/gpo-packing-slip-template-order-printer.liquid)
{% endstep %}

{% step %}
### **Copy the code** and **paste to Template Details** section

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
              <span>{{ p.last }}</span>
            {%- endif -%} 
          {% endunless %} 
        </div> 
      {% endfor %}
    {% endif %} 
  </div>
```

<figure><img src="../.gitbook/assets/screenshot-packing-slip-template-details.png" alt="The Order Printer packing slip editor with the snippet pasted into the Template Details field"><figcaption><p>Paste the snippet into the Template Details section.</p></figcaption></figure>
{% endstep %}

{% step %}
### **Save the change**
{% endstep %}
{% endstepper %}

## Through Shopify settings

This method lets you directly update Shopify's built-in packing slip template from your store's settings.

{% stepper %}
{% step %}
### From your **Shopify admin**, click on **Settings**
{% endstep %}

{% step %}
### Go to **Shipping and Delivery**
{% endstep %}

{% step %}
### Scroll down to the **Packing Slip Template** section

Click **Edit** next to the Packing Slip Template.

<figure><img src="../.gitbook/assets/screenshot-packing-slip-shipping-settings.png" alt="Shopify's Shipping and delivery settings with the Packing slip template row highlighted"><figcaption><p>Shipping and delivery, then the Packing slip template.</p></figcaption></figure>
{% endstep %}

{% step %}
### **Download the packing slip template**

[Click this button to download](https://github.com/globo-software/display-cart-line-item-in-notification/blob/main/gpo-packing-slip-template.liquid)
{% endstep %}

{% step %}
### **Copy the code** and paste to **Edit Packing Slip Template** field

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

<figure><img src="../.gitbook/assets/screenshot-packing-slip-edit-template.png" alt="The Edit packing slip template field in Shopify settings with the snippet pasted in"><figcaption><p>Paste the snippet into the Edit Packing Slip Template field.</p></figcaption></figure>
{% endstep %}

{% step %}
### Save
{% endstep %}
{% endstepper %}

{% hint style="info" %}
📧 **Need Help?**

If you run into any issues while setting up your option set, feel free to reach out to us at **Chat** or email [contact@globo.io](mailto:contact@globo.io).

See [Contact support](../help/contact-support.md).
{% endhint %}
