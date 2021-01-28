# 401 .NET Read 14: Routing and Navigation Properties

## MVC Routing
[Microsoft docs: MVC Routing](https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions-1/controllers-and-routing/asp-net-mvc-routing-overview-cs)<br>

Routing is the codes way taking incoming information from the browser, using a controller to figure out what to do with it, and then returning a response.

At runtime the routing engine will match incoming urls with the urls defined in the route table.

When the routing engine finds a matching url in the route table, it calls the appropriate controller and does the things. 

A routes default parameters are:
+ `new { controller = "Home", action = "Index", id = "" }`
+ HomePage/Users/7
  + controller = HomePage
  + action = Users
  + id = 7

<br>

## Routing in ASP.NET Core
[Microsoft docs: Routing in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/routing?view=aspnetcore-3.1)<br>

Routing basically connects the front to the code by taking in requests, and getting those requests to the proper `EndPoint`. 
The `EndPoint` extracts the information from the provided request, and sends it off for processing. 

### middleware - the go between pipeline
+ `UseRouting` - Looks at all sets of Endpoints and finds the best match.
+ `UseEndpoints` - Runs the delegate associated with the selected endpoint.

Each Endpoint is a functional unit, and distinct from other Endpoints.

<br>

[Back to the main page](../README.md) 