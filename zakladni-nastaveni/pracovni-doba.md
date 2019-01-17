# Working hours

This section allows you to set up working hours. That prevents your customers from making bookings that your agents wouldn't be able to e-ticket because they're out of the office \(outside of working hours\). However, we highly recommend to use one of the integrated payment gateways and set up the automated e-ticketing. Another option is to set up notifications and check the bookings also outside of your working hours in order to sell as many tickets as possible.

You can find the settings under **Agency -&gt; Working hours**.

![](../.gitbook/assets/image%20%2825%29.png)

You can set working hours for each day, including a lunch break, for example 9:00 – 11:30, 12:00 – 17:30. If the agency doesn't have a lunch break, it is necessary to set the entire working time 9:00 – 18:30 in the morning fields.

## The logic of setting working hours

This setting is a protection against a situation when your customer books a ticket at 17:35, but your office closes at 17:30. The booking must be e-ticketed on the same day but there's nobody at your office to do it. The same applies to weekends and days off in general. Your working hours are always compared to the latest ticketing date. The latest ticketing date displayed to customers is determined based on the fare conditions \(this can be limited in the settings\).

Díky nastavení pracovní doby je ale omezeno na den, kdy má agentura pracovní dobu tak, aby se vystavení stihlo.

Pro správné fungování je ještě třeba definovat u jednotlivých způsobů plateb, kolik času v rámci pracovní doby je potřeba na vyřízení obchodního případu. Výchozí nastavení je 1 hodina. Tím můžete ovlivnit, které způsoby plateb se budou nabízet, pokud se blíží nejpozdější datum vystavení. Pokud je toto datum určeno na den rezervace \(musí se vystavit "ihned"\), pak ostatním způsobům plateb mohu nastavit vyšší hodnotu a nebudou vůbec k dispozici pro zaplacení.

Může tedy dojít ke třem různým situacím:

1. Klient zarezervuje letenku, přičemž zbývá dostatek času v rámci pracovní doby pro zpracování rezervace a vystavení letenky – vše je v pořádku a rezervace se provede.
2. Klient zarezervuje letenku, avšak způsoby platby obsahují různé minimální časy pro zpracování rezervace. Některé v rámci pracovní doby lze stihnout, některé nikoliv. Ve výběru se zákazníkovi zobrazí jen ty, které stihnout lze, a pouze tyto bude klient moci zvolit pro dokončení rezervace a platbu.
3. Žádný způsob platby neumožní vystavení letenky v rámci pracovní doby. V tomto případě GOL IBE nedovolí rezervaci dokončit \(nepůjde vyplnit rezervační formulář\) a klient bude na tuto skutečnost upozorněn textem. Text lze libovolně upravit v GOL IBE zázemí v sekci **Doprovodné texty**.

## Úpravy standardní pracovní doby - svátky apod.

Do sekce Úprava pracovní doby se dostanete přes menu **Agentura -&gt; Úprava pracovní doby - jednorázová**

Slouží k definování výjimek z nastavené Pracovní doby, tj. definuje svátky a jiné dny, kdy agentura nepracuje. V současné době neexistuje číselník, který by upravoval státní svátky. Pokud agentura potřebuje tyto možnosti ošetřit, pak je nutné svátky ručně zadat.

![](../.gitbook/assets/image%20%2839%29.png)

{% hint style="warning" %}
Pokud uživatel zadá pouze datum, určuje tím, že agentura nepracuje celý den. Pokud zadá časy od – do, zužuje tím pracovní dobu v daný den pouze na uvedený interval hodin.
{% endhint %}

