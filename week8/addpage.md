###Week 1: Creating a Webpage

-----

After [installing the LAMP stack](lampinstall.md), the AWS server is now serving a webpage to interested browsers at your allocated IP address. The page being served is Apache's default welcome message, which can be easily replaced.

[Use ssh](serveraccess.md) to get into your machine, and then use `cd` to move to Apache's default folder.

`cd /var/www/html/`

Anything in this folder will be served to web browsers. By default `index.html` is provided to web browsers by the server, we often call this a 'homepage'. If you run `ls`, you will find a default `index.html` in this directory which contains the Apache welcome message. Rename it for later reference.

`mv index.html apachewelcome.html`

If you were to visit your IP address now, there would be an error, as the web browser can't find the default `index.html` file. Let's create it and add content.

`touch index.html`

`echo "hello world!" > index.html`

Visiting your IP address now should result in a simple webpage exclaiming "hello world!" 

-----

We can easily replace and append content on your `index.html` with `echo`. Something worth adding other than text might be  `anchors`. Anchors allow individual files to reference one another, and web browsers interpret anchors as clickable links.

The HTML scripting language uses `tags` to distinguish computer-readable page structure and functionality from human-readable content and styling. Tags are always surrounded by `<` and `>` characters, and are closed off with a near duplicate of themselves. Tags include `attributes`, which shape their functionality and behavior.

`<tag attribute1="value" attribute2="value">Optional Visible Information</tag>`

Anchors are created with the `<a>` tag. They have an attribute called `href` which indicates their destination.

`<a href="secondpage.html">Second Page</a>`

This tag will link to a file called `secondpage.html` from the current page. We can `echo` that to `index.html`.

`echo '<a href="secondpage.html">Second Page</a>' > index.html`

Note that, since attributes use `"..."` in their syntax, `echo` is instead given a string of text surrounded with single quotation marks `'...'`.

If you visit your IP address, you should find a clickable link. Of course, `secondpage.html` doesn't exist yet!

`echo '<a href="index.html">Go Back Home</a>' > secondpage.html`

The two pages now link back and forth to one another.

-----

At this stage, we've setup a server, connected it to the internet, and built out some content. Now, [practice and take some next steps](homework.md).
