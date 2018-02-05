### Images and Videos

---
A reminder on how to include images in HTML...

```
<img src="path/name.jpg" alt="description" title="tooltip"/>
```

Note again, a self-closing tag. All we need to do is specify a path and filename and the image can be dropped into any other tag on your website.

Adding a `title` is optional -- it will show up if a user hovers over the image with their mouse pointer.

Videos are [included similarly](https://www.w3schools.com/html/html5_video.asp
).

```
<video width="320" height="240" autoplay>
  <source src="movie.mp4" type="video/mp4">
	This is a video of some content. Your browser does not support the video tag.
</video>
```

The "Your browser..." bit shows up if the video fails to load. Check out [Mazwai](http://mazwai.com) and [Coverr](https://coverr.co) for mp4 content!

---
#### A very important note!

`<img>` should *always* include an `alt=""` attribute. This attribute is an opportunity to embed a short textual description in the image for two primary audiences.

1. Any user accessing your website using assistive technologies such as screen readers or switch controls. We want to design our website to be responsive to the needs of all of our users, it's an important part of contemporary responsive design practice!
2. Google robots behave very similarly to screen readers. If there are not `alt` attributes for your content, Google's robots have no idea what the content of the images are and accordingly cannot include that content in your ranking.  

The text within the `<video>` tag serves the same purpose.

---

`<img>` tags behave similarly to inline elements. They flow like text if place within text, but they can have width and height values associated in CSS like block elements. For this reason, they are called *inline-block* elements, as they mix the behavior of both.

By default `<img>` elements will display at their native size. Assign a classname, id, or do some inline sizing to set their size. Note that setting both `height` and `width` will allow you to change the aspect ratio of the image.

To center a nested image in a parent container, our CSS might look like this. Note that we ask the browser to treat the image like a block level element for positioning purposes.

```
img.heroImage {
  width:75%;
  display:block;
  margin-left:auto;
  margin-right:auto;
}
```

There are some new, fun CSS properties that allow the coded manipulation of image content, all passed through the `filter` property. [Try them out](http://www.w3schools.com/cssref/css3_pr_filter.asp).

```
img.heroImage {
filter: blur(15px);
filter: contrast(150%);
filter: hue-rotate(90deg);
}
```

-----

In addition, CSS allows the use of the `background-image` property to have images or gradients, in addition to `background-color`, to fill up any container behind any text. [Check out the reference](https://www.w3schools.com/cssref/pr_background-image.asp) for more information and options.


```
body {
   background-image: url("sample.png");
   background-color: #cccccc;
}
```


We can now advance to more formal layout systems, but let's begin with [resetting default css styles](reset.md).
