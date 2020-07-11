# Scott's Reading Notes

<!-- chapter 10 -->
### CSS
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

<!--

chapter 11
vocab
RGB
HSL
Hex codes
Layout
Curly braces
-->



[Back to the mainpage](README.md)<br />
