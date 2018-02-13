### Capturing Clicks!

-----

Let's do something when our user clicks [using JQuery](jquery.md)! 

Add a `<script>` tag at the bottom of your `<body`.

```html
<script>
//do things when the page has finished loading
$(document).ready(function(){
   	
   	//look for something with an ID of 'jellyfish', and when it is clicked on... 
    $("#jellyfish").click(function(){
    	//add an emoji jellyfish as a child
        $("#jellyfish").append( "<i class='em em-octopus'></i>");
    });
   	
   	//look for something with an ID of 'turtle', and when it is clicked on... 
    $("#turtle").click(function(){
    	//remove a child object
        $(".em-turtle").last().remove();
    });

    //look for something with an ID of 'turtle', and when it is clicked on... 
    $("#heroImage").click(function(){
      //switch image source attribute
      $("#heroImage").attr('src','image2.png')
    });
    
});

</script>
```

JQuery always follows this convention. We search for something on the page `$(element, id, or class name)`, and assign a *handler* to it. In this case, we're telling these identified elements to listen for a `click` event. There are [many other events](https://www.w3schools.com/jquery/jquery_events.asp) that we can respond to as well!  

When a click is detected on that element, the associated code, wrapped in a `function` is executed. Here, we are simply adding or removing elements in the first two examples. The third example changes the `src` attribute of the selected image, switching the image to a different file.

-----

Now, let's learn how we can [trigger an animation with a click event](animate.md).
