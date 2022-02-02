# 301 Read-04: CSS Grid and Regex
### References/Resources
[css grid reference](https://css-tricks.com/snippets/css/complete-guide-grid/)<br>


## CSS Grid
[css grid garden](https://cssgridgarden.com/)

```
#container {
  grid-template-columns; 20% 20% 20% 20% 20%;
  grid-template-rows; 20% 20% 20% 20% 20%;
}

#thing {
  grid-column-start: 2;
  grid-column-end: 5;
}
```
+ The columns and rows are counted at the lines starting at the edge with 1.  You can use negative values.
+ `grid-column-end: span 2;` will span that many columns
+ `grid-column: 3/5;` is the short hand
+ `grid-area: <row start>/<column start>/<row end>/<column end>;`
+ `order: <value>;` will force an element into a certain spot
+ `grid-template-rows: repeat(5, 20%);` can be used as shorthand
+ `grid-template-columns: 1fr 4fr;` would be 1/4 or 20% 80% 
+ `grid-template: rows / columns` template shorthand

## Responsive Design with Grid
[article](https://medium.com/samsung-internet-dev/common-responsive-layouts-with-css-grid-and-some-without-245a862f48df)<br>
[design demo](https://grid-cats.glitch.me/)

+ Grid gives us control over how wide or narrow each of the *grid cells* get.
  + `grid-template-column: repeat(auto-fill, minmax(250px, 1fr));`
  + `auto-fill` will create as many tracks as it takes to fill the container.
  + `minmax(<min-size>/<max-size>)` 
  + `object-fit: cover;` keeps image size relative


## Regex: Treehouse Class Notes

+ `?` match if existing but does not require.  Looks at one space directly to the left.
+ `[]` character set.  Matches the characters or character ranges within.
  + Character range: `[A-Za-z]` `[0-9]`
  + regex matches all below entries
  + `/[tTJ]OY[ -]?[bB]oats?/`
    + toyboat
    + toyboats
    + toy boats
    + Toy boats
    + joy boats
    + toy-boats
    + toy-Boats

+ `\d` all digits
+ `\w` all characters, digits and _
  + `[A-za-z0-9_]`
+ `\s` all white spaces, tabes, returns
  + `\D` `\W` `\S` 'not'
+ `.` any character, inside `[]` its a literal '.'
+ `*` zero or more
+ `+` one or more
  + `/toy\w+/` = toyboat toycar
  + `/toy\w*/` = toyboat toycar toy

+ `{}` repetitions
  + `{3}` 3 times
  + `{3,}` 3 or more
  + `{3,5}` 3 to 5 times

+ `[^]` negate character set
  + `[^A]` matches any character that isn't an 'A'.

+ `|` alteration, 'or'

+ `(sub){2}` matches 'subsub'

+ `^` beginning of string
+ `$` end of string

[Back to Mainpage](../code-fellows.md)<br>