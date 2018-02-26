### Image Gallery

---

Imagine a page with the following structure. You'll see that multiple classes are used to ensure more uniform margins amongst a set of image thumbnails, underneath a large hero image.

```
<!DOCTYPE html>
<html>
<head>
    <title></title>
    <style>
        img {width:100%;}
        #container {width:800px; height:1000px;margin-left:auto; margin-right:auto;background-color:lavender;}
        .storyboard-div {width:185px;float:left;}
        .left{margin-right:10px;}
        .right{margin-left:10px;}
        .middle{margin-left:10px; margin-right:10px;}
        #hero-div{width:100%;}
    </style>

    <script src="https://code.jquery.com/jquery-latest.js"></script>
    <script src="https://code.jquery.com/color/jquery.color-git.js"></script>
    <script src="http://gsgd.co.uk/sandbox/jquery/easing/jquery.easing.1.3.js"></script>
</head>
<body>
    <div id="container">
        <div id="hero-div">
            <img id="hero-image" src="1.jpeg">
        </div>


        <div class="storyboard-div left"> 
            <img class="storyboard-image"  src="1.jpeg">
        </div>

        <div class="storyboard-div middle"> 
            <img class="storyboard-image" src="2.jpeg">
        </div>

        <div class="storyboard-div middle"> 
            <img class="storyboard-image" src="3.jpeg">
        </div>

        <div class="storyboard-div right"> 
            <img class="storyboard-image" src="4.jpeg">
        </div>
    </div>


    <script>
        
    </script>
</body>
</html>
```

Within the script, we can make all of the individual image thumbnails clickable. When the user clicks on one of the thumbnails, a chain of animations fades the hero image out, swaps its `src` attribute, and fades it back in.

```
	//when something with .storyboard-image class is clicked
    $(".storyboard-image").click(function(){
        //store the path to the image that was clicked
        var image = $(this).attr("src");
        //make the hero image invisible
        $("#hero-image").animate({"opacity":0}, 1500, function(){
        	//switch the hero image source path
        	$("#hero-image").attr('src', image);});
        //make the hero image visible again! 
        $("#hero-image").animate({"opacity":1}, 1500 );
    });
```

-----

Let's leave these structures behind and prepare for our [midterm presentation](homework.md).
