# 401 .NET Read 10: Stacks and Queues

## Stacks
A stack is exactly that.  I stack of nodes that follow a first in last principle.  The top node on a stack is referenced as the `top`.  Nodes in a stack have a value and next property.  
When you add a new node to a list you have to set it's next to the current `top` node and the current `top` node points to the new node.
```
method Push(n)
  Node newNode = new Node(n);
  newNode.next = Top;
  Top = newNode;
```
```
method Pop(n)
  Node placeHolder = new Node();
  placeHolder = Top;
  Top = Top.Next;
  placeHolder.Next = null;
  return placeHolder.Value;
```

## QUEUES
A queues is like a stack but it's first in first out.  So who ever gets in line first gets in first.  The first node in the queue is the `front` and the last is the `rear`.
```
method Enqueue(n)
  Node newNode = new Node(n);
  Rear.Next = newNode;
  Rear = newNode;
```


[Back to the main page](../README.md) 