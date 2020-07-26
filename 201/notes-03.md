## 201 notes.  HTML lists, CSS boxes, JS control flow

## Lists
*html and css, pages 62-73*

+ **Ordered Lists**: A numbered list, used for listing steps.
+ **Unordered Lists**: Bullet point list.
+ **Definition Lists**: Made up of terms and definitions.
  + ```
    <d1>
      <dt></dt>
        <dd></dd>
      <dt></dt>
        <dd></dd>
    </d1>      
    ```
+ You can also **nest** lists within lists


## Boxes
*html and cs, pages 300-329*

> CSS treats each element in HTML as a box.
+ Control the dimensions of your boxes
  + control the **width** and **height** of a box.
    + ```
      section {
        width: 960px;
        height: 200px;
      }
      ```
  + You can **limit** the **width** and **height**.  This if a browser is resized or if the content is being viewed on mobile as opposed to a monitor.
    + ```
      section {
        min-width: x;
        max-width: x;
        min-height: x;
        max-height: x;
      }
      ```
  + **Overflowing Content**: The overflow property tells the browser what to do if the content is larger than the box.
    + `overflow: hidden;`  `overflow: scroll;`
 
+ control borders, margins and padding
  + `border:` `margin:` `padding:`
    + top, right, bottom, left
+ hide elements, make them inline, block-level, inline-block
  + `display: hide` 
  + `display: inline;`
+ Legibility can be improved by controlling the width of boxes containing text.
  + `min-width` `max-width` `overflow`
+ CSS3 can create image borders and rounded borders

*For more reference 308-322 Duckett, HTML and CSS*


## Decisions and Loops
*JavaScript, pages 162-182*

### Switch Statements
> A **swtich** statement starts with a variable called the **switch value**.  Each case indicates a possible **value** for this variable.
```
switch (varName) {
  case 'n1':
    //do something
    break;
  
  case 'n2':
    //do something
    break;
  
  default:
  //do something
  break;
}
```
> The above script checks the value of the variable `varName`.  If `varName === n1` it does the first thing.  If `varName` does not equal any of the cases the statements in `default` are run.

> **Type Coercion**:  JavaScript will change a variable type to complete an operation.  For example `'6' > 4` will evaluate true because the string `'6'` will automatically be converted to an number.

### Truthy & Falsy Values
> Due to **type coercion** every value in JavaScript can be treated as if it were `true` or `false`.  Falsy values can also be treated as `0` and truthy values can be treated as `1`.
  + Falsy values: `varName = false;`, `varName = 0;`, `varName ='';`, `varName = NaN` or `varName` is undeclared.
  + Almost everything that isn't a falsy is treated as true.

> Because the presence of an **object** or **array** can be considered truthy, it is often used to check for the existence of an element within a page.

*reference pages 168 and 169, Duckett, HTML and CSS for falsy/truthy rules.*


[Previous notes on While, Do While, and For Loops](../102/ops-loops.md)


[Back to the main page](../README.md)