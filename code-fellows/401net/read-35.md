# 401 .NET Read 35: Graphs


A graph is a data structure that can hold multiple nodes, each having zero to multiple connections with other nodes in the struct.

Nodes in a `Graph` are called `Vertices` and the connections are called `Edges`.  A binary tree is an example of a graph.

Graphs can be directed and undirected.  This means that an edge can either just connect two vertices, or it can connect them with a directional flow.

+ A complete graph is when every node is connected by ane dge to every other node.
+ A connected graph is basically a kAryTree.
+ A disconnected graph is one which contains nodes that do not attach to any other nodes.  These are referred to as islands.

Graphs can by Acyclic and Cyclic.
Acyclic - nodes only attach to each other in a linear way.
Cyclic - nodes may eventually connect back to each other creating a loop.

We cant Traverse a graph either using a breadth first or depth method.  Breadth first is similar to a binary tree and uses a queue to move tier by tier through the struct.

For an order search we use a stack in a similar way to breadth first.

To avoid infinite loops on cyclical graphs we will also employee a hashTable to track nodes that we've already looked at.

[Back to Mainpage](../code-fellows.md)<br>