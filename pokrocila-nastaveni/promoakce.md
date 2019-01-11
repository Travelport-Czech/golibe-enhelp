# Promoakce

Jsou určeny k prodeji cen vybraných leteckých společností za pomoci kalendářů s vyznačením dostupnosti.

**Promoakce mohou vznikat:**

1. **Ručně**, založením promoakce a zadáním všech potřebných parametrů spojení.
2. **Automaticky**, kdy GOL IBE navrhuje promoakce sám, na základě provedených rezervací uživatelů. Každý takovýto návrh promoakce je přidán v zázemí jako nová neaktivovaná promoakce. Navrhovaná promoakce na určité spojení je až do své případné aktivace stále porovnávána s každou další vzniklou rezervací, a pokud je cena nově vzniklé rezervace nižší, je původní promoakce nahrazena.

{% hint style="info" %}
Odlety a přílety jsou u automatických promoakcí přednastaveny od prvního dne v měsíci, ve kterém byl rezervován let, do posledního dne 3. měsíce ode dne, na který byl rezervován let. Platnost promoakce je přednastavena od aktuálního data do posledního dne možného odletu.
{% endhint %}

### Nastavení

Administrovat Promoakce je možné v zázemí v sekci **Ceny &gt; Promoakce - letenky \(rozšířené\)**.

Vedle klasických tlačítek - **SMAŽ/EDIT/DETAIL** \(detail zobrazuje všechny informace stejně jako edit, jen needitovatelné\), jsou zde ještě funkce:

* Kopírování promoakcí – tlačítko **KOPIE**. KOPIE otevře editaci nové Promoakce, se všemi položkami stejnými jako u původní.
* Tlačítko **SPUSTIT CACHE**, které spustí robota pro načtení informací o letech z rezervačního systému. Aby mohla být Promoakce zobrazována na FE, je třeba mít zaškrtnut check-box: „Zobrazovat“ v detailu Promoakce.

![](../.gitbook/assets/image%20%289%29.png)

### Editace/Přidání nové promoakce

Stránka nastavení Promoakce je rozdělena do několika sekcí \(povinné položky jsou označeny tučně\):

## 1. Základní nastavení Promoakce

![](../.gitbook/assets/image%20%2816%29.png)

| Pole | Popis |
| :--- | :--- |
| **Agentura** | Výběr agentury, které bude promoakce zobrazována. |
| **Cena letenky** | Cena letenky a tax. Výše ceny letenky + tax je navíc porovnávána s oceněním v GDS a pokud by cena v GDS byla vracena vyšší o více jak 10%, bude takovéto spojení označno jako nedostupné. |
| **Servisní poplatek** | Výše servisního poplatku. Promoakce má vlastní servisní poplatek, který může být stejný nebo rozdílný od poplatku při běžném vyhledávání. |
| **Celková zobrazovaná cena** | Celková cena vzniklá součtem částek Cena letenky a Servisní poplatek. Tato cena je zobrazována na FE koncovým zákazníkům. |
| **Skutečná konc. cena z FS min** | Minimální cena tarifu a tax, vrácená při dotazování na kombinace letů. |
| **Skutečná konc. cena z FS max** | Maximální cena tarifu a tax, vrácená při dotazování na kombinace letů. |
| **Zobrazovat na webu od-do** | Časový interval, ve kterém bude Promoakce zobrazována zákazníkům na webu. |
| **Cesta tam možná od - do** | Časový interval, kdy je možná cesta tam. |
| **Cesta zpět možná od - do** | Časový interval, kdy je možná cesta zpět. |
| **Zařazena do množiny** | Pole pro vložení množiny, do které promoakce patří. Například Evropa, Asie, Promoakce s cenou do 5000 apod. Dle těchto množin lze Promoakce zobrazovat na FE. |

## 2. Statistika promoakce

![](https://bo.golibe.com/help/cz/lib/NewItem260.png)

| Pole | Popis |
| :--- | :--- |
| **Poslední měření cache** | Čas, za který proběhlo poslední načtení informací o letech. |
| **Počet dotazů na availabilitu** | Počet availabilitních dotazů položených při poslední aktualizaci pro tuto Promoakci. |
| **Aktuální ocenění z Galilea** | Zobrazení výsledků kontrolního ocenění. Ocenění se provádí bez ohledu na dostupnost. Pokusů je učiněno max. 5 s tím, že jsou prováděny na kombinaci dní na začátku platnosti Promoakce a následně o týden později, přes víkend apod. aby bylo dosaženo vysoké pravděpodobnosti úspěšného ocenění. |

Technické poznámky:

{% hint style="info" %}
Informace o dostupnosti je občerstvována na základě používání Promoakcí klienty. Pokud klient narazí na nedostupnou kombinaci, není již dalším zákazníkům nabízena. Současně dochází k občerstvování informací o dostupnosti v pravidelných intervalech, minimálně však 1x za 24hodin v nočních hodinách.
{% endhint %}

## 3. Stav Promoakce

![](https://bo.golibe.com/help/cz/lib/NewItem261.png)

| Pole | Popis |
| :--- | :--- |
| **Ověřovat robotem** | Pokud je zaškrtnuto, data jsou automaticky občerstvována v pravidelných intervalech. |
| **Zobrazovat** | Pokud je zaškrtnuto, je Promoakce zobrazována klientům na FE. |
| **Zneaktivnit při chybné ceně** | Promoakce podstupuje kontrolní ocenění \(stav je možné vidět v tabulce Statistika Promoakce\). Pokud je rozdíl ceny pod hranicí +/-10%, je cena korigována. Pokud by byl rozdíl ceny nad touto hranicí, například chybou nastavení promoakce, pak při aktivované volbě bude Promoakce deaktivována ze zobrazení na webu. |
| **Automatická promoakce** | Zobrazení ANO/NE, zda byla Promoakce založena automaticky. |
| **Nacachováno** | Zobrazení ANO/NE, zda byla Promoakce nacachována \(načteny informace z rezervačního systému\). |
| **Nalezeny lety** | Zobrazení ANO/NE, zda byly u Promoakce nalezeny v rezervačním systému dostupné lety. |
| **Sedí cena** | Zobrazení ANO/NE, zda byla vyhledána cena v požadovaném rozsahu. |

## 4. Obecná omezení Promoakce

![](https://bo.golibe.com/help/cz/lib/NewItem212.png)

| Pole | Popis |
| :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Min/Max stay</b>
      </th>
      <th style="text-align:left">
        <p>Pole pro upřesnění omezení letů. V pořadí:</p>
        <p>1. pole – číslovka značící počet dnů, nebo text SU v případě, kdy je potřeba
          aplikovat pravidlo Sunday Rule.</p>
        <p>2. pole (výběr) – upřesnění pro 1. pole, zda se jedná o dny či měsíce.</p>
        <p>3. pole (výběr) – upřesnění celého pravidla, zda určuje minimální či maximální
          počet dní / měsíců.</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>Každá část cesty musí být nadefinována. Pro jednoduchá nepřestupní spojení, např. VIE-CDG, je nutné v sekci "Cesta tam" definovat spojení dle obrázku níže. Pokud je spojení přestupní, např. VIE-FRA-CDG, je nutné nejdříve nadefinovat spojení VIE-FRA a klikem na tlačítko "Přidat další segment letu pro stejný směr" přidat pole, do kterého vyplníte druhý úsek cesty FRA-CDG.

Pokud je cesta zpáteční, je třeba to samé pro sekci "Cesta zpět". Cesta zpět lze vytvořit za pomoci tlačítek "Přidat cestu zpět" pro stejný systém zadávání, jako je tomu pro "Cesta tam", nebo za pomoci tlačítka "Vytvořit automaticky cestu zpět", která vytvoří automaticky zrcadlově zadání pro cestu zpět.

![](https://bo.golibe.com/help/cz/lib/NewItem213.png)

| Pole | Popis |
| :--- | :--- |
| **Počátek cesty \(IATA kód\)** | ATA kód odletového místa. |
| **Cíl cesty \(IATA kód\)** | IATA kód cíle cesty. |
| **Marketingový dopravce** | Dopravce uvedený na availabilitě. |
| **Bookovací třídy** | Bookovací třída \(RBD\). |
| **Fare Basis Code** | Fare Basis, kterým je oceněna tato část letu. |
| **Fare Basis dopravce** | Kód dopravce, kterému patří Fare Basis \(uvedeno na Fare Display\). V některých případech může letět jiný marketingový dopravce na Fare Basis svého interline partnera. |
| **Tlačítko "Aktualizovat podmínky"** | Toto tlačítko znovu načte tarifní podmínky z rezervačního systému. Podmínky jsou zobrazovány v dalších záložkách. |

![](https://bo.golibe.com/help/cz/lib/NewItem214.png)

| Pole | Popis |
| :--- | :--- |
| **Časová omezení** | Pole pro výběr intervalu dní od /do, výběr dnů v týdnu a definic, zda je pravidlo povolující nebo zakazující. |
| **Podmínky** | Textové pole pro zobrazení vybraných pasáží tarifních podmínek v originální textové podobě. |

![](https://bo.golibe.com/help/cz/lib/NewItem215.png)

| Pole | Popis |
| :--- | :--- |
| **Čísla letů** | Pole pro zadání letecké společnosti, rozsahu čísel letů a definic, zda je pravidlo povolující nebo zakazující. |
| **Podmínky** | Textové pole pro zobrazení vybraných pasáží tarifních podmínek v originální textové podobě. |

![](https://bo.golibe.com/help/cz/lib/NewItem216.png)

| Pole | Popis |
| :--- | :--- |
| **Hledat společně s následujícím** | Je-li zaškrtnuto, availabilita se ověřuje společně s následujícím segmentem pomocí O&D, tedy na celou cestu. V opačném případě je availabilita ověřována jednotlivě po segmentech pro každou část cesty zvlášť. |
| **Inhibit status link** | Je-li zaškrtnuto, není ani v případech, ve kterých je to možné, availabilita ověřována přímo u dopravce za pomocí tzv. seamless availability. Nezaškrtnutí může při zvýšené míře užití negativně ovlivnit poměr dotazování na dopravce oproti počtu rezervací a vyvolat sankce dopravce. |
| **Posun + 1 den** | Je-li zaškrtnuto, pak je pro ověřování dostupnosti dotaz na následující segment letu pokládán o den později. Je využíváno ve speciálních případech dálkových letů. |

![](https://bo.golibe.com/help/cz/lib/NewItem217.png)

Obdoba nastavení dle bodu 4, v tomto případě však pro pravidla týkající se výhradně nastavovaného segmentu letu.

Pokud je v záložce "Vazby" zaškrtnuta volba "Hledat společně s následujícím", jsou aktivní i záložky "Časová omezení O&D" a "Upřesnění O&D", kde je možné nastavit již dříve zmíněná pravidla pro celou cestu.

### Jak Promoakce fungují? Zjednodušené schema

1. Po kliku na „Spustit cache“ nebo v pravidelném nočním občerstvování dostupnosti Promoakcí se z nastavení sestaví kalendář pro cestu tam a zpět, ve kterých dnech je potřeba načíst informace o dostupnosti. Pro tento kalendář se zjistí dostupnost pro všechny dny.
2. Promoakce se zobrazí na webu a při prokliknutí se zobrazí stránka kalendářů, kde jsou vysvíceny dostupné dny, kde je dostupná zadaná třída a data nejsou omezena jinou podmínkou \(například AP\).
3. Pokud zákazník vybere den v kalendáři pro cestu tam, aplikace překontroluje podle podmínek zadaných v zázemí, které dny pro cestu zpět jsou akceptovatelné. Ty pak nechá rozsvícené, ostatní zhasne.
4. Po výběru i dne pro cestu zpět se provede ověření dostupnosti pro tuto přesnou kombinaci dní, Provede se ocenění a výsledná cena se porovná se zadanou v zázemí. Pokud bude cena vyšší o více jak 10 %, nebo nebude dostupnost, systém odpoví chybou. V opačném případě zákazník přejde na výběr konkrétních letů na další stránku.

## Co překontrolovat, pokud zadaná Promoakce nefunguje správně?

### **Existuje celé spojení na neutrální availabilitě?**

Např. zadáváte promoakci A20MAYPRGPTY.MAD/IB. Pokud takové spojení nenajdete na neutrální availabilitě, může to být způsobeno tím, že tak dlouhý přestup není na neutrální availabilitě možný. V zázemí se to obvykle projeví tak, že na konci řádku promoakce jsou zobrazeny červené křížky.

### **Není u vícesegmentové cesty posun o den?**

Pokud je cesta vícesegmentová, může být nástup na druhý nebo třetí segment cesty nástup až další den. Pokud to tak je, je třeba tuto skutečnost zaškrtnout v sekci „Vazby“ checkboxem: „Posun +1 den:“

### **Jsou pro Promoakci dostupné zadané knihovací třídy?**

U některých nejnižších cen již nemusí být dostupné požadované třídy. Prosím překontrolujte stav otevření tříd na neutrální availabilitě.

### **Existuje tarif pro daného dopravce?**

Pokud se podíváte v systému vstupem FD na FareDisplay, najdete tam zadaný FareBasis u správného kódu dopravce? Pokud by Farebasis patřil jinému než marketingovému dopravci, je třeba toto zadat do pole „Fare Basis patří dopravci:“.

### **Je možné nasimulovat rezervaci s oceněním přes terminál?**

Při existenci dostupnosti a tarifu - je možné v terminálu rezervaci vytvořit a ocenit?

