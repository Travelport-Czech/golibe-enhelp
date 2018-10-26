# MIR

MIR \(Machine Interface Record\) je jedním z nejjednodušších nástrojů Galilea pro generování dat o rezervacích. Jedná se o textové soubory s pevným formátem, které generuje přímo rezervační systém Galileo, bez ohledu na to, jestli rezervace pocházejí z GOL IBE.

Dokumentaci najdete [&gt;zde&lt;](https://support.travelport.com/webhelp/MIR/Default.htm).

Ke standardnímu obsahu vkládá GOL IBE do rezervací navíc následující položky nalezitelné v souborech MIR:

## Telefonický kontakt na objednavatele:

**A12PRGM \*00420123123123**  
**A12** _- sekce podle které jde najít údaj  
**PRGM** **\***_ _- statický údaj_  
**00420123123123** _- tel. číslo na objednavatele_

## E-mailová adresa objednavatele:

**A12PRGE \*MARTIN//TRAVELPORTGDS.CZ  
A12** _- sekce podle které jde najít údaj_  
**PRGE \*** _\_- statický údaj  
_**MARTIN//TRAVELPORTGDS.CZ** - \_emailové adresa, // je vkládáno namísto @ \(rezevační systém má pro @ speciální využití a proto není tento znak používán\)._

## Fakturační adresa:

**A13W-JANOSLAV NOVAK\*TRAVELPORT S.R.O\*123456789/CZ123456789/PRAHA\*SOKOLOVSKA 1234/5\*CZ 11800\*** _Jednotlivé bloky informací jsou odděleny \*_  
**A13W-** _sekce podle které jde najít údaj_  
**JANOSLAV NOVAK** _- jméno osoby_  
**TRAVELPORT S.R.O** _- název firmy_  
**123456789/CZ123456789/PRAHA** _- IČO/DIČ/Město_  
**SOKOLOVSKA 1234/5** _- Ulice_  
**CZ 11800** \_- Kód\_země PSČ  
Pokud některý z údajů nebyl zákazníkem zadán, je nahrazen textem: "NONE".

## Variabilní symbol \(variabilní symbol pod kterým lze najít rezervaci v backoffice GOL IBE\):

**A1500VARIABLE SYMBOL:785972  
A1500** - _sekce podle které jde najít údaj_  
**VARIABLE SYMBOL:** _- statický údaj_  
**785972** _- číselný variabilní symbol_

