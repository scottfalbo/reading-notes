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
+ `search <> <value>`
+ Search across one or more table and one, or more column, for a value.
  + `search "value"` : only matches exact value.
  + `search "*value*"` : wildcard.
  + `in (Table)`
    + same as:
    + ```
      Table
      | search ""
      ```
  + `kind=case_sensitive`
  + exact phrase in a column `ColumnName=="value"`
  + partial phrase `ColumnName:"value"`
  + `startswith "value"`
  + `endswith "value"`
  + `search "start*end"` begins with start, ends with end, and everything in between.
  + `search "value" and ("foo" or "bar")` logical operators.
  + `search ColumnName matches regex "[A-Z]"` can use regex.

---

+ ## `where`
  + stuff
+ ## `take`
  + stuff
+ ## `count`
  + stuff
+ ## `summarize`
  + stuff
+ ## `extend`
  + stuff
+ ## `project`
  + stuff
+ ## `distinct`
  + stuff
+ ## `top`
  + stuff



---

[Back to KQL Index](kql-main.md)<br>
[Back to Main](../README.md)