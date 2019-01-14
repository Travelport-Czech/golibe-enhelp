# Vložení vyhledávacího formuláře letenek

Vyhledávací formulář letenek je možné implementovat jako:

## 1. html-php balíček - Doporučené!

Formulář je responzivní a přizpůsobuje se různým velikostem stránky \(zobrazení na mobilních zařízeních\).

![](../../.gitbook/assets/image%20%2859%29.png)

Příklad zobrazení při změnách velikosti okna \(na mobilních zařízeních\):

![](../../.gitbook/assets/image%20%2813%29.png)

HTML balíček si stáhnete z administračního zázemí:

a\) pokud máte agenturní účet, tak v sekci **Dealeři** -&gt; Vyberte dealera \(web\) o kterého vám jde a klikněte na tlačítko: **Detail,** dále **\*\*tlačítko** Nastavení Frontendu **a klikněte na odkaz: "**Statické HTML ke stažení\*\*".

b\) pokud máte dealerský účet, tak přímo v sekci **Dealeři** -&gt; **Nastavení Frontendu** -&gt; Odkaz: "**Statické HTML ke stažení**".

Tento formulář obsahuje HTML, CSS, obrázky a patřičné scriptování pro implementaci přímo do vaší stránky s plnou funkcionalitou našeptávače destinací. Můžete si jej také libovolně upravovat.

## 2. iframe

Další možností je iframe, který vyniká snadnou implementací, má ale své nevýhody. Pokud například u vícefázových letů bude zákazník přidávat další a další části cesty, bude se formulář natahovat a musíte tedy nechat na stránce dostatek místa, nebo umožnit skrolování. To ale není moc hezké.

Příklad implementace následuje.

{% hint style="info" %}
**Nezapomeňte doplnit i sekce "&lt;meta name="viewport".." a "&lt;style..", které jsou důležité pro správné rozměry a responsivní zobrazení.**

**Namísto XXXXXX \(níže\) doplňte vaše URL.**
{% endhint %}

```markup
<!doctype html>
<html>
 <head>
   <meta name="viewport" content="width=device-width">
   <title>Iframe</title>
   <style type="text/css">

       /* optional */
       body { background-color: gray; }
       .golSearchFlightsIframe { background-color: transparent; }

       /* mandatory */
       .golSearchFlightsIframe { border: none; width: 550px; max-width: 100%; height: 520px; }
       @media only screen and (max-width: 566px) {
         .golSearchFlightsIframe { height: 800px; }
       }

   </style>
 </head>
 <body>
       <iframe class="golSearchFlightsIframe" src="//XXXXXX.golibe.com//static.php" frameborder="0" allowtransparency="true">
   </iframe>

   <!--Iframe's language can be set by parameter lang>
     <iframe class="golSearchFlightsIframe" src="//XXXXXX.golibe.com//static.php?lang=en" frameborder="0" allowtransparency="true">
     </iframe>
   -->

 </body>
</html>
```

## **Pro zvídavé: Úprava výchozího nastavení formuláře**

Pro obě výše uvedené varianty platí, že parametry vyhledávacího formuláře lze předvolit a klient je tedy uvidí již předvyplněné.

Nejjednodušší způsob, jak se dozvědět způsob, jakým link vyrobit, je:

* Nastavit vyhledávací formulář do takové podoby, v jaké chcete mít předvoleno vyhledávání.
* Vyhledat a dostat se na stránku výsledků vyhledávání.
* Na tlačítku "Nové hledání", které by Vás vrátilo na vyhledávání od začátku, kliknout pravým tlačítkem myši a zvolit zkopírování odkazu.

Příklady toho co získáte:

`https://xxxx.golibe.com/index.php?action=vFlights&flights[0][origin]=PRG&flights[0][destination]=LON&flights[0][departureDate]=2013-01-09&flights[1][origin]=LON&flights[1][destination]=PRG&flights[1][departureDate]=2013-01-16&searchType=FromFour&travelers[0]=ADT&dateVariants=exact&returnTicket=on&step=one2`

Pokud chcete ve formuláři předvolit vyhledávání PRG-LON, vynechte v URL ostatní parametry \(například datum\) a ponechte si jen potřebnou část. Tento link můžete použít jako odkaz:

```http
?action=vFlights&flights[0][origin]=PRG&flights[0][destination]=LON&flights[1][origin]=LON&flights[1][destination]=PRG&searchType=FromFour&travelers[0]=ADT&dateVariants=exact&returnTicket=on&step=one2
```

...nebo použít v iframu:

```markup
<iframe src="https://xxxx.golibe.com/static.php?action=vFlights&flights[0][origin]=PRG&flights[0][destination]=LON&flights[1][origin]=LON&flights[1][destination]=PRG&searchType=FromFour&travelers[0]=ADT&dateVariants=exact&returnTicket=on&step=one2" scrolling="no" width="530px" height="510px" frameborder="0" allowtransparency="true">
```

Pokud chcete přesměrovat klienty rovnou na výsledky vyhledávání ze své stránky a přitom je nechat čekat na čekací stránce, namísto zobrazení bílé stránky, je možné vložit redirect. Pozor: Část za "...redirect=" musí být URL encodovaná. Například:

```http
https://xxxx.golibe.com/index.php?action=vWait&redirect=http%3A%2F%2Fxxxx.golibe.com%2Findex.php%3Faction%3DvFlights%26flights%5B0%5D%5BdepartureDate%5D%3D2014-11-07%26flights%5B0%5D%5Bdestination%5D%3DPTP%26flights%5B0%5D%5Borigin%5D%3DPAR%26flights%5B0%5D%5BdeparturePlusMinusDay%5D%3D3%26flights%5B1%5D%5BdepartureDate%5D%3D2014-11-14%26flights%5B1%5D%5Bdestination%5D%3DPAR%26flights%5B1%5D%5Borigin%5D%3DPTP%26flights%5B1%5D%5BdeparturePlusMinusDay%5D%3D3%26travelers%5B0%5D%3DADT%26returnTicket%3Don%26vendor%3DTX%26dateVariants%3Dclose%26step%3DChooseFromFour%26target%3Dflights
```

Pro URL enkódování můžete použít například tuto veřejně dostupnout utilitu: [https://www.freeformatter.com/url-encoder.html](https://www.freeformatter.com/url-encoder.html)

