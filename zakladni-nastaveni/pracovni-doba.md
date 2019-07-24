# Working hours

This section allows you to set up working hours. That prevents your customers from making bookings that your agents wouldn't be able to e-ticket because they're out of the office \(outside of working hours\). However, we highly recommend to use one of the integrated payment gateways and set up the automated e-ticketing. Another option is to set up notifications and check the bookings also outside of your working hours in order to sell as many tickets as possible.

You can find the settings under **Agency -&gt; Working hours**.

![](../.gitbook/assets/image%20%2834%29.png)

You can set working hours for each day, including a lunch break, for example 9:00 – 11:30, 12:00 – 17:30. If the agency doesn't have a lunch break, it is necessary to set the entire working time 9:00 – 18:30 in the morning fields.

## The logic of setting working hours

This setting is a protection against a situation when your customer books a ticket at 17:35, but your office closes at 17:30. The booking must be e-ticketed on the same day but there's nobody at your office to do it. The same applies to weekends and days off in general. Your working hours are always compared to the last ticketing date. The last ticketing date displayed to customers is determined based on the fare conditions \(this can be limited in the settings\). However, thanks to the working hours settings, it is limited to the day when your agency is open so that there's enough time for the e-ticketing.

In order for this feature to function properly, it is also necessary to define for individual payment methods how much time within the working hours is needed to handle a business case. The default setting is 1 hour. This way you can affect which payment methods are offered when the last date of e-ticketing is approaching. If you want this date to match the date of booking \(ie. it has to be issued "immediately"\), you can set a higher value for the other payment methods and those are not offered at all.

You can encounter three different situations:

1. The customer books a ticket and there's enough time within your working hours to process the booking and to issue the ticket – everything is all right and the booking can be made.
2. The customer books a ticket but the payment methods have different minimum times required to handle bookings. Some can still be used within your working hours, some not. The customer is offered and can select only those that can be used within your working hours.
3. None of the payment methods allows the ticket to be issued within your working hours. In such case, GOL IBE does not allow the booking to be finished \(the booking form cannot be completed\) and it informs the customer. You can customize this notification in the GOL IBE back office under **Supporting texts**.

## Customization of standard working hours - public holidays etc.

Go to **Agency -&gt; Working hours modifications**

Here you can define exceptions to the set working hours, ie. to define public holidays and other days when your agency is closed. At this moment, there's no code list available for public holidays. If you need to define these days, please do so manually.

![](../.gitbook/assets/image%20%2856%29.png)

{% hint style="warning" %}
If you set only a date, it means that your agency is closed whole day. If you set time Since - Till, you limit your working hours on that day only to the defined period of time.
{% endhint %}

