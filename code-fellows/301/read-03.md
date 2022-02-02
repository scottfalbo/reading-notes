# 301 Read-03: Mustache and Flexbox

## Templating with Mustache
[article link](https://medium.com/@1sherlynn/javascript-templating-language-and-engine-mustache-js-with-node-and-express-f4c2530e73b2)

> **Javascript Templating**:<br>
Javascript templating is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. The template is HTML markup, with added templating tags that will either insert variables or run programming logic.<br>
The template engine then replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.

### Mustache

+ Mustache is a logic-less syntax template system.
  + It works by expanding tags in a template using provided values.
  + It is referred to as logic-less because there are no if else statements or loops.
  + `Mustache.someName('hello, {{variable}}', {variable: 'value'});`
  + The `{{  }} is mustache syntax to show that it's a **placeholder**.


1. Configure mustache-express in your JavaScript file.
2. Create a folder with html view templates.
3. Then in the router configuration, use `res.render(TEMPLATE_NAME, JSON_DATA)`

[Mustache Documentation](https://github.com/janl/mustache.js/blob/master/README.md)

## Flexbox
[article link](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

+ **Properties for the PARENT container**: `display: flex;` or `inline-flex;`
  + This enables a flex context for all direct children.
  + Flex basically lays out item on horizontal rows or vertical columns.  
  + `flex-direction:`
    + `row;` (default): left to right in ltr; right to left in rtl
    + `row-reverse;` right to left in ltr; left to right in rtl
    + `column;` same as row but top to bottom
    + `column-reverse;` same as row-reverse but bottom to top
  + By default flex items will try to fit on one line.
  + `flex-wrap:`
    + `nowrap;` (default): all flex items will be on one line
    + `wrap;` flex items will wrap onto multiple lines, from top to bottom.
    + `wrap-reverse;` flex items will wrap onto multiple lines from bottom to top.
  + `flex-flow` is the short hand for `direction` and `wrap`
    + `flex-flow: column wrap;` default is `row` `nowrap`
  + **Justify content** defines the alignment along the main axis.
  + `justify-content:`
    + `flex-start;` (default): items are packed toward the start of the flex-direction.
    + `flex-end;` items are packed toward the end of the flex-direction.
    + `center;` items are centered along the line
      + There are also two additional keywords you can pair with these values: `safe` and `unsafe`. Using `safe` ensures that however you do this type of positioning, you can’t push an element such that it renders off-screen.
  + **Align-items** defines how flex items are laid out along the cross axis.
  + `align-items:`
    + `stretch;` (default): stretch to fill the container (still respect min-width/max-width)
    + `flex-start;`, `start;`,  `self-start;` items are placed at the start of the cross axis.
    + `flex-end;`, `end;`, `self-end;` items are placed at the end of the cross axis.
    + `center;` items are centered in the cross-axis
    + `baseline;` items are aligned such as their baselines align
    + `safe` and `unsafe` modifiers work here as well.
  + **Align-content** aligns a flex container’s lines within when there is extra space in the cross-axis.
    + `align-content;`
      + `normal;` (default): items are packed in their default position as if no value was set.
      + `flex-start;`, `start;` items packed to the start of the container. 
      + `flex-end;`, `end;` items packed to the end of the container. 
      + `center;` items centered in the container 
      + `space-between;` items evenly distributed; the first line is at the start of the container while the last one is at the end
      + `space-around;` items evenly distributed with equal space around each line
      + `space-evenly;` items are evenly distributed with equal space around them
      + `stretch;` lines stretch to take up the remaining space
+ **Properties for the CHILDREN (flex items)**:
  + **Order**: By default, flex items are laid out in the source order. However, the order property controls the order in which they appear in the flex container.
    + `order: 3;` default is 0
  + **Flex-grow** defines the ability for a flex item to grow if necessary.
    + If all items have flex-grow set to 1, the remaining space in the container will be distributed equally to all children.
    + `flex-grow: 2;` default is 0
  + **Flex-shrink** defines the ability for a flex item to shrink if necessary.
    + `flex-shrink: 3;` default is 1
  + **Flex-basis** defines the default size of an element before the remaining space is distributed. If set to 0, the extra space around content isn’t factored in. If set to `auto`, the extra space is distributed based on its `flex-grow` value.
    + `flex-basis: auto;` default is auto
  + **Flex** is a short hand for `flex-grow`, `flex-shrink` and `flex-basis`
    + `flex: <flex-grow> <flex-shrink>*opt* <flex-basis>*opt*;`
  + **Self-align** allows the default alignment to be overridden for individual flex items.
    + `align-self: auto | flex-start | flex-end | center | baseline | stretch;`


[Back to Mainpage](../code-fellows.md)<br>