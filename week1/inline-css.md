###Week 2: Inline Styling

-----

There are many ways to add customized style to [any html element](inline.md).

The aspects that we can change are defined in a simple language called CSS, Cascading Style Sheets.

CSS properties can be added to an html document in many different places, but the simplest is directly inline with the element being modified.

Unfortunately, GitHub doesn't display inline CSS, so it is impossible to show the result of this code here.

```
<html>
  <head>
  </head>

  <body>
    <p>
      This is unstyled text.
    </p>
    
    <p style="color:red">
      This is styled text.
    </p>
  </body>
</html>
```
This code, loaded in a browser, should show one paragraph in black text, and another in red.

CSS style attributes can be added to any element, and the many [CSS properties](http://www.w3schools.com/cssref/) are well documented.

The *cascading* part of Cascading Style Sheets refers to how styles propogate to their children.

```
<html>
  <head>
  </head>

  <body>
    <p style="color:red">
      This is styled text.
        <strong>
          This text will also be red, inherited from its parent
        </strong>
    </p>
  </body>
</html>
```

The `strong` tag adds bold styling, but the text stays red. There are complex rules that govern style inheritance, which will be documented in future guides.

In general, inline styling is reserved for overriding styles [declared in the head of the document](span-div.md).
