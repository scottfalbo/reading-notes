# Routing

> In single-page apps **(SPAs)**, routing is responsible for loading and unloading content while matching the URL with the set of components being rendered. Routing should also keep track of browser history and link users to specific sections of your app.

+ `npm install --save react-router-dom`

  + ```
    import React from 'react';
    import {
      BrowserRouter,
      Route
    } from 'react-router-dom';

    import HomePage from './HomePage';
    import Page2 from './Page2';

    const App () => (
      <BrowserRouter>
        <div className="container>
          <Route exact path="/" component={HomePage} />
          <Route path="/page2" component={Page2} />
        </div>
      </BrowserRouter>
    );
    ```

+ Pass Route as a call back with `render` if you want to send props to the component.
  ```
  <Route path="/page2" component={Page2} />
  <Route path="/page2" render={ () => <Page2 var='whatever'/>}/>
  ```

+ ### Navigation
  + ```
    import { Link } from 'react-router-dom';
    ...
    <li><Link to="/Page3">Page3</Link></li>
    ...
    ```



[Back to Main](../README.md)