# Objects


+ A `Class` is a template for making individual `Objects` 
  + Each `Object` is an instance of that `Class`.
  + ```
    class ClassName
    {
      public int Stat;
      private int Stat2;
    }

    //instantiation 
    ClassName newObject = new ClassName();
    newObject.Stat = 2;
    newObject.Stat2 = 6; // will throw an error because it's private
    ```
      + `private` *(default)* means the variable can only be changed by methods inside of the object.
      + `public` can be modified from outside of the object.


  







[Back to Main](cnet.md)