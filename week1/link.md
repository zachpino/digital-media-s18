### Week 1: Creating Links

-----

Something worth adding other than text to these simple pages might be `anchors`. Anchors allow individual files to reference one another, and web browsers interpret anchors as clickable links.

Anchors are created with the `<a>` tag. They have an attribute called `href` which indicates their destination.

`<a href="secondpage.html">Second Page</a>`

This tag will link to a file called `secondpage.html` from the current page. Make a page called `secondpage.html` within the same folder, and check if the link works!

Let's construct a link back inside of `secondpage.html`.

`echo '<a href="index.html">Go Back Home</a>' > secondpage.html`

The two pages now link back and forth to one another. Links are fundamental to the [open web](https://en.wikipedia.org/wiki/Open_Web) and [search engine rankings](https://en.wikipedia.org/wiki/Search_engine_indexing). Sprinkle them everywhere! 

Let's add some visual flair to these boring pages with some [images](image.md).


