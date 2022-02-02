##201 Read04 Notes, HTML Links, CSS Layout, JS Functions


### HTML Links, Chapter 4
*html, css 74-93*

+ Links are created using `<a href=""><a>`
+ When linking to your own site it's best to use relative links.
  + `<a href="images/photo.png">`
+ You can link to external sites with the url.
  + `<a href="http://www.someUrl.com>`
+ You can link to an email.
  + `<a href="mailto:email@some.net">`
+ To open a link in a different window give the element a target attribute.
  + `<a href="" target="_blank">`
+ You can link to specific parts of a page using id attributes.
  + `<a href ="#idName">`
+ You can add this same id tag syntax to link to a specific part of another page so long as the id exists.
  + `<a href="name #idName"> `


### CSS Layout, Chapter 15
*html, css 358-404*

#### Building Blocks

Each element is its own box.  These boxes are block-level or inline.
  + **Block-level** boxes start on a new line and are the main building blocks.
  + **Inline** boxes go around text within the block-level elements.
  + **Containing Element**: A block-level element with other, usually multiple, block-level elements inside of it.

**Controlling the Position of Elements**

+ **Normal Flow**: Boxes are stacked one on top of each other.
+ **Relative Flow**: This shifts an element to the top, left, bottom or right of where it would have been placed in a normal flow.
+ **Absolute Positioning**: Positions the element in relation to its containing element.  Absolute elements move as the user scrolls.
+ **Fixed Positioning**: A for of absolute positioning that places the box in its relation to the window.  This box will not move when the user scrolls up or down.
+ **Floating Elements**: Takes the element out of normal flow and plces it all the way left or right.
  + When moving an element that may over lap.  The `z-index` controls which shows on top.

*Examples in hand written notebook for visual references*

+ **Screen Sizes**: Different users will use different devices so content needs to be designed to fit multiple screen sizes.
+ **Screen Resolution**: Exactly that
+ **Page Sizes**: Standard page size is 960px across because that is viewable on most screens.  Height is harder to guess but 570px-600px is when the user will have to scroll.

+ **Fixed Width Layouts**: Fixed with layouts do not move as a user changes their window size.  You have more control over the page but may have large gaps and small content if the users screen size or resolution is higher.
+ **Liquid Layouts**: These layouts stretch and squish as the user changes the window size.  This is good for larger or smaller viewing devices as the content will stretch or shrink to the size.  You lose some layout control and things might not appear as you intend.

+ **Layout Grids**: *page 389, Duckett, html and css for reference*

+ Use multiple style sheets with @import.
  + HTML `<link rel="" href="styles.css">`
  + styles.css ```
              @import url("other.css");
              @import url ("anotherOne.css");
               ```
+ You can also link each on separately in the HTML.

[Back to Read-08 notes](read-08.md)

### JS Functions, Methods and Operations, Chapter 3
*javascript 86-99*

[previous notes, pages 88-94](../102/prog-with-java.md)

You can return multiple vales from a function in an array.
  + ```
      var sendMEBack = [thingOne, thingTwo, thingThree];
      return sendMeBack;
    ```
> If there is a function where the interpreter would expect an expression it's called a **function expression**.  These functions often don't have name and are called **anonymous functions**.
  + ```
      var product = function(x, y) {
        return x * y;
      };

      var result = product(5, 7);
    ``` 
> **Immediately Invoked Function Expressions, aka IFFY**:  These functions are not given a name.  They are executed when the interpreter comes across them.
  + ```
    var name = (function() {
      var whatever = 6;
      return whatever;
    }())
    ```
#### Variable Scope
A variables scope defines where it can be called.  
+ Variables created inside a function are **local** and cannot be accessed outside of that function.
+ Variables created outside of functions are **global** and can be used anywhere in the script.

#### How memory and variables work
> Global variables use more memory as the are stored in browser memory for as long as the page is open.  Local variables only remembered while the function they are in is executing.

Global variables can lead to naming collisions.

### Pair Programming

> Pair programming is the practice of two developers sharing a single work station to interactively work on a task together.

+ The **Driver** is the one typing
+ The **Navigator** guides the driver with words but never touches the keyboard

The fundamental skills to learning any a new language are listening, speaking, reading and writing.  Paired programming serves to help with all of these.


+ **Greater efficiency**: Pair programmer may take slightly longer but produces higher quality code with less bugs.
+ **Engaged collaboration**: When programmers work together it is more engaging and easier to stay on focus.  You are less likely to doddle when working with a partner.
+ **Learning from fellow students**: Working with a partner can expose you to techniques you may not have otherwise thought of.  
+ **Social skills**: Different personalities and programmings styles require good communication.  Pair programming helps build social skill that are essential to the job place. 
+ **Job interview readiness**: Pair programming is a common interview practice to see how you can communicate and how you'll work with a team.
+ **Work environment readiness**: Learning pair programming will be a head start moving into the work place.


[Back to Mainpage](../code-fellows.md)<br>