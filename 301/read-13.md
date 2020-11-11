# 301 Read-12: Update and Delete

### Client Side: Sending Data
[from article](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)<br>
+ The `form` element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. The two most important attributes are `action` and `method`.
  + `<form action="/route">`
  + `<form>` with no attribute will be sent to the page it is on.
+ **The `method` Attribute** defines how the data is sent.
  + An HTTP request consists of two parts:
    + A `header` that contains a set of global metadata about the browser's capabilities.
    + A `body` that can contain information necessary for the server to process the specific request.
  + `GET` asks the server to send something back.  The browser sends an empty body so if a form was used the data sent will be appended to the URL.
  + `POST` talks to the server, and when asking for a response, takes into account data provided in the request.  Data from these forms are not appended to the URL.
    + When the form is submitted using the POST method, you get no data appended to the URL
+ You can see HTTP requests in the Chrome Dev Tools under the `Network` tab.

### Server Side: Retrieving Data
+ Which ever method you use the server will receive a string that is parsed into a list of `key:value` pairs.


## Styling forms
[video series on form styling](https://www.youtube.com/playlist?list=PL4cUxeGkcC9g5_p_BVUGWykHfqx6bb7qK);<br>
[tutorial repo](https://github.com/iamshaunjp/styling-html5-forms-playlist)



[Back to the main page](../README.md) 