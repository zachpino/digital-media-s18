### Hovering

[Clicks](clicks.md) were easy. Let's do some hovering too!

```js
    $("#system-ul").hover(function(){
    	$("#more-info").text("Part 1 of my system")
    },
    function(){
		$("#more-info").text("The major parts of the platform...")
	}	
    );

    $("#system-um").hover(function(){
    	$("#more-info").text("Part 2 of my system")
    },
    function(){
		$("#more-info").text("The major parts of the platform...")
	}	
    );

    $("#system-ur").hover(function(){
    	$("#more-info").text("Part 3 of my system")
    },
    function(){
		$("#more-info").text("The major parts of the platform...")
}	
    );
```

And finally, some generalized [animation](animate.md)!
