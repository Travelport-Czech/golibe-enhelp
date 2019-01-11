# Pracovní doba

Stránka slouží k nastavení pracovní doby agentury tak, aby bylo zabráněno rezervacím, které nebude možné z důvodu nepřítomnosti letenkářů vystavit \(mimopracovní doba\). Vřele ale doporučujeme využít některou platební bránu a nastavit automatizovaný ticketing, nebo si nastavit notifikace a hlídat rezervace i mimo pracovní dobu v zájmu co největšího množství prodaných letenek.

Na nastavení pracovní doby se dostanete přes menu **Agentura -&gt; Pracovní doba**.

![](../.gitbook/assets/image%20%2810%29.png)

Pro jednotlivé dny lze nastavit pracovní dobu s polední přestávkou, například 9:00 – 11:30, 12:00 – 17:30. Pokud nemá agentura polední přestávku, je nutné nastavit celou pracovní dobu 9:00 – 18:30 do polí určených pro dopoledne.

## Logika nastavení pracovní doby

Nastavení slouží jako ochrana před situací, kdy si klient zarezervuje letenku v 17:35 ale v 17:30 již skončila pracovní doba agentury. Letenku je třeba vystavit téhož dne, ale již ji nemá kdo vystavit. To samé platí pro víkendy a dny volna obecně. Pracovní doba je vždy porovnávána s nejpozdějším datem pro vystavení letenky. Nejpozdější datum vystavení, zobrazované zákazníkům, je určeno na základě podmínek tarifu \(nastavením může být omezeno\). Díky nastavení pracovní doby je ale omezeno na den, kdy má agentura pracovní dobu tak, aby se vystavení stihlo.

Pro správné fungování je ještě třeba definovat u jednotlivých způsobů plateb, kolik času v rámci pracovní doby je potřeba na vyřízení obchodního případu. Výchozí nastavení je 1 hodina. Tím můžete ovlivnit, které způsoby plateb se budou nabízet, pokud se blíží nejpozdější datum vystavení. Pokud je toto datum určeno na den rezervace \(musí se vystavit "ihned"\), pak ostatním způsobům plateb mohu nastavit vyšší hodnotu a nebudou vůbec k dispozici pro zaplacení.

Může tedy dojít ke třem různým situacím:

1. Klient zarezervuje letenku, přičemž zbývá dostatek času v rámci pracovní doby pro zpracování rezervace a vystavení letenky – vše je v pořádku a rezervace se provede.
2. Klient zarezervuje letenku, avšak způsoby platby obsahují různé minimální časy pro zpracování rezervace. Některé v rámci pracovní doby lze stihnout, některé nikoliv. Ve výběru se zákazníkovi zobrazí jen ty, které stihnout lze, a pouze tyto bude klient moci zvolit pro dokončení rezervace a platbu.
3. Žádný způsob platby neumožní vystavení letenky v rámci pracovní doby. V tomto případě GOL IBE nedovolí rezervaci dokončit \(nepůjde vyplnit rezervační formulář\) a klient bude na tuto skutečnost upozorněn textem. Text lze libovolně upravit v GOL IBE zázemí v sekci **Doprovodné texty**.

## Úpravy standardní pracovní doby - svátky apod.

Do sekce Úprava pracovní doby se dostanete přes menu **Agentura -&gt; Úprava pracovní doby - jednorázová**

Slouží k definování výjimek z nastavené Pracovní doby, tj. definuje svátky a jiné dny, kdy agentura nepracuje. V současné době neexistuje číselník, který by upravoval státní svátky. Pokud agentura potřebuje tyto možnosti ošetřit, pak je nutné svátky ručně zadat.

![](../.gitbook/assets/image%20%2813%29.png)

{% hint style="warning" %}
Pokud uživatel zadá pouze datum, určuje tím, že agentura nepracuje celý den. Pokud zadá časy od – do, zužuje tím pracovní dobu v daný den pouze na uvedený interval hodin.
{% endhint %}

