# Implementation of the air ticket special offers

You can find more details on the implementation of special offers also on [https://xxxx.golibe.com/gol-js/](https://xxxx.golibe.com/gol-js/) where xxxx designates the URL of your GOL IBE implementation. You have several options:

## 1. Easy implementation

The easiest way to implement the list is to use the following script. If you need another language version, you need to call it by the name of the script. For example: **gol-js-loader\_en.js** for English and **gol-js-loader\_ru.js** for Russian etc.

```markup
<script type="text/javascript" src="https://xxxx.golibe.com/gol-js/gol-js-loader_en.js"></script>
```

{% hint style="warning" %}
If the HTML includes the element id="GOLJS\_SpecialOffers", the list of special offers will be added there instead of after the loading script. Caution - this option does not switch languages, destinations and countries are returned in the default language.
{% endhint %}

## 2. Configurable implementation, selection of displayed special offers, retrieve of special offers by their name.

In this case, the list of special offers is implemented via the following configurable script:

```markup
<script type="text/javascript">
 var GOLJS = {
   dontLoadCss: true,                        // A switch to decide whether the default CSS should be used, or whether the web designer will create their own style.
   includeTags: ['tag1', 'tag2'],                // Names of special offers that should be selected (needs to be defined for the special offer), eg. Asia.
   excludeTags: ['tag3'],                        // You can also use the opposite logic, to display all special offers except for the selected ones.
   tmpl: {
     specialOffers: // ...jQuery.tmpl() template...you can prepare your own jQuery template.
   }
   specialOffersTag: '.mojeUmisteni' // you can create a class, it can be any jQuery selector, the default one is #GOLJS_SpecialOffers
 }
</script>
```

Example:  
The simplest case where you add just one special offer named \(tagged\): "OffersInEurope"

```markup
<html>
       <head>
       <meta http-equiv="content-type" content="text/html; charset=utf-8" />

       <script type="text/javascript">
               var GOLJS = {
                       dontLoadCss: false,
                       includeTags: ['OffersInEurope']
               }
       </script>
       </head>
       <body>
               <script type="text/javascript" src="https://xxxx.golibe.com/gol-js/gol-js-loader_cz.js"></script> // kde xxx je URL základního FE.
       </body>
</html>
```

You can add more names \(tags\) of special offers at once into the script. You add the names \(tags\) in the GOL IBE back office under: **Prices -&gt; Special offer extended**

Also, each special offer can have more names \(tags\). You can then display only the desired groups on your website:

![](../../.gitbook/assets/image%20%2830%29.png)

## 3. Your own implementation

The third option is to download the list of special offers and process it as you need.

```http
http://xxxx.golibe.com/json/special-offers-list/en //where xxxx is the URL of your GOL IBE and /en is the language code
```

