## 201 Read-07 Notes: Domain Modeling, Tables, Functions, Methods and Objects

### Domain Modeling
> **Domain Modeling** is the process of creating a conceptual model for a specific problem.

+ When modeling a single entity that will have many instances use a constructor function to build self-contained objects with the same attributes.
+ Each **method** should be small and have one job.

[see more below](#creating-multiple-objects)

### Tables, chapter 6
*Duckett html and css, pages 126-145*

+ > A **table** represents information in a grid format.
+ > Grids allow us to understand complex data by referencing information on two axes.
+ > Each block of the grid is referred to as a **table cell**.

**Basic Table Structure**
```
<table>
  <tr> //table row
    <th></th>  //table heading
    <td></td>  //table cell
    <td></td>  
  </tr>
</table>
```
The `<th>` element is a heading for a column or row and is utilized by screen readers to improve accessability.

+ Spanning Columns: spanning multiple horizontal cells.
  + `<td colspan="3">` 
+ Spanning Rows: spanning multiple vertical cells.
  + `<tr rowspan='2'>`

+ For better accessability and styling purposes it is best to use the following elements on longer tables.
  + `<thread>` is used to wrap the `<tr><th>`
  + `<tbody>` wraps the first set of `<tr><td>`
  + `<tfoot>` wraps the last set of `<tr><td>`


### Functions, Methods and Objects, chapter 3
*Duckett javascript, pages 106-144*

#### Creating an Object: Constructor Notation

> The `new` keyword and the **object constructor** create a blank object that you can then add properties and methods to.
  + Create and object with the `new` keywords and `Object()` constructor.
    + `var exampleName = new Object();`
  + Add properties and methods using **dot notation**.
    + ```
      exampleName.p1 = 'something';
      exampleName.p2 = 'something else';
      exampleName.m1 = function(){
        //do a thing
      }
      ```
+ You can create an empty object with literal notation `var name = {}`.

+ Update objects with **dot notation** or **square brackets**
  + `exampleName.p1 = 'a different thing';`
  + `exampleName['p2'] = 'excelsior';`
    + Square brackets is required when using a variable instead of the key name.
+ `delete exampleName.p1;` will remove the property.

#### Creating Multiple Objects

> Object constructors can use a function as a **template** for creating objects.

+ ```
  function Store(name, minCust, maxCust) {
    this.storeName = name;
    this.minimumCustomers = minCust;
    this.maximumCustomers = maxCust;
    this.someMethod = function() {
      // do a thing
    }
  }
  ```
  + `.this` is used instead of the object name to indicate the key belongs to the object that *this* function creates.
  + Each statement uses a `;` unlike literal notation.
  + The constructor function name begins with a capital letter.

  + The `new` keyword followed by a call to the function creates a new object.
    + `var newStore = new Store('S'Mart', 10, 30);`

*Duckett javascript page 111 for a good object to DOM example*

#### This

+ When a function is created in the global scope `.this` refers to the window object.
+ Global variables also become properties of the window object.
+ In a method `.this` refers to the object the key lives in.

> Arrays are a special type of object.  They hold key/value pairs but the key for each value is an index number.

#### Built in Objects
+ **Browser Object Model**: Contains objects that represent the current browser window such as browser history and the device's screen.
+ **Document Object Model**: the DOM uses objects to create a representation of the current page.
+ **Global JavaScript Objects**: Things that JavaScript needs to create a model of.

An **Object Model** is a group of objects that form a model of something larger.

*see pages 123-139 for an extensive list of built-in objects*


[Back to the main page](../README.md)