### Homework for 3/5

---

Constructing a container for your presentation content. 

Things to include: 

- Terrain and Territory Definitions
- System Diagram
- Information about Individual Elements in the System
- Storyboard Frames
- Textual Descriptions
- Evocative Images or Videos
- First Stabs at Branding
- Some Designed Interactions/Personality

These can all be included on one page, or on multiple linked pages, depending on how you would like to present.

Code like the following will be useful for handling your storyboard frames interactively.

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
