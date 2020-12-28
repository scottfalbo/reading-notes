# Data Fetching

+ ## `fetch()`
  + ```
    //set state
    ...
    componentDidMount() {
      fetch('api end point')
        .then(response => response.json)
        .then(responseData => {
          this.setState({ whatever: responseData});
        })
    }
    ...
    ```
  

[Back to Main](../README.md)