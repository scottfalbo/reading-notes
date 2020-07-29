## 201 Read-05, HTML Images, CSS Color and Text

### Images, chapter 5
*Duckett, html and css, 94-125*

Choosing images for your site:
  + Be relevant
  + Convey information
  + Convey the right mood
  + Fit the color palette

`<img src="imagesDir/filename.jpg" alt="" title="">`
+ `alt` Describes the image, important for accessability
+ `title` You can add a title to the image if you want to provide additional information.  It will usually show up in a tooltip when hovered over.

*When placed inline text will align with the bottom edge of the photo.*

+ Save images in the right format.
  + `.jpg` is best for images with many colors.
  + `.png` is best for images with few or one color.
    + `.png` also allows for use of non-square shapes if saved against a transparency layer.
+ Save images at the right size.
+ Measure images in pixels.

Use `<figure>` element to contain the `<img>` and `<figcaption>` so that the two are associated.


### Color, chapter 11
*Duckett, html and css, 246-263*

[previous notes from 102](../102/design-css.md)


### Text, chapter 12
*Duckett, html and css, 264-299*

The properties that are used to control fonts can be broken into two groups.
  + Those that directly affect the fonts appearance. **bold**, *italic*, and size are a few examples.
  + Those that have the same effect regardless of the font type.  color, spacing and kerning are examples.

*See page 271-272 for a ton of typeface info*

+ Specify typefaces with `font-family: value;`
+ Specify size of type with `font-size: value;`
  + Size values can be in px, em, or percentages.  `small`, `large`, `x-large` and other sizes work as well.

> `@font-face` allows you to use a font even if it's not installed on the user's machine.  Be cautious of license types. 

*See page 277 for reference on @font-face, also [www.fontsquirrel.com/fontface/generator](www.fontsquirrel.com/fontface/generator.com)*

+ Font styles: `font-weight`, `font-style`, `text-transform`, `text-decoration`, `line-height`, `letter-spacing`, `word-spacing`, `text-align`, `vertical-align`, `text-indent`, `text-shadow`.
  + *reference pages 279-289 for values to the above attributes.*
+ First letter or line:  You can specify values for the first letter or first line of text.
  + `p:first-letter {}`, `p:first-line {}`
+ Styling links: 
  + `a:link {}` will style an unvisited link
  + `a:visited {}` will style a visited link
+ Responding to user interaction:
  + `:hover` styles will be applies to an element while the user is hovering over it
  + `:active` will be applied will when activated by the user, mouse down.
  + `:focus` will be activated when an element has focus, such as an active text entry bar.

  #### Attribute Selectors

  > Attribute selectors let you create rules that apply to elements that have attributes with a specific value.

  + **Existence**: `[]` match a specific attribute no matter the value.
    + `section[class]` targets all `<section>` elements with attribute called `class`
  + **Equality**: `[=]` matches a specific attribute with a specific value.
    + `div[class="var"` targets any `<div>` elements with an attribute called `class` with a value of `var`.
  + **Space**: `[~=]` matches an attribute whose value appears in a space separated list. *multiple values*.
    + `figure[class~="thing3"]` targets any `<figure>` element with an attribute called `class` whose value is a list of values, one of which is `thing3`.
  + **Prefix**: `[^=]` matches an attribute whose value begins with a specific string.
    + `article[attr^"th"]` targets any `<article>` elements with an attribute whose value starts with `th`.
  + **Substring**: `[*=]` matches an attribute with a value that contain a specific substring.
    + `p[attr*"teh"]` targets any `<p>` elements with an attribute whose value contains the string `teh`.
  + **Suffix**: `[$=]` matches an attribute whose value ends a specific string.
    + `div[attr$"ism"]` targets any `<div>` element with an attribute whose value ends with the string `ism`.



[Back to the main page](../README.md)