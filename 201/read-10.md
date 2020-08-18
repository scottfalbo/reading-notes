## 201 Read-10: Errors, Handling and Debugging
[jump to debugging](#errors-debugging-and-handling)

> **Order of Execution**.  To find the source of an error, it helps to know how scripts are processed.

Execution Context

  + **Global Context**: Code in the script that is not in a function.
  + **Function Context**: Code that is being run within a function.
  + **Eval Context**: Text is executed like code in an internal function.

### The Stack
> The JavaScript interpreter processes one line of code at a time.  When a statement needs data from another function, it stacks the new function on top of the current task.

```
                        thing3
                        return
            thing2                  thing2
            thing3()    waiting     return       
thing1
thing2()    waiting     waiting     waiting     thing1
```

+ Each time a script enters a new **execution context**, there are two phases.
  1. **Prepare**: *or hoisting*
    + The new scope is created
    + Variables, functions and arguments are created.
  2. **Execute**:
    + Now it can assign values to variables
    + Reference functions and run code
    + Execute statements
+ Because the variables and functions are prepared, or hoisted, they can be declared and called in the code before they are declared.

**Lexical Scope**: Functions in JavaScript are linked to the objects they are defined within.  So the scope of each object is the current execution context and each parent object. 
  + A child object can use data in it's parent objects.  The parent objects scope does not include it's children.

### Understanding Errors
> If a JavaScript statement generates an error, then it throws an **exception**.  The interpreter stops and looks for exception handling code.
  + The interpreter starts looking for an **exception handler** within the current context.  If it cannot find one it will search the next parent context until reaching the global context at which time it stops reading the code and creates an **error object**.

**Error Objects** can help you locate your mistakes and browsers contain the tools to help read them.
  + Error Objects have these properties:
    + **name**: type of error
    + **message**: description
    + **fileName**: name of javascript file
    + **lineNumber**: code line number of the error
+ There are 7 different types of built in error objects in JavaScript.
  + `Error`: Generic error object `.prototype` for other error objects
  + `SyntaxError`: Incorrect use of language, usually a typo. 
  + `ReferenceError`: Variable is either undeclared or not in scope.
  + `TypeError`: Often caused my trying to use and object or method that does not exist. 
  + `RangeError`: If you call a function using numbers outside of its accepted range.
  + `URIError`: *Uniform Resource Identifier*: Happens if the following characters are not escaped:
    + `/` `?` `&` `#` `:` `;` 
  + `EvalError`: Incorrect use of `eval()`
> The `eval()` function evaluates text through the interpreter and runs it as code.

### Errors, Debugging and Handling

> Debugging is about deduction: eliminating potential cause of an error.

+ **Where is the problem?**
  1. Look at the error message.  Find the relevant script, line number, and type of error.
  2. Check how far the script is getting.  Use `console.logs` to tell you where you are.
  3. Use **breakpoints** where things are going wrong.  

+ **What is the Problem?**
  1. When you use breakpoints, you can see if the variables around them have the values you would expect.
  2. Break down the code into smaller pieces to test functionality.
    + Write values of variables in the console.
    + Call functions from the console to test them.
    + Check if objects exist and have the properties you think.
  3. Check parameters for functions and number of items in an array.

> The JavaScript console will tell you when there is a problem with a script, where to look for the problem, and what kind of issue it is.

+ **Console Methods**
  + `console.info()` used for general information.
  + `console.warn()` used for warnings
  + `console.error()` used for errors
+ Grouping Messages
  + ```
    console.group('collection');
      console.info(whatever);
      console.log(some more whatever);
    console.groupEnd();
    ```
+ Tabular Data
  + `console.table();` outputs a table showing objects and arrays that contain other arrays.
+ Writing on a Condition
  + `console.assert(some condition, 'some output');` write to the console if the condition is met.

**Breakpoints**:  *Duckett, javascript pages 476-479 for console controls and visuals*

### Handling Exceptions
> If you know your code might fail use, `try`, `catch`, and `finally`.
  + ```
    try {
      // try to execute this code
    } catch (exception) {
      // if there is an exception run this
    } finally {
      // this always gets executed
    }
    ```
+ **Try**: This is the code you think might not work.  If an exception occurs control is passed to the catch block.  If you use `continue`, `break`, or `return` in the try block it passes to `finally`.
+ **Catch**: Steps in with an alternative set of code.  It has one parameter, the error object.  This lets you tell the user that something went wrong instead of the script just stopping.
+ **Finally**: This block always runs no whether the `try` block succeeded or not.

**Throwing Errors**
> If you know something might cause a problem for your script, you can generate your own errors before the interpreter creates them.
+ `throw new Error('message')`
  + This creates a new `Error` object.  The parameter is the message you want associated with the error and should be as descriptive as possible.


[Back to the main page](../README.md)