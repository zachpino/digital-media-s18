###Nested Positioning and Centering

-----

Let's write similar html code to the [simple positioning example](single.md). The only difference is that, rather than having two divs in sequence, this example nests one div inside another.

```
<html>
<head>
	
	<style>
		
		#parent{
			width:500px;
			height:500px;
			border:1px solid darkgray;    
		}

		#child{
			width:50px;
			height:50px;
			border:1px solid cyan;    
		}


	</style>
</head>

<body>

	<div id="parent"> 
		<div id="child"> 
		</div>
	</div>
</body>


</html>
```

This will render as a cyan square inside a gray square in the upper-left corner of the browser window. We can position the parent div to move it around on the page with `margin-left` and `margin-top`.

```
#parent{
	width:500px;
	height:500px;
	border:1px solid darkgray;    
	
	margin-left:400px;
	margin-top:300px;
}
```

Note that, like with all css properties, rules of inheritance means that the child is moved along with its parent.

The converse is not true.

```
#child{
	width:500px;
	height:500px;
	border:1px solid darkgray;    
	
	margin-left:100px;
	margin-top:300px;
}
```

This positions the child inside of the parent. Inheritance means properties only descend in the tag heirarchy, and never ascend. The child can be moved relative to its parent, just as the parent is moved relative to its parent — the body of the webpage.

A common use case for nested divs is in centering content. Setting `margin-right:auto` and `margin-left:auto` on a child element with a set width will center it relative to its parent.

```
<html>
<head>
	
	<style>
		
		#parent{
			width:500px;
			height:500px;
			border:1px solid darkgray;    
			margin-right:auto;
			margin-left: auto;
		}

		#child{
			width:50px;
			height:50px;
			border:1px solid cyan;    
			margin-top:25px;
			margin-right:auto;
			margin-left: auto;
		}


	</style>
</head>

<body>
	<div id="parent"> 
		<div id="child"> 
		</div>
	</div>
</body>
</html>
```

Now, let's do some housekeeping and [reset our css](reset.md).
