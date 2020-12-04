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
        // do a thing
      }
      ...
      <button className="counter-action increment" onClick={this.incrementScore}>+</button>
      ```
      + `onClick` is a specific React method and added inline.
  


[Back to Main](react.md)