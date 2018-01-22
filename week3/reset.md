###Reset Default Styles

-----

You might have noticed in the [last examples](nested.md) a small margin running around elements positioned at `margin-left:0px;`. This is due to how browsers maintain default styles for most html elements, including the `<body>`.

This can be problematic, as this invisible padding can obstruct precise positioning. It is a best practice to strip out any unneeded default styling with a set of css rules, often called a *reset stylesheet*. 

The following css code intentionally does not remove all default styling -- for instance it leaves behind default `<button>` and `<form>` styling so that those elements are recognizable without extra work -- but it does remove most positioning styles that might ruin your layout calculations. It also removes default styling on the `<h#>` elements, so those will no longer be visually distinct.

```
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
```

This code can be included in a `<style>` tag in the `<head>` of your page. But, a better practice is to include it in a separate, linked stylesheet.

Pasting that content into a new file on your server called `reset.css`, we can include it in our page like so.

```
<html>
<head>

<link rel="stylesheet" href="reset.css" />

  <style>
	</style>
</head>

<body>

</body>


</html>
```

You might recognize the `href` attribute from our time spent making links, and the terminating `/>` when we discussed self-closing tags like `<hr />`.

The `rel=` attribute, short for relationship, defines how the browser will incorporate the named file. In this case, we want the browser to include this file as a `stylesheet` for the rendered page.

The order is important here. If `<link rel="stylesheet" href="reset.css" />` was included below the `<style>` block in the `<head>` of your page, the reset styles would override the styles you set! Make sure you link your `reset.css` before any other styling.

The browser takes css rules into account from a variety of sources.

- Linked Stylesheets
- Style Tags in the Head of the Page
- Style Tags in the Body of the Page
- Inline CSS

The closer a rule is to the element it defines, the more power it has to override matching styles declared elsewhere.

Now that we've reset the page, we can advance to [floating elements](float.md).
