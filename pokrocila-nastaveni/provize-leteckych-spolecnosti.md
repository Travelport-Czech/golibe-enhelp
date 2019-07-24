# Commissions from airlines

Airlines tend to give commissions from sold tickets to travel agencies less and less, but they still do. You can easily set up these commissions and GOL IBE then adds them automatically to the bookings.

You can also specify discounts in this settings. The discounts may work independently of commissions, or you may want to set a discount on tickets in the amount of your earned commission. Therefore, we have combined these two settings, but you can also use them independently.

In the back office, go to **Prices -&gt; Commissions and discounts**.

You will see a list of already set up commissions. You can either delete them by clicking on **DELETE**, or edit them by clicking on **EDIT**.

To add a new rule, click on the button:

![](../.gitbook/assets/image%20%288%29.png)

## 1. Select basic parameters

![](../.gitbook/assets/image%20%2851%29.png)

| Item | Description |
| :--- | :--- |
| **Priority** | Priorities apply if multiple different commissions are set for a particular airline. GOL IBE then proceeds as follows: 1. It selects all rules for the validating carrier from the booking, 2. It sorts the rules according to the set priority, 3. It takes the rule with the highest priority \(higher number = higher priority\) and checks that it suits the booking. If so, it applies the commission for the booking. If not, it continues with the next rule based on priority. |
| **Use as a commission** | The rule is set for a commission from an airline. |
| **Use as a discount** | The rule is set for a discount. |

{% hint style="info" %}
Rules _Use as commission_ and _Use as discount_ can be used together, or separately. You may want to set a discount on tickets in the amount of your earned commission, and then it is convenient for your to set this up with a single rule.
{% endhint %}

## 2. Select airline

![](../.gitbook/assets/image%20%2832%29.png)

| Item | Description |
| :--- | :--- |
| **Plating carrier** | The carrier for which the ticket is issued. |

![](../.gitbook/assets/image%20%2852%29.png)

| Item | Description |
| :--- | :--- |
| **Marketing carriers** | Without restrictions - the booking can include any marketing carrier, there are no restrictions. |
|  | Different marketing carriers - the rule applies only if the itinerary includes at least one marketing carrier, other than the plating carrier. |
|  | Plating carrier only - the rule applies only if the itinerary includes the plating carrier exclusively. |
|  | Only other than plating carrier - the rule applies only if the itinerary does not include the plating carrier. |

![](../.gitbook/assets/image%20%2861%29.png)

| Item | Description |
| :--- | :--- |
| **Operating carriers** | Without restrictions -  the booking can include any operating carrier, there are no restrictions. |
|  | Operated only by some of the listed - the itinerary can include only the listed operating carriers. This option offers a field where you can enter IATA codes of the carriers separated by comma. |
|  | Not operated by - the itinerary cannot include any of the listed carriers. This option offers a field where you can enter IATA codes of the carriers separated by comma. |
|  | Operated by all listed - the itinerary must include **all** selected operating carriers. Moreover, the itinerary cannot include any other carrier. This option offers a field where you can enter IATA codes of the carriers separated by comma. |

## 3. Set amount of commission

![](../.gitbook/assets/image%20%2836%29.png)

| Item | Description |
| :--- | :--- |
| **Commission / Discount** | Fixed amount -  a fixed amount of commission/discount in agency's currency. |
|  | Percentage - a percentage amount of commission/discount calculated from the amoun of the fare. |

## 4. Select routing

![](../.gitbook/assets/image%20%283%29.png)

| Item | Description |
| :--- | :--- |
| **Origin & Destination** | Without restrictions - for any origin and destination. |
| \*\*\*\* | IATA code - IATA code of the destination. |
| \*\*\*\* | Type of destination - a continent or other defined sets of destinations. |
|  | Country |
| **Both ways** | If ticked, the rule applies for both directions, eg. in case of PRG-LHR, it applies also for LHR-PRG. |

## 5. Select type of journey

![](../.gitbook/assets/image%20%2871%29.png)

| Item | Description |
| :--- | :--- |
| **One way flights** | If ticked, the rule applies only for one-way flights. |
| **Return flights** | if ticked, the rule applies only for return flights. |
| **One way flights & Return flights** | If ticked, the rule applies for both types of journey. |

## 6. Select bookings classes and types of passengers

![](../.gitbook/assets/image%20%2828%29.png)

| Item | Description |
| :--- | :--- |
| **Usage of the listed classes** | The itinerary must include at least one of the selected classes. |
|  | The itinerary cannot include other than the selected classes. |
| **Booking class \(RBD\)** | Letters designating classes. Multiple classes need to be separated by comma \(eg. U,T,Q\). |
| **Applied only for passenger types** | Codes of passenger types, for which the rule should apply \(eg. ADT,YTH,INF\). |

## 7. Select validity period

![](../.gitbook/assets/image%20%2811%29.png)

| Item | Description |
| :--- | :--- |
| **Sales \(ticketing\) since - till** | Here you can set up the period during which the commission is active. |
| **Departures \(Returns\) since - till** | Here you can set up the allowed date range for the journey. |

## How can you test out the rules?

You can use [this page](https://cm.golibe.com/) to verify how the commissions will be calculated for a specific booking. Let us know and we're happy to create an authorization token for you.

## How to use your commission settings for 3rd-party applications or Travelport Smartpoint addon?

If you wish to use the set commissions also for your other systems like Travelport Smartpoint, in other words to enter your commissions also to non-GOL IBE bookings, you need to export your settings by clicking on:

![](../.gitbook/assets/image%20%285%29.png)

[Here](https://misecz.gitbooks.io/commission-microservice/content/) is the integration instruction for programmers.

