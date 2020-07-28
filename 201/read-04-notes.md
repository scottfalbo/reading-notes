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

### CSS Layout, Chapter 15
*html, css 358-404*

Doing these notes by hand for visuals.

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


[Back to the main page](../README.md)