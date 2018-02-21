### Hovering

---

Rememeber from last week that [capturing clicks](../week4/clicks.md) was easy. Let's capture more subtle user mouse behavior as well.

The structure for handling hovering is straightforward, almost like two animation blocks joined together.

```
    $("#thing-looking-for-hovering").hover(function(){
            //what should happen when the mouse hovers over this object
        },
        function(){
            //what should happen when the mouse leaves this object
        }
    );
```

Note that the brace + parenthesis combo here is a bit different logically than what we've seen before, though it's ultimately the same result.

As an example: imagine that, when an image is hovered over, we want a separate div to show dynamic information about that image.

```js
    //look for something with an id of 'heroImage'. When it is hovered over...
    $("#heroImage").hover(function(){
        //look for something with an ID of 'moreInfo' and change its internal text
    	$("#moreInfo").text("Hello World!")
    },
    //on stop hovering
    function(){
		$("#moreInfo").text("...")
	}
    );
    
```

Hover events, like [all events](https://www.w3schools.com/jquery/jquery_events.asp) allow us to design experiences that are engaging and have personality. With the addition of a [small library](https://github.com/benmajor/jQuery-Touch-Events) multitouch events can also be handled separately.

-----

Let's add to our HTML drawing repertoire by diving a bit into [Scalable Vector Graphics](svg_basics.md).