# Jquery Pre-work
+ 301 installs
  + Heroku: Used to launch and deploy web servers to a cloud.
    + 7.43.0 linux-x64 node v12.16.2
  + Postgres (SQL): Relational database server.
    + psql (12.4)
    + `pgstart`, `pgstop`

[attributes and content](#attributes-and-content)<br>
[manipulating CSS](#manipulating-css)<br>
[manipulating the DOM](#manipulating-the-dom)<br>
[events](#events)<br>
[effects](#effects)<br>

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

### Adding and Removing Classes

+ JQuery has several methods for CSS manipulation.
  + `addClass()` adds one or more classes to a selected element.
    + `$('section').addClass('className className');`
  + `removeClass()` removes one or more classes from an element.
    + `$('section).removeClass('className);`
  + `toggleClass()` toggles between adding/removing classes from the selected elements, meaning that if the specified class exists for the element, it is removed, and if it does not exist, it is added.

### CSS Properties

+ The `css()` method can be used to get and set CSS property values.
  + `$('section').css('background', 'green');`
+ To set multiple properties the `css()` method uses `JSON` syntax.
  + `.css({'property':'value', 'property':''value'});`
+ **Dimensions**
  + `.width(50)` and `.height(75)`
  + width and height does not include padding, borders or margins
  + `.innerWidth()` and `.innerHeight()` includes padding
  + `.outerWidth()` and `outerHeight()` includes padding and borders.

## Manipulate the DOM

+ `.parent()` returns the direct parent of the selected element.
+ `.parents()` all ancestor elements of the selected element.
+ `.children()` all direct children.
+ `.siblings()` all sibling elements.
+ `.next()` and `.nextAll()` next sibling or all next siblings
+ `.prev()` and `.prevAll()` previous sibling or all previous siblings
+ `.eq()` elements with a specific index number of the selected elements.
  + `$('div').eq(2);` is essentially `div:nth-child(3)`
  + the index starts at 0.

+ **Remove Elements**
+ `.remove()` remove selected element(s).
  + `$('section').eq(1).remove();` will remove the 2nd section element from a group of sections.
+ `.empty()` removes all child elements from the selected element.
  + `$('section').empty()` would remove all children from section.
+ *empty the second child element of the element with id="nav"*.
+ ```
  var n = $('#nav').children();
  n.eq(1).empty();
  ```

### Events

## Handling Events
+ **Normal JavaScript**
+ ```
  var x = dcument.getElementById('test');
  x.onclick = function(){
    document.body.innerHTML = 'something';
  }
  ```
+ **Using JQuery**
+ ```
  $('#test').click(function(){
    $('body').html('something');
  });
  ```
+ Common Mouse Events: `click`, `dblclick`, `mouseenter`, `mouseleave`, `mouseover`
+ Keyboard: `keydown`, `keyup`
+ Form Events: `submit`, `change`, `focus`, `blur`
+ Document Events: `ready`, `resize`, `scroll`
+ **Change the content of a div with an input form:**
  + ```
    HTML:
    <input type="text" id="name" />
    <div id="output"></div>

    JavaScript:
    $("#name").keydown(function() {
      $("#outPut").html($("#name").val());
    });
    ```
+ The `.on()` method is another way to handle events.
  + ``` 
    $('section').on('click', function(){
      // do stuff
    });
    ```
+ The `.off()` method will remove the event handler
  + `$('section').off('click');`

+ > very event handling function can receive an event object, which contains properties and methods related to the event:
  + `pageX`, `pageY` mouse position when event occurred relative to top left of the page.
  + `type` the type of event.
  + `which` the button or key that was pressed.
  + `data` any data that was passed in when the event was bound.
  + `target` the DOM element that initiated the event.
  + `preventDefault()` prevent the default action of the event.
  + `stopPropagation()` stop the event from bubbling up to other elements.
+ `.trigger()` can trigger an even programmatically.
  + `$('section').trigger('click');`


### Effects

+ `.hide()` and `.show()` to hide or show the selected element.
  + `.toggle()` is used to toggle between hiding and showing an element.
    + ```
      $(function() {
        $("p").click(function() {
          $("div").toggle();
        });
      });
      ```
    + `.toggle()` can take in optional arguments to specify animation speed as well as a callback function that runs after the animation is complete.
     + `.toggle(1000, callBack)`
+ `.fadeIn()`, `.fadeOut()` is similar to hide and show.
  + `.fadeToggle()` acts the same and accepts the same optional parameters of speed and callback.
  + `.fadeTo()` always fading to a given opacity.
    + `fadeTo(2000, 0.6)`
+ `slideUp()`, `slideDown()` and `slideToggle()` same as the above methods.


+ `.animate()`
  + > The animate() method lets you animate to a set value, or to a value relative to the current value.
  You need to define the CSS properties to be animated as its parameter in JSON format ("key":"value" pairs).  The seconds parameter defines the animation speed.
    + The following code will change the `width` of `div` to `250px` over 1 second.
    + ```
      $("div").click(function() {
        $("div").animate({width: '250px'}, 1000);
      });
      ```
    + **Note** You can animate any CSS property.  However you must use camelCase when references the property.
      + `margin-top` = `marginTop`
  + You can select multiple properties by separating them with a comma.  It is also possible to define relative values.
    + ```
      $("div").animate({
        width: '+=250px',
        height: '+=250px'
      }, 1000);
      ```
  + `.stop()` can be used to stop an animation before it's duration.
+ **Animation Queue**
  + If you call multiple `.animate()` methods JQuery creates an internal queue and runs them one by one.
+ Like the other methods `animate()` cas also have an optional callback parameter.

[back to top](#jquery-pre-work)<br>
[Back to Mainpage](../code-fellows.md)<br>