# 401 .NET Read 01: Exception Handling

## Debugging
+ ### Clarify the Problem
  + What did you expect the code to do? And what did it do instead?
+ ### Examine tour assumptions
  + Are you using the right method, class, api, object, etc.
  + Are you using the thing correctly?
  + Could it be another change elsewhere in the code?
  + Did you expect a different type of value?
  + Do you know the intent of the code?
+ ### Step thru Code in Debugging Mode
  + When you run a program normally you only get errors afterwards.  Running a **debugger** allows you to monitor everything that is happening while the program is running.
  + Using **breakpoints** gives you a chance to examine parts of code more closely.

## Try-Catch Blocks
+ ### Handling exceptions
  + Place any code that might throw errors in the `try` block, and the exception handlers in the `catch` block.
  + ```
    try
    {
      // try to run some code
    }
    catch (FileNotFoundException e);
    {
      // Console.WriteLine($"error {e}");
    }
    finally
    {
      // do a thing
    }
    ```
### Exception Handling
+ `throw` - `throw [e];` where `e` is a class derived from  `System.Exception`.
+ try-catch - statements consist of a `try` block followed by one or more `catch` blocks.  The CLR looks for a `catch` to handle exceptions.  If it can't find one it displays on unhandled exception.
  + The `catch` clause can be used without arguments, but it's best to use an object argument.
  + An async method is marked by an `async` modifier. When control reaches an `await` in the `async` method, progress in the method is suspended until the awaited task completes.
+ try-finally - A `finally` block is used to run code even if an exception occurs. 
  + A `finally` block executes either:
    + After a `catch` block finishes.
    + After control leaves the `try` block because of a `jump` statement.
    + After the `try block ends.
  + A `finally` block helps add determinism to a program.
+ try-catch-finally - A common usage of `catch` and `finally` together is to obtain and use resources in a `try` block, deal with exceptional circumstances in a `catch` block, and release the resources in the `finally` block.


*When using multiple `catch` blocks you must put the more specific handlers first*
+ You can specify an exception filter in a `catch` clause by adding a `when` clause.
  + ```
    catch (WebException e) when (e.Status == WebExceptionStatus.Timeout)
    {
      // do stuff
    }
    ```
  + If the conditional is false the `catch` block is ignored.
+ ### The `using` Statement
  + Many classes encapsulate un-managed resources, these implement `System.IDisposable`, which cleans up these resources with a parameterless method called `Dispose`.
<br>

*`throw` exceptions can be either a statement or an expression.*
  + `string whatEver() => throw new WhatEverError();`

## `System.Exception`
+ ### Key properties
  + `StackTrace` - A string of all the methods called from the origin of the exception to the `catch`.
  + `Message` - A string with a description of the error.
  + `Inner Exception` - The inner exception that caused the outer exception.  
  + *All exceptions in C# are runtime exceptions.*
+ ### Common Exception Types
  + `ArgumentException` - a method is called with a bogus argument.
  + `ArgumentOutOfRangeException` - when an argument is either too big or too small.
  + `ArgumentNullException` - when an argument is unexpected `null`.
  + `InvalidOperationException` - when the state of an object is unsuitable for a method to successfully execute.
  + `NotSupportedException` - indicates a particular functionality is not supported.
  + `NotImplementedException` - indicates that a function is not yet implemented.
  + `ObjectDisposedException` - when the object upon which a method is called has been disposed. 

Therac-25 take away: 
+ Don't assume that reused software is safe.
+ Give exception handling messages meaning.  

[Back to Mainpage](../code-fellows.md)<br>