## 201 Read 06. Problem Domain, JS Object Literals, The DOM


### Problem Domain


### Object Literals
*Duckett, javascript 100-105*

> Objects group together a set of variables and functions to create a model of a thing.  A variable inside of an object is called a **property** and a function is called a **method**.  These are referred to as **keys**.

+ Property values can be a string, number, boolean, array or another object.
+ Method values are always functions.


**Literal Notation**
```
var myObject {
  name: 'Spaceghost',
  numOne: 66,
  numTwo: 13,
  TruthyFalsy: true,
  myArray: ['item1', 'item2', 'item3'];

  addTheNumbers: function() {
    return this.numOne + this.numTwo;
  }
};
```
`this.varName` references keys in this object.

#### Accessing an Object
+ Dot Notation:
  + `var kittyName = myObject.name;`
  + Access a property or method using dot notation.  `objectName.key`
  + The `.` is called a **member operator**
+ Square bracket syntax
  + `var kittyName = myObject['name'];`
  + This notation is used when:
    + The name of the key contains special characters.
    + The name of the key is a number... *why would I ever do that*?
    + A variable is being used in place of a property name.

    


### Document Object Model (DOM)
*Duckett, javascript 183-242*

[Back to the main page](../README.md)