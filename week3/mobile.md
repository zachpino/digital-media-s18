###Mobile Breakpoints
---

Having satisfied our [large screen issues](breakpoints.md), we can move on to addressing the needs of the more common mobile browser situation.

Again, let's add some CSS code to the `style` block within the `head` of the page.

```
/*Standard Mobile Style: Half or Full Widths*/
 @media only screen and (min-width : 320px) and (max-width : 479px) {
      #container {background-color:#edd;}
      .one { display:none; }
      .two { display:none; }
      .three { display:none }
      .four { display:none}
      .five { display:none }
      .six { width:49%; }
      .seven { width:99%; }
      .eight { width:99%; }
      .nine { width:99%; }
      .ten { width:99%; }
      .eleven { width:99%; }
      .twelve { width:99%; }
  }
```

Again, we ask the browser to report how big its viewport is. In this case, if the browser returns any size bigger than `320px` *and* smaller than `479px`, these style are applied to the elements on the page.

Note that we have added `display:none` to `col` divs smaller than `.six`. This allows us to hide divs and their contents on smaller devices! We change our background color to a pale red, and only allow `col` divs at half and full width.

We now have content that looks much better on small mobile screens. The visitors to our sites should get a designed experience regardless of their device -- this is called *responsive design*.

Now, let's add some styles for [larger phones and tablets](tablet.md). 
