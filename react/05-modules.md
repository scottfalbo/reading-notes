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


[Back to Main](react.md)