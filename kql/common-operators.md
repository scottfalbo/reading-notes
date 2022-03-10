# Common Operators

+ [search](#search)
+ [where](#where)
+ [take](#take)
+ [count](#count)
+ [summarize](#summarize)
+ [extend](#extend)
+ [project](#project)
+ [distinct](#distinct)
+ [top](#top)

---
 
+ ## `search`
+ Search across one or more table and one, or more column, for a value.
  + `search <> <value>`
  + `search "value"` - only matches exact value.
  + `search "*value*"` - wildcard.
  + `in (Table)`
    + same as:
    + ```
      Table
      | search ""
      ```
  + `kind=case_sensitive`
  + exact phrase in a column - `ColumnName=="value"`
  + partial phrase - `ColumnName:"value"`
  + `startswith "value"`
  + `endswith "value"`
  + `search "start*end"` begins with start, ends with end, and everything in between.
  + `search "value" and ("foo" or "bar")` - logical operators.
  + `search ColumnName matches regex "[A-Z]"` - can use regex.

---

+ ## `where`
+ Limits the result based on conditions.
  + `| where ColumnName == ""`
  + ```
    Table
    | where TimeStamp >= ago(1d)
        and ColumnOne == "valueOne"
        and ColumnTwo > "valueTwo"
    ```
+ 
  + `| where * has "value"` - looks in all columns.
  + `| where * hasprefix "value"` - any word begins with value.
  + `| where * hassuffix "value"` - any word ends with value.
  + `| where * contains "value"` - contains value anywhere.
  + `| where ColumnName matches regex "[A-Z]"` - supports regex.

---

+ ## `take`
+ Use take to grab n random number of rows from the data.
  + `| take 10` takes 10 random entries. 
  + Because results are random queries will return different data each time.

---

+ ## `count`
+ Returns the number of rows in a dataset.
    + `| count`

---

+ ## `summarize`
+ Aggregate function.
  + `| summarize function() by ColumnName, ColumnTwo`

---

+ ## `extend`
+ Create a calculated column and adds it to the result set.
  + `| extend NewColumn = ColumnCount / 5, NewColumnTwo = ColumnCount * 5`
    + By default created columns will appear all the way to the right in the output.

---

+ ## `project`
+ Selects subsets of columns to return.
  + `| project ColumnName, ColumnTwo, ColumnThree`
  + Combine project and extend.
  + ```
    | where ColumnName == "value"
    | extend NewData = CounterValue / 100,
             NewDataTwo = CounterValue * 100
    | project ColumnName,
              SomeOtherData,
              AndSomeMore
    ```
+
  + Project can simulate extend.
  + ```
    | project ColumnName,
              SomeOtherData,
              AndSomeMore,
              NewData = Counter + 10,
              NewDataTwo = Counter - 10
    ```
+
  + `| project-away HiddenColumn, DontShowMe` - hides defined columns.
  + `| project-rename MyNewColumn = ColumnName` - rename a column.

---

+ ## `distinct`
+ Returns a list of de-duplicated values.
  + `| distinct ColumnName`

---

+ ## `top`
+ Returns the first n rows.
  + `| top 10 by ColumnName desc` - top 10 rows ordered by ColumnName, descending.

---

[Back to KQL Index](kql-main.md)<br>
[Back to Main](../README.md)