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

[Back to Main](../README.md)