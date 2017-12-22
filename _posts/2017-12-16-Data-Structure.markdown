---
layout: post
title: Data structure
date: 2017-12-12 00:00:00 +0300
description:  # Add post description (optional)
img: how-to-start.jpg # Add image post (optional)
tags: [Competitive programming] # add tag
---


# Data Structure
1. Arrays
2. Linked Lists  
A typical linked list implementation
```Java
class ListNode{
  String data;
  ListNode nextNode;
}
ListNode firstNode;
```
you can then write a method to add new nodes by inserting them at the begining of the list:  
```Java
ListNode newNode = new ListNode();
newNode.nextNode = firstNode;
firstNode = newNode;
```
Iterating through all of the items in the list is a simple task:
```Java
ListNode curNode = firstNode;
while(curNode!=null){
  ProcessData(curNode);
  curNode = curNode.nextNode;
}
```

3. Queues  
the most common use of a queue is to implement a Breadth First Search .
**BSF** means to first explore all the states that can be reached in one step, then all states that can be reached in two steps. etc. A queue assists in implementing this solution because it stores a list of all state speaces that have been visited.  
Whenever a **shortest path** or **least number of moves** is requestedm there is a good chance that a BFS, using a queue, will lead to a successful solution.  
```Java
class StateNode{
  int xPos;
  int yPos;
  int moveCount;
}
class MyQueue{
  StateNode[] queueData - new StateNode[2500];
  int queueFront = 0;
  int queueBack= 0;

  void Enqueue(StateNode node){
    queueData[queueBack] = node;
    queueBack++;
  }

  StateNode Dequeue(){
    StateNode returnValue = null;
    if(queueBack>queueFront){
      returnValue = queueData[queueFront];
      queueFront++;
    }
    return returnValue;
  }

  boolean isNotEmpty(){
    return (queueBack>queueFront);
  }
}
```

4. Stacks
5. Trees  
One of most common examples of tree is an XML document. The top-level; document element is the root node and each tag found within that is a child. Each of those tags may have children, and so on.  
[PermissionTree](http://community.topcoder.com/stat?c=problem_statement&pm=3093&rd=5864) provides an unusual problem on a common file system.  
[bloggoDocStructure](http://community.topcoder.com/stat?c=problem_statement&pm=3025&rd=5860) is another good example of a problem using trees.  

6. Binary trees  
  - A special type of tree is a binary tree.  
  - most efficient way to store and read records that can be indexed by a key value in some way  
  - each node has at most 2 children  
7. Priority Queues  
  - a special type of binary tree called a heap is typically used for priority queues.   
8. HashTables
HashTables are a unique data structure and are typically used to implement a "dictionary" interface, whereby a set of keys each has an associated value.  
