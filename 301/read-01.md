# 301 Read 01: SMACSS and Reponsive Web Design
*Scalable and Modular Architecture*

## Intro to Responsive Web Design
[link](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)<br>
> Responsive web design is the practice of building a website suitable to work on every device and every screen size.
  + **Responsive Design**: React quickly and positively to any change.
  + **Adaptive Design**: Easily modified for a new purpose or situation
  + **Mobile Design**: Separate site for mobile specific, *not good practice*.



### **Responsive web design** is broken into three main components.
+ **Flexible Layouts**: The practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width. Flexible grids are built using relative length units.

<br>

+ **Media Queries**: Provide the ability to specify different styles for individual browser and device circumstances.
  + `@media`: Each media query may include a media type followed by one or more expressions.
    + Common media types: `all`, `screen`, `print`, `tv`, `braille`.  If not defined the default type is `screen`.
    + the expression that follows the type can be true or false.  When true the style is applied.
    + Logical Operators: `and`, `not`, `only`
      + `and` allows and extra condition to be added.
        + `@media all and (min-width: 800px) and (max-width: 1024px){}`
        + selects all media types between 800px and 1024px wide.
      + `not` negates the query, specifying any query but the one identified.
      + `only` selects specific 
    + When using `not` or `only` the media type may be omitted making it `all` by default.
  + **Media Features**
    + Media features identify what attributes or properties will be targeted within the media query expression.
    + The `height` and `width` features are based off the height and width of the viewport rendering area.
      + `@media all and (min-width 320px) and (max-width: 780px){}`
    

<br>

+ **Flexible Media**: 

## All About Floats
[link](https://css-tricks.com/all-about-floats/)<br>


## Don't Over Think Grids
[link](https://css-tricks.com/dont-overthink-it-grids/)<br>


## CSS floats
[link](https://www.freecodecamp.org/news/css-floats-explained-by-riding-an-escalator-57fa55232333/)<br>


## Official SMACSS Documentation
[link](http://smacss.com/)<br>


[Back to the main page](../README.md) 