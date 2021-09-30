# JQuery

## jQuery Selectors

jQuery selectors are one of the most important parts of the jQuery library.

jQuery selectors allow you to select and manipulate HTML element(s).

jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more. It's based on the existing CSS Selectors, and in addition, it has some own custom selectors.

All selectors in jQuery start with the dollar sign and parentheses: $().

## The element Selector

The jQuery element selector selects elements based on the element name.

You can select all <p> elements on a page like this:

~~~jquery
$("p")
~~~jquery


When a user clicks on a button, all <p> elements will be hidden:

~~~jquery
$(document).ready(function(){
  $("button").click(function(){
    $("p").hide();
  });
});
~~~

### The #id Selector

The jQuery #id selector uses the id attribute of an HTML tag to find the specific element.

An id should be unique within a page, so you should use the #id selector when you want to find a single, unique element.

To find an element with a specific id, write a hash character, followed by the id of the HTML element:

~~~jquery
$("#test")
~~~

When a user clicks on a button, the element with id="test" will be hidden:

Example
~~~jquery
$(document).ready(function(){
  $("button").click(function(){
    $("#test").hide();
  });
});
~~~

### The .class Selector

The jQuery .class selector finds elements with a specific class.

To find elements with a specific class, write a period character, followed by the name of the class:

~~~jquery
$(".test")
~~~

When a user clicks on a button, the elements with class="test" will be hidden:

~~~jquery
$(document).ready(function(){
  $("button").click(function(){
    $(".test").hide();
  });
});
~~~

### More Examples of jQuery Selectors

| Syntax	| Description	| Example |
| --- | --- | --- |
| $("*")	Selects all elements	| 
| $(this)	| Selects the current HTML element	| 
| $("p.intro")	| Selects all <p> elements with class="intro"	| 
| $("p:first")	| Selects the first <p> element	| 
| $("ul li:first")	| Selects the first <li> element of the first <ul>	| 
| $("ul li:first-child")	| Selects the first <li> element of every <ul>	| 
| $("[href]")	| Selects all elements with an href attribute	| 
| $("a[target='_blank']")	| Selects all <a> elements with a target attribute value equal to "_blank"	| 
| $("a[target!='_blank']")	| Selects all <a> elements with a target attribute value NOT equal to "_blank"	| 
| $(":button")	| Selects all <button> elements and <input> elements of type="button"	| 
| $("tr:even")	| Selects all even <tr> elements	| 
| $("tr:odd")	| Selects all odd <tr> elements	| 

Use our jQuery Selector Tester to demonstrate the different selectors.

For a complete reference of all the jQuery selectors, please go to our jQuery Selectors Reference.

## Functions In a Separate File

If your website contains a lot of pages, and you want your jQuery functions to be easy to maintain, you can put your jQuery functions in a separate .js file.

When we demonstrate jQuery in this tutorial, the functions are added directly into the <head> section. However, sometimes it is preferable to place them in a separate file, like this (use the src attribute to refer to the .js file):

Example
~~~html
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script src="my_jquery_functions.js"></script>
</head>
~~~

