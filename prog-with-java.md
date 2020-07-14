# Scott's Reading Notes

### Programming with JavaScript

**Intro and Scripts**
+ Access content:  JavaScript can access any element, attribute, or text from an HTML page.
+ Modify content: Add elements, attributes and text, or remove them.
+ Program rules: Specify steps for the browser to follow which allows to access or change the contents of a page.
+ React to events: Specify that a script should run when an event occurs like a button is pressed.

>Scripts are made up of instructions a computer can follow step by step.  A browser may use different parts of the script depending on how the user interacts with the web page.  Scripts can run different sections of the code in response to the situation around them.

+ Start with the big picture
    + Define the goal
        + Design the script
            + code each step

Programmatic problem solving.  Think like a computer, they do not solve tasks like a human.  They follow a series of instructions, one after another.  


### Expressions

An expression evaluates into (results in) a single value.
+ `var cat = 'spaceghost';`
+ `var howMany = 1 + 1 + 1 + 1;`

Operators allow programmers to create a single value from one or more values.
+ assignment operator:  `var color = 'green';`
+ arithmetic operator:  `var area = 6 * 6;`
+ string operator: `var greeting = 'Hello' + ' world';`
+ comparison operator = `value = 5 > 7;`
    + *returns true or false*
+ logical operator: `value = ( 6 > 2 ) && ( 3 < 8 );`
    + *returns true or false*

Arithmetic Operators:
+ increment: `++` : adds one to the current value
+ decrement: `--` : subtracts one from the current value
+ modulus: `%` : divides two values and returns the remainder.


### Functions

**Functions** allow you to groups a series of statements together to perform a specific task that can be called at will from different parts of your script.

Function Declaration
+ ```
    function functionName() {
        document.write('say something');
    }
  ```
+ ```
    var sayHelloTwo = function(){
    console.log("say something else");
}
  ```
+ The above code declared a function named `functionName`.  **Calling the Function** will execute the script contained within.
    + `functionName();`
+ When a function needs specific information you assign it **parameters**.  The **parameters** cat like variables inside the function.
    + ```
        function someNumber(item1, item2){
            return item1 + item2;
        }
      ```
    + When you call a function with parameters you have to include the proper *arguments*.
    + ```
        someNumber(2, 6);
      ```
    + Some functions **return** information to the code that called them.  in the above example if we call the function with `someNumber(11, 15);` it would return a value of 26.

### Refactoring
>Refactoring is a disciplined technique for restructuring an existing body of code, altering its internal structure without changing its external behavior.  Refactoring is intended to improve the design, structure, and/or implementation of the software (its non-functional attributes), while preserving its functionality.



[Back to Mainpage](README.md)

<!--


Return value
Refactoring -->