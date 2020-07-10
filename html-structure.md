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
        + note: width and height are style elements and should be handled by CSS.

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
        + `<figcaption>` should be the first or last thing within the figure.  Elaborate alt tag that describes the image.  Important for screen readers.
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

+ Begin your code by telling the browser what type of document it is. 
    + HTML5 would be `<!DOCTYPE html>` *This should be the first line of code before the opening* `<html>` *tag*.
+ `<!-- -->` Tag for making comments in your code that will not show up in the presentation.
+ The **id** attribute allows you to define and indentify unique elements in your code.  The **class** attribute allows you to define and indentify multiple elements that you want to act the same.
+ The `<div>` element allows you to group a set of elements together in one block-level box.  The `<span>` element is an inline equivalent that can contain a section of text or other inline elements.
+ `<iframe>` is a smaller window cut into your site that can be used to run other sites.  A few key attributes of `<iframe>` include `src`, `height` and `width`.
    + `<iframe width="200" height="200" scr="site source">` `</iframe>`
+ The `<meta>` element lives inside the `<head>` element and contains information about the page such as a description and keywords.  This information is invisible to the user but fulfill other purposes like telling search engines about your page.
+ Some characters are reserved by HTML code for specific use and cannot be typed as plain text without the browser interpreting it as code.  These are HTML **entities** and can be used with **escape characters**.
    + `<` = `&lt;` or `&#60;`
    + `&` = `&amp;` or `&#38;`
    + Lists of escape characters can easily be found online.


<br>

[Back to the mainpage](README.md)<br />
