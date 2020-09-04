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
var myObject = {
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

[jump to get/update element content](#get-and-update-element-content)<br>
[jump to Attribute Nodes](#Attribute-Nodes)


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
    + `var itemColors` contains a NodeList with all `<li>` whose class attribute is `.green`.
    + As usual `.length` is as the conditional in the for loop.

+ **Traversing the DOM**: When you have an element node you can select another element in relation to it.
  + `parentNode`: The element above the element you're in.
  + `previousSibling`, `nextSibling`: Find the previous or next sibling element.
  + `firstChild`, `lastChild`: Find the first or last child of the current element.
  + *javascript pages 210-211 for examples*
+ This way of traversing the DOM is difficult because most browsers treat space between elements as text nodes so the above properties are not best practice.  It is best to avoid using them.

### Get and Update Element Content

+ To work with an element you can:
  + Navigate to text nodes.  This is best when the element contains only text.
    + text nodes have one property called `nodeValue`. *pg 214*
  + Work with the containing element: This allows access to chid elements and text nodes.
+ When you are working with an element it can contain mark up.  You can choose whether to grab the markup as well as the text.
  + `innerHTML`: get/set markup and text *pg 220*
  + `textContent`, `innerText`: get/set text only *pg 216*

  *javascript pages 214-221 for examples and reference with tree diagrams for visual aid.*

  + Adding elements using DOM manipulation.
    1. Create the element: `createElement()`
    2. Give it content: `createTextNode()`
    3. Add it to the DOM: `appendChild()`
  + *see page 223 for example*.

+ Removing elements with DOM manipulation.
  1. Store the element to be removed in a variable.
  2. Store the parent of that element in a variable.
  3. Remove the element from its containing element.
      + `removeChild()` is used on the containing element from step 2.
  + *see page 225 for example*

**Comparing the three ways to update html content.**  
  + `document.write`
  + **advantages**:
    + It's quick and easy
  + **disadvantages**:
    + It only works when the page initially loads.
    + It can cause issues if used after the page is loaded.
    + This method is *rarely used* and *not best practice*.
  + `element.innerHTML`
  + **advantages**:
    + Can add more markup with less DOM manipulation code.
    + Can be faster than DOM manipulation when adding a lot of new elements.
    + It is a simple way to remove all of the content from element.
  + **disadvantages**: 
    + It should not be used to enter information from the user as it is a significant security risk.
    + It can be difficult to isolate specific elements on a larger DOM.
    + Event handlers may no longer work as intended.
  + `DOM Manipulation`
  + **advantages**:
    + It is good for targeting one element if there are many siblings.
    + It does not affect event handlers.
    + It allows script to add things incrementally.
  + **disadvantages**:
    + If you have to make a lot of changes it is slower than `innerHTML`.
    + You need to write more code to achieve the same thing as `innerHTML`

#### Cross-site scripting Attacks, or XSS
Using `innerHTML` can cause security risks.  *pages 228-231 for deeper detail and possible work arounds*.


### Attribute Nodes

> Once you have an element node, you can use other properties and methods on that element node to access and change its attributes.

+ Select the element node that carries the attribute.
+ Then use a property or method
+ `document.getElementById('ethel').getAttribute('class');`
+ *pages 233-235 for other methods and uses*.

You can examine the DOM in Chrome in element > properties

*pages 240-241 for an implemented use.*


[Back to the main page](../README.md)