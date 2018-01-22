###Simple Positioning

-----

Setup a basic html file on your server and access it with your browser.

```
<html>
  <head>
  </head>

  <body>
  </body>
</html
```

Recall that an html file needs a `<head>` and `<body>` tag to be valid.

Let's create an arbitrary page division, a `<div>`, inside of the body of the page and give it a name. Let's also assign an ID for easier styling.

```
<body>
  <div id="positioning">
  </div>
</body>
```

In the head of the page, assign some styles so we can see the div.

```
<head>
  <style>
    #positioning{
		width:50px;
		height:100px;
		border:1px solid darkgray;    
    }
  </style>
</head>
```

The syntax for the css `border` property shorthand used here is `border: strokeweight strokestyle color`. 

You should now see a thin gray rectangle in the upper left corner of the page.

We can move this rectangle around with some useful css positioning properties. There are many options available, we'll focus on the standards.

```
<head>
  <style>
    #positioning{
		width:50px;
		height:100px;
		border:1px solid darkgray;    
		
		margin-left:100px;
		margin-top:20px;
}
  </style>
</head>
```

Using different kinds of units in those `margin` properties allows for more flexiblity. For instance, we can use `%` units to specify the dimensions and positions of items relative to the *width* of the item's parent -- in this case the browser width itself.


```
<html>
<head>
	
	<style>
		#positioning{
			width:50px;
			height:100px;        
			border:1px solid darkgray;    
			
			margin-left:10%;
			margin-top:20%;
		}
	</style>
</head>

<body>

<div id="positioning"> 
</div>

</body>


</html>
```

With this css in place, you can resize the page and see the rectangle change position depending on the width of the browser window. You can use the `vh` unit to specify a percentage of the vertical space.

Other available proportional units include `em` and `rem`, which are values that are derived from the width of the styled typeface. We'll discuss this later when introducing responsive design.

Let's see how positioning impacts the *flow* of subsequent elements on the page. 

```
<html>
  <head>
	<style>	
		#positioning{
			width:50px;
			height:100px;
			border:1px solid darkgray;    

			margin-left:10%;
			margin-top:10vh;
		}

		#follower{
			width:50px;
			height:100px;
			border:1px solid darkgray;    
		}


	</style>
  </head>

  <body>

	<div id="positioning"> 
	</div>
	<div id="follower"> 
	</div>

  </body>
</html>
```

After adding a second div, giving it styling, and assigning it the appropriate `id`, you should see in your browser window a set of rectanges. The first is positioned according to your values. The second should fall below it.

Each block level element is *pushed down* a vertical level, and it defaults to sitting the left-side of the screen. This behavior can be changed, as we will do when we build a grid system.

Let's move on to [nested div positioning](nested.md).
