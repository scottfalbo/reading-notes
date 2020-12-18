# React Context API

> React provides a way to pass data to components without having to pass props manually at every single level
> Context is mainly used when certain data needs to be accessed by many components at different nesting levels.

+ **Context API**
  + `createContext()` - Sets up a context and returns and object with a provider and a consumer, the two main components of the context API.
  + **Provider** - Used as high as possible in the component tree.  It allows a consumer to subscribe to context changes.
  + **Consumer** -  Accesses the provider to get the data that it needs.  The consumer is what helps avoid *Prop Drilling*.

+ Add a context directory to the components folder with an `index.js`.
+ ```
    src
      - components
      - Context
        - index.js
      App.js
      Other.js
    ```
+ ```
    index.js...
    import React from 'react';

    const AppContext = React.createContext();

    export const Provider = AppContext.Provider;
    export const Consumer = AppContext.Consumer;
    ```
+ ```
    App.js...
    import { Provider } from './Context';

    ...

    render(){
      return(
        <Provider value={this.state.whatever}>
          ...
        </Provider>
      )
    }
    ```
+ **Render Prop** - A technique for sharing code between React components using a prop whose value is a function.
+ ```
  Other.js...
  import { Consumer } from './Context';

  const Other = () => {
    return(
      <Consumer>
        { context => {
          return(
            <section>
              <p>{this.context}</p>
            </section>
          );}
        }
      </Consumer>
    )
  }
  ```
+ **Higher Order Component** - A technique in React for reusing component logic.  A HOC takes an existing component and returns a new component.
+ ** Children ** - A special React prop that lets you pass components as data to other components.

[Back to Main](../README.md)