# Modules

> Components should be broken down into **Modules**.  ES modules is a feature in JavaScript that lets you break up your code into individual JavaScript files. Modules provide a better way to organize and maintain your code, as well as provide scope for your variables, functions and classes.

+ src
  + components
    + App.js
    + Header.js
    + Thing1.js
    + Thing2.js
+ index.css
+ index.js

Then each module is exported and imported to be used.
+ ```
  index.js:
  import React from 'react';
  import ReactDOM from 'react-dom';

  import App from './components/App';
  import './index.css';
  
  ReactDOM.render(
  <App />, 
  document.getElementById('root')
  );
  ```
+ ```
  App.js:
  import React from 'react';
  import Header from './Header';
  ...
  export default App;
  ```
+ ```
  Header.js:
  import React from 'react';
  ...
  export default Header;
  ```
+ `import React, { Component } from 'react'`
+ changes the `class` declaration from
  + `class App extends React.Component {}`
  + to
  + `class App extends Components {}`

+ Another way to export a `class`
  + ```
    export default class Counter extends Component {
      render( ... )
    }
    ```
+ Another way to export functions
  + ```
    export const Counter = () => {
      return( ... )
    }
    ```
  + ```
    import { Counter } from './Counter';
    ```
## Unidirectional Data Flow
> In React, data naturally flows down the component tree, from the app's top-level component down to the child components, via props. This is called "unidirectional data flow".

+ **Lifting State Up** - When two or more components need access to the same state, move the state into their common parent.
+ To data to flow up the parent can pass a callback function to a child that returns a change in state.
+ **Controlled Components** - To manage an input field's state, we need to build a "controlled component." A controlled component renders a form element whose values are controlled by React, with state.
  + **Creating a Controlled Component**
    1. Initialize state for the value of the input.
    2. Listen for changes on the input to detect when value is updated.
    3. Create an event handler that updates the value state.

## Stateful Components and Lifecycle Methods
 > Component Lifecycle - Every component instance follows a cycle: It's mounted onto the DOM, it's updated with changes in data, and it's unmounted from the DOM.

+ React Lifecycle Methods
  + Built-in methods that get called at each point in the life cycle.
  + Hooks that run code at key times in a component's life cycle.
  + Give you the ability to control what happens when a component mounts, updates, and un-mounts.

+ > **Prevent Memory Leaks** - Since components do not always stay in the DOM, React also provides the componentWillUnmount lifecycle method to help you handle unmounting of components. This can help prevent memory leaks in your application.
+ `componentWillUnmount()`




[Back to Main](react.md)