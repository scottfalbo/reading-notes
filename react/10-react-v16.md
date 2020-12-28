# React 16

+ ### ComponentDidCatch()
  + Prevents run time errors from crashing the whole App.
  + ```
    ...
    this.state = {
      hasError: false
    };
    componentDidCatch() {
      this.setState({hasError: true});
    }
    render () {
      if (this.state.hasError){
        return <p>error</p>
      }
      else {
        // return normal stuff
      }
    }
    ```
+ ### Error Boundaries
+ > With componentDidCatch() comes a new concept of an error boundary. Error boundaries are wrapper components that use componentDidCatch() to capture errors anywhere in their child component tree and display a fallback UI.
  + You can move the above code to a separate component. Then wrap any children components within the boundary component.
  + In the boundary component return error or `this.props.children`
+ ### Return Types
  + Multiple components can be returned in an array.

[Back to Main](../README.md)