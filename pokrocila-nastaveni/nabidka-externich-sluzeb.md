# Nabídka externích služeb

Po dokončení rezervace letenky je možné navázat na libovolnou další externí službu přes tzv. deeplink. Příkladem může být například rent-car společnost, jejíž nabídka bude vytvořena přímo na data příletu do destinace a odletu zpět. Může být připravena ihned po dokončení rezervace letenky jako proklik, nebo iframe s výsledky.

Dotaz se staví za pomocí tzv. placeholderů, které se vkládají na místo, kam mají přijít informace z rezervace.

Například:

`http://www.carbook.com/ELBanner.do?iataCode={itinerary.stream.1.destination}&amp;display=airplane&amp;affiliateCode=testAgency&amp;puDay={itinerary.stay.1.start.day}......`

| Placeholder | Příklad vracené informace | Popis |
| :--- | :--- | :--- |
| **{language}** | cs | Kód jazykové verze |
| **{reservation.locator}** | BRK5XA | Galileo rezervační kód |
| **{reservation.type \(flight/hotel\)}** | flight | Typ služby |
| **{itinerary.streams.count}** | 2 | Počet cest |
| **{itinerary.stream.1.origin}** | PRG | Odkud \(cesta tam\) |
| **{itinerary.stream.1.destination}** | SYD | Kam \(cesta tam\) |
| **{itinerary.stream.1.start}** | 2016-12-06T18:40:00 | Odlet \(cesta tam\) |
| **{itinerary.stream.1.end}** | 2016-12-08T07:20:00 | Přílet do destinace \(cesta tam\) |
| **{itinerary.stream.2.origin}** | SYD | Odkud \(cesta zpět\) |
| **{itinerary.stream.2.destination}** | PRG | Kam \(cesta zpět\) |
| **{itinerary.stream.2.start}** | 2016-12-24T15:55:00 | Odlet \(cesta zpět\) |
| **{itinerary.stream.2.end}** | 2016-12-25T13:55:00 | Přílet do destinace \(cesta zpět\) |
| **{itinerary.stays.count}** | 1 | Počet přerušení cesty |
| **{itinerary.stay.1.start.day}** | 08 | Od kdy zůstává cestující v destinaci |
| **{itinerary.stay.1.start.month}** | 12 |  |
| **{itinerary.stay.1.start.year}** | 2016 |  |
| **{itinerary.stay.1.start.hour}** | 07 |  |
| **{itinerary.stay.1.start.minute}** | 20 |  |
| **{itinerary.stay.1.end.day}** | 24 | Do kdy zůstává cestující v destinaci |
| **{itinerary.stay.1.end.month}** | 12 |  |
| **{itinerary.stay.1.end.year}** | 2016 |  |
| **{itinerary.stay.1.end.hour}** | 15 |  |
| **{itinerary.stay.1.end.minute}** | 55 |  |
| **{passengers.count}** | 1 | Počet cestujících |
| **{passenger.1.firstname}** | martinez | Jméno 1. cestujícího |
| **{passenger.1.surname}** | martin | Příjmení 1. cestujícího |
| **{passenger.1.age}** | 30 | Věk 1. cestujícího \(pokud není zadáno, doplní se 30\) |
| **{passenger.1.birthdate}** | 1986-12-06 | Datum narození 1. cestujícího \(pokud není zadáno, doplní se pro věk 30\) |

Vše vložíte přes Menu **Doprovodné texty**, kam můžete link vložit do typ textu: **Letenky - Text - Stránka úspěšná rezervace letenky**

