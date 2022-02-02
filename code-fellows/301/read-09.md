# 301 Read-09: Refactoring
[refactoring javascript for readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)<br>

## Refactoring for Performance and Readability

> There's a middle ground between speed and comprehension and that's where good code lives.

+ **Be explicit and throw an error** so that problems can be spotted during development.
+ Performance-wise, be careful if you're iterating through a flat array very often, especially if it's a core piece of your program.
+  A hash function is used to map a given key to a location in the hash table.
+ `Map()` is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type.
  + `new Map()` – creates the map.
  + `map.set(key, value)` – stores the value by the key.
  + `map.get(key)` – returns the value by the key, undefined if key doesn’t exist in map.
  + `map.has(key)` – returns true if the key exists, false otherwise.
  + `map.delete(key)` – removes the value by the key.
  + `map.clear()` – removes everything from the map.
  + `map.size` – returns the current element count.
+  **A function should do one thing.**
+ Avoid duplicate logic.
+ Here are some straightforward to implement methods that can lead to easier to read code:
  + Return early from functions.
  + Cache variables so functions can be read like sentences.
  + Check for Web APIs before implementing your own functionality.
  

[Back to Mainpage](../code-fellows.md)<br>