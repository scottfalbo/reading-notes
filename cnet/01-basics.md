# The Basics

+ **Namespace**
  + `using System;`
  + `System.Console` -> `Console`

+ **Data Types**
  + `.GetType()`: method to get type
  + `int`: whole number
  + `double`: decimal
  + `string`: "string" - double quotes
  + `bool`: boolean
  + `char`: 'z' - single quotes

+ `Console.WriteLine(" ")`: writes to console
+ `Console.ReadLine()`: read from console

+ `System.Threading.Thread.Sleep(ms)` - needs System
  + or 
  + ```
    using System.Threading;
    Thread.Sleep(1000);
    ```

+ **Declaring a Method**
+ ```
  static void methodName(int numVar, string textVar)
  {

  }
  methodName();
  ```
    + `static` signifies it can be called on it's own, it is not part of an object.
    + `void` means there is no return value
      + This type must match the return value if there is one.
    + parameters are datatype and name `(int numVar)`

+ **String Interpolation**
  + `$"text {1+2} more text"`
+ Escape sequences
  + `\n` newline
  + `\t` tab
  + `\"` "






[Back to Main](cnet.md)