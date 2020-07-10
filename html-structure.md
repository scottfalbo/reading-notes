# Scott's Reading Notes

### Structure web pages with HTML

#### Process and Design
*Chapter 18*

+ Understand your target audience.  Why would they visit your site, what information do they want/need and how often the will revisit.
+ Creating a **site map** lets you plan the over all structure of the site.
+ A **wireframe**, or rough site sketch, is used to organize the layout and content of each page.
+ Design is about communication.  Visual hierarchy helps visitors understand the information on the site.
    + Size, color and style are all ways to differentiate between information or sections and groups of information.

#### Structure
*Chapter 1*

+ HTML pages are text documents that use tags to give information.
+ **Tags** are often refered to as **elements** and usually come in pairs of opening and closing. `<html></html>` or `<p></p>` are examples of open and closing tags.
+ Opening tags can carry attributes which can affect how the element will appear in the browser.
    + `<img src="imagename.png" alt="alt text" width="200">`
    + In the above line of code *alt* and *width* are both **attributes** of the `<img src>` **element** or **tag** and the information contained within each is a **value**.

#### HTML 5 Layout
*Chapter 17*

+ HTML5 elements indicate the purpose of the different parts of a page and helps describe it's structure.  These elements provide clearer code than using multiple `<div>` elements. 
+ These descriptive tags are refered to as Semantic Elements.  Semantic elements clearly describe their meanings to both the browser and developer.
+ Further more semantic elements are used by access tools in browsers to assist impared users.
+ Semantic elements include:
    + `<header>`
    + `<footer>`
    + `<main>`
    + `<article>`
    + `<aside>`
    + `<nav>`
    + `<section>`
    + `<figure>`
        + `<figcaption>`
    + `<details>`
    + `<mark>`
    + `<summary>`
    + `<time>`

Older browsers do not understand HTML5 elements and need to be told which elements are block-level elements.

**CSS**
```
header, section, footer, aside, nav, article, figure, figcaption {display: block;}
```
**HTML**
```
<!--[if lt IE 9]>
    <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js></script>
<![end if]-->
```

*For HTML5 work in IE 8 extra java script is needed.*

#### Extra Markup
*Chapter 8*

+ 
+ 
+ 

<br>

[Back to the mainpage](README.md)<br />
[Growth Mindset](growth-mindset.md)<br />
[Markdown Notes](markdown-notes.md)<br />
[Coder's Computer](coders-computer.md)<br>
[Revisions and the Cloud](revisions-cloud.md)<br>
*HTML Structure* 

<!--- 
Vocabulary

HTML / Markup:

Semantics:


Personas:

Meta:

Content:


Structure vs Presentation:
--->