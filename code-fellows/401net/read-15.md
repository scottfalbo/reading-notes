# 401 .NET Read 15: Binary Trees

## Parts of a  Binary Tree

A binary tree is a structure or `Node` objects.  The top node in the tree is called the `Root`.  Each node can have a `Left Child`, or `Right Child` creating two paths for each node.

The link between each node is called the `Edge`.

The last node on a branch that has no children is referred to as a `Leaf`.

The `Height` of a tree is defined by how many edges exist between the root and the bottommost leaf.

## Transversal
+ ### Depth First
  + Pre-order - `root - > left -> right`
    + Starts at the top printing left to right for each level.
  + In-order - `left -> root -> right`
    + Prints in order from left, to center, to right.  Basically the left most node is returned, then the next left most, and the next until empty.
  + Post-order - `left -> right -> root`
    + Prints the entire left side of tree left to right.  Then the entire right side, left to right, then the root.
+ ### Breadth first
  + Uses a `Queue` to go through and print top to bottom, left to right.

## Binary Search Tree
A `Binary Search Tree` organizes the nodes based on value.  If a new node is less than the root value it goes on the left, if its greater it goes on the right.

This allows for quicker more memory efficient searches because we don't have to iterate through the entire tree to find what we are looking for.

[Back to Mainpage](../code-fellows.md)<br>