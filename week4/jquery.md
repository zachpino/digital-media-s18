### JQuery

---

[JQuery](http://jquery.com) is a javascript library -- a set of functions that we can freely use that makes writing a complex and inconsistent language like Javascript easier. It is implemented by a huge percentage of the internet, at least [71% as of February, 2017](https://w3techs.com/technologies/details/js-jquery/all/all). JQuery is designed specifically to help create interactive and animated web experiences.

Let's bring JQuery into our website. Within the `<head>` of your page, include the following...

```js
<script src="https://code.jquery.com/jquery-latest.js"></script>
<script src="https://code.jquery.com/color/jquery.color-git.js"></script>
<script src="http://gsgd.co.uk/sandbox/jquery/easing/jquery.easing.1.3.js"></script>
```

This brings in the JQuery library itself, as well as two modules for it to help handle color and motion better.

You don't need JQuery, it just makes lots of things simpler and more convenient. There are also alternative Javascript libraries worth exploring that have different focuses.

- [D3](http://d3js.org) for Data Visualization
- [AngularJS](https://angularjs.org) and [React](https://facebook.github.io/react/) for Web Apps
- [Paper.js](http://paperjs.org) and [Raphael](http://dmitrybaranovskiy.github.io/raphael/) for Diagramming
- [MooTools](https://mootools.net) for Complex Interactions

-----

Now, let's deploy JQuery to find out what a user [clicks](clicks.md) on.
