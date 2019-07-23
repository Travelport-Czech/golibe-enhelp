# Email notifications

To set up emails automatically sent by GOL IBE, go to **Notifications**.

All notifications are already pre-set for you.

In the clear table of set notifications, you can see columns showing to whom the emails are delivered.

| **To** | Description |
| :--- | :--- |
| **Customer** | Delivered to the customer who entered their email address during the booking process |
| **Dealer** | Delivered to the dealer whose email address is set in the section **Dealers** |
| **Agency** | Delivered to the agency whose email address is set under **Agency -&gt; Agency settings** |
| **Configurator** | Delivered to the system admin \(only for the purpose of fine-tuning or consultation\) |

If you wish to change this setting, click on **DELIVERY**.

{% hint style="warning" %}
GOL IBE sends email confirmations to customers on your behalf. For example, if your travel agency name was abtravel, your customers would get booking confirmations from the email address info@abtravel.com.

However, due to today's trend of maximum protection against spam the emails sent by GOL IBE on your behalf may not always be delivered to your customers.

Therefore, you need to set your emails / domain as follows:

If you use SPF, please allow our mail server in your domain settings:

**v=spf1 mx mx:golibe.com ~all**

If your domain already has an SPF record, then you must add the following SPF to the existing record:  
  
**include:golibe.com**

Allways add this CNAME record to your domain:

**golibe.\_domainkey.agentura.cz CNAME golibe.\_domainkey.golibe.com**
{% endhint %}

