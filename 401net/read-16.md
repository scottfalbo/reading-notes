# 401 .NET Read 16: Refactoring with DTOS
[Microsoft docs: Data Transfer Objects](https://docs.microsoft.com/en-us/aspnet/web-api/overview/data/using-web-api-with-entity-framework/part-5)<br>
[Using DTOs](https://www.infoworld.com/article/3562271/how-to-use-data-transfer-objects-in-aspnet-core-31.html)<br>

Data Transfer Objects let us add an extra layer of abstraction to our code, separating the client from the Database.

This allows us to massage the data from the database before sending it off as opposed to the user receiving the raw data.  We can hide properties, remove circular references and omit irrelevant data to reduce payload size.

DTOs are meant to transport data from one layer of an application to another.  They are serialized so they can be used independently of the language it's written in.  The consumer of the DTO might be another technology.

DTOs usually don't contain logic, just data.




[Back to the main page](../README.md) 