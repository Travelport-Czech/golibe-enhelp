# Commission from airlines

Airlines tend to give commissions from sold tickets to travel agencies less and less, but they still do. You can easily set up these commissions and GOL IBE then adds them automatically to the bookings.

In the back office, go to **Prices -&gt; Commissions** 

You will see a list of already set up commissions. You can either delete them by clicking on **DELETE**, or edit them by clicking on **EDIT**.

To add a new commission, click on the button:

![](../.gitbook/assets/image%20%2810%29.png)

## 1. Select commission parameters

![](../.gitbook/assets/image%20%2842%29.png)

| Item | Description |
| :--- | :--- |
| **Plating carrier** | The carrier for which the ticket is issued. |
| **Origin & Destination** |  |

![](../.gitbook/assets/image%20%2834%29.png)

| Pole | Popis |
| :--- | :--- |
| **Both ways** | If you check this, the rule applies for both directions, eg. if set for PRG-LHR, it applies also for LHR-PRG. |

![](../.gitbook/assets/image%20%2861%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Origin & Destination** | Without restrictions - for any departure and arrival point |
|  | IATA code - IATA code of the destination |
|  | Destination type - continents and other defined sets of destinations |
|  | Country |

![](../.gitbook/assets/image%20%289%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Commission** | Fixed - a fixed amount of the commission in agency's default currency |
|  | % - a percentual amount of the commission calculated from the fare amount |

![](https://travelport.gitbooks.io/gol-ibe-cz/content/assets/commission8.png)

![](../.gitbook/assets/image%20%2835%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Booking class \(RBD\)** | Booking classes that are allowed in the booking in order for the rule to apply. |
|  |  |

![](../.gitbook/assets/image%20%2820%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Marketing carriers** | Without restrictions - the booking can include any marketing carrier, there are no restrictions. |
|  | Different marketing carriers - the rule applies only if the itinerary includes at least one marketing carrier, other than the plating carrier. |
|  | Plating carrier only - the rule applies only if the itinerary includes the plating carrier exclusively. |
|  | Only other than plating carrier - the rule applies only if the itinerary does not include the plating carrier. |

![](../.gitbook/assets/image%20%286%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Operating carriers** | Without restrictions -  the booking can include any operating carrier, there are no restrictions. |
|  | Operated only by some of the listed - the itinerary can include only the listed operating carriers. This option offers a field where you can enter IATA codes of the carriers separated by comma. |
|  | Not operated by - the itinerary cannot include any of the listed carriers. This option offers a field where you can enter IATA codes of the carriers separated by comma. |
|  | Operated by all listed - the itinerary must include **all** selected operating carriers. Moreover, the itinerary cannot include any other carrier. This option offers a field where you can enter IATA codes of the carriers separated by comma. |

![](../.gitbook/assets/image%20%2862%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Priority** | Priorities are used in case there are several different commissions defined for a particular carrier. GOL IBE then proceeds as follows: 1. It retrieves all rules for the plating carrier from the booking, 2. It sorts the rules based on the defined _Priority_, 3. It takes the rule with the highest priority \(higher number = higher priority\) and it checks whether it can be applied to the booking. If so, it records the relevant commission to the booking. If not, it applies the next rule in line based on priority. |

## 2. Select the type of journey

![](../.gitbook/assets/image%20%2844%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **One way flights** | If you check this, the rule is applied only for one-way flights. |
| **Return flights** | If you check this, the rule is applied only for return flights. |
| **One way flights & Return flights** | If you check both options, the rule is applied for both types of journey. |

## 3. Select the validity period

![](../.gitbook/assets/image%20%287%29.png)

| Pole | Popis |
| :--- | :--- |
| Sales since - till | Here you can set up the period during which the commission is active. |
| Departures \(Returns\) since - till | Here you can set up the allowed date range for the journey. |

## How can you test out the rules?

You can use [this page](https://cm.golibe.com/) to verify how the commissions will be calculated for a specific booking. Let us know and we're happy to create an authorization token for you.

## How to use your commission settings for 3rd-party applications?

If you wish to use the set commissions also for your other systems, in other words to enter your commissions also to non-GOL IBE bookings, you need to export your settings by clicking on:

![](../.gitbook/assets/image%20%284%29.png)

[Here ](https://misecz.gitbooks.io/commission-microservice/content/)is the integration instruction for programmers.

