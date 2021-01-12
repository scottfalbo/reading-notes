# 401 .NET Read 02: Unit Testing and Documentation
[jump to documentation notes](#documentation)

## Unit Testing Best Practices
  + ### What is Unit Testing?
    + A unit tests isolate and exercise specific part of a specific method in your code.
    + To write a test you can create a new console project.
      + Within the test you can reference the target project by using it's name as the class name the calling the method.
  + ### Unit Test Anatomy
    + ```
      [TestClass]
      public class AppTests
      {
        [TestMethod]
        public void MathodName()
        {
          var appClassName = new appClassName();
          var result = appClassName.MethodName(x, y);
          Assert.AreEqual(result, control);
        }
      }
      ```
  + **Arrange, Act, Assert**
    + Arrange - everything that needs to run for the test.
    + Act - after getting arranged invoke the method, seed the data, etc.
    + Assert - general category of action.
      + One assert per test method.
  + Each test should handle its own set up and break down.  Tests do not maintain state between tests.
  + Keep tests simple so if it fails it is easy to figure out what went wrong as opposed to many moving parts.
  + If you find yourself laboring heavily to get a class and method setup so that you can test it, you have a design problem.
  + Add tests to *CI* build, if any test fails the entire build fails.

*Using .NET Core with the .NET SDK command line*<br>
[xUnit.net docs](https://xunit.net/#documentation)<br>

## Documentation
### README best practices
1. Explain what the thing is, with context.
2. Show what it looks like when run.
3. Include instructions on how to use the thing.
4. Share any other relevant details.

+ A good README is as short as it can be without being shorter.
  1. Name - something descriptive.
  2. One-liner - Simple one line explanation of what it does.
  3. Usage - What does it look like in action.
  4. API - Detail modules `objects`, `methods`, `types`, etc.  What will I get back?
  5. Installation - How do I install and the thing.

+ Stick to standard README formatting.  When reading through multiple documentations having predictable patterns goes a long way.



[Back to the main page](../README.md) 