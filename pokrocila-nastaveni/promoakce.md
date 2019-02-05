# Special offers

This module lets you sell special fares of selected carriers through calendars showing their availability. 

**Special offers can be created:**

1. **Mannually** by adding a special offer and defining all required parameters of the connection.
2. **Automatically** by letting GOL IBE suggest special offers based on bookings passengers have made before. Each such suggested special offer is added in the back office as a non-activated offer. Until their possible activation, all suggested offers are being compared to every newly created offer for the same connection, and if the newly created offer is cheaper, the original one is replaced. 

{% hint style="info" %}
Departures and arrivals for automatically suggested special offers are preset from the first day of the month in which the flight was booked until the last day of the third month since the day for which the flight was booked. Validity of the special offer is preset from the current date until the last possible date of departure.
{% endhint %}

### Settings

You can change settings of special offers in the back office under **Prices &gt; Special offer extended**. 

Besides the regular buttons - **DELETE/EDIT/DETAIL** \(detail shows all information as well as edit, but you cannot edit it\) - there are also the following functions:

* Copy special offer – button **COPY**. COPY opens a new special offer for editting, including all items as the original one.
* Button **RUN CACHE** launches a robot which retrieves information about flights from the reservation system. To display the special offer at your front-end, check the _Display_ box in the detail of the offer.

![](../.gitbook/assets/image%20%2824%29.png)

### Edit/Add new special offer

The settings page is divided into several sections \(mandatory fields are in bold\): 

## 1. Basic settings of special offers

![](../.gitbook/assets/image%20%2833%29.png)

| Pole | Popis |
| :--- | :--- |
| **Valid since - till** | Time period during which the special offer is shown to customers on your website. |
| **Departure since - till** | Time period during which departure is possible. |
| **Returns since - till** | Time period during which return is possible. |
| **Included in the set** | This field defines which set the special offer belongs to. For example: Europe, Asia, Special offers for up to 5000 etc. You can display special offers on your website based on these sets. |

## 2. Prices and fees settings

![](../.gitbook/assets/image%20%283%29.png)

| Pole | Popis |
| :--- | :--- |
| **Use a manually set up fee** | If you don't check this, the service fee is calculated based on the default settings for air ticket service fees. |
| **Ticket price** | Price of tickets and taxes. The total price of air ticket + taxes is compared with the quote in the GDS, and if the price in the GDS is higher by more than 10 %, such connection will be marked as not available. |
| **Service fee** | This is the amount of the service fee, if you checked the option _Use a manually set up fee_. The special offer can use its own fee that can be the same or different from the fee used for regular search. |
| **Service fee for infant in % from** | Here you can set a fee for infants. It is defined as a percentual discount from the price for adult passengers. |
| **Rounded** | Range of rounding. |
| Displayed final price | The total price, ie. the combination of _Ticket price_ and _Service fee_. This price is shown to end customers on your website. |

## 3. Special offer statistics

![](../.gitbook/assets/image%20%2840%29.png)

| Pole | Popis |
| :--- | :--- |
| **Last measurement of cache** | The last time when information about flights has been retrieved. |
| **Number of availability requests** | The number of availability requests sent during the last update of the special offer. |
| **Current price from Galileo GDS** | Here you can see results of the verification quote. The quote is done regardless of availability. GOL IBE does a maximum of 5 attempts to get a quote, combining days at the beginning of validity of the special offer, then a week later, during weekends etc. to increase the chance of getting a successful quote. |

Technical notes:

{% hint style="info" %}
The availability information is refreshed based on how the special offer is used by customers. If a customer finds an unavailable combination, it is no longer offered to the next customers. GOL IBE also refreshes the availability information regularly, at least once every 24 hours during the nighttime.
{% endhint %}

## 4. Status

![](../.gitbook/assets/image%20%281%29.png)

| Pole | Popis |
| :--- | :--- |
| **Validate by robot** | If you check this, the data is automatically refreshed regularly. |
| **Display** | If you check this, the special offer is shown to customers at your front-end. |
| **Deactivate if quoted price is incorrect** | GOL IBE gets a verification quote for the special offer \(you can see the status in the section _Special offer statistics_. If the price difference is within +/- 10 %, the price is corrected. If the price is outside of this range, for example due to incorrectly set up special offer, and if you activate this option, the offer is not displayed on your website. |
| **Automatic special offer** | Whether the special offer has been created automatically, or not. |
| **Cached** | Whether the special offer has been cached \(ie. information has been retrieved from the reservation system\), or not. |
| **Found flights** | Whether available flights have been found in the reservation system for the special offer. |
| **FQCS Price OK** | Whether a quote has been found for the requested range. |

## 5. General restrictions

![](../.gitbook/assets/image%20%2811%29.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Pole</th>
      <th style="text-align:left">Popis</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Min/Max stay</b>
      </td>
      <td style="text-align:left">
        <p>Here you can restrict certain flights, in this order:</p>
        <p>1st field – a figure defining a number of days, or the text <em>SU</em> in
          case you need to apply the Sunday Rule.</p>
        <p>2nd field (selection) – specification for the 1st field, whether you mean
          days or months.</p>
        <p>3rd field (selection) – specification for the whole rule, whether you
          mean minimum or maximum number of days/months.</p>
      </td>
    </tr>
  </tbody>
</table>You need to define each leg of the journey. Simple connections without transfer, such as VIE-CDG, need to be defined in the section _Forward_  as shown in the picture below. In case of connections with transfer, such as VIE-FRA-CDG, you first need to define the leg VIE-FRA, then click the button _Add another flight segment for the same direction_ and add the second leg FRA-CDG to the new field.

In case of return connections, you need to do the same in the section _Backward_. You can create the return journey by clicking either the button _Add backward route_ where you go through the same process as in case of the forward journey, or the button _Create backward route automatically_ which will automatically create a mirror version of the forward journey.  

![](../.gitbook/assets/image%20%2829%29.png)

| Pole | Popis |
| :--- | :--- |
| **Origin \(IATA code\)** | IATA code of the departure point. |
| **Destination \(IATA code\)** | IATA code of the arrival point. |
| **Marketing carrier** | Carrier shown in availability. |
| **Booking classes** | Booking class \(RBD\). |
| **Fare Basis Code** | Fare Basis used for pricing this leg of the flight. |
| **Fare Basis Carrier** | Code of the carrier to which the Fare Basis belongs \(shown in Fare Display\). In some cases, another marketing carrier can operate the flight using a Fare Basis of its interline partner. |
| **Button** _**Update conditions**_ | This button refreshes fare conditions from the reservation system. The conditions are shown in other tabs. |

![](../.gitbook/assets/image%20%2836%29.png)

| Pole | Popis |
| :--- | :--- |
| **Search together with following** | If you check this, availability is verified together with the following segment based on O&D, ie. for the whole journey. Otherwise, availability is verified for individual segments separately for each part of the journey. |
| **Inhibit status link** | If you check this, availability is not verified at the carrier via seamless availability, even if it's possible. If not checked, a higher use intensity can negatively impact the ratio between the number of requests sent to the carrier and the number of bookings, which may lead to sanctions from the carrier. |
| **Add +1 day** | If you check this, GOL IBE adds one day to the availability verification request. This is useful in special cases of long-haul flights. |

### How do special offers work? Simplified scheme

1. When you click _RUN CACHE_ or during the regular night refresh of availability of special offers, GOL IBE creates a calendar based on the settings for the onward and return journey. The calendar shows dates for which the availability information needs to be retrieved. GOL IBE retrieves availability for all days shown in the calendar.
2. Special offers are displayed on your website and when the customer clicks on one of them, GOL IBE shows them calendars with highlighted days on which the selected class is available and the date is not restricted by another condition \(for example AP\).
3. When the customer selects a date in the calendar for the onward journey, GOL IBE checks your settings to see which dates are available for the return journey. Only those are then highlighted. 
4. When the customer selects also a date for the return journey, GOL IBE checks availability for this precise combination of days, gets the fare quote and the final price is compared with the one set up in the back office. If the price is higher by more than 10 % or if there's no availability, GOL IBE returns an error notification. Otherwise the customer continues to the next page where they select specific flights.

## What should you check, if the created special offer does not function properly?

### **Does the whole connection exist in neutral availability?**

For example, you may want to create a special offer A20MAYPRGPTY.MAD/IB. If such a connection doesn't exist in neutral availability, the reason may be that such a long transfer flight is not possible in neutral availability. In the back office, this is then usually shown by red crosses at the end of the row with the special offer.

### **Doesn't a multi-segment journey include a 1-day shift?**

If the journey consists of multiple segments, the departure date on the second or third segment may be shifted by one day. If that's the case, you have to acknowledge that by checking _Add +1 day_ on the _Bindings_ tab.

### **Are selected booking classes available for the special offer?**

For some of the lowest prices, the requested booking classes may no longer be available. Please check in neutral availability which classes are open.

### **Does a fare exist for the selected carrier?**

If you have a look at the Fare Display by using the FD entry in the reservation system, can you see the selected Fare Basis with the correct carrier code? If the Fare Basis belongs to a carrier other than the marketing carrier, you need to acknowledge that in the field _Fare Basis Carrier_.

### **Can you simulate the booking using the fare quote via your terminal window?**

If both availability and the fare exist - are you able to create the booking via your terminal window and get a fare quote for it?

