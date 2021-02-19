# 401 .NET Read 30: Hash Tables

A hash table is an array of key: value pairs.  When a value is entered the key is hashed, providing an index number.  The key:value pair then lives at that index in the array.

This creates an O(1) search time because we can do directly to an index based on a hash code as opposed to iterating through the entire array checking each value, which would be an O(N).

If more than one value shares the same hashed key the bucket will employee a linked list to hold multiple key:value pairs.

[Back to the main page](../README.md) 