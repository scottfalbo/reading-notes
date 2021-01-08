# 401 .NET Pre-Work: Reading Notes

## History of .NET and C#

> The C# language relies on types and methods in what the C# specification defines as a standard library for some of the features. The .NET platform delivers those types and methods in a number of packages.

+ ### What is .NET
  + .NET is an open source developer platform for building different types of apps.
    + A developer platform is a collection of Languages and Libraries
+ You can find the application in your local directory here:
  + `/bin/Debug/netcoreapp3.0/`
+ ### Debugging
  + Breakpoints will stop your code at a given line and let you inspect things before moving on.
    + Used to search data nested ten layers deep while the code is running.
    + You can set conditionals.
+ ### Managed Code
  + Code that is managed by a runtime.  The Common Language Runtime, or CLR, is in charge of taking managed code, compiling it to machine code, and running it.  The runtime includes important services like automatic memory management, security boundaries, and type safety.

*The chief architect since its first version is Anders Hejlsberg, creator of Turbo Pascal and architect of Delphi.*

+ **Encapsulation** means creating a boundary around an object so it may have external and internal behavior.
+ **Type-safe** - meaning that types can interact only through certain rules, ensuring internal consistency.  You can't interact with a boolean as if it's an integer.
+ **Strongly Typed** - means the type rules are very strict.  You can't send a method a float if it's expecting an int.
+ The container for managed code is called an **assembly** or **portable executable**.  This can be an `*.exe` or `*.dll` file.  These files contain metadata allowing assemblies to reference types in other assemblies.
+ 

[Back to the main page](../README.md) 