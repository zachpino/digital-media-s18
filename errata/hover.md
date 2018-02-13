### Hovering

---

[Clicks](clicks.md) were easy. Let's do some hovering too!

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

And finally, some generalized [animation](animate.md).
