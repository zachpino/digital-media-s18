### Showing Video Content

---

Showing videos on a website is very similar to showing images. We use a special tag, set some attributes, and make sure the file is in the right place.

```html
<video autoplay controls muted id="hero-vid" width="100%" src="assets/aquarium.mp4">
```

Pull down some videos from the amazing [Mazwai](http://mazwai.com) -- a sort [Unsplash](http://www.unsplash.com) for video -- is in the mp4 format which is fairly cross-compatible across modern browsers.

The `<video>` tag takes a `src` attribute, pointing it to an individual video file. It can be assigned width and/or height to specify non-native playback size (here set to 100% of its parent).

Most importantly, though, are some useful attributes that don't take values. Namely, `autoplay`, `muted`, `controls` which respectively determine whether or not the video starts playing on page load, has sound by default and show playback controls. Try your video with and without those attributes!

-----

We can also add some visual interest by introducing some [typographic bells and whistles](fonts.md). 