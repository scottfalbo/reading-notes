# 401 .NET Read 07: Interfaces
[MicroSoft docs Interfaces: Guide](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/interfaces/)<br>
[MicroSoft docs Interfaces: Reference](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/interface)<br>

**Interfaces** are basically pure `abstract` classes.  All methods and properties are empty and an `interface` cannot instantiate on it's own.

Interfaces are a good way to share the same template with multiple other classes.  A class can also reference multiple `interfaces` at once.

```
//declare first interface
interface IDoThingOne
{
    void DoTheFirstThing();
}

// declare second interface
interface IDoThingTwo
{
    void DoTheSecondThings();
}

// declare class and give it the interfaces
class ThingDoer : IDoThingOne, IDoThingTwo
{

  // give the empty methods bodies
  public void DoTheFirstThing()
  {
      // do the thing
  }
  public void DoTheSecondThing()
  {
      // do the thing
  }

}
```
```
ThingDoer newDoer = new ThingDoer();
newDoer.DoFTheFirstThing();
newDoer.DoTheSecondThing();
```

[Back to Mainpage](../code-fellows.md)<br>