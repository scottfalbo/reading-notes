# Jquery Pre-work
[attributes and content](#attributes-and-content)<br>
[manipulating CSS](#manipulating-css)<br>

## Overview 

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

## Attributes and Content

+ `.attr('')`JQuery can easily manipulate HTML element attributes.
  + `<form id="name"></form>` 
    + `var n = $('form').attr('id');` 
      + n = 'name'
+ JQuery can also quickly set the value of an attribute.
  + `$('form').attr('id', 'newName');`
  

+ `removeAttr()` is a method used to remove attributes.
  + `$('section').removeAttr('border');`

### Get Content

+ > There are several methods for manipulating the content of HTML elements via jQuery.
+ `html()` This method is used to get the content of an element including the HTML markup.
  + `$('p').html();`
+ `text()` This method will return only the text content without markup.
  + `$('p').text();`
+ The same methods are used to **set values** as well.
  + `$('p').text('hello');`

+ `val()` method used to get and set the value of form fields.
  + ```
    <input type="text" id="name" value="Spaceghost">

    var x = $('#name').val();
    ```
    + x = 'Spaceghost'

### Adding Content

+ Adding content without overwriting current content.
  + `append()` inserts content at the end.
  + `prepend()` inserts content at the beginning.
  + `after()` insert content after selected elements.
  + `before()` insert content before selected elements.
+ You can create a new element:
  + `var x = $('<p></p>).text('hello)`;
  + `$('#target').append(x);`
  + The above will make var x = the `<p>` element and then append it `after()` the `#target` element.

## Manipulating CSS


  

[Back to the mainpage](../README.md)