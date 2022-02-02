# 301 Read-05: Heroku Deployment

## Heroku

+ Your Git repository contains your application as well as a `package.json` file, which is used by Node’s dependency manager.
+ `heroku create` prepares Heroku to receive your source code.
  + When you create an app, a git remote called `heroku` is also created and associated with your local git repo.
  + Heroku generates a random name for your app, or you can pass a name in as a parameter.
+ `git push heroku main` to Deploy the app
+ `heroku ps:scale web=1` ensure at least one instance of the app is running.
+ `heroku apps:rename serverName` to rename after creation
+ `heroku open` open the live app
+ **View Logs**
  + Heroku treats logs as streams of time-ordered events aggregated from the output streams of all your app and Heroku.
    + `heroku logs --tail`

## Node.js
[node.js, deploy to heroku](https://howtonode.org/deploy-blog-to-heroku)<br>

+ **Node.js** is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications.
+ Creating a simple server
+ ```
  let http = require("http");

  http.createServer((request, response) => {
    response.writeHead(200, {'Content-Type': 'text/plain'});
    response.write(`It's Alive!`);
    response.end();
  }).listen(3000);
  ```
  + Run `node filename.js` from the terminal then go to `localhost:3000` in the browser to see it.


+ This is an example of how Node provides you with non-blocking and event-driven behavior.
+ ```
  $.post('/some_requested_resource', function(data) {
    console.log(data);
  });
  ```
  + This code performs a request for some resource. When the response comes back, an anonymous function is called. It contains the argument data, which is the data received from that request.


[Back to Mainpage](../code-fellows.md)<br>