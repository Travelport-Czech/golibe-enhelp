# MIR

MIR \(Machine Interface Record\) is one of the simplest tools provided by Galileo for generating data on bookings. These are text files with a fixed format, generated directly by the Galileo system regardless of whether the bookings were created via GOL IBE.

You can find the documentation [&gt;here&lt;](https://support.travelport.com/webhelp/MIR/Default.htm).

Besides the standard content, GOL IBE adds the following items to the bookings, and you can see them in MIR files:

## Customer's telephone contact:

**A12PRGM \*00420123123123**  
**A12** _- section in which you can find the information  
**PRGM** **\***_ _- statistical information_  
**00420123123123** _- customer's phone number_

## Customer's email address:

**A12PRGE \*MARTIN//TRAVELPORTGDS.CZ  
A12** _- section in which you can find the information_  
**PRGE \*** - statistical information  
_**MARTIN//TRAVELPORTGDS.CZ** - \_email address, // is used instead of @ \(the reservation system uses @ for other special features and therefore this character is not used\)._

## Billing address:

**A13W-JAROSLAV NOVAK\*TRAVELPORT S.R.O\*123456789/CZ123456789/PRAHA\*SOKOLOVSKA 1234/5\*CZ 11800\*** _individual blocks of information are separated by \*_  
**A13W-** _section in which you can find the information_  
**JANOSLAV NOVAK** _- name of the person_  
**TRAVELPORT S.R.O** _- name of the company_  
**123456789/CZ123456789/PRAHA** _- BID/VAT ID/City_  
**SOKOLOVSKA 1234/5** _- Street_  
**CZ 11800** \_- _Country\_code ZIP_  
If the customer doesn't enter any of the above details, it is replaced with "NONE".

## Variable symbol \(the variable symbol under which you can find the booking in the GOL IBE back office\):

**A1500VARIABLE SYMBOL:785972  
A1500** - _section in which you can find the information_  
**VARIABLE SYMBOL:** _- statistical information_  
**785972** _- numeric variable symbol_

