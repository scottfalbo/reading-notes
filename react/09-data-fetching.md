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
+ ## Axios
  + Axios has some built in stuff that makes it a bit better than fetch() ike automatically making the response json.  It also allows for posting for data as well as fetching.
  + `npm install --save axios`
  + ```
    import axios from 'axios';
    ...
    componentDidMount() {
      axios.get('api end point')
        .then(response => {
          this.setState({
            whatever: response.data
          });
        })
        .catch()
    }
    ```

[Back to Main](../README.md)