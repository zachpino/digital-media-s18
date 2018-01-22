###Spans and Divs

-----

Despite the proliferation of block-level and inline html elements, two reign supreme.

The `<div>` element, a page *division*, and the `<span>` element, a span of text, serve as the arbitrary block and inline element, respectively. 

```
<html>
  <head>
  </head>
  
  <body>
    <div>
        <p>
            This is a paragraph tag within the <span>first</span> div tag.
        </p>
    </div>
    <div>
        <p>
            This is a paragraph tag within the <span>second</span> div tag.
        </p>
    </div>
  </body>
</html  
```

On its own, this code doesn't do much different than using only `<p>` tags and leaving the `<span>`s out.

But, we can add styles to the divs and spans.

```
<html>
  <head>
  </head>
  
  <body>
    <div style="color:red">
        <p>
            This is a paragraph tag within the <span style="color:pink">first</span> div tag.
        </p>
    </div>
    <div style="color:blue">
        <p>
            This is a paragraph tag within the <span style="color:cyan">second</span> div tag.
        </p>
    </div>
  </body>
</html>  
```

`<div>` and `<span>` are by a significant margin the most used html tags, especially when combined with *class* names.

```
<html>
  <head>
    <style>
      .redText {
      color:red
      }
      
      .blueText {
      color:blue
      }
    </style>
  </head>
  
  <body>
    <div class="redText">
        <p>
            This is a paragraph tag within the <span style="color:magenta">first</span> div tag.
        </p>
    </div>
    
    <div class="redText">
        <p>
            This is a second paragraph tag within the <span style="color:orange">first</span> div tag.
        </p>
    </div>
    
    <div class="blueText">
        <p>
            This is a paragraph tag within the <span style="color:teal">second</span> div tag.
        </p>
    </div>
  </body>
</html>  
```

Some new learnings! By defining a style in CSS with the `<head>` of our web page, we can give a name to a style, and then use and reuse it throughout the document. We assign a `class=""` attribute to the `<div>`s on the page to associate that `<div>` with the matching styling in the `<head>` of the page. 

Classnames in CSS are preceded by a `.`.

Note that styling with class names results in easier to read code, and separates aesthetics from page strucure. Also, see how inline styling overrides class definitions? Again, cascading styles in action! The closer a style definition is to its content, the more power it has. 

A very similar concept is `id`s. Unlike classnames, which can be reused, `id`s should be used exactly once in a document. 

```
<html>
  <head>
    <style>
      .redText {
      color:red
      }
      
      #blueText {
      color:blue
      }
    </style>
  </head>
  
  <body>
    <div class="redText">
        <p>
            This is a paragraph tag within the <span style="color:magenta">first</span> div tag.
        </p>
    </div>
    
    <div class="redText">
        <p>
            This is a second paragraph tag within the <span style="color:orange">first</span> div tag.
        </p>
    </div>
    
    <div id="blueText">
        <p>
            This is a paragraph tag within the <span style="color:teal">second</span> div tag.
        </p>
    </div>
  </body>
</html>  
```

To assign an `id`, use the tag attribute `id=""` and define the styling in the `<head>` of the document with a `#` character.
