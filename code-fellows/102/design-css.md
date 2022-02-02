[jump to chapter 11](#color)

<!-- chapter 10 -->
## CSS
*Chapter 10*
+ CSS, or Cascading Style Sheet, allows you to create rules that control how elements will appear on your site.
+ CSS works by associating rules with HTML elements.  These rules control how the content of the specified element, or elements, should be displayed.
+ A CSS rule contains two parts, a **selector** and a **declaration**.
    + ```
        body{
            font-family: Arial;}
      ```
      + in the above code the `body` is the selector and `font-family: Arial;` is the declaration.
+ The selector indicates which element to apply the rule to.  You can have multiple elements seperated with comma's.
+ The declaration is how the element is to be styled.  The declaration is made up of two parts.  `property: Value;`

## Implementing CSS

### Using External CSS
**HTML portion**

This is contained within the `<head></head>`
```
<head>
    <link href="css/styles.css" type="text/css" rel="stylesheet" />
</head>
```
+ The `link` element can be used to tell the HTML where to find the CSS file used.
+ `href` is telling it where the file is.  You can link to multiple stylesheets.
+ `type` specifies the type of document being linked to.  The value should be `text/css`
+ `rel` specifies the relationship between the HTML and the file we are linking to.  When linking to CSS we use `stylesheet` as the value.

**CSS Portion**

```
body {
    font-family: arial;
    background-color: rgb(x,x,x);}
h1 {
    color: rgb(x,x,x);}
```
### Using Internal CSS

**Internal CSS** is contained within the HTML file.  It is best to use a seperate file, but this works too for smaller single page stuff.

To implement internal CSS you use the `<style></style>` element within the `<head></head>`.  The `type` value should be `text/css`.
```
<head>
    <style type="text/css">
        body {
            font-family: arial;
            background-color: rgb(x,x,x);}
        h1 {
            color: rgb(x,x,x);}
    </style>
</head>
```
### CSS Selectors
Bookmarked CSS selectore reference page:
[w3schools.com](https://www.w3schools.com/cssref/css_selectors.asp)

**How Class Rules Cascade**
+ *Last Rule*: If two selectors are identical the latter of the two will take precedence.
+ *Specificity*: If one selector is more specific than another it will take precedence.
+ *Important*: You can add `!important` after any property value to indicate it is the most important rule to apply to the element.

Some properties are inherited by child elements.  For instance defining the `font-family` property in the `<body>` would also apply that property to most child elements.

You can force a property to inherit it's parents property by putting `inherit` as the value.

## Color
*Chapter 11*

You can specify color one of three ways:
+ **RBG values**: This expresses color in terms of how much red, green and blue are used to make it up. `rgb(x,x,x)`
+ **Hex Codes**: This is the 6 digit code to an rgb value.   `#ee3e80`
+ **Color Names**: There are 147 predefined color names that are recognized. `red`, `white`, `green`
    + [recognized color names](https://www.w3schools.com/colors/colors_names.asp)

`color: rgb(x,x,x);` - `color: #ee3e80;` - `color: green;`

Each element is considered a box, and each box has a background color. `background-color: white;` will set that box to a specific color.

**Opacity**
The opacity value is between 0.0 and 1.0.  
+ `opacity: 0.3;`  would set the opacity to 30%

In CSS3 you can define opacity along with color using `rbga`.  The added `a` is an *alpha value*.
+ `background-color: rgba(x,x,x,a)`  where `a` is 0.0 - 0.1

#### CSS3 HSL Colors
Hue, Saturation, Lightness
+ saturation: `0.0` = full grey, `1.0` = full saturation
+ lightness: `0.0` = black, `1.0` = white, 50% is normal

`color: hsl(h,s,l);`
+ Hue is expressed by an angle between 0 and 360.
+ Saturation and Lightness are expressed by a % of 0-100

Like `rgba` you can do `hsla` to specify the `alpha value` 

`color: hsla(90,100%,50%,0.9);`

### Accessabiilty Considerations
+ Add enough color contrast.
+ Don't use color alone to make information stand out.
+ Design usable focus states
    + focus indicators show what element the keyboard has focus on.
+ Use labels or isntructions with form fields and input prompts.
    + placeholder text is often skipped over by accessibility features and a title is better.
+ Useful `alt` text for images.  Be descriptive and meaningful.
+ Use correct markup on your content.
    + it's important to use proper structural elements.  Do not use HTML tags for style.
+ Support Keyboard navigation.
    + The order of interactive elements is essential.






[back to read 02 notes](../201/class-02.md)<br>
[back to read 05 notes](../201/read-05.md)<br>
<br>

[Back to Mainpage](../code-fellows.md)<br>
