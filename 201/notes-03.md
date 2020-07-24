## 201 notes.  HTML lists, CSS boxes, JS control flow

### Lists
*html and css, pages 62-73*

+ **Ordered Lists**: A numbered list, used for listing steps.
  + ```
    <ol>
      <li></li>
      <li></li>
    </ol>
    ```
+ **Unordered Lists**: Bullet point list
  + ```
    <ul>
      <li></li>
      <li></li>
    <ul>
    ```
+ **Definition Lists**: Made up of terms and definitions.
  + ```
    <d1>
      <dt></dt>
        <dd></dd>
      <dt></dt>
        <dd></dd>
    </d1>      
    ```

You can also **nest** lists within lists:
```
<ul>
  <li></li>
  <li>
    <ul>
      <li></li>
      <li></li>
    </ul>
  </li>
</ul>
```

### Boxes
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


### Decisions and Loops
*JavaScript, pages 162-182*




[Back to the mainpage](../README.md)