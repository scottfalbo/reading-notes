# More on Components and Props

+ **PureComponent**
+ > React provides a special type of component, called PureComponent, that helps prevent unnecessary re-renders. If your component’s render() method renders the same result given the same props and state, you can use PureComponent for a performance boost in some cases.
  + ```
    import React, { PureComponent } from 'react';

    class ClassName extends PureComponent {
      ...
    }
    ```
  + A PureComponent should only contain child components that are also PureComponents.

+ **Destructuring Props**
+ Unpacks values from arrays, or properties from objects, into distinct variables. 
  + In a stateless function:
    + ```
      before...
      const functionName = (props) => {
        console.log(props.var1, props.var2);
      }

      after...
      const functionName({ var1, var2 }) => {
        console.log(var1, var2);
      }
      ```
  + In a `class`
    + ```
      before...
      class ClassName extends Component {
        render(){
          console.log(this.props.var1, this.props.var2);
        }
      }

      after...
      class ClassName extends Component {
        const {
          var1,
          var2
        } = this.props;
        render(){
          console.log(var1, var2)
        }
      }
      ```
+ **Refs and the DOM**
+ `React.createRef()`
+ There are a few good use cases for refs:
  + Managing focus, text selection, or media playback.
  + Triggering imperative animations.
  + Integrating with third-party DOM libraries.
+ *Avoid using refs for anything that can be done declaratively.*

+ **validate Props with Type Checking:
+ Ensures the right data type is being sent.
+ As your app grows, it's a good practice to "type check" or validate the data a component receives from props. Other developers working on the same project will know exactly which props your components take, and what types they should be.
  + `npm install --save props-types`
  + ```
    import PropTypes from 'prop-types';

    const Thing = ({name, age, doSomething}) => {
      ...
    }

    Thins.propTypes = {
      name: PropTypes.string,
      age: PropTypes.number,
      doSomething: PropTypes.func
    };
    ```


[Back to Main](react.md)