# 401 .NET Read 06: Object Oriented Principles

## Inheritance
[Microsoft docs](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/inheritance)<br>

There are `base` classes and `derived` classes.  A class derived from a base class can use the properties of that class.  A derived class can only have one direct base.  A derived class can have it's won derived class and accessibility chains.

Constructors cannot be inherit so the derived class needs it's own constructor for the base class properties.

if `okily` is derived from `Ned`, and `dokily` is derived from `okily`, then `Ned` has access to both `okily` `dokily`

### My Take Away
Inheritance is basically one classes way of using parts of another class but with it's own set of instantiation parameters.

<br>

## Abstract
[Microsoft docs](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members)<br>
`abstract` class and members are incomplete.  They are not meant for instantiation on their own, but rather to be used as a `base` for multiple `derived` classes.  The derived classes must override the `abstract` class.

`abstract` methods also have no implementation, they really just define the parameters and return type of the method.  The inheriting class defines the `code block`.

`sealed` classes are locked and cannot be used as a base class.  For this reason they cannot be `abstract`

### My Take Away
I'm thinking about this as a lump of clay class.  It kind of has some properties and characteristics, buy each derivative class can form it as it pleases.

<br>

## Polymorphism
[Microsoft docs](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/polymorphism)<br>

### My Take Away
Polymorphism is basically allows class objects derived from a bas to take more than one form.  This is accomplished by the derived class object, instantiating it's own unique object via it's own constructor for the base class.  The derived class object utilizes the `override` modifier in this case.

## OOP Principles
[Microsoft docs](https://docs.microsoft.com/en-us/dotnet/csharp/tutorials/intro-to-csharp/object-oriented-programming)<br>
[OOP for a 6 year old](https://www.freecodecamp.org/news/object-oriented-programming-concepts-21bb035f7260/)<br>

### My Take Away
A programming approach built around objects.  Each object can hold fields and methods, or data and 'things to do', which can be defined by a class constructor at instantiation.  
To me it's basically building a bunch of templates that can create objects on their own, or with the help and input of other templates.

[Back to Mainpage](../code-fellows.md)<br>