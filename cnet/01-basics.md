# The Basics

+ **Namespace**
  + `namespace ProjectName` for grouping files

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

+ ## **Declaring a Method**
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

+ Cast a value
  + `int number = (int)12.5;`
    + will drop the decimal and change type to int
    + only works with numeric types
+ Convert String to Integer
  + `int dozen = int.Parse("12");`

+ ## **Comparison Operators**
  + `==`, `!=`, `>`, `<`
  + ```
    if (num > 100)
    {
      //run code
    }
    else
    {
      //run code
    }
    ```
      + variables inside `if` is scoped to block
      + C# wants an `else` clause
  

[Back to Main](cnet.md)