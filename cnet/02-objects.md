# Objects

+ A `Class` is a template for making individual `Objects` 
  + Each `Object` is an instance of that `Class`.
  + ```
    class ClassName
    {
      public int Stat;
      private readonly int Stat2;

      // constructor 
      public ClassName(int stat, int stat2)
      {
        Stat = stat;
        Stat2 = stat2;
      }
    }

    //instantiation 
    ClassName newObject = new ClassName(5, 7);
    newObject.Stat = 2;
    newObject.Stat2 = 6; // will throw an error because it's private and readonly
    ```
      + `private` *(default)* means the variable can only be changed by methods inside of the object.
      + `public` can be modified from outside of the object.
      + `readonly` cannot be changed

+ **Cartesian Coordinates**
  - `x` is left most and `y` is bottom most
  
## Object Methods

+ ```
  class ClassName
    {
      public int Stat;
      private readonly int Stat2;
      public ClassName(int stat, int stat2)
      {
        Stat = stat;
        Stat2 = stat2;
      }

      // object method, public, returns a boolean
      public bool objectMethod (int whatever, int another)
      {
        bool checker = whatever > 5 && another < 10;
        return checker;
      }
    }
  ```






[Back to Main](cnet.md)