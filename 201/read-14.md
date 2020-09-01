## Read 14: Psychological Safety, CSS Transforms, Transitions, and Animations

> **Psychological safety** — a group culture that the Harvard Business School professor Amy Edmondson defines as a ‘‘shared belief held by members of a team that the team is safe for interpersonal risk-taking.’’ Psychological safety is ‘‘a sense of confidence that the team will not embarrass, reject or punish someone for speaking up,’’ Edmondson wrote in a study published in 1999. ‘‘It describes a team climate characterized by interpersonal trust and mutual respect in which people are comfortable being themselves.’’

## CSS Transforms
[article link](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

> `transform` **Property**: General layout techniques with alternative ways to size, position, and change elements.<br>
The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

+ Browser support for `transform` isn't always great.  Vendor prefixes are encouraged for the best support.
  + ```
    element {
      -webkit-transform: scale(1.5);
      -moz-transform: scale(1.5);
      -o-transform: scale(1.5);
      transform: scale(1.5);
    }
    ```
    + This includes multiple vendor prefixes.  The last un-prefixed `transform` will overwrite the others if the browser has full support.

### 2D Transforms
+ `transform:` property values:
  + `rotate(60deg);` rotate the element
  + `scale(.5);` change the size of an element, 1 is default
    + You can scale just the height or width of an element with `scaleX` and `scaleY`.
    + `scaleX(.5)` and `scaleY(1.25)`: shorthand: `scale(.5, 1.25);`
  + `translate` Push and pull the position of an element without interrupting the normal flow.
    + `translateX(value);` `translateY(value);`
    + `translate(xValue, yValue);`
  + `skew(x,y);` distorts an element on the horizontal or vertical axis.
+ Combining `transforms`:
  + `transform: rotate(30deg) scale(1.5) skew(15deg, 30deg);`
+ `transform-origin: x y;` The default transform origin is the dead center of an element.
+ `perspective();` is like a vanishing point.  The higher the value the further away the vanishing point will appear.
  + you can add perspective to single element or to a group by applying the property to the parent element.
  + `perspective-origin: x y;`


### 3D Transforms
+ 2D transforms alter the x and y axes.  Using 3D dimensional transforms you can change elements on the z axes, `rotateZ`.
+ `scaleZ` scales the element on the z axes
+ `translateZ` Push the z Axes away or bring it closer.
+ `transform-style;`
+ > On occasion three-dimensional transforms will be applied on an element that is nested within a parent element which is also being transformed. In this event, the nested, transformed elements will not appear in their own three-dimensional space. To allow nested elements to transform in their own three-dimensional plane use the `transform-style` property with the `preserve-3d` value.
+ `backface-visibility;`
+ > When working with three-dimensional transforms, elements will occasionally be transformed in a way that causes them to face away from the screen. This may be caused by setting the `rotateY(180deg)` value for example. By default these elements are shown from the back. So if you prefer not to see these elements at all, set the `backface-visibility` property to `hidden`, and you will hide the element whenever it is facing away from the screen.



[Back to the main page](../README.md) 