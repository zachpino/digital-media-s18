### Animating

---

And finally, arbitary CSS animations. Read more about the super flexible animation tools that JQuery gives interaction designers on the [JQuery animation reference](http://api.jquery.com/animate/).

JQuery handles animation by manipulating CSS properties smoothly over time. 

The structure looks like this:

```js        

$("thing-to-animate").animate({"css-property" : "ending-value"}, duration-in-ms, "easing-name" );

```

That last bit, easing, is a concept unique to animation *how should the object animate with respect to time*. It is optional in JQuery, though provides so much expressability to interaction designers. You could think about it as an acceleration parameter. Read more and [view the possible variations and settings here](http://gsgd.co.uk/sandbox/jquery/easing/).

Here, the `margin-left` property of an element is incremented over 1.5 seconds (all time in Javascript is notated in milliseconds). The object will bounce at the end of its motion due to its easing settings.

```js

	//look for something called id 'animate' and make it clickable
    $("#animate").click(function(){
      
        //look for an item called 'boxy' on the page and animate it moving 
        $("#boxy").animate({"margin-left":"+=100px"}, 1500, "easeOutBounce" );
   
    });

```

Many properties can be simultaneously animated...

```js
	//look for something called id 'animate' and make it clickable
    $("#animate").click(function(){
        //look for an item called 'boxy' on the page and animate many properties
        $("#boxy").animate(
        	{
        		"opacity":.6,
        		"margin-left": "+=50px",
        		"height": "300px",
        		"border": "3px solid green",
        		"background-color" : "#f0f" 
        	}, 1500 //duration of 1.5 seconds, no special easing
        )
    });

```

And we can run custom code when the animation finishes. This is called a *callback* function

```js
//look for something called id 'animate' and make it clickable
    $("#animate").click(function(){
        //look for an item called 'boxy' on the page and make it disappear
        $("#boxy").animate({"opacity":0}, 1500, 
        	function(){
        		alert('boxy is gone!');
        	}
        );
    });    

```

We also can sequence animation by duplicating the `.animate` *block* of code.

```js
	//look for something called id 'animate' and make it clickable
    $("#animate").click(function(){
      
        //look for an item called 'boxy' on the page and animate it moving to the right
        $("#boxy").animate({"margin-left":"300px"}, 1500 );
	
	//look for an item called 'boxy' on the page and animate it moving down the page
        $("#boxy").animate({"margin-top":"600px"}, 1200, easeOutBounce );

        //look for an item called 'boxy' on the page and animate it moving to the left
        $("#boxy").animate({"margin-left":"0px"}, 1500 );
	
	//look for an item called 'boxy' on the page and animate it moving to the left
        $("#boxy").animate({"margin-top":"0px"}, 1800, easeInQuad );

   
    });

```

And many elements can move simultaneously.

```js
	//look for something called id 'animate' and make it clickable
    $("#animate").click(function(){
      
        //look for an item called 'boxy' on the page and animate it moving to the right
        $("#boxy").animate({"margin-left":"300px"}, 1500, easeInBounce );
	
	//look for an item called 'boxy2' on the page and animate it moving to the right
        $("#boxy2").animate({"margin-left":"300px"}, 1500, easeOutBounce );
	
    });

```

As a time-saving utility, JQuery offers the ability to use relative values in animation calls. We can use `+=` and `-=` to move an element on the page from where it currently is a certain amount. In other words, the motion is *relative to the current position rather than absolute to its parent*. This saves time, and also allows the animation button to be pressed many times for repeated animation.

```js
	//look for something called id 'animate' and make it clickable
    $("#animate").click(function(){
      
        //look for an item called 'boxy' on the page and animate it 
	//moving rightwards from wherever it is and slowly becoming transparent
	
        $("#boxy").animate({"margin-left": "+=50", "opacity":"-=.1"}, 1500 );

   
    });

```

-----

Let's [try this code out to develop personality in pixels](homework.md)!  
