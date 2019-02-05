# Offering external services

After the customer books the air ticket, you can offer them any other external services through a deeplink. An example would be a car rental offer customized for the arrival and departure date. It can be shown right after the air ticket booking is finished as a link or an iframe with search results.

The request is created with placeholders that you put where you want the booking information to be displayed.

For example:

`http://www.carbook.com/ELBanner.do?iataCode={itinerary.stream.1.destination}&amp;display=airplane&amp;affiliateCode=testAgency&amp;puDay={itinerary.stay.1.start.day}......`

| Placeholder | Example of returned information | Description |
| :--- | :--- | :--- |
| **{language}** | cs | Language version code |
| **{reservation.locator}** | BRK5XA | Galileo reservation code |
| **{reservation.type \(flight/hotel\)}** | flight | Type of service |
| **{itinerary.streams.count}** | 2 | Number of journeys |
| **{itinerary.stream.1.origin}** | PRG | Where from \(onward journey\) |
| **{itinerary.stream.1.destination}** | SYD | Where to \(onward journey\) |
| **{itinerary.stream.1.start}** | 2016-12-06T18:40:00 | Departure \(onward journey\) |
| **{itinerary.stream.1.end}** | 2016-12-08T07:20:00 | Arrival to destination \(onward journey\) |
| **{itinerary.stream.2.origin}** | SYD | Where from \(return journey\) |
| **{itinerary.stream.2.destination}** | PRG | Where to \(return journey\) |
| **{itinerary.stream.2.start}** | 2016-12-24T15:55:00 | Departure \(return journey\) |
| **{itinerary.stream.2.end}** | 2016-12-25T13:55:00 | Arrival to destination \(return journey\) |
| **{itinerary.stays.count}** | 1 | Number of stopovers |
| **{itinerary.stay.1.start.day}** | 08 | From when passengers stay in the destination |
| **{itinerary.stay.1.start.month}** | 12 |  |
| **{itinerary.stay.1.start.year}** | 2016 |  |
| **{itinerary.stay.1.start.hour}** | 07 |  |
| **{itinerary.stay.1.start.minute}** | 20 |  |
| **{itinerary.stay.1.end.day}** | 24 | Until when passengers stay in the destination |
| **{itinerary.stay.1.end.month}** | 12 |  |
| **{itinerary.stay.1.end.year}** | 2016 |  |
| **{itinerary.stay.1.end.hour}** | 15 |  |
| **{itinerary.stay.1.end.minute}** | 55 |  |
| **{passengers.count}** | 1 | Number of passengers |
| **{passenger.1.firstname}** | martinez | First name of the 1st passenger |
| **{passenger.1.surname}** | martin | Last name of the 1st passenger |
| **{passenger.1.age}** | 30 | Age of the 1st passenger \(if not entered, GOL IBE enters 30\) |
| **{passenger.1.birthdate}** | 1986-12-06 | Date of birth of the 1st passenger \(if not entered, GOL IBE enters a date for the age of 30\) |

You can add everything through the section **Supporting texts**. You can add the link to 

Vše vložíte přes Menu **Doprovodné texty**, kam můžete link vložit do typ textu: **Letenky - Text - Stránka úspěšná rezervace letenky**

