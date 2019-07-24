# Implementation of the air ticket search form

You can implement the air ticket search form via:

## 1. html-php package - RECOMMENDED!

The form is responsive and adjusts to screens of different sizes \(mobile responsiveness\).

![](../../.gitbook/assets/image%20%2882%29.png)

An example of how the form is displayed, if the size of the window changes \(on mobile devices\):

![](../../.gitbook/assets/image%20%2816%29.png)

You can download the HTML package from the GOL IBE back office:

a\) if you have agency credentials, go to the section **Dealers**, choose the relevant dealer \(website\), click **Detail**, click on the button **Front-End settings** and then click on the link **Static HTML for download**.

b\) if you have dealer credentials, then go straight to **Dealers** -&gt; **Front-End settings** -&gt; link **Static HTML for download**.

The form includes HTML, CSS, pictures and relevant scripts for implementation into your website, including the full functionality of the destination search tooltip. You can customize the form as you wish.

## 2. iframe

Another option is the iframe which offers an easy implementation, however it does have some disadvantages. For example, if your customers search for an open-jaw flight and they keep adding more and more flights, the form will keep extending and you either need to leave enough space on your website, or allow scrolling. Neither looks very nice.

Here's an example of the implementation.

{% hint style="info" %}
**Don't forget to include also sections "&lt;meta name="viewport".." and "&lt;style.." which are important for correct dimensions and responsive display.**

**Replace XXXXXX \(below\) with your URL.**
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

## **For geeks: Customize the default settings of the search form**

In both above cases, parameters of the search form can be predefined and your customers then see them pre-filled.

The easiest way to find out how to create the link is to:

* Set up the search form the way you want to predefine the search.
* Search and get to the page with search results.
* Find the button _New search_ that would normally get you back to the search form, right-click on it and click _Copy link_.

Examples of what you'll get:

`https://xxxx.golibe.com/index.php?action=vFlights&flights[0][origin]=PRG&flights[0][destination]=LON&flights[0][departureDate]=2013-01-09&flights[1][origin]=LON&flights[1][destination]=PRG&flights[1][departureDate]=2013-01-16&searchType=FromFour&travelers[0]=ADT&dateVariants=exact&returnTicket=on&step=one2`

If you want to predefine the search form for PRG-LON, omit other parameters in the URL \(such as the date\) and keep only the relevant part. You can then use the amended URL as a link:

```http
?action=vFlights&flights[0][origin]=PRG&flights[0][destination]=LON&flights[1][origin]=LON&flights[1][destination]=PRG&searchType=FromFour&travelers[0]=ADT&dateVariants=exact&returnTicket=on&step=one2
```

...or use it in the iframe:

```markup
<iframe src="https://xxxx.golibe.com/static.php?action=vFlights&flights[0][origin]=PRG&flights[0][destination]=LON&flights[1][origin]=LON&flights[1][destination]=PRG&searchType=FromFour&travelers[0]=ADT&dateVariants=exact&returnTicket=on&step=one2" scrolling="no" width="530px" height="510px" frameborder="0" allowtransparency="true">
```

If you want to redirect your customers straight to the search results and let them wait on the waiting page instead of displaying a blank page, you can add a redirection. Caution: the part after "...redirect=" must be an encoded URL. For example:

```
https://xxxx.golibe.com/index.php?action=vWait&redirect=http%3A%2F%2Fxxxx.golibe.com%2Findex.php%3Faction%3DvFlights%26flights%5B0%5D%5BdepartureDate%5D%3D2014-11-07%26flights%5B0%5D%5Bdestination%5D%3DPTP%26flights%5B0%5D%5Borigin%5D%3DPAR%26flights%5B0%5D%5BdeparturePlusMinusDay%5D%3D3%26flights%5B1%5D%5BdepartureDate%5D%3D2014-11-14%26flights%5B1%5D%5Bdestination%5D%3DPAR%26flights%5B1%5D%5Borigin%5D%3DPTP%26flights%5B1%5D%5BdeparturePlusMinusDay%5D%3D3%26travelers%5B0%5D%3DADT%26returnTicket%3Don%26vendor%3DTX%26dateVariants%3Dclose%26step%3DChooseFromFour%26target%3Dflights
```

For URL encoding, you can use for example this open source utility:

[https://www.freeformatter.com/url-encoder.html](https://www.freeformatter.com/url-encoder.html)

