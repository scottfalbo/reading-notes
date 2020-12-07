# React State

> In React, "state" is the data you want to track in your app. State is what allows you to create components that are dynamic and interactive, and it's the only data that changes over time.

+ State is what keeps UI in sync with your data, as the data changes different components of the app will update what they show to the use.
+ **States are only available to `class` components.**
+ If a component is only receiving input through props and rendering UI it's best to use a function.
+ ```
  class Counter extends React.Component {
    render() {
      return (
        <div className="counter">
          <button className="counter-action decrement">-</button>
          <span className="counter-score">{ this.props.score }</span>
          <button className="counter-action increment">+</button>
        </div>
      );
    }
  }
  ```
  + Basically the same as the function method but everything is wrapped in `render()` and to access props you use `this.props`.
  + Below is a **Stateful React Component**
+ ```
  class Counter extends React.Component {
  //------------------ long way
    constructor() {
      super()
      this.state = {
        score: 0
      };
    }
  //---------------- short hand
  state = {
      score: 0
  }

    render() {
      return (
        <div className="counter">
          <button className="counter-action decrement">-</button>
          <span className="counter-score">{ this.state.score }</span>
          <button className="counter-action increment">+</button>
        </div>
      );
    }
  }
  ```
  ## Handling Events
  + Adding an Event Listener to the above snippet.
    + ```
      incrementScore(){
        this.setState({
          score: this.state.score + 1
        });
      }
      ...
      <button className="counter-action increment" onClick={this.incrementScore}>+</button>
      ```
      + `onClick` is a specific React method and added inline.
+ `setState()` is a React method that changes the state and tells it to render again.
+ Custom methods in classes are not bound by default and therefore do not recognize `this`.  There are few ways to bind the function to the component.
  + `<button className="counter-action increment" onClick={this.incrementScore.bind(this)}>+</button>`
    + uses the `bind()` method
  + `<button className="counter-action increment" onClick={() => this.incrementScore()}>+</button>`
    + `() =>` are bound to the scope in which they are defined.
  + Lastly you can change the function to an `() =>`
  + `incrementScore = () => {`
+ `setState()` may happen asynchronously so you shouldn't rely on `this.setState()`
  + To work around this `setState()` accepts a callback with an optional parameter of the previous state as an object.  You can also pass in a second optional parameter of 'props`
    + `setState((prevState, props) => {});`
  + ```
    incrementScore = () => {
      this.setState(prevState =>({
       score: prevState.score + 1
      }));
    }
    ```
+ When a key and property match inside `setState()` you can just type the name once.
  + `value: value,` is the same `value,`
+ **Types of State**
  + **Application state** - Data that is available to the entire app.
  + **Component state** - State that is specific to a component and not shared outside of the component.

[Back to Main](react.md)