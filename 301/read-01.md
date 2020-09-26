# 301 Read 01: SMACSS and Reponsive Web Design
*Scalable and Modular Architecture*<br>

[all about floats](#all-about-floats)<br>


## Intro to Responsive Web Design
[link](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)<br>
> Responsive web design is the practice of building a website suitable to work on every device and every screen size.

  + **Responsive Design**: React quickly and positively to any change.
  + **Adaptive Design**: Easily modified for a new purpose or situation
  + **Mobile Design**: Separate site for mobile specific, *not good practice*.

### **Responsive web design** is broken into three main components.

### Flexible Layouts

+ **Flexible Layouts**: The practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width. Flexible grids are built using relative length units.

<br>

### Media Queries

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
    + `height` and `width` features are based off the height and width of the viewport rendering area.
      + `@media all and (min-width 320px) and (max-width: 780px){}`
    + `orientation` determines whether the device is `landscape` or `portrait`.
      + `@media all and (orientation: landscape) {}`
    + `aspect-ratio` and `device-aspect-ratio` features specifies the `width`/`height` **pixel ratio** of the targeted rendering area or output device. 
      + The value for the aspect ratio is `width` / `height`.
      + `@media all and (min-device-aspect-ratio: 16/9){}`
        + `device-pixel-ratio` is great for identifying high definition devices.
  + **Mobile First**
    + Using styles targeted at smaller view ports as the default styles, then use media queries to add styles as the viewport grows.
      + ```
        @media screen and (min-width: 400px){}
        @media screen and (min-width: 600px){}
        @media screen and (min-width: 1000px){}
        @media screen and (min-width: 1400px){}
        ```
    + > Generally speaking, avoiding CSS3 shadows, gradients, transforms, and animations within mobile styles isn’t a bad idea either. When used excessively, they cause heavy loading and can even reduce a device’s battery life.

### The View Port

  + The `viewport` meta tag helps identify the `size`, `scale`, and `resolution` of a website for mobile devices.
    + `<meta name="viewport" content="width=device-width">`
      + Letting devices know the intended width of the website allows the website to be sized properly and to pick up any qualifying media queries.
  + **Viewport Scale**
    + To control how a website is scaled on a mobile device, and how users can continue to scale a website, use the `minimum-scale`, `maximum-scale`, `initial-scale`, and `user-scalable` properties.
    + The `initial-scale` is a value between 1 and 10.  1 being normal 100% view.
  + `minimum-scale` and `maximum-scale` values determine how large or small a viewport may be scaled.
  + `user-scalable` can be set to yes or no.  If no the user cannot change the scale of the site.  *This is generally not a good idea.*
  + You can combine viewport values
    + `<meta name="viewport" content="width=device-width, initial-scale=1">`
    + The viewport rules can also be implemented in CSS
      + ```
        @viewport {
          width: device-width;
          zoom: 1;
        }
        ```
<br>

### Flexible Media

+ **Flexible Media**: Media types need to be scalable, changing their size as the size of the viewport changes.
  + One quick way to make media scalable is by using the max-width property with a value of 100%.
    + ```
      img, video, canvas {
      max-width: 100%;
      }
      ```
  + **Embedded Media** does not automatically scale.  The work around is to put it in a parent container and set media's `position` to `absolute` so it scales with the parent container.
    + ```
      figure {
        height: 0;
        padding-bottom: 56.25%; /* 16:9 */
        position: relative;
        width: 100%;
      }
      iframe {
        height: 100%;
        left: 0;
        position: absolute;
        top: 0;
        width: 100%;
      }
      ```
  

## All About Floats
[link](https://css-tricks.com/all-about-floats/)<br>


## Don't Over Think Grids
[link](https://css-tricks.com/dont-overthink-it-grids/)<br>


## CSS floats
[link](https://www.freecodecamp.org/news/css-floats-explained-by-riding-an-escalator-57fa55232333/)<br>


## Official SMACSS Documentation
[link](http://smacss.com/)<br>


[Back to the main page](../README.md) 