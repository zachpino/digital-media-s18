### Animating

---

And finally, arbitary CSS animations. Read more about the super flexible animation tools that JQuery gives interaction designers on the [JQuery animation reference](http://api.jquery.com/animate/).

JQuery handles animation by manipulating CSS properties smoothly over time. 

The structure looks like this:

```js        

$("thing-to-animate").animate({css-property:ending-value}, duration-in-ms, easing );

```

That last bit, easing, is a concept unique to animation *how should the object animate with respect to time*. It is optional in JQuery, though provides so much expressability to interaction designers. You could think about it as an acceleration parameter. Read more and [see the possible values here](http://gsgd.co.uk/sandbox/jquery/easing/).

Here, the `left` property of an element is incremented over 1.5 seconds (all time in Javascript is notated in milliseconds). Note that `+=` is a set of characters that will take the current value, and add onto it. `-=` is similarly available. The object will bounce at the end of its motion due to its easing settings.

```js

	//look for something called id 'animate' and make it clickable
    $("#animate").click(function(){
      
        //look for an item called 'boxy' on the page and animate it moving 
        $("#boxy").animate({"left":"+=100px"}, 1500, "easeOutBounce" );
   
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
        		"left": "+=50px",
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

-----

Let's [try this code out to develop personality in pixels](homework.md)!  