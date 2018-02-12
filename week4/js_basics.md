### Javascript Basics

---

All of this code goes inside of a `<script>` tag inside of a the body of an html page.

First, let's add a javascript variable and look at it.

```html
<script>
	//make a variable
	var myText = "hello world";

	//print a variable
	alert(myText);
</script>

```

This will produce a popup window saying "hello world," should the code above be saved and opened in a web browser. This is the ideal workflow — edit code in a text editor of your choice, and then preview the results by reloading it in a browser. Small difference in how browsers handle Javascript and HTML will lead to minor variations in the instructions that follow — sadly, the reality of all web programming.

First things first, all lines in Javascript terminate in a semicolon, `;`. This is the most common issue that will get in the way of new coders. Indentation and empty lines are ignored by the Javascript compiler, so use whitespace to keep code legible and intelligently structured.

Javascript, a weakly typed language, doesn't care what kind of data is saved into variables. Here, a string of text, enclosed in either double or single quotation marks, is saved into a variable called `myText`. Camel Case (all lowercase letters except for the beginning of words, no spaces or hyphens) variable names are used by convention. Note that 2 slashes makes lines into comments in Javascript. Multi line comments begin with `/*` and end with `*/`.

We could similarly save integers into variables. Note that numbers don't need quotation mark encapsulation, and all the standard arithmetic operators work as expected.

```javascript

//make a variable
var myFirstInteger = 5;
var mySecondInteger = 3;

/*
returns 8
because JS can add! 
*/

alert(myFirstInteger + mySecondInteger);

```

Be careful, because Javascript doesn't care about data types, it's easy to make mistakes.

```javascript

//make a variable
var myFirstInteger = "5";
var mySecondInteger = 3;

//returns 53
alert(myInteger + yourInteger);

```

Because Javascript is treating the first variable as the actual text `"5"` and not the counting integer `5`, it *concatenates*, or glues, the two together as a string.

Text can be concatenated together with the addition `+` operator.

```javascript

//make a variable
var myIntro = "Greetings";
var space = " ";
var myStatement = "my name is";
var myName = "Robot";

//returns "Greetings, my name is Robot"
alert(myIntro + "," + space + mystatement + space + yourInteger);

```

---

Now, with the basics out of the way, let's use a [JS library to manipulate the content on the page](jquery.md).
