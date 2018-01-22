###Animating

And finally, arbitary CSS animations.

```
    $(".storyboard-image").click(function(){
        var image = $(this).attr("src");
           
        $("#hero-image").animate({"opacity":0}, 1500, function(){$("#hero-image").attr('src', image);});

        $("#hero-image").animate({"opacity":1}, 1500 );
    });
```
