# 301 Read-12: Update and Delete

> Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included.

+ There are three main reasons to normalize a database
  1. minimize duplicate data
  2. minimize and avoid modification issues
  3. simplify queries

It is best to make a database about a single thing instead of storing information about multiple things.  This can cause, *Insert Anomalies*, *Update Anomalies* and *Deletion Anomalies*.

+ There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively. 
  + **First Normal Form** – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
  + **Second Normal Form** – The table is in first normal form and all the columns depend on the table’s primary key.
  + **Third Normal Form** – the table is in second normal form and all of its columns are not transitively dependent on the primary key

[Back to the main page](../README.md) 