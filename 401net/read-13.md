# 401 .NET Read 13: Dependency Injection and Repository Design Pattern

## Dependency Injection

A dependency is an object that your class needs to work.  It is created outside of the class and injected.  This helps prevent coupling in the code.

When a constructor receives a class or abstraction of another class parameter it is dependency injection.

You can inject code into a prop with a getter/setter.
```
get
{
  return thingToInject;
}
set => thingToInject = value;
```

Another way to inject data is if a class has a method that takes in an abstraction as a parameter.

A service locator (container) is a class that holds many instances that can be requested by methods in other classes.

<hr>

## Repository Design

This is like a mediator between the domain and data mapping.  This is done with an interface for accessing domain objects.  It separates the data collection logic from the rest of the application.

<hr>

## SOLID Principles
**SOLID Principles** represent the idea that every method has only one job or purpose, it changes only one thing.  Having a method perform only one task makes it easier for testing and therefore easier to debug.

**Open/Close Principle (OCP)** means that a class/method should be open for extension, but closed for modification.  This lets you extend class behavior without changing the behavior of the class.  

**Liskov Substitution**
Basically means that a class derived from another class can act in the same way.  This seems like basic inheritance. 

**Interface Segregation**
Makes it so classes only have methods that they can execute, instead of inheriting useless functions they can't use.

**Dependency Inversion**
You don't fuse the tool to the class.  Rather you give the class an interface that allows connection to the tool.  

<hr>

[Back to the main page](../README.md) 