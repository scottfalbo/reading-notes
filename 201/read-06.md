## 201 Read 06. Problem Domain, JS Object Literals, The DOM


### Problem Domain

> Understanding the problem domain can be one of the most difficult parts of programming.  Programming is easy if you understand the problem domain or have it spelled out for you step by step.  Often times this is not the case and you will be working with vague concepts or trying to build something without all of the information. *Understanding the problem is the most critical piece to the equation*.
  + > You can make the problem domain easier by breaking it down into smaller bits and narrowing focus to a particular part of the problem.
  + > Take the time to talk and listen to the client.  Make sure you understand the problem before tackling the code.  Try to avoid starting work with "just enough" information.


### Object Literals, chapter 3
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

  

### Document Object Model (DOM), chapter 5
*Duckett, javascript 183-242*

> The DOM specifies how browsers should create a model of the HTML page and how JavaScript can access and update the content while it's in the browser window.

The browser creates a model of the page called a **DOM Tree** which is stored in the browser's memory.  It consists of four main types of nodes:
  + **The Document Node**: The document node represents the whole page.  It is the starting point for all visits to the DOM Tree.  It corresponds to the `document` object in JavaScript.
  + **Element Nodes**: The describe the elements of the site. `<body>`, `<h1>`, `<p>` and so on.  
    + To access the DOM Tree you start by looking for elements.
  + **Attribute Nodes**: This targets the attributes inside of HTML tags.  Attribute nodes are not children of the element that carries them.
  + **Text Nodes**: Once you've accessed the element node you can access the text node.  text nodes cannot have children so it is the end of the branch.  

**Accessing and updating the DOM Tree involves two steps:**
1.  Locate the node that represents the element you want to work with.
2. Use its text content, child elements, and attributes

*reference javascript pgs 188-189 for an index on ways to access nodes*

> Methods that find elements in the DOM tree are called **DOM Queries**.  If you plan to work with an element more than once you should store it in a variable.  More accurately you are storing the location of the node in the variable.
This is known as **caching** the selection.

DOM queries may return a **single element** or a collection of nodes, or a **NodeList**.
  + If a method can return more than one node it will always return a NodeList.  You can then select the element from the list using an index number just like an array.
  + Always find the fastest way to an element to keep the page fast and responsive.
    + *page 193* 
    + Methods that return a single element node:
      + `getElementById('elementId')`
      + `querySelector('css selector')`
    + Methods that return a NodeList:
      + `getElementByClassName('class')`
      + `getElementsByTagName('tagName')`
      + `querySelectorAll('css selector')`

*Reference javascript pages 194-203 for using each of the above methods.*

You can loop through a NodeList in the same way you would an array.
  + ```
    var itemColors = document.querySelectionAll('li.green');
    for (var i = 0; i < itemColors.length; i++){
      itemColors[i].className = 'blue';
    }
    ```
    + `var itemColors` 


[Back to the main page](../README.md)