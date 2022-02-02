# 401 .NET Read 12: EF Core and APIs
[Microsoft docs: Setup Tutorial](https://docs.microsoft.com/en-us/aspnet/core/data/ef-mvc/intro?view=aspnetcore-5.0)<br>

EF Core is an Object-Relational Mapper.  It allows us to work with databases using objects by using a model made up of entity classes, and a context object.  The context object represents a session with the database and can allows querying and saving of data.

We can generate models from existing databases.  We can also write a model to match the database and us EF Migrations to evolve the database.

Instances of the entity class are retrieved with LINQ.

+ EF Core NuGet Packages
```
Install-Package Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore

Install-Package Microsoft.EntityFrameworkCore.SqlServer
```
### Data Seeding
[Microsoft docs: Data Seeding](https://docs.microsoft.com/en-us/ef/core/modeling/data-seeding)<br>
Data seeding is filling the database with starting data.  There are a few ways to do this in EF Core.  
+ Model Seed Data - seeding data is associated with the entity type as part of the model configuration.
  + This is best for static data that does not depend on anything else in the database.
+ Manual Migration - uses migration to perform CRUD actions to manually add data.
+ Custom Initialization - A way to perform data seeding before the main logic begins.  `DbContext.SaveChanges()`

### Secrets
[Enabling User Secrets](https://codefellows.github.io/code-401-dotnet-guide/resources/user-secrets.html)<br>
User secrets are like the .env from JavaScript.  It is a way to hold data such as API keys, that you don't want to made accessible to the public.

[Back to Mainpage](../code-fellows.md)<br>