---
title: Delete Node In a Singly Linked List
tags:
  - linked list
  - leetcode
categories:
  - Data Structure & Algorithm
date: 2019-10-02 15:48:28
---
<sub>_[Source - Leetcode](https://leetcode.com/problems/delete-node-in-a-linked-list/)_</sub>

### <span style="background-color: #FFFBCC"> Problem 
Write a function to delete a node (except the tail) in a singly linked list, given only access to that node.

<!-- more -->

Given linked list -- head = [4,5,1,9]
__Example 1__:
```
Input: head = [4,5,1,9], node = 5
Output: [4,1,9]
```
__Example 2__:
```
Input: head = [4,5,1,9], node = 1
Output: [4,5,9]

```

Note:

- The linked list will have at least two elements.
- All of the nodes' values will be unique.
- The given node will not be the tail and it will always be a valid node of the linked list.
- Do not return anything from your function.

### <span style="background-color: #FFFBCC"> Approach
1. Delete the first node
2. Assign next node to head

```javascript
var deleteNode = function(node) {    
        node.val = node.next.val
        node.next = node.next.next
};
```

### Take Away
- [Deleting the Linked List](https://leetcode.com/explore/learn/card/linked-list/209/singly-linked-list/1289/)
