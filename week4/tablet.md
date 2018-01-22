### Large Mobile Phones and Tablets

[Mobile devices](mobile.md) are fairly homogenous, but this is a wide class of devices with huge variations in interaction. For instance, some will have stylus inputs, others will have reorientable displays, kickstands, or hardware keyboards -- and many are portable. We want our grid system to look good and be usable throughout the diverse class. 

```
/*Large Mobile Styles: Full, Half, Third Widths*/
@media only screen and (min-width : 480px) and (max-width : 767px) {
      #container {background-color:#eed;}
      .one { display:none; }
      .two { display:none; }
      .three { display:none }
      .four { width:32.333%}
      .five { width:49% }
      .six { width:49%; }
      .seven { width:49%; }
      .eight { width:65.666%; }
      .nine { width:99%; }
      .ten { width:99%; }
      .eleven { width:99%; }
      .twelve { width:99%; }
  }


/*Tablets: Full, Half, Third, Quarter Widths*/
 @media only screen and (min-width : 768px) and (max-width : 1023px) {
       #container {background-color:#ded;}
      .one { width:24%; }
      .two { width:24%; }
      .three { width:24%; }
      .four { width:32.333%; }
      .five { width:49% }
      .six { width:49%; }
      .seven { width:49%; }
      .eight { width:65.666%; }
      .nine { width:74%; }
      .ten { width:74%; }
      .eleven { width:74%; }
      .twelve { width:99%; }
  }
  ```

Here, again, some elements remain hidden with `display:none` and others are resized and simplified to accomodate specific layout needs.

Let's move on to [laptop styles](laptop.md).
