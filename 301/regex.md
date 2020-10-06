# Regex: Treehouse Class Notes

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

[Back to the main page](../README.md) 