## 201 Read-07 Notes: CSS Layout, chapter 15
*Re-vising Duckett HTMl and CSS chapter 15.*

[previous notes on chapter 15](read-04-notes.md)

### More on Float

+ **Clearing Floats**:  `clear: (left, right, both):` is used to make sure no other elements inside of the containing element touch the specified side.
+ **Parent of floated element**: If a containing element only contains floating elements some browsers will set the height of the element to 0px.
  + The following code in the parent element will fix this:
    + ```
      element {
        overflow: auto;
        width : 100%;
      }
      ```  
+ **Multi-column with float**: This will put three columns side by side be side within the containing element.
  + ```
    .col1, .col2, .col3 {
      width: 300px;
      float: left;
      margin: 10px;
    }
    ```
### Layout Grids

> Many designers use a grid structure to help plan and organize where elements will sit on their page.

*example grids on pages 389 and 390*

[previous notes on chapter 15](read-04-notes.md)

[Back to the main page](../README.md)


