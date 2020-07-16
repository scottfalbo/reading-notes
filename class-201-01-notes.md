## Course 201 class 01 reading notes


**Duckett HTML Book**
+ Chapter 1: Structure
+ Chapter 8: Extra Markup
+ Chapter 17: HTML5 Layout
+ Chapter 18: Process and Design

[Previous reading notes from the above chapters](html-structure.md)

## JS Chapter 1: "The ABC of Programming"
*pages 11-52*

[Previous reading notes for pages 1-24](prog-with-java.md)

### How do computers fit in with the world around them

>Programmers create models, or objects, that can be defined and then used by a computer.

### Objects and Properties
Each object, or thing can have its own:
+ **Properties**:  Each property has a **name** and **value** and each pair tells us something about the object.
+ ```
    var myObject = new Object();
    myObject.color = 'black';
    myObject.name = 'spaceghost';
    ```

    or
    ```
    var myObject = {
        color: 'black',
         name: 'spaceghost
    };
    ```
+ **Events**: Programs are designed to do different things when the user interacts with them.
    + > An **event** is the computer's way of saying, "Hey, this just happened."
    + > When an event happens it can be used to trigger a specific section of code.  Scripts use event to trigger different functionality.
+ **Methods**: Methods represent things the user can do with an object.   Methods can retireve or update the values of an objects properties.  It's basically a *property with a value of a function*.

**Putting it all together**

> Computers use data to create models of things in the real world.  the events, methods, and properties of an object all relate to each other.  Events can trigger methods, and methods can retrieve or update an objects properties.

>Using the document object, you can access and change what content users see on the page and respond to how they interact with it.



[Previous notes from pages 43-52](javascript.md)



[Back to Mainpage](README.md)