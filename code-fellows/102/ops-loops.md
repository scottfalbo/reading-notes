## Operators and Loops

### Comparison and Logical Operators

*JavaScript and Jquery, pgs 150-151 and 156-157*

> You can **evaluate** a situation by comparing one value in the script to what you expect it might be.  Evaluating a **condition** results in a **boolean**.  This is a **comparison operator**.
+ `==` similarly equal to
+ `===` strict equal to
+ `!=` similarly not equal
+ `!==` strict not equal
+ `>` greater than
+ `<` less than
+ `>=` greater than or equal to
+ `<=` less than or equal to

> **Logical operators** allow you to compare the results of more than one comparison operator.

+ `&&` **Logical and**: If all expressions evaluate to `true` the result will be `true`.  If any part if `false` the result is `false`
    + `(( 34 > 21 ) && ( 13 > 8 ) && ( 5 > 3 ))` would return `true` because all conditions are met. 
+ `||` **Logical or**: If and part evaluates to `true` than the result is `true`.
    + `(( 5 > 8) || ( 13 > 21 ) || ( 34 < 55 ))` would evaluate to `true` because at least one of the conditions is `true`.
+ `!` **Logical not**: Inverts a single boolear value.  If it was `false` it will return `true`, if it was `true` it will return `false`.
    + `!( 34 < 21)` this will return `true` because 34 is not less than 21.

### `for` and `while` Loops
*JavaScript and Jquery, pgs 170-173 and 176*

> **Loops** check a conidiotn.  If it returns `true` a code block will run.  Then the condition will be checked again and if it still returns true it will run again.  It will keep running until the conidiotn returns false.
+ **For loop**: This will run a code a specific number of times.
    + ```
      for ( var i = 0; i < 6; i++ ){
          document.write(i);
      }
      for ( initialization; condition; update ){
          statement
      }
      ```
+ **While loop**: If you do not have a set number of times you want a loop to run use a a while loop.  The code will continue to loop for as long as the condition is `true`. 
    + ```
      var index =1;
      var msg = '';

      while ( i > 10){
          msg += index + ' x 5 = ' + ( index * 5) + '<br />';
      }
      ```
        + Take the variable `msg`
        + add the following to its value `+=`
        + the value of `index`

+ **Do While loop**: Almost the same as a while loop except it will always run the code in the `{}` at least once even if the condition evaluates to `false`


[Back to 201 class 02 notes](../201/class-2.md)<br>
[Back to 201 JS Control Flow](../201/notes-03.md)<br>
[Back to Mainpage](../code-fellows.md)<br>