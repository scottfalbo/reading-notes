# React Basics

+ `createElement();`
+ ```
  const thing = React.createElement(
    'h1', //type
    {id: 'container', title: 'some words'}, //object with properties of element
    'Hello' //children property
  );
  ```
  + If the element has no properties pass either `{}` or `null`
  + After the properties argument all other arguments are read as children.
  + ```
    'h1',
    null,
    'some stuff',
    'some more stuff',
    variable
    ```
+ React does not create DOM nodes.  It instead creates JavaScript text that describes DOM nodes.

+ `ReactDOM.render();`
+ ```
  ReactDOM.render(
    thing, //object
    document.getElementById('element') //target container element
  );
  ```
  + *Anything inside of the container element is replaced with the new react object.*


[Back to Main](react.md)