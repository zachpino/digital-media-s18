###Box Model

------

Due to historical complications, the `width` of any given element in html may or may not include different properties. For instance, the dimensions of `padding` and `border` properties, which sit outside the actual content of the element, are not included. This means that [floated divs](float.md) might not behave how you expect. Consider this example.

```
<html>
<head>
	<link href="reset.css" rel="stylesheet">

	<style>
		
		.series{
			width:33.333%;
			height:500px;
			border:2px solid darkgray; 
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

Three floated divs, in sequence. Each is set to 33% of the horizontal dimension of their parent (the body of the page). We would expect these to meet nicely and take up the full width of the page. They do not, however. Two will fit in a row, and the third will be pushed a line below in the page flow.

The problem is that our `border` property is not counted toward the specified width of the element. So, in this case, each element is 33.333% (it's never worth specifying to more than 3 decimal places in html) of the width of the page *plus* two times the stated border thickness of 2px. 

So, in a browser window with a width of 1000px, each element is `333.33px + 2px + 2px = 337.33px`. Two of those elements measure 674.66px wide together, so there is not enough room for the third div on the same horizontal line!

This is *infuriating*. Luckily, there is an easy fix in your head `<style>` declaration.

```
<html>
<head>
	<link href="reset.css" rel="stylesheet">
	
	<style>
		html {
			box-sizing: border-box;
		}
		*, *:before, *:after {
			box-sizing: inherit;
		}

		.series{
			width:33.3333%;
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

The `*` character is a *wildcard*, it matches all elements. The `box-sizing:border-box` property, now being inherited by everything on the page, forces the browser to calculate borders and padding inside of the set `width`.

Now, let's use these skills to make a page construction resource called a [grid system](grid.md).
