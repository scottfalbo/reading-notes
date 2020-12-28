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
 + Change `Link` to `NavLink` to assign active class tags
  + ```
    import { NavLink } from 'react-router-dom';
    ...
    <li><NavLink to="/Page3" activeClassName="highlight-me">Page3</NavLink></li>
    <li><NavLink to="/Page4" activeStyle={{background: 'bisque'}}>Page4</NavLink></li>
    ...
    ```
      + the default class name given is `.active`
      + You can do inline styling with `activeStyle`
  + **Redirect**
    + This is useful when loaded embedded content.
    + ```
      import { ..., Redirect } from 'react-router-dom';
      ...
      <Route exact path="/rootPath" render={ () => <Redirect to="rootPath/child" />} />
      <Route path="/rootPath/child" component={Child} />
      ```
      + Calling `Redirect` as a call back ensures normal behavior for the parent nav as well as on refresh.
  + Embedded routes can be handled dynamically with the `props.match` property.
    + ```
      ...
      const RootPath = ({match}) => (
        ...
        <li><NavLink to={`${match.url}/child`}>child</NavLink></li>
        ...
        <Route path={`${match.path}/child`} component={Child}/>
      );
      ```
+ ### 404 Error Handling
  + ```
    import {..., Switch} from 'react-router-dom';
    ...
    <Switch>
      //routes
      <Route component={NotFound} />
    </Switch>
    ```


[Back to Main](../README.md)