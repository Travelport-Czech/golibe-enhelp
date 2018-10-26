# Servisní poplatky

V zázemí přejděte do menu **Ceny -&gt; Servisní poplatky letenek - agentura**

{% hint style="warning" %}
Pokud využíváte Dealerský prodej, nebo potřebujete definovat servisní poplatek na zákazníka, čtěte detaily k **Servisní poplatky letenek - dealer** na závěr textu.
{% endhint %}

Pro přidání nového servisního poplatku klikněte na tlačítko:

![](../.gitbook/assets/image%20%2814%29.png)

## 1. Zvolte leteckou společnost

Letecká společnost může zůstat nevyplněna, a v tom případě platí pravidlo pro všechny airlines.

![](../.gitbook/assets/image%20%2836%29.png)

| Pole | Popis |
| :--- | :--- |
| **Transportní společnost** | Výběr let. společnosti, pro kterou zadávané pravidlo platí |
| **Konektor** | Letenky Galileo - poplatky pro letenky pocházející z GDS Galileo |
|  | Letenky Travelfusion - poplatky pro letenky pocházející od TravelFusion |

## 2. Zvolte podmínky platnosti

![](../.gitbook/assets/image%20%2815%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Podmínky platnosti** | Obecně platné - platí bez jakýchkoliv omezení |

![](../.gitbook/assets/image%20%283%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Podmínky platnosti** | Platné pro destinace - omezuje platnost na vyspecifikované typy cest a konkrétní spojení. |
| **Typ** | OW+RT - platí pro jednosměrné i zpáteční cesty |
|  | OW - platí jen pro jednosměrné cesty \(OneWay\) |
|  | RT - platí jen pro zpáteční cesty \(Return\) |
|  | Tato pravidla nejsou aplikovatelná pro vícefázové cesty, nebo Open Jaw. Pro ty je nutné využívat pouze Obecné podmínky platnosti \(viz. výše\). |
| **Počátek cesty \(IATA kód\)** | Odkud se letí |
| **Cíl cesty \(IATA kód\)** | Kam se letí / Odkud se letí zpět |

![](../.gitbook/assets/image%20%2834%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Podmínky platnosti** | Platné pro typy destinací - omezuje platnost na skupiny destinací |
| **Typ** | OW+RT - platí pro jednosměrné i zpáteční cesty |
|  | OW - platí jen pro jednosměrné cesty \(OneWay\) |
|  | RT - platí jen pro zpáteční cesty \(Return\) |
|  | Tato pravidla nejsou aplikována pro vícefázové cesty, nebo Open Jaw. Pro ty je nutné využívat pouze Obecné podmínky platnosti \(viz. výše\). |

## 3. Stanovte výši servisního poplatku

![](../.gitbook/assets/image%20%2824%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Stanovená výše poplatku** | Fixní poplatek - pevná částka ve výchozí měně agentury. |
| **Fixní poplatek** | Číselná hodnota poplatku |

![](../.gitbook/assets/image%20%282%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Stanovená výše poplatku** | Fixní poplatek podle ceny letenky - pevná částka připočítaná za podmínky, že se cena pohybuje v nastaveném rozpětí. |
| **Fixní poplatek** | Číselná hodnota poplatku |
| **Pro letenky v ceně nad** | Spodní hranice ceny letenky. Při překročení bude aplikován poplatek. |
| **Pro letenky v ceně do \(vč.\)** | Horní hranice ceny letenky \(včetně\). Při překročení této částky přestává být aplikován poplatek. |
| **Rozsah cen zahrnuje taxy** | Ceny letenek jsou uvažovány včetně tax |

{% hint style="warning" %}
Poznámka: Platí vždy nejkonkrétnější pravidlo. Pokud máte například vloženo obecné pravidlo bez zvolené letecké společnosti a současně pravidlo se specifikovanou společností, bude použito to druhé v případě, že bude letecká společnost souhlasit.
{% endhint %}

## Nastavení poplatků pro dealery a přihlášené uživatele

Pokud využíváte Dealerský prodej, nebo potřebujete definovat servisní poplatek na konkrétního zákazníka, pak v přejděte do menu **Ceny -&gt; Servisní poplatky letenek - dealer**

Najdete zde shodná nastavení, jako pro **Servisní poplatky letenek - agentura** a něco navíc.

**Toto nastavování je vhodné ve dvou základních situacích:**

a\) **Máte více Dealerů \(webů\)** a každému chcete nadefinovat jiný servisní poplatek.

![](../.gitbook/assets/image%20%2828%29.png)

| Pole | Popis |
| :--- | :--- |
| **Dealer** | Výběr pro kterého dealera nastavení platí |

**b\) Máte registrovaného zákazníka**, kterému chcete přiřadit jeho vlastní servisní poplatek. Obvykle se to používá v situacích, kdy máte nějakého důležitého zákazníka \(nebo firmu\), se kterým máte dohodnuty speciální podmínky a speciální výši servisních poplatků.

![](../.gitbook/assets/image%20%2835%29.png)

| **Pole** | Popis |
| :--- | :--- |
| **Platné pro zákazníky** | Platné pro všechny - bez omezení na konkrétního zákazníka |
|  | Platné pro zvoleného - konkrétní registrovaný zákazník, kterého je možné vybrat ze seznamu. |

{% hint style="warning" %}
Výsledná částka poplatku je součtem nastavení od agentury a od dealera. Pokud chcete nastavovat poplatky pouze dealerům a nenastavovat si žádnou agenturní základní provizi, nastavte si v Servisní poplatky letenek - agentura výchozí hodnotu poplatku 0.
{% endhint %}

