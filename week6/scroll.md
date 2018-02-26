### Animating Based on Scroll Position

---

One of the most common contemporary web design trends is to execute specific behaviors or animate based on the user's scroll position on the page. JQuery provides easy access to how many pixels the used has scrolled with the `.scrollTop()` method. When called on its own, it returns the pixels that the user has scrolled. It also can be used with a value to animate the browser auto-scrolling.

Let's look at the latter behavior first: auto-scrolling the page. Let's set our page to this structure (note how easy it is to set a [CSS background gradient](https://www.w3schools.com/css/css3_gradients.asp)!). There is a tall container div, with a fixed button inside of it. Fixed elements and auto-scrolling go well together! 


```html
<!DOCTYPE html>
<html>
<head>
	<title>Scroll Animation</title>
	<style type="text/css">
		#container {height:5000px; background: linear-gradient(magenta, blue);}
		#button {background-color: lavender; height:100px; width:100px; position:fixed;} 
	</style>

	<script src="https://code.jquery.com/jquery-latest.js"></script>
	<script src="https://code.jquery.com/color/jquery.color-git.js"></script>
	<script src="http://gsgd.co.uk/sandbox/jquery/easing/jquery.easing.1.3.js"></script>

</head>

<body>
	<div id="container">
		<div id="button">
		</div>
	</div>


	<script>

	</script>
</body>
</html>

```

Within that latter script, we can easily animate the scroll position of the page when a user clicks on the button using the same animation pattern we've been using for everything else.

```js
$(document).ready(function(){
	//look for something called id 'button' and make it clickable
    $("#button").click(function(){
      
        //change the body and html elements of the page to have a top position
        //within the browser of 1000, over 6 seconds. 
        $('html,body').animate({scrollTop:1000}, 6000);
   
    });
});
```

Both `<body>` and `<html>` are animated to account for different browser quirks. Now you can *scrolljack*, control the user's scrolling behavior! 

More usefully, perhaps, is to animate other elements based on the user's scrolling. Here, we listen for the *scroll* event, and then animate an element based on it. This is more complicated, as we need to keep track of the user's position with a `counter` variable, so that animations don't fire repeatedly. The `scroll` event occurs whenever the user even slightly adjust the page position, so we need to make sure pointless animations don't stack up. Read more about this, and see other options, [here](https://howchoo.com/g/yjfjmty1zjb/how-to-animate-scroll-in-jquery).

```js
$(document).ready(function(){

	//variable to keep track of the user's position
	var counter = 0;

	//do something when the user scrolls
	$(window).scroll(function() {
		//store the user's scroll position in a variable
		var height = $(document).scrollTop();

		//the user has scrolled a bit down the page
		if(height >= 400 && counter == 0) {
			//change the background color of the button
			$("#button").animate({"background-color":"white"}, 500);
			//this animation has now fired, and shouldn't fire until some other animation fires
			counter = 1;
		}
		
		if (height < 399 && counter == 1) {
			//change the background color of the button
			$("#button").animate({"background-color":"lavender"}, 500);
			//this animation has now fired, and shouldn't fire until some other animation fires
			counter = 0;

		}
	});
});
```

-----

Let's add to our HTML drawing repertoire by diving a bit into [Scalable Vector Graphics](svg_basics.md).