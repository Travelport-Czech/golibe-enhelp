# Vložení vyhledávacího formuláře ubytování

Vyhledávací formulář ubytování je možné implementovat jen jako iframe:

Příklad implementace iframu je možné najít na [http://xxxx.golibe.com/iframe.php?action=vHotels](http://xxxx.golibe.com/iframe.php?action=vHotels), kde xxxx je označení URL pro vaši implementaci GOL IBE.

```markup
<iframe src="https://xxxx.golibe.com/?iframe=1?action=vHotels" scrolling="no" width="530px" height="510px" frameborder="0" allowtransparency="true">
```

