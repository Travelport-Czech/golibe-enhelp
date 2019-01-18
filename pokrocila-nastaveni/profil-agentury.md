# Agency profile

Under **Agency -&gt; Agency settings**, you can change the basic settings affecting the functionality of your GOL IBE.

![](../.gitbook/assets/image%20%2849%29.png)

| Pole | Popis |
| :--- | :--- |
| **Time zone** | In order for some settings and calculations to function properly, it is neccessary to select the correct time zone where your agency is located. This setting affects also for example calculation of your working hours. |

## Galileo settings

Here you can set up the connector for air tickets from Galileo GDS.

### Settings affecting the behaviour of air tickets

![](../.gitbook/assets/image%20%2821%29.png)

| Pole | Popis |
| :--- | :--- |
| **Currency** | The currency in which search results are displayed. If the currency differs from your default one set in Galileo GDS, an exchange rate is used. The exchange rate is used to calculate the prices displayed to customers. The original prices remain in Galileo GDS. |
| **Last ticketing date** | The date displayed to customers as the maximum date for paying for / issuing tickets. It is shown during the booking process and also in booking confirmations. |
|  | Based on tarif in GDS - set exactly according to fare conditions |
|  | Date of booking creation - on the same day when the booking is made |
|  | Date of booking creation +1 - the following day after the booking, if the fare conditions don't command a shorter deadline |
|  | Date of booking creation +2 up to +6 - see above |
| **Maximum number of requests on multiHAPs** | This one is related to the MultiPCC functionality and defines the maximum number of parallel requests that are sent to the GDS per one search request done by the customer \(this setting can be changed only by the system admin\) |
| **Reservation check in GDS** | Activation of the robot checking the status of bookings in the GDS. If the agent changes the ticket status through the terminal from Active to Issued/Cancelled, this status is changed also in GOL IBE. The robot runs 4 times a day. \(this setting can be changed only by the system admin\) |
| **Start date for check** | The date from which active tickets are checked in the GDS. Before the check, the robot prepares a set of bookings between the current date and the date set in the GOL IBE back office \(inclusive\). Out of this set, it only checks those bookings for which 48 hours haven't passed yet since the date and time of arrival of the last segment. \(this setting can be changed only by the system admin\) |
| **Don't include the surrounding airports in search results** | Here you can set whether during a search of flights to a particular airport \(eg. LHR\) GOL IBE should include search results also for other airports within the city / parent destination \(eg. LON\). |

### Settings of communication with Galileo GDS

![](../.gitbook/assets/image%20%2846%29.png)

| Pole | Popis |
| :--- | :--- |
| **Host Access Profile** | You need to configure a MasterGTID and create a robotic GWS sign-on withe settings Multiterminal U \(Unlimited\). With that information ready, request a HAP at API Support. DynGalileoProd or DynGalileoCopy designates whether this the Production or the Copy system. |
| **Pseudo City Code** | An agency PCC used for searching and booking. You always need to have a separate PCC, different from the one used for your agency. In AAT, set PLAT to Y and AUTH carriers or set the TKT agency. |
| **PrivateFaresAccount code** | Account Code for private fares \(ariline, agency private fares\). In case that agencies use private fares loaded under this designation. If you need to use more account codes, request a MasterAccountCode and include them there. |
| **PNR Queue number** | A Queue within the above set PCC. Created bookings are sent to this Queue. |
| **PNR Queue category** | Queue categories, in case you use them to sort messages. |

### Queues - notifications for agents in Galileo GDS

![](../.gitbook/assets/copy-queues.JPG)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Pole</th>
      <th style="text-align:left">Popis</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Pseudo City Code - copy</b>
      </td>
      <td style="text-align:left">An agency PCC where copies of created bookings are sent</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>PNR Queue number - copy</b>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>A Queue within the above set PCC. Created bookings are sent to this Queue.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>PNR Queue category - copy</b>
      </td>
      <td style="text-align:left">Queue categories, in case you use them to sort messages.</td>
    </tr>
  </tbody>
</table>![](../.gitbook/assets/image%20%2858%29.png)

| Pole | Popis |
| :--- | :--- |
| **Pseudo City Code - priority** | An agency PCC where copies of bookings created on the same day are sent. This is to make sure that your agents process bookings in time, if automated ticketing is not activated. |
| **PNR Queue number - priority** | A Queue within the above set PCC. Created bookings are sent to this Queue. |
| **PNR Queue category - priority** | Queue categories, in case you use them to sort messages. |

