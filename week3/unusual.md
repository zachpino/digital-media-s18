### Unusual CSS Layouts

---

The `position` CSS property unlocks lots of layout potential. [This reference page](https://www.w3schools.com/css/css_positioning.asp) lists more examples and options


##### Fixed Position

Fixed positioned objects stay exactly where you place them with `left`, `right`, `top`, and `bottom`, not reacting at all to users' scrolling.

```
<!DOCTYPE html>
<html>
<head>
<style>
div.fixed {
    position: fixed;
    top: 0;
    right: 0;
    width: 50%;
    height:100%
    text-align:center;
    background-color: #0cc;
}

div.scrollableA {
    width: 50%;
    height: 200px;
    background-color:#dfd;
}

div.scrollableB {
    width: 50%;
    height: 200px;
    background-color:#ddf;
}

</style>
</head>
<body>

<div class="scrollableA">
</div>
<div class="scrollableB">
</div>
<div class="scrollableA">
</div>
<div class="scrollableB">
</div>
<div class="scrollableA">
</div>
<div class="scrollableB">
</div>
<div class="scrollableA">
</div>
<div class="scrollableB">
</div>

<div class="fixed">
This div element is fixed.
</div>

</body>
</html>
```

##### Sticky Headers

`position: sticky` elements move like regular block or inline elements, until a certain condition is met. Then, they stay exactly where they are. Note that `sticky` also has to be set differently for `webkit` browsers like Safari. This *vendor-prefixing* is common practice for many cutting edge web technologies, until a universal standard has emerged.

```
<!DOCTYPE html>
<html>
<head>
<style>
div.sticky {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  padding: 5px;
  background-color: #fdf;
  height: 50px;
}
</style>
</head>
<body>

<p> <em>Scroll me!</em> </p>

<div class="sticky">Sticky Header</div>

<div style="padding-bottom:2000px">
  <p>
      Lorem ipsum dolor sit amet, illum definitiones no quo, maluisset concludaturque et eum, altera fabulas ut quo. Atqui causae gloriatur ius te, id agam omnis evertitur eum. Affert laboramus repudiandae nec et. Inciderint efficiantur his ad. Eum no molestiae voluptatibus.
    </p>
</div>

</body>
</html>
```

Now, let's move on to 


