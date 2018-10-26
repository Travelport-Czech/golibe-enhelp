# Provize leteckých společností

Letecké společností sice čím dál méně, avšak stále poskytují cestovním agenturám provize z prodeje letenek. Provize můžete snadno nastavit a ty pak budou automaticky vkládány do rezervací.

V zázemí přejděte do menu **Ceny -&gt; Provize leteckých společností**

Na stránce uvidíte přehled již nastavených servisních poplatků, které můžete smazat klikem na **SMAŽ**, nebo upravit klikem na **EDIT**.

Pro přidání nového servisního poplatku klikněte na tlačítko:

![](https://travelport.gitbooks.io/gol-ibe-cz/content/assets/AddCommission.png)

## 1. Zvolte parametry provize

![](../.gitbook/assets/image%20%289%29.png)

| Pole | Popis |
| :--- | :--- |
| **Validační dopravce** | Dopravce na kterého je vystavena letenka |
| **Místo odletu & Cíl cesty** |  |

![](../.gitbook/assets/image%20%2813%29.png)

| Pole | Popis |
| :--- | :--- |
| **Obousměrné** | Při zaškrtnutí platí pravidlo pro oba směry, například při zadání pro PRG-LHR platí i pro LHR-RG |

![](../.gitbook/assets/image%20%2819%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Místo odletu & Cíl cesty** | Bez omezení - pro jakékoliv odletové místo a cíl cesty |
|  | IATA kód - IATA kód destinace |
|  | Typ destinace - světadíl a jiné ustálené množiny destinací |
|  | Stát |

![](../.gitbook/assets/image%20%281%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Typ provize** | Fixní částka - pevná částka provize v měně agentury |
|  | Procenta - % částka provize vypočítávaná z výše tarifu |

![](https://travelport.gitbooks.io/gol-ibe-cz/content/assets/commission8.png)

![](../.gitbook/assets/image%20%2832%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Knihovací třída \(RBD\)** | Knihovací třídy, které smí být v rezervaci, aby pravidlo platilo. |
|  |  |

![](../.gitbook/assets/image%20%2827%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Marketingoví dopravci** | Bez omezení - v rezervaci může být jakýkoliv marketingový dopravce, není nastaveno žádné omezení. |
|  | Různí marketingoví dopravci - pravidlo se uplatní jen v případě, že je v itineráři alespoň jeden jiný marketingový dopravce, než je validační. |
|  | Pouze validační dopravce - pravidlo se uplatní jen v případě, že je v itineráři zastoupen pouze validační dopravce. |
|  | Pouze jiní, než je validační dopravce - pravidlo se uplatní jen v případě, že v itineráři není zastoupen validační dopravce. |

![](../.gitbook/assets/image%20%2811%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Operující dopravci** | Bez omezení - v rezervaci může být jakýkoliv operující dopravce, není nastaveno žádné omezení. |
|  | Povoleni pouze vyjmenovaní - v itineráři musí být zastoupeni pouze vyjmenovaní operující dopravci. Volba je doplněna polem pro vložení IATA kódů dopravců oddělených čárkou. |
|  | Nepovoleni vyjmenovaní - v itineráři nesmí být zastoupen žádný z vyjmenovaných dopravců. Volba je doplněna polem pro vložení IATA kódů dopravců oddělených čárkou. |
|  | Musí obsahovat všechny vyjmenované - v itineráři musí být zastoupeni **všichni** uvedení operující dopravci. Itinerář nesmí _\*\*_navíc obsahovat ještě nějakého dalšího. Volba je doplněna polem pro vložení IATA kódů dopravců oddělených čárkou. |

![](../.gitbook/assets/image%20%2818%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Priorita** | Priority se uplatní, pokud je nastaveno více různých provizí na konkrétní leteckou společnosti. GOL pak postupuje následujícím způsobem: 1. Vybere všechna pravidla pro validačního dopravce z rezervace, 2. Seřadí pravidla dle nastavené "Priority", 3. Vezme pravidlo s nejvyšší prioritou \(vyšší číslo = vyšší priorita\) a zkontroluje, že vyhovuje rezervaci. Pokud ano, tak zapíše příslušnou provizi do rezervace. Pokud ne, pokračuje dalším pravidlem dle priority. |

## 2. Zvolte typ cesty

![](../.gitbook/assets/image%20%286%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Jednosměrné lety** | Při zaškrtnutí se pravidlo použije jen na jednosměrné lety. |
| **Zpáteční lety** | Při zaškrtnutí se pravidlo uplatní jen na zpáteční lety. |
| **Jednosměrné lety & Zpáteční lety** | Při zaškrtnutí obou pravidel je pravidlo aplikováno pro oba druhy cest. |

## 3. Zvolte období platnosti

![](../.gitbook/assets/image%20%2826%29.png)

| Pole | Popis |
| :--- | :--- |
| Provizi lze uplatnit od-do | Nastavení v jakém období je pravidlo pro provizi aktivní. |
| Cesta tam \(zpět\) možná od-do | Nastavení povoleného rozsahu dat, ve kterých je uskutečněná cesta. |

## Jak pravidla otestovat?

Ověřit, jak vám budou provize napočítány na konkrétní rezervaci, můžete ověřit přes [tuto stránku](https://cm.golibe.com/). Autorizační Token vám na požádání poskytneme.

## Využití pro aplikace třetích stran

V případě, že chcete nastavené provize použít i pro vaše další systémy a vkládat tak provize i do ne-GOL IBE rezervací, je třeba nastavení exportovat klikem na tlačítko:

![](../.gitbook/assets/image%20%284%29.png)

Popis programátorského napojení [najdete zde](https://misecz.gitbooks.io/commission-microservice/content/).

