# 401 .NET Read 11: Entity Relationship Diagram (ERD)
`System.ComponentModel.DataAnnotations`

[Microsoft docs: data base model](https://docs.microsoft.com/en-us/aspnet/core/data/ef-mvc/complex-data-model?view=aspnetcore-2.0)<br>
[DBMS Overview](https://www.tutorialspoint.com/dbms/dbms_overview.htm)<br>

A database is a collection of related data. A **Data Management System** (DBMS) aides in retrieval, manipulation, and production of the information.

Modern DMBS use real world entities to layout it's architecture.  It uses the behavior and attributes of the data to help organize it.


## Schema
+ A database schema is a set of rules that governs the way the database holds its data.  It is often a visual representation, or a road map and holds no data itself.
+ The schema tells the program how users can interact with the database.
+ A schema drawing is similar to a UML.  It is a diagram of entities with connections made to it's attributes.

## Database Keys
Data keys help us identify unique records from the database.
+ The primary key is a column, or group of columns, that identifies every row in the table.
+ A foreign key creates a relationship between two tables.  This allows for navigation between the entities and attributes.
+ A composite key uniquely identifies each record.  These are used when you don't have a natural primary key.  Also called *surrogates*.
+ A primary key would access the top level, a foreign key helps access related attributes and entities and a composite key would be used for specific unrelated data.

## Relational Database
+ A 1:1 relationship is when one record is a table is associated with one record from another table.
+ A many:many relationship is when multiple records in a table associated with multiple records in another table.
+ 1:many is when one record in a table has many relationships with records in another table.
+ many:1 is the reverse in which many records have a relationship with one outside record.  


[Back to the main page](../README.md) 