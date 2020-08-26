## 201 Read 12: Charts.js, Canvas


### Charts
[chart.js reading](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)<br>
[chart.js download](https://www.chartjs.org/docs/latest/)

> Charts are better for displaying data visually than tables.  They are easier to look at and convey data quickly.

`Charts.js` uses the `<canvas>` element to draw the graph to the screen.
  + `<script src="Chart.js"></script>`

+ Create canvas element:
  + `<canvas id="idName" width="500" height="400"></canvas>`
+ Retrieve context in JavaScript:
  + `var whatever = document.getElementById('idName').getContext('2d');`
+ `Chart.js` can make `.Line`, `.Pie` and `.Bar` charts.
  + The *chart.js reading* link above goes to syntax

[previous canvas experiments](https://scottfalbo.github.io/testing-lab/html/box-mover.html)<br>
[git link to code](https://github.com/scottfalbo/testing-lab/blob/master/js/box-mover.js)


## Canvas

### Basic Usage
[basic usage](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

+ The `<canvas>` element has two attributes, width and height.
+ You can supply the `<canvas>` with **Fallback Content**.
  + `<canvas><img src=""></canvas>`
+ **Rendering Context**.  The canvas creates a fixed-size drawing surface that exposes one or more rendering contexts.
  + `.getContext('2d')` is what we'll be looking at here.


### Drawing Shapes
[drawing shapes](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

+ 1 unit on the grid is equal to 1 pixel and origin is top left (0,0).
  + All elements are placed relative to this origin.  So to make a box `(x,y)` would represent the top left corner of the box and it would be `x` pixels from the left edge of the canvas and `y` pixels from the top edge.
+ **Drawing Rectangles**:
  + `fillRect(x, y, width, height)` draws a solid rectangle
  + `strokeRect(x, y, width, height)` draws rectangle outline
  + `clearRect(x, y, width, height)` clears specified area
+ **Drawing Paths**: A path is a list of points connected by segments of lines that can be different shapes.
  1. Create the path.
  2. Use draw commands to draw the path.
  3. Stroke or fill the path to render it.
+ *drawing shapes* link at the beginning of the section for more on path drawing.

### Applying Style and Color
[Applying style](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

+ **fillStyle and strokeStyle**
  + `fillstyle = color` used for filling shapes
  + `strokeStyle = color` used for shape outlines
+ Transparency, can change the opacity of shapes.
  + `globalAlpha = (0-1);` to set the opacity for all shapes being drawn
  + `rgba(150, 25, 45, 0.8)` or you can set the opacity of each shape with `alpha` using `rgba`
+ Line styles, Gradients, Patterns, and Shadows:
  + *Applying Style* link at beginning of section.


### Drawing Text
[Drawing text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)

+ The canvas rendering context provides two methods to render text:
  + `fillText(text, x, y [, maxwidth])` fills text at x,y
  + `strokeText(text, x, y [, maxwidth])` strokes text at x,y
+ Styling Text:
  + `varName.font = value` same syntax as CSS, `'10px san-serif'`.
  + `varName.textAlign = value` alignment setting, `start, end, left, right, center`.
  + `varName.textBaseline = value` baseline alignment, `top, hanging, middle, alphabetic, ideographic, bottom`.
  + `varName.direction = value` directionality, `ltr, rtl, inherit`
+ `measureText()` returns a `TextMetrics` object containing the width in pixels that the specified will text will be when drawn.

[Back to the main page](../README.md) 