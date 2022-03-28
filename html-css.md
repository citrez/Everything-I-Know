---
description: HTML is what it says it is, hyper text **markup** language. It is used to mark up text. You can later go in to your HTML and style it with CSS. CSS is the way to style HTML documents.
---



# HTML/CSS/ General UI

* [Font Awsome](https://fontawesome.com/)
* [picture slideshow](https://www.w3schools.com/howto/howto_js_slideshow.asp)

## Notes

### Introduction and basic tags

[https://www.w3schools.com/tags/default.asp](https://www.w3schools.com/tags/default.asp)

\<!DOCTYPE html> - this is a tag that tells the browser its html

\<html> \</html> this is the root tag of the document

\<head> \</head> this is meta data about the page but does not get redered

\<body> \</body> this actually gets rendered 

\<p> \</p> a paragraph tag

\<strong> \</strong> makes something bold

\<em> \</em> italic

\<small> \</small> make this word a bit smaller

\<h1>\<h1> - headings, they go from h1 to h6

\<ul> \</ul> unordered list. This is a wrapper for \<li>\</li> tags

\<li>\</li> list items

\<ol> \</ol> orderied list. wrapper for \<li> \</li>

\<div> \</div> division tag. Used to group documents into sections. Makes it eaasier to refer to them later. 

some elements do not have an opening and closing tag with content between them

\<br> break tag

\<hr> horizontal rule

there used to be \<hr /> making this a 'self closing' tag. But this is no longer necessary in html5.

\<img> - some tags .also need \*\*attributes\*\*. In img tags the attribute src is needed to tell the image tag where to look. The path is relative to where the document in (the index.html) i.e if it is in a folder called img then scr = 'img/image.png'. alt attribute is a description of it for accesabilty.

\<a> \</a> anchor tag. These have href attributes. anchor tags redirect you to other pages. The href tells you where to go. You can link to other html pages in your directory.

\<blockquote> \</blockquote> these link quotes from other sources. It has a cite attribute which tells you where the quote comes from. 

you can use the style attribute in paragraphs for example. 

\<!- - This is how you comment things in HTML you can use cmd + / shortcut  - ->

### HTML webform

Webform are used to capture user information. Link username and passwords. sighn up form. feedback form. Form to search for properties. Anytime we need data from the user. forms are made up of differenet input fields. 

\<form> \</form> action attributes are not for now. 

\<input> is a single tag. The attribute type is the type of data we expect from the user type = "text" is commonly used. id attributes have to be unique.

\<label> \</label> this is used in conjuction with \<input>. There is a for attribute, which you put the id of the input tag you want to link it to. 

Radio button is another type of input

dropdown boxs are also a thing

\<textarea> \</textarea> this is just a querk that this isnt a form, maybe it should be. \
There are name, id, cols, rows, placeholder and other attributes. You can also make a label for textareas.

You can add required attribute to input tags. You just need to add required it defaults the attribute to required =true



## CSS

HTML is for structuring content on a webpage, css is for styling it, making it look more presentable. CSS selectors are the things we actually want to target on a webpage. after the selectors, inside the curly braces there are the decloation, these are properly value pairs, such as color : red;



You can add css directly to an html page as style attributes in tags. You can also do it as a \<style> \</style> tag in the head of the document. The better way to do it is using external style sheets. The style tags need to be in the of every page you want the styling in. That is why you might use an external style sheet instead. 



\<link> is used to link style sheets to HTML pages. rel attribute means relation. rel = 'stylesheet' is standard. href attribute is the path relative to the document. Link is put in the \<head>,\</head> tags

### Common CSS declorations

\<p> \</p>

color - control the text color\
background-color\
font-size - given in px, rem etc\
text-decoration - for underlining, strikethrough or none to get rid of stuff\
font-family \
text align - left, right, center\
line-height - width between lines\
letter-spacing - space between letters\
column-count - how many columns you want\
column-gap - the size of gap between columns



border-width\
border-style - solid, dashed etc\
border-color\
or shorthand...\
border : 4px solid crimson\
you can also control the left right bottom top directly\
border-bottom : 4px dotted crimson

\<li> \</li>

list-style-type - this is the lift item dot. By default it is disc, but can be changed to square or none.\
text-shadow : 2px 2px lightgray this is the horizontal, vertical and color of the shadow. 

### Inline element vrs block elements

Inline elements line up againsts each other is the browser and dont take up any more space than thye acually need. examples include \<span> \<img> \<strong> \<em> \<a> and more...\
They will sit next to each other on the page until they run out of room.

Block level elements take up the whole width of the page and do not sit side by side they start on a new line. Examples include \<p> div,h1, h2, h3, ul, li and more..

You typically see inline elements nested inside of block level elements, but you should not see block level elements nested inside of inline elements.

Inline / block elements are controlled by the display property, and different tags have different defaults, but this can be controlled and overridden.

Margin, border, padding. For div elements Margin gets applied all around, for inline, margin only gets applied at the sides.

Inline-block is a mesh of the two. The sit next to each other in the page, and dont take up the whole width. But the margin works like block level margin.  

Margin collpse exists. 

Default browser styles. They are just default styles applied by the browser, like \<a> \</a> tags are purple and underlined. A user agent style sheet. You can see these defaults in chrome developer tools. 

### CSS selectors are important to know about

url="https://www.w3schools.com/cssref/css_selectors.asp"

### Cascading

html elements can inherit css properties that are applied to their parents. 

but not all properties are inheritted things like margin, background are not enherted by childern and grandpadred etc. Things like fonts, text styles, colors etc that are inherited. 



Imagine as a child of a parent we want to inheerit something that isnt automatically enherited (color and fonts are). we can just use\
border: inherit\
margin: inherit\
this will look at the parents and inherit from them.\
You can override inheritnce by just picking a value. More specific seletors override less specific ones. 

CSS works from top to bottom, so when there is a conflict, it is the one that is further down that takes precidence. div p {} is a more specific selector than p {}

### HTML semantic tags

This can make our code more descriptive. Helps the browser know what he page is all about.

\<main> \</main> for the mian content of the page, unique to that page. It wont inlcude navigation, since that is on all webpages.

\<section> \</section> unique section of a page. blog list, contact info

\<article> \</article> 

\<header> \</header> not to be confused with head. Title, logo navigation, things on everything



### Position

static is the default, just where it is meant to be

**relative** is relative to where it is meant to be use when position: relative use left: 20px or bottom: 20px  to move it around

**fixed** is positioning elemts relative to the view port. That meants that it will stay there even when we scroll. 

**Absoloute** positioning possitions the element relative to the parent element that has not been given a position of static

**sticky** is a mixture of static and fixed. Its static to begin with and then becomes fixed when the scroll posiition reaches a certain point. 



Where you use position relative, the space where the element was stays there, 

Where you position absoloutely, it does not retain the space, you take it out of doucment flow and it is eaten up by the space beneath it



### Pseudo Classes/ Pseudo Elemenets

This lets us select elements when they are in a particular states. e.g we are hovering over them  or when a form is in focus. You just add the psudeo class :hover to the end of the CSS selector to select it in its hovered state. 



nav li:hover{\
border: 2px solid red;\
}

:focus psudeo class to style when a form is in focus. 

:valid to style when a form is valid. Think: going green when it is valid.

url="https://www.w3schools.com/css/css_pseudo_elements.asp"



Psudeo elemts are picking things like the first line in a paragraph. \
I styles specific parts of an element.

::first-line .notice, 2 colons. 

::after

### Responsive Desiegn

How your desiegn looks on different screens of different dimensions. 

media queries style things differently at different widths.

viewport meta tag tells the browser what width the view port should be. 



**Dont forget **all HTML elemets can be thought of as boxs. This is known and the [box model](https://www.w3schools.com/css/css_boxmodel.asp). 

### Links

* [Incredible gamification of learning about CSS selectors](https://flukeout.github.io) 
* [w3schools](https://www.w3schools.com/html/) - great reference
