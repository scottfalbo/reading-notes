# 401 .NET Read 31: Razor Pages

Razer Pages is similar to Razer Views and a built in part of the MVC Framework.  The main difference is that Razer Pages are an MVC action and do not need a controller to operate.
They take in a `using` directive and a `class`, and can then access that classes props in the view.  This is useful in small projects where having separate models and controllers might be overkill.

To separate logic while using Razer pages you can put a another file behind it.  So each `.cshtml` view has another `.cshtml.cs` file behind it which does work so the view doesn't.





[Back to the main page](../README.md) 