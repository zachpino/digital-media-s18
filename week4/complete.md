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
            width:100%;
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
            min-height:50px;
            margin-left:.5%;
            margin-right:.5%;
            margin-top:.5%;
            margin-bottom:.5%;
            overflow:scroll;
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


/*Standard Mobile Style: Half or Full Widths*/
 @media only screen 
 and (min-width : 320px) 
 and (max-width : 479px) {
      #container {background-color:#edd;}
      .one { display:none; }
      .two { display:none; }
      .three { display:none }
      .four { display:none}
      .five { display:none }
      .six { width:49%; }
      .seven { width:99%; }
      .eight { width:99%; }
      .nine { width:99%; }
      .ten { width:99%; }
      .eleven { width:99%; }
      .twelve { width:99%; }
  }

/*Large Mobile Styles: Full, Half, Third Widths*/
@media only screen 
 and (min-width : 480px) 
 and (max-width : 767px) {
      #container {background-color:#eed;}
      .one { display:none; }
      .two { display:none; }
      .three { display:none }
      .four { width:32.333%}
      .five { width:49% }
      .six { width:49%; }
      .seven { width:49%; }
      .eight { width:65.666%; }
      .nine { width:99%; }
      .ten { width:99%; }
      .eleven { width:99%; }
      .twelve { width:99%; }
  }


/*Tablets: Full, Half, Third, Quarter Widths*/
 @media only screen 
 and (min-width : 768px) 
 and (max-width : 1023px) {
       #container {background-color:#ded;}
      .one { width:24%; }
      .two { width:24%; }
      .three { width:24%; }
      .four { width:32.333%; }
      .five { width:49% }
      .six { width:49%; }
      .seven { width:49%; }
      .eight { width:65.666%; }
      .nine { width:74%; }
      .ten { width:74%; }
      .eleven { width:74%; }
      .twelve { width:99%; }
  }

  /* Laptops: All 12 Widths */
 @media only screen 
 and (min-width : 1024px) 
 and (max-width : 1223px) {
       #container {background-color:#dee;}
      .one { width:15.666%; }
      .two { width:15.666%; }
      .three { width:24% }
      .four { width:32.333%}
      .five { width:40.666% }
      .six { width:49%; }
      .seven { width:57.333%; }
      .eight { width:65.666%; }
      .nine { width:74%; }
      .ten { width:82.333%; }
      .eleven { width:82.333%; }
      .twelve { width:99%; }
  }

/*Desktop: All 12 Widths*/
@media only screen and (min-width : 1224px) {

          #container{ 
              width:1224px;
              background-color:#dde;
          }
      }

</style>
</head>

<body>

    <div id="container"> 
        <div class="row">
            <div class="col twelve"> </div>
        </div>

        <div class="row">
            <div class="col one"></div>
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
            <div class="col six centered"> </div>
        </div>
    </div>
</body>
</html>
```
