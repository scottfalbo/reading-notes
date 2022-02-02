# 401 .NET Read 04: Classes and Memory Management

## Reference Types
[Microsoft docs: Classes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes)<br>

+ A type that is defined as a `class` is a reference type.  When you create a variable of a reference type it contains `null`. 
+ `SomeClass newInstance = new SomeClass();`
+ You must explicitly create an instance of the class by using the `new` operator.  You can also assign it the value of a compatible type that was created some where else.
+ `SomeClass newInstanceTwo = newInstance;`
+ *Memory is allocated when the object is created.  Variables hold a reference to that location.*

### Declaring Classes
```
public class NewClass
{
  // do stuff
}
```
+ `public` - access level
+ `class` - class keyword
+ `NewClass` - class name, `potato`

### Creating Objects
> Although they are sometimes used interchangeably, a class and an object are different things. A class defines a type of object, but it is not an object itself. An object is a concrete entity based on a class, and is sometimes referred to as an instance of a class.

```
public class CatMaker 
{
  // make a cat
}

CatMaker spaceghost = new CatMaker();
```
+ When the instance is created an `object`, `spaceghost` is passed back.  This is a reference to the `class`, `CatMaker`. The reference refers to the new object but does not contain it.

### Class Inheritance 
+ Classes can inherit `properties`, `methods` and events from other `public` classes.
+ `public class Creatures : Cats`
+ The `Creatures` class will inherit everything in the `Cat` class.
  + The base class does in inherit `constructors`

## Constructors
[Microsoft docs: Constructors](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors)<br>

+ When a `class`, or `struct`, is created its constructor it's called.
+ If you don't provide a constructor for your class C# provides one that sets all fields to the default values.
  + [Default value types](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/default-values)
+ A constructor method shares the same name with th `class` type.  It takes in parameters and has no return.
+ ```
  public class CatMaker
  {
    private string name;
    private int age;

    public CatMaker(string nameInput, int ageInput)
    {
      name = nameInput;
      age = ageInput;
    }
    // or you can make static constructor
    static CatMaker()
    {
      name = "spaceghost";
      age = 12;
    }
  }
  ```
## Properties
[Microsoft docs: Properties](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties)<br>
+ Properties are special methods called accessors.  They expose a `class` to public ways of getting and setting values while still hiding the rest.
+ `get` - returns a property value.
+ `set` - assign a new value.
+ Properties can be *read-write*, *read-only*, or *write-only*.

### Properties with Backing Fields



## Heaping vs Stacking
+ Basically stacking is a 'first in, first out' operation, like Magic card timing resolution.  You can't get to the next thing until the first thing resolves.  Or in this case is unpacked and thrown away.
+ Heaping is the rest of it, stuff you can just grab whenever you want.  I pile of data basically.

## Fundamentals of Garbage Collection
[Microsoft docs: Garbage Collection](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)<br>
+ The Common Language Runtime, CLR, performs memory management tasks so I don't have to.
  + Don't have to manually release memory.
  + Allocates objects on managed heap efficiency.
  + Reclaims objects that are no longer being used, clears their memory, and keeps the memory available for future allocations.
  + Provides memory safety so objects can't use content of another object.



[Back to Mainpage](../code-fellows.md)<br>