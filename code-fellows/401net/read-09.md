# 401 .NET Read 09: LINQ
### *Language Integrate Query*
### `using System.Linq`

LINQ unifies data access from multiple sources, and allows mixing of data from those different sources. So instead of having to learn a different type of query for each data source you are working with you can just use LINQ queries.

The basic make up of a data in LINQ are sequences and elements.  A sequence is any object that uses IEnumerable<>. (Arrays, Lists, Collections).  The elements are the items in the sequence.

A query is is made up of three actions:
  + Get the data source
  + Create the query, what are we looking for?
  + Execute the query, find the thing


+ ```
  int[] things = new in[]{1, 2, 3, 4, 5};

  int ThingQuery =
    from stuff in things
    where stuff == 2
    select stuff
  ```


[Microsoft docs: Query Operations](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/basic-linq-query-operations)<br>


We get a bunch of cool things like filtering, sorting, grouping and joining.  Basically all of the javaScript things that we can't normally do to arrays in C#.

Array are enumerable because the are arrays.  When working with data structures like a `List<>` the query looks like this:
  ```
  IEnumerable<Cats> catQuery =
    from cat in cats
    where cat.Girl == true
    select cat 

  foreach (Cats cat in catQuery)
    Console.WriteLine(cat);
  ```
This query will look at a `List<Cats>` full of `Cats` objects.  It checks cat.Girl for true and returns any objects that fit the condition.


[Back to Mainpage](../code-fellows.md)<br>