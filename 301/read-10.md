# 301 Read-10: The Call Stack

## The Call Stack, MSN
[msn call stack definition](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)<br>

+ A **Call Stack** is a mechanism for an interpreter to keep track of its place in a script that calls multiple functions.
  + When a script calls a `function`, the interpreter adds it to the **call stack** and then starts carrying out the `function`.
  + Any `functions` that are called by that `function` are added to the **call stack** further up, and run where their calls are reached.
  + When the current `function` is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
  + If the stack takes up more space than it had assigned to it, it results in a "stack overflow" `error`.
+ ```
  function one(){
    // do stuff
    two();
    // finish stuff
  }

  function two(){
    // do some stuff
  }

  one();
  ```
  1. Ignore all functions, until it reaches the `one()` function invocation.
  2. Add the `one()` function to the call stack list.
  3. Execute all lines of code inside the `one()` function.
  4. Get to the `two()` function invocation.
  5. Add the `two()` function to the call stack list.
  6. Execute all lines of code inside the `two()` function, until reaches its end.
  7. Return execution to the line that invoked `two()` and continue executing the rest of the `one()` function.
  8. Delete the `two()` function from our call stack list.
  9. When everything inside the `one()` function has been executed, return to its invoking line to continue executing the rest of the JS code.
  10. Delete the `one()` function from the call stack list.

## JavaScript Call Stack - What It Is
[JavaScript Call Stack - What It Is](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)<br>

+ An understanding of the call stack will give clarity to how “function hierarchy and execution order” works in the JavaScript engine.
+ The call stack runs functions one at a time so it is synchronous.
+ A **Call Stack** is basically a data structure that manages function calls using last in, first out (LIFO) principle.
+ Like magic card order resolution.
+ A **Stack Overflow** occurs when there is a recursive function without an exit point. 


## JavaScript Error Messages
[error message article](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)<br>

+ **Types of Error Messages**
  + Reference errors: When you try to use a variable that is not yet declared.
    + `const` and `let` are hoisted like var and function but there is a time between the hoisting and being declared.  This is called the **Temporal Dead Zone**, sounds cool.
  + Syntax errors: Something that cannot be parsed in terms of syntax.
  + Range errors: Manipulating the length of an object with an invalid length.
  + Type errors: Trying to access incompatible types or undefined types.

+ **Debugging**
  + `console.log` variables to check output.
  + ctrl+o to run lines of individual code in the browser console.
  + Breakpoints can be used by putting a *debugger* statement on the line of code you want to break.

+ **Call Stack**
  + Giving functions meaningful names makes the call stack easier to navigate.
  + See the stack trace at any given point in your code with `console.trace()`

+ **Handling Errors**
  + `try` `catch` to return anything instead of a broken page.

[MDN JavaScript Error Messages](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)<br>

[Back to the main page](../README.md) 