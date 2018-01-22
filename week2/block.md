###Week 2: Block Elements

-----

Inside of [Sublime Text](sublime.md), press `command/control + shift + p` to open the command palette. There, type in `Browse Server`, select it, and then select your previously created SFTP configuration file. You should see the contents of your `/var/www/html` directory.

Create a new file called `index.html`. This is the file that browsers load when a website address is visited.

Visit your elastic IP address in a browser, and reload the page after each following step to see the results of you code visualized.

Rather than just typing text into this file as we have done previously, let's begin writing specially formatted HTML code for in-browser rendering.

First, let's declare the document as an html file, a file written in the *hypertext markup language*, by wrapping the whole file in the appropriate tag.

```
<html>

</html>
```

Now, let's add a few structural tags that each html document should have.

```
<html>
  <head>
  </head>
  
  <body>
  </body>
</html>
```

The `<head>` tag contains any code or data that *should not be displayed* on the resulting web page. For instance, tags specifying links to necessary scripts, stylesheets, and analytics libraries will be placed inside of the `<head>` tag.

The `<body>` tag contains all of the visible parts of the webpage. Let's add some content!

```
<html>
  <head>
  </head>
  
  <body>
    <h1>Webpage Title</h1>
    <p>
    This is some body text.
    </p>
    <p>
    This is some more body text.
    </p>
  </body>
</html>
```

This should render like this in a browser.

<hr />

<h1>Webpage Title</h1>
<p>
This is some body text.
</p>
<p>
This is some more body text.
</p>
<hr />

The `<h1>` element, abbreviated from "first-level-header", adds some default title styling to the text contained within the tags, and `<p>` for simple "paragraph" does not. By convention, elements contained within other elements are indented, to show the hierarchy of the page.

There are many levels of headers.

```
<html>
  <head>
  </head>
  
  <body>
    <h1>First Level Webpage Title</h1>
    <h2>Second Level Webpage Title</h2>
    <h3>Third Level Webpage Title</h3>
    <h4>Fourth Level Webpage Title</h4>
    <h5>Fifth Level Webpage Title</h5>
    <h6>Sixth Level Webpage Title</h6>
  </body>
</html>
```

<hr />
<h1>First Level Webpage Title</h1>

<h2>Second Level Webpage Title</h2>

<h3>Third Level Webpage Title</h3>

<h4>Fourth Level Webpage Title</h4>

<h5>Fifth Level Webpage Title</h5>

<h6>Sixth Level Webpage Title</h6>
<hr /> 

The styling you see in your browser will likely differ. But, you should see six clearly different styles on the page. These can be customized easily in CSS, which we will cover in subsequent lessons.

Note, though, in html scripts, white space is not observed. 

This code...

```
<html>
  <head>
  </head>
  
  <body>
    <h1>First Level Webpage Title</h1>
    <h2>Second Level Webpage Title</h2>
  </body>
</html>
```

renders the same as this code.

```
<html>
  <head>
  </head>
  
  <body>
    <h1>First Level Webpage Title</h1>




    <h2>Second Level Webpage Title</h2>
  </body>
</html>
```

In order to introduce spacing, we will need to use CSS.

The `<h#>` and `<p>` tags are *block-level* elements. They define a rectangle of space around themselves that takes up 100% of the width of their parent element, which is in this case the `<body>` of the html document. As a result, each block-level element makes a new vertical place for itself on the page.

Another set of useful block-level elements are the list elements.

```
<html>
  <head>
  </head>
  
  <body>

    <ul>
      <li>Unordered List Item</li>
      <li>Unordered List Item</li>
      <li>Unordered List Item</li>
    </ul>
    
    <hr />
    
    <ol>
      <li>Unordered List Item</li>
      <li>Unordered List Item</li>
      <li>Unordered List Item</li>
    </ol>    

  </body>
</html>
```

<hr />
<ul>
<li>Unordered List Item</li>
<li>Unordered List Item</li>
<li>Unordered List Item</li>
</ul>

<hr />

<ol>
<li>Ordered List Item</li>
<li>Ordered List Item</li>
<li>Ordered List Item</li>
</ol>    
<hr />

The `<ul>` and `<ol>` tags define the beginning and ends of lists, which contain items defined by `<li>` tags. 

Also note another block-level element, `<hr />`, which creates a horizontal rule line on the page. Its a different kind of html element, called a *void element*, that cannot contain other content. For this reason, the ending slash is included in the initial tag. 

Lists can also be nested.

```
<html>
  <head>
  </head>
  
  <body>

    <ul>
      <li>Unordered List Item</li>
      <ol>
        <li>Ordered List Item</li>
        <li>Ordered List Item</li>
        <li>Ordered List Item</li>
      </ol>    
      <li>Unordered List Item</li>
    </ul>
 
  </body>
</html>
```

<hr />
<ul>
<li>Unordered List Item</li>
<ol>
<li>Ordered List Item</li>
<li>Ordered List Item</li>
<li>Ordered List Item</li>
</ol>    
<li>Unordered List Item</li>
</ul>
<hr />


And don't forget 90's favorite `<marquee>`.

```
<html>
  <head>
  </head>
  
  <body>

    <marquee>
      Moving Text
    </marquee
 
  </body>
</html>
```

There are many other block-level elements, but for now, let's move on to [another type of element](inline.md) to be placed *inside* of the block-level discussed here.
