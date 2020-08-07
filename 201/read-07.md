##201 Read-07 Notes: Domain Modeling, Tables, Functions, Methods and Objects

### Domain Modeling


### Tables, chapter 6
*Duckett html and css, pages 126-145*

+ > A **table** represents information in a grid format.
+ > Grids allow us to understand complex data by referencing information on two axes.
+ > Each block of the grid is referred to as a **table cell**.

**Basic Table Structure**
```
<table>
  <tr> //table row
    <th></th>  //table heading
    <td></td>  //table cell
    <td></td>  
  </tr>
</table>
```
The `<th>` element is a heading for a column or row and is utilized by screen readers to improve accessability.

+ Spanning Columns: spanning multiple horizontal cells.
  + `<td colspan="3">` 
+ Spanning Rows: spanning multiple vertical cells.
  + `<tr rowspan='2'>`

+ For better accessability and styling purposes it is best to use the following elements on longer tables.
  + `<thread>` is used to wrap the `<tr><th>`
  + `<tbody>` wraps the first set of `<tr><td>`
  + `<tfoot>` wraps the last set of `<tr><td>`


### Functions, Methods and Objects, chapter 3
*Duckett javascript, pages 106-144*




[Back to the main page](../README.md)