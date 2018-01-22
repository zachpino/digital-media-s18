###Laptops

---

The [tablet style rules](tablet.md) still kept some elements hidden, but the laptop style bring everything in -- and allows for more display flexibility. 

```
/* Laptops: Full, Half, Third, Quarter, Sixth Widths */
 @media only screen 
 and (min-width : 1024px) 
 and (max-width : 1223px) {
       #container {background-color:#dee;}
      .one { width:15.666%; }
      .two { width:15.666%; }
      .three { width:24% }
      .four { width:32.333%}
      .five { width:40.666% }
      .six { width:49%; }
      .seven { width:57.333%; }
      .eight { width:65.666%; }
      .nine { width:74%; }
      .ten { width:82.333%; }
      .eleven { width:82.333%; }
      .twelve { width:99%; }
  }
  ```
  
The laptop max breakpoint is `1px` less than the desktop `min-width` assigned earlier, so our grid flows nicely if a user resizes their browser on large displays.
  
This covers all classes of devices with a general css breakpoint ruleset. However, depending on the design, these breakpoints should be changed to accomodate the needs of the specific layout. No two stylesheets will have the same breakpoints, and the breakpoints don't even need to correspond to device sizes! Let the layout of the content dictate the breakpoints.

You can view the [complete html document](complete.md).

Now, as a last step, let's leave text behind and [add some images](image.md) to our nascent website.
