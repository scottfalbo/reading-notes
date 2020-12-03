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

## JSX
+ A syntax extension to JavaScript that is used with React to describe elements in the UI.
+ `<script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>`
+ `<script type ="text/babel" src="./js/app.js"></script>`
  + type="text/babel"

+ `JSX` and `babel` lets you create elements in one line.
  + `const title = <h1> Title </h1>;` is the same as....
    + ```
      const title = React.createElement(
        'h1',
        null,
        'Title'
      );
      ```
+ There is a repel on the Babel page that shows the conversion.

+ You can include children and pass variables as arguments.
+ ```
  const title = 'Title Text';
  const paragraph = 'Here is some more text';
  const elementId = 'title-element';

  const header = (
    <h1 id={ elementId }>{ title }</h1>
    <p>{ paragraph }</p>
  );
  ```
+ `{ }` means you are leaving JSX and entering JavaScript.  Anything in the `{ }` is JavaScript.




[Back to Main](react.md)