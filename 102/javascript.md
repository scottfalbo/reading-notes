## Dynamic web pages with JavaScript
*Chapter 1c*

+ HTML: Content layer.  Structure and Semantics.
+ CSS: Presentation layer.  Colors, fonts, borders, etc.
+ JavaScript: Behavoior Layer.  Adds interactivity.

These three layers form a popular basis for web design called **Progressive Enhancement**.

The `script` tag is used to tell HTML to add JavaScript.  Most `scripts` are including just before the `</body>` tag.

`script src="file.js"></script>`

### Objects and Methods

`document.write('Hello');` = `object.method(parameter);`

> **Objects** have several **methods** and **properties**.  These are known as **members** of that object.  You access the members with a `.` between the object and member you want to access.  The `.` is called a **member operator**.

- `document` represents the entire page.  All browsers implement this object.

- The `write()` method allows content to be written to the screen where the `<script>` element lives.

## Basic JavaScript Instruction
*Chapter 2*

+ Statements
    + A script is a series of instructions known as statements.  In JavaScript a statement is ended with a `;`
+ Comments
    + use comments to explain parts of code and organize larger codes.  Comments are great for others looking at your code.
+ Variable
    + A variable is a temporary place for your code to hold data types.
        + Naming rules:
            + must start with a letter, $ or _
            + no - or . n the name
            + cannot use reserved words
            + variables are case sensitive
            + be descriptive
            + camel case for more than one word




### Basic Vocab 
+ conditionals
    + if, else if, else
    + for

+ operators
    + +, -, ==, >=, etc.
    + basic math operators

+ data types
    + number: full interger 
    + float: decimal
    + boolean: true/false
    + string: `'value'` or `"value"` both single and double quotes work
    + 


[Back to 201 class 01 notes](../201/class-201-01-notes.md)<br>
[Back to 201 class 02 notes](../201/class-02.md)<br>
[Back to the mainpage](../README.md)

