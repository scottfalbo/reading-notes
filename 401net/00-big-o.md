# 401 .NET Pre-Work: Big O Notation

## Big O Notation
+ Big O basically figures out the amount of resources an algorithm needs and allocates enough for the worst case max scenario.
+ `O(1)` - Describes an algorithm that will always execute in the same time regardless of the size of the input data.
  + *a single return element or variable*
+ `O(N)` - Describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set.
  + *one dimensional loop iteration*
  + In the case of a loop iterating through an array enough resources will be allocated to perform the entire iteration whether it stops short or not.
+ `O(N²)` - Represents an algorithm whose performance is directly proportional to the square of the input data.
  + A common case of this would be nested iterations.
  + `O(N³)`.... and so on depending on how many iterations are nested
+ O(2<sup>n</sup>) - Denotes an algorithm whose growth doubles with each addition to the input data set.
  + This is an exponential growth curve.
  + A common case of this would be recursion.
+ **Logarithms**
+ `O(log N)` - This would represent a binary search which would have a growth curve that peaks at the beginning and slowly flattens in size as the data set is halved.


[Back to the main page](../README.md) 