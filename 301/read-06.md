# 301 Read-06: node.js

[sitepoint article](https://www.sitepoint.com/an-introduction-to-node-js/)<br>

> **Node.js** is a JavaScript runtime built on Chrome’s V8 JavaScript engine.  It is an event-based, non-blocking, async I/O runtime.

+ The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers
+ Unlike JavaScript which must be run in a browser, Node can be run in a terminal.
+ *npm* is the 'node package manager'
  + In addition to being the package manager for JavaScript, npm is also the world’s largest software registry.
  + `npm install <package name>`
+ Installing npm will create a `node_modules` directory.  This is where it saves libraries that node will use.
+  It also creates a `package.json` that will have the dependencies for installed libraries.

+ **What is Node used for:**
  +  Installing (via npm) and running (via Node) various build tools
     + > These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.
      + Modern JavaScript Framework such as React will require a working knowledge of node and npm.
  + Running JavaScript on the server.
    + Node.js is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event.
    + Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections.
  + ![](https://uploads.sitepoint.com/wp-content/uploads/2012/10/1516152673node_event_loop.png)
  + The fact that Node runs in a single thread does impose some limitations. For example, blocking I/O calls should be avoided
+ ```
  const http = require('http');

  http.createServer((request, response) => {
  response.writeHead(200);
  response.end('Hello, World!');
  }).listen(3000);

  console.log('Server running on http://localhost:3000');
  ```
    1. Require Nodes native `HTTP module`
    2. Use `createServer()` to create a new web server object. The anonymous function is called with two arguments `(request and response)`.
    3.  Then we listen on port 3000.
+ Node is good for applications that require real-time interaction or collaboration.  

> Aside from speed and scalability, an often-touted advantage of using JavaScript on a web server — as well as in the browser — is that your brain no longer needs to switch modes. You can do everything in the same language 

[Back to the main page](../README.md) 