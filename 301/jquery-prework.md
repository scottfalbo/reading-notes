## Jquery Pre-work

+ JQuery is a JavaScript library
+ `<script src="https://code.jquery.com/jquery-3.1.1.js"></script>`

> It is good practice to wait for the HTML document to be fully loaded.  For that we use the **ready** event of the document `object`.
+ ```
  $(document).ready(function(){
    // jquery code goes here
  });
  ```
  + The `?` is used to access JQuery...
  + then the code assess the document object...
  + and defines a function to be called the ready event fires.
+ This prevents JQuery from running before the document is finished loading.
+ Since this code is almost always used there is a shorthand:
+ ```
  $(function(){
    // code
  });
  ```

### Syntax

+ JQuery is used to select HTML elements and perform actions on them.
+ `$('selector').action()`
  + `$` accesses JQuery.
  + `('selector')` finds the HTML element.
  + `.action()` is then performed on the element.

### Selectors

+ `$('section')` selectors based on element name.
+ `$('.class')` selectors based on element `.class`.
+ `$('#id`)' selectors based on element `#id`.
+ CSS type selectors can also be used:
  + `$('div.className')` all `divs` with class `className`.
  + `$('section:first')` the `first` element of `section`.
  + `$(*)` all elements of the DOM.



[Back to the mainpage](../README.md)