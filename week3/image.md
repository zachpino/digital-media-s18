###Image Uploads

---

Everything has been text so far, let's add imagery. We have to leave Sublime Text behind and return to the terminal to upload an image to our server.

The SCP command allows secure file copy from your local machine to your AWS server. The syntax for SCP is similar to SSH.

```
scp -i ~/.ssh/identity_file.pem path/to/local/file ubuntu@[IP Address]:/path/to/target/directory
```

For instance, moving a file from your local desktop to your web folder on AWS looks like this.

```
scp -i ~/.ssh/proto_class.pem ~/Desktop/image.jpg ubuntu@12.345.678.999:/var/www/html/
```

Easy!

Now, to include an image in html.

```
<img src="path/name.jpg" alt="description" title="tooltip"/>
```

Note again, a self-closing tag. All we need to do is specify a path and filename and the image can be dropped into any other tag on your website.

Adding a `title` is optional -- it will show up if a user hovers over the image with their mouse pointer.

---
####A very important note!

`<img>` should *always* include an `alt=""` attribute. This attribute is an opportunity to embed a short textual description in the image for two primary audiences.

1. Any user accessing your website using assistive technologies such as screen readers or switch controls. We want to design our website to be responsive to the needs of all of our users, it's an important part of contemporary responsive design practice!
2. Google robots behave very similarly to screen readers. If there are not `alt` attributes for your content, Google's robots have no idea what the content of the images are and accordingly cannot include that content in your ranking.  

---
`<img>` behave similarly to inline elements. They flow like text if place within text, but they can have width and height values associated in CSS like block elements. For this reason, they are called *inline-block* elements, as they mix the behavior of both.

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

[Next steps and homework](nextsteps.md)