### Settings of secondary communication with Galileo GDS

![](../.gitbook/assets/image%20%2855%29.png)

This setting is similar to the above for Primary HAP. A secondary HAP is used, if you have multiple PCCs with different settings and for some reason you need to search through two PCCs at the same time and to combine the results. In order for this feature to function properly, complete the settings under **Parallel search**.

![](../.gitbook/assets/image%20%2826%29.png)

| Pole | Popis |
| :--- | :--- |
| **Allowed Store price higher than BB maximum of** | The limit value of how much higher the maximum price saved in the booking may be higher than the price returned during the search. If the limit is exceeded, from customer's perspective the booking is not finished and it is cancelled in the GDS. |
| **Allowed Store price smaller than BB maximum of** | The limit value of how much the lowest price saved in the booking may be lower than the price returned during the search. If the limit is exceeded, from customer's perspective the booking is not finished and it is cancelled in the GDS. |
| **Block non e-ticketable bookings** | If checked, GOL IBE blocks bookings that cannot be e-ticketed. |
| **Block unconfirmed reservation within 5 sec** | If checked, GOL IBE blocks bookings with segments not confirmed within 5 seconds since the bookings is created. |

### Special offers settings

![](../.gitbook/assets/image%20%288%29.png)

| Pole | Popis |
| :--- | :--- |
| **Maximum of automatic special offers** | When you enter a value, you activate automated saving of offers for each created booking to suggestions of special offers. You can then activate the special offers in the back office. |
| **Create automatic special offers with fixed fee** | If checked, GOL IBE automatically saves the service fee from the original bookings for the suggested special offers. |

### Settings of mandatory document information - DOCS

![](../.gitbook/assets/image%20%2857%29.png)

| Pole | Popis |
| :--- | :--- |
| **Countries requiring passport** | Zkratky zemí, pro které jsou vyžadovány údaje DOCS \(pokud vkládáte více kódů, je nutné je oddělit čárkou\). Zadaný stát vyžaduje pas, pokud je na jeho území letiště odletu, přestupu nebo cíle cesty. Pokud má být nastavení platné pro všechny státy, je nutné vyplnit kód: ALL. |
| **Přepravci vyžadující pas** | Kódy přepravců, kteří vyžadují vložení DOCS. Pokud je dopravce v itineráři \(marketingový nebo operující\), pak bude povinné zadávání čísel pasů bez ohledu na destinaci, tedy pro veškeré destinace s tímto dopravcem. Pokud má být nastavení platné pro všechny státy, je nutné vyplnit kód: ALL. |
| **Forma zobrazení** | Základní s vynecháním čísla pasu – DOCS údaje jsou vyžadovány ve zkrácené formě, což umožní dokončení rezervace, avšak neumožní vystavení letenky. Tato volba je nejčastější, potřeba informace o cestovních dokladech pro všechny pasažéry často komplikuje rezervaci a odrazuje klienty. Je vhodnější informace zjistit dodatečně. |
|  | Rozšířená včetně čísla pasu – DOCS údaje jsou vyžadovány v plné formě, a tedy včetně čísla cestovního dokladu. |
| **Vyplnění je povinné** | Při zaškrtnutí této volby a vyplnění některého z parametrů výše nemůže klient bez vyplnění DOCS údajů dokončit rezervaci, a aplikace zobrazí chybu. |

### Nastavení povinných informací o dokladech - FOID

![](../.gitbook/assets/image%20%285%29.png)

| Pole | Popis |
| :--- | :--- |
| **Státy vyžadující pas** | Zkratky zemí, pro které jsou vyžadovány údaje FOID \(pokud vkládáte více kódů, je nutné je oddělit čárkou\). Zadaný stát vyžaduje pas, pokud je na jeho území letiště odletu, přestupu, nebo cíle cesty. Pokud má být nastavení platné pro všechny státy, je nutné vyplnit kód: ALL. |
| **Přepravci vyžadující pas** | Kódy přepravců, kteří vyžadují vložení FOID. Pokud je dopravce v itineráři \(marketingový nebo operující\), pak bude povinné zadávání čísel pasů bez ohledu na destinaci, tedy pro veškeré destinace s tímto dopravcem. Pokud má být nastavení platné pro všechny státy, je nutné vyplnit kód: ALL. |
| **Vyplnění je povinné** | Při zaškrtnutí této volby a vyplnění některého z parametrů výše nemůže klient bez vyplnění FOID údajů dokončit rezervaci, a aplikace zobrazí chybu. |

