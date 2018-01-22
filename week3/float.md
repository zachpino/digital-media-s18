###Floating Elements in Sequence

-----

We saw how to [reset CSS](reset.md), and previously how each [subsequent block element](single.md) we have used always pushes itself down below its predecessor. This behavior is easy to understand when we recall that block elements by default take up 100% of the width of their parent. By default, they stack!

This is rarely the behavior we want when divs are narrower than the page width. Instead, for nice page layouts, we often want divs to be positioned next to one another. For this goal, we need a new css property: `float`. Floating removes the default 100% width, and allows a block-level element to shift up in the flow of the page.

```
<html>
<head>
	<link href="reset.css" rel="stylesheet">

	<style>
		
		.series{
			width:30%;
			height:500px;
			border:1px solid darkgray; 
			float:left;
		}

	</style>
</head>

<body>

	<div class="series"> 
	</div>
	<div class="series"> 
	</div>
	<div class="series"> 
	</div>

</body>
</html>
```

You should see three outlined rectangles, each roughly 30% of the width of the page. Each should be pushed up adjacent to the left-hand preceding div. Changing the styling to `float:right` would shove the divs to the upper-right corner of the browser.

If we add a fourth `series` div, you will find that it is pushed down to the next line. Floating an element forces the element to do its best to move up and to the right or left (depending on your `float:` setting) so long as there is room. If there is not adequate space, its former block-level behavior kicks in and it moves down the flow of the page.

If we wanted to introduce some margins we could do easily do so.

```
<html>
<head>
	<link href="reset.css" rel="stylesheet">

	<style>
		
		.series{
			width:30%;
			height:500px;
			border:1px solid darkgray; 
			float:left;
			margin-left:1.25%;
			margin-right:1.25%;
			margin-top:10px;
		}

	</style>
</head>

<body>

	<div class="series"> 
	</div>
	<div class="series"> 
	</div>
	<div class="series"> 
	</div>
	
</body>


</html>
```

Combining the behavior of regular block elements, inheritance rules for positioning, and floated elements gives web designers tremendous expressiveness in shaping the layout of their sites. 

There is one catch, though, in understanding the [box model](boxmodel.md).

