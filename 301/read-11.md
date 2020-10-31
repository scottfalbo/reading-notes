# 301 Read-11: EJS

> EJS is a simple templating language that lets you generate HTML markup with plain JavaScript.

+ **getting started**
  + `npm install ejs body-parser`
    + `const bodyParser = require('body-parser');`
    + `app.use(bodyParser());`
  + `path` is a built in method in node.  It doesn't need to be installed but still needs to be brought in.
    + `const path = require('path');`
    + ```
      app.set('views', path.join(_dirname, 'views'));
      app.set('view engine', 'ejs');
      ```
      + `views` is a directory with an `*.ejs` file
    + ```
      response.render('index.ejs');
      ```  
+ **Evaluate an injected variable**
  + `.render` takes in 3 parameters. string of file name, object of local variables and a call back.
  + ```
    //server
    response.render('index', {name: Spaceghost});
    ```
    ```
    //*.ejs file
    <p> My cat's name is <%= name %>.</p>
    ```
+ **Iterate over an array**
  + ```
    //server
    response.render('index', {
      cats: [
        {name: Spaceghost},
        {name: Harry}
      ]
    });
    ```
    ```
    <ul>
      <% for(let i of cats){ %>
      <li><%= i.name %></li>
      <% } %>
    </ul>
    ```
+ **Conditionals**
  <!-- + ```
    <ul>
      <% for(let i of cats){ %>
        <% if(i.name === 'Spaceshost'){%>
          <li>Here is the loaf, <%= i.name %></li>
        <% }else{ %>
          <li>It's Mr. <%= i.name %></li>
        <% } %>
      <% } %>
    </ul>
    ``` -->
+ **Layouts**
  + Layouts are not native to EJS.  
    + `npm install --save express-ejs-layouts`
    + `const expressLayouts = require('express-ejs-layouts);`
    + `app.use(expressLayouts)`
  + `layout.ejs`
    + ```
      <body>
        <%- body %>
      </body>
      ```
+ **Partials**
   + Partials ar reused pieces of code like header, footer and head.

### File Structure 
```
- views
  - partials
    - footer.ejs
    - head.ejs
    - header.ejs
  - pages
    - index.ejs
    - page2.ejs
- package.json
- server.js
```
+ Partials are pieces of code that are reused a bunch of times.  Head, header and footer.
+ ```
  <head>
    <%- include('../partials/head'); %>
  </head>
  ```


[Google Books API docs](https://developers.google.com/books/docs/v1/using#WorkingVolumes)<br>
[EJS docs](https://ejs.co/)<br>



[Back to the main page](../README.md) 