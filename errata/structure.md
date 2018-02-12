### Base Page Structure

---

[Our topic this week](readme.md) is interactivity, but first we will need to construct the html structure of our page with spaces for...

- Project Title
- Subtitle
- Video
- Storyboard Gallery
- Some Images
- Interactive Fun!

To produce this, our grid system has been implemented as follows.

Note that the grid system css rules have been linked as an external file, just like the css reset rules. A final css file will be included, `style.css`, which will contain general typography and layout rules for the page.

```html
<html>
<head>
	<title>Digital Media Project</title>
	
	<link href="css/reset.css" rel="stylesheet">
	<link href="css/grid.css" rel="stylesheet">
	<link href="css/style.css" rel="stylesheet">
	<style>

		/*Room for Page Specific Styles*/
		
	</style>

</head>

<body>

	<div id="container"> 
		<div class="row">
			<div class="col twelve aqua-title"> 
				Future Aquatic Life
			</div>
		</div>
		
		<div class="row">
			<div class="col six">Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Phasellus et risus sed urna elementum dictum. Vestibulum finibus augue gravida, vulputate felis ut, varius tellus. Curabitur finibus tellus vel velit iaculis, at accumsan ligula sollicitudin. Sed luctus dignissim dui sed gravida. Donec iaculis ut ante sit amet aliquam. Etiam rhoncus lacinia felis ut cursus. Ut aliquet, libero porta pharetra rhoncus, velit nibh rutrum justo, ac aliquam libero nibh at libero. Phasellus ullamcorper elit ut felis aliquam, vitae ultrices nunc vehicula. Sed pretium dolor vel aliquet viverra. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In quis tempor diam, eget rhoncus leo. Sed tincidunt, purus in tincidunt sodales, sapien tellus consectetur dolor, sed dignissim dui dolor in sem.</div>
			
			<div class="col six"><img style="width:100%" src="assets/pufferfish.jpg" /></div>
		</div>
		
		<div class="row">
			<div class="col four aqua-subtitle" id="jellyfish"> 
				There will be more jellyfish. 
			</div>
			<div class="col four aqua-subtitle" id="turtle"> 
				There will be fewer turtles.
			</div>
			<div class="col four aqua-subtitle" id="ice"> 
				There will less ice too!
			</div>
		</div>

		<div class="row">
			<hr />
		</div>

		<div class="row">
			Video Here!
		</div>

		<div class="row">
			<hr />
		</div>

		<div class="row">
			<div class="col eight">
				System Diagram Here!
			</div>
			<div class="col four" id="more-info">
				"The major parts of the platform..."
			</div>
		</div>
		
		<div class="row">
			<hr />
		</div>

		<div class="row">
			<div class="col twelve" id="hero-image-container"><img id="hero-image" src="assets/sb/1.png"/></div>
		</div>

		<div class="row">
			<div class="col three"><img class="storyboard-image" src="assets/sb/1.png"/></div>
			<div class="col three"><img class="storyboard-image" src="assets/sb/2.png"/></div>
			<div class="col three"><img class="storyboard-image" src="assets/sb/3.png"/></div>
			<div class="col three"><img class="storyboard-image" src="assets/sb/4.png"/></div>
		</div>

		<div class="row">
			<div class="col three"><img class="storyboard-image" src="assets/sb/5.png"/></div>
			<div class="col three"><img class="storyboard-image" src="assets/sb/6.png"/></div>
			<div class="col three"><img class="storyboard-image" src="assets/sb/7.png"/></div>
			<div class="col three"><img class="storyboard-image" src="assets/sb/8.png"/></div>
		</div>
	</div>
</body>
</html>
  ```

Now, let's make sure we satisfy the [appropriate dependencies](includes.md).
