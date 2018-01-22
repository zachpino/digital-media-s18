###Small Improvements

---

The 12 column grid system we have built out works well, but there are some small tweaks we can make to handle our content more seamlessly.

Returning to our simple gridsystem example, with the CSS compressed a bit. Make sure you have a `reset.css` in the same folder as this file.

```
<html>
<head>
    <title>Grid System</title>

    <link href="reset.css" rel="stylesheet">

    <style>
        html {
            box-sizing: border-box;
        }

        *, *:before, *:after {
            box-sizing: inherit;
        }

        #container{
            width:80%;
            margin-left: auto;
            margin-right: auto;
        }

        .row::after {
            content: "";
            clear: both;
            display: table;
        }

        .col{
            background-color: lightgray;            
            float:left;
            height:50px;
            margin-left:.5%;
            margin-right:.5%;
            margin-top:.5%;
            margin-bottom:.5%;
        }

        .centered{
            margin-left:auto;
            margin-right:auto;
            float:none;
        }

        .one{ width:7.333%; }
        .two{ width:15.666%; }
        .three{ width:24%; }
        .four{ width:32.333%; }
        .five{ width:40.666% }
        .six{ width:49%; }
        .seven{ width:57.333%; }
        .eight{ width:65.666%; }
        .nine{ width:74%; }
        .ten{ width:82.333%; }
        .eleven{ width:90.666%; }
        .twelve{ width:99%; }

    </style>
</head>

<body>

    <div id="container"> 
        <div class="row">
            <div class="col twelve"> </div>
        </div>

        <div class="row">
            <div class="col one"> </div>
            <div class="col eleven"> </div>
        </div>

        <div class="row">
            <div class="col two"> </div>
            <div class="col ten"> </div>
        </div>

        <div class="row">
            <div class="col three"> </div>
            <div class="col nine"> </div>
        </div>


        <div class="row">
            <div class="col four"> </div>
            <div class="col eight"> </div>
        </div>

        <div class="row">
            <div class="col five"> </div>
            <div class="col seven"> </div>
        </div>

        <div class="row">
            <div class="col six"> </div>
            <div class="col six"> </div>
        </div>

        <div class="row">
            <div class="col seven"> </div>
            <div class="col five"> </div>
        </div>

        <div class="row">
            <div class="col eight"> </div>
            <div class="col four"> </div>
        </div>

        <div class="row">
            <div class="col nine"> </div>
            <div class="col three"> </div>
        </div>      

        <div class="row">
            <div class="col ten"> </div>
            <div class="col two"> </div>
        </div>
        <div class="row">
            <div class="col eleven"> </div>
            <div class="col one"> </div>
        </div>

        <div class="row">
            <div class="col twelve"> </div>
        </div>
        
        <div class="row">
            <div class="col seven centered"> </div>
        </div>
    </div>
</body>
</html>
```

This example scales fluidly on all browser sizes and devices. But, if you view the page on an iPhone for example, those `col one` divs are *very narrow*. So narrow, in fact, any amount of textual content would likely overflow them and cause all kinds of layout nightmares. You can try that by stuffing a *lorem ipsum* paragraph into a `col one` and shrinking your browser.


```
<html>
<head>
    <title>Grid System</title>

    <link href="reset.css" rel="stylesheet">

    <style>
        html {
            box-sizing: border-box;
        }

        *, *:before, *:after {
            box-sizing: inherit;
        }

        #container{
            width:80%;
            margin-left: auto;
            margin-right: auto;
        }

        .row::after {
            content: "";
            clear: both;
            display: table;
        }

        .col{
            background-color: lightgray;            
            float:left;
            height:50px;
            margin-left:.5%;
            margin-right:.5%;
            margin-top:.5%;
            margin-bottom:.5%;
        }

        .centered{
            margin-left:auto;
            margin-right:auto;
            float:none;
        }

        .one{ width:7.333%; }
        .two{ width:15.666%; }
        .three{ width:24%; }
        .four{ width:32.333%; }
        .five{ width:40.666% }
        .six{ width:49%; }
        .seven{ width:57.333%; }
        .eight{ width:65.666%; }
        .nine{ width:74%; }
        .ten{ width:82.333%; }
        .eleven{ width:90.666%; }
        .twelve{ width:99%; }

    </style>
</head>

<body>

    <div id="container"> 
        <div class="row">
            <div class="col twelve"> </div>
        </div>

        <div class="row">
            <div class="col one">
                Pasuk ke suk adt 'ninnauwaet mohtukquasemes quequeshau. Ho moocheke tohkoi.
                Peyau yean anumwussukuppe. Pumukau mehtugq waeenu kah waeenu. Teanuk waban ootshoh. Sonkquesu. Wussin, "nussonkques".
                Popomshau mehtuhq nano. Naim ushpuhquaeu kesukquieu. Wussin, "Pish muhpoo."
                Naim muhpooi. Pumukau moocheke waeenu kah waeenu anumwussukuppe. Togkodtam muhpoo manunne.
                Naim sauùnum onk tohkootaau mehtugq yeuyeu onk kussukkoueu. Koueu noadtuk. Tookshau. Muhpoo mohtupohteau. Quinnupohke ashkashki.
                Noh wahteunk mohtukquasog, wahheau nag na sohqutteahhauhaog. Nagum nont qushitteaonk. Mat queshau wutche mehtukq. Paskanontam. Yanunum wuskesukquash onk queshau wutche mehtukq.
                Tiadche petshau kenompskut. Wussissetoon kuhkukque musqueheongane. Yeuyeu nishnoh mohtukquas mahche pohki kuhkukque mussisstoon -- mahche neese kuhkukque mussisstoonash.
                Asuh ahquompak kepshont wusseettash waapemooash adt wuhhog. Yeuyeu nishnoh mohtukquas onk nishnoh mahche neese tiohquekekontash.
                Aoog adt touohkōmuk onk nok wompiyeuash dtannetuog ut anumwussukuppe nummukkiog Indiansog newutche mohtugquasemesog wussukqunnash.
                Kesteausu. 
            </div>
            <div class="col eleven"> </div>
        </div>

        <div class="row">
            <div class="col two"> </div>
            <div class="col ten"> </div>
        </div>

        <div class="row">
            <div class="col three"> </div>
            <div class="col nine"> </div>
        </div>


        <div class="row">
            <div class="col four"> </div>
            <div class="col eight"> </div>
        </div>

        <div class="row">
            <div class="col five"> </div>
            <div class="col seven"> </div>
        </div>

        <div class="row">
            <div class="col six"> </div>
            <div class="col six"> </div>
        </div>

        <div class="row">
            <div class="col seven"> </div>
            <div class="col five"> </div>
        </div>

        <div class="row">
            <div class="col eight"> </div>
            <div class="col four"> </div>
        </div>

        <div class="row">
            <div class="col nine"> </div>
            <div class="col three"> </div>
        </div>      

        <div class="row">
            <div class="col ten"> </div>
            <div class="col two"> </div>
        </div>
        <div class="row">
            <div class="col eleven"> </div>
            <div class="col one"> </div>
        </div>

        <div class="row">
            <div class="col twelve"> </div>
        </div>
        
        <div class="row">
            <div class="col seven centered"> </div>
        </div>
    </div>
</body>
</html>
```

Note the few problems we can identify. Since the `col` divs have a set `height` in the css declaration, the grid columns do not expand to match their content. Worse still, when a word is too long, it overflows its container. Let's fix that by making a change to the `.col` CSS declaration.

```
 .col{
            background-color: lightgray;            
            float:left;
            min-height:50px;
            margin-left:.5%;
            margin-right:.5%;
            margin-top:.5%;
            margin-bottom:.5%;
            overflow:scroll;
        }
```

Two changes to note. `min-height` rather than `height` allows our divs to still take up vertical space on the page even though they have no content. And, if there is long content, our divs will swell vertically to contain it like normal html elements. 

But we still have words that expand horizontally outsider their bounds. Of course, this could be solved by using `col two`, but we can also use the `overflow` property to either hide any amount of horizontally overflowing text with `overflow:hidden;` or, usually better, make it scrollable with `overflow:scroll;`.

With these tweaks in place, let's advance to [adding our first css breakpoint](breakpoints.md).
