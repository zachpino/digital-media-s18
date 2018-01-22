###Webfonts and Emoji

---

With our [CSS dependencies](includes.md) in place, get to know the amazing resource that is [Google Fonts](https://fonts.google.com). You can easily use any of the thousands of available fonts for free by clicking on the (+) icon next to a font, and then copying the code from the "@IMPORT" tab into the `<style>` section of your webpage, or a separate stylesheet.

This code, in the `<style>` tag, allows us to use the high-quality "Lato" font family.
```
@import url('https://fonts.googleapis.com/css?family=Lato');

#title{ font-family: 'Lato' }
```
Webfonts do slow down page load times, but it is often a worthwhile exchange for greater design expressiveness.

You can also download the fonts for use on your machine by clicking on the download arrow button.

In addition, we might want to use emoji on our page. Include this in the head of your page.

```
<link href="https://afeld.github.io/emoji-css/emoji.css" rel="stylesheet">
```

And then use emoji in your page like so. Use [this page](https://afeld.github.io/emoji-css/) as reference.

```
<i class="em em-octopus"></i>
```

Now, let's add a [video](video.md) to the page!
