## Read 14: Psychological Safety, CSS Transforms, Transitions, and Animations

> **Psychological safety** — a group culture that the Harvard Business School professor Amy Edmondson defines as a ‘‘shared belief held by members of a team that the team is safe for interpersonal risk-taking.’’ Psychological safety is ‘‘a sense of confidence that the team will not embarrass, reject or punish someone for speaking up,’’ Edmondson wrote in a study published in 1999. ‘‘It describes a team climate characterized by interpersonal trust and mutual respect in which people are comfortable being themselves.’’

[jump to CSS transitions](#css-transitions)<br>
[jump to CSS animations](#css-animations)

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

## CSS Transitions
[article link](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

+ For a transition to take place an element must have a change of state.
  + `:hover` `:focus` `:active` `:target`
+ There are four transition properties:
  + `transition-property` Determines what properties will be altered in conjunction with the transition properties.
    + `transition-property: background, border, scale();` 
    + **Transitional Properties** `background-color`, `background-position`, `border-color`, `border-width`, `border-spacing`, `bottom`, `clip`, `color`, `crop`, `font-size`, `font-weight`, `height`, `left`, `letter-spacing`, `line-height`, `margin`, `max-height`, `max-width`, `min-height`, `min-width`, `opacity`, `outline-color`, `outline-offset`, `outline-width`, `padding`, `right`, `text-indent`, `text-shadow`, `top`, `vertical-align`, `visibility`, `width`, `word-spacing`, `z-index`
  + `transition-duration` Sets the duration of the transition in `s` -seconds or `ms` -milliseconds.  If there are multiple properties each duration may be specified.
    + ```
      transition-property: color, border-color, opacity;
      transition-duration: 1s, .5s, .8s;
      ```
  + `transition-timing-function` 
    + `linear;` Moving in a constant speed from one state to another.
    + `ease-in;` Starts slowly and speeds up throughout the transition
    + `ease-out;` Starts quickly and slows down
    + `ease-in-out;` Starts slowly, speeds up in the middle, then slows down.
    + ```
      transition-property: color, border-color, opacity;
      transition-duration: 1s, .5s, .8s;
      transition-timing-function: linear, ease-in, ease-out;
      ```
  + `transition-delay` Sets a delay before the transition happens.
+ Transition Shorthand
  + `transition: background .5s linear 1s;`
  + transition: *property* *duration* *timing* *delay*;


## CSS Animations
[article link](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

+ **Animation Keyframes**
  + > To set multiple points at which an element should undergo a transition, use the `@keyframes` rule. The `@keyframes` rule includes the animation name, any animation breakpoints, and the properties intended to be animated.
  + ```
    @keyframes animationName {
      0% {
        thing to change
      }
      50% {
        thing to change
      }
      100% {
        thing to change
      }
    }
    ```
    + Keyframe Vendor Prefixes:
    + ```
      @-moz-keyframes
      @-o-keyframes
      @-webkit-keyframes
      ```
+ **Animation Name**
  + > Once the keyframes for an animation have been declared they need to be assigned to an element. To do so, the `animation-name ` property is used with the animation name.
    + `animation-name: animationName;`
+ **Animation Duration, Timing Function and Delay**  
  + `animation-duration` As with transitions, the duration may be set in seconds or milliseconds.
  + `animation-timing-function:` and `animation-delay:` both work the same as with transitions as well.
+ **Customizing Animation**
  + `animation-iteration-count:` can have an integer value or `infinite` to loop forever.
  + `animation-direction:`
    + `normal` plays as intended from beginning to end.
    + `reverse` plays opposite as identified in the `@keyframes`.
    + `alternate` plays normal and then reverse.
    + `alternate-reverse` plays reverse and then normal.
      + Both directions count as an iteration when using `alternate`
  + `animation-play-state:` lets you start and stop and animation.
    + `running` plays the animation
    + `paused` pauses the animation in its current place and restarts from that same spot.
  + `animation-fill-mode` Defines how an element should be styled either before, after, or before and after an animation is run.
    + `none` will apply no style before or after.
    + `forwards` keep the style declared in the last specified keyframe.
    + `backwards` apply style from the first specified keyframe.
    + `both` applies both `forward` and `backwards` values.
**Short Hand Animation**
  + Just like transitions animations can be done short hand.
  + ```
    .className:hover .thing {
      animation-name: mover;
      animation-duration: 3s;
      animation-timing-function: linear;
      animation-daley: .5s;
      animation-fill-mode: forwards;
    }
    .className:active .thing {
      animation-play-state: paused;
    }
    ```
  + ```
    .className:hover .thing {
      animation: mover 3s linear .5s forwards;
    }
    .className:active .thing {
      animation-play-state: paused;
    }
    ```

[Back to the top](#read-14-psychological-safety-css-transforms-transitions-and-animations)<br>
[Back to Mainpage](../code-fellows.md)<br>
