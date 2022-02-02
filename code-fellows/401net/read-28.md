# 401 .NET Read 28: MVC Forms
[Microsoft docs: Views](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/overview?view=aspnetcore-2.2)<br>

The *View* is the part of our application that presents the data to the front end.  We accomplish this by adding a `View` folder to our app.  The view folder contains `.cshtml` files who's names coincide a controller.  

We can use layouts, partials and components, to build reusable parts of code, like headers and footers.

Using a view offers a separation of concerns by separating the UI markup from other parts of the application.  It helps with organization, and because the parts of the app are loosely coupled changing any one part becomes easier.

When controllers return a view they can send data to the view for use during rendering.

---

+ ### Types of Forms
  + Weakly typed - sends in a viewbag.  This is good for one or two pieces of data.
  + Strongly typed - sends an object, usually built from a view model, to the front.
  + Strongly typed AJAX -  
  + HTML, AJAX, and JQuery - 

[Back to Mainpage](../code-fellows.md)<br>