###Simple Grid System

-----

With all of these lessons in place and a clear understanding of the [box model](boxmodel.md), we can construct a toolkit for building websites called a grid system. Grid systems allow easy and flexible construction of columns and rows of content based on simple ratios. Commonly, the page is divided up into 12 columns.

We will assume in this example a .5% margin on both sides of each column to serve as the *gutter* between columns. This yields a 1% margin between all elements.

The formula for calculating the values below is as follows.


To calculate your one column width:

```
(100 - (n * 2m)) / n 

n = desired column count
m = margin
```

Take that value, and use it to create all other values.

```
w * n + ((n-1)*2m)

w = column width calculated above
n = desired column count
m = margin
```

And here is the grid!

```
<html>
<head>
	<title>Grid System</title>
	
	<link href="reset.css" rel="stylesheet">

	<style>
		html {
			box-sizing: border-box;
		}

		*, *:before, *:after {
			box-sizing: inherit;
		}

		#container{
			width:80%;
			margin-left: auto;
			margin-right: auto;
		}

		.row::after {
			content: "";
			clear: both;
			display: table;
		}

		.col{
			background-color: lightgray;			
			float:left;
			height:50px;
			margin-left:.5%;
			margin-right:.5%;
			margin-top:.5%;
			margin-bottom:.5%;

		}

		.centered{
			margin-left:auto;
			margin-right:auto;
			float:none;
		}

		.one{
			width:7.333%;
		}

		.two{
			width:15.666%;
		}

		.three{
			width:24%;
		}

		.four{
			width:32.333%;
		}

		.five{
			width: 40.666%
		}

		.six{
			width:49%;
		}

		.seven{
			width:57.333%;
		}


		.eight{
			width:65.666%;
		}

		.nine{
			width:74%;
		}

		.ten{
			width:82.333%;
		}

		.eleven{
			width:90.666%;
		}

		.twelve{
			width:99%;
		}
	</style>
</head>

<body>

	<div id="container"> 
		<div class="row">
			<div class="col twelve"> </div>
		</div>

		<div class="row">
			<div class="col one"> </div>
			<div class="col eleven"> </div>
		</div>

		<div class="row">
			<div class="col two"> </div>
			<div class="col ten"> </div>
		</div>

		<div class="row">
			<div class="col three"> </div>
			<div class="col nine"> </div>
		</div>


		<div class="row">
			<div class="col four"> </div>
			<div class="col eight"> </div>
		</div>

		<div class="row">
			<div class="col five"> </div>
			<div class="col seven"> </div>
		</div>

		<div class="row">
			<div class="col six"> </div>
			<div class="col six"> </div>
		</div>

		<div class="row">
			<div class="col seven"> </div>
			<div class="col five"> </div>
		</div>

		<div class="row">
			<div class="col eight"> </div>
			<div class="col four"> </div>
		</div>

		<div class="row">
			<div class="col nine"> </div>
			<div class="col three"> </div>
		</div>		

		<div class="row">
			<div class="col ten"> </div>
			<div class="col two"> </div>
		</div>
		<div class="row">
			<div class="col eleven"> </div>
			<div class="col one"> </div>
		</div>

		<div class="row">
			<div class="col twelve"> </div>
		</div>
	</div>
</body>


</html>
```
