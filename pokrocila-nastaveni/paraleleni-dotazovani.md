# Parallel requests

The search request sometimes returns better results, if one more request is sent parallely including the preferred carrier, departure time, transfer airport etc. During the search using the BB entry, GOL IBE sends a request without any preference, and parallely another request with a preference, and it then merges the results. The overview below shows which preferred carrier \(or multiple carriers\) should be used for which itineraries.

![](../.gitbook/assets/image%20%2823%29.png)

Edit/New preference

![](../.gitbook/assets/image%20%2851%29.png)

| Item | Description |
| :--- | :--- |
| **Connector** | For which connector the preference should be used. |
| **Type of origin** | Type of origin point. You can select the itinerary either by the destination type or by directly entering an IATA code - see the item below. See more on destination types in chapter 7.5. |
| **Origin** | IATA code of the departure point. |
| **Type of destination** | Type of destination point. You can select the itinerary either by the destination type or by directly entering an IATA code - see the item below. See more on destination types in chapter 7.5. |
| **Destination** | IATA code of the destination point. |
| **Return flight** | The preference is used only for the return flight. |
| **Carrier codes of preferred carriers** | The code of the carrier that should be preferred in case of multiple carriers separated by comma. |

