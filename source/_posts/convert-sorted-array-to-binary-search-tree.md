---
title: Convert Sorted Array To Binary Search Tree
tags:
  - tree
  - depth-first search
  - leetcode
categories:
  - Data Structure & Algorithm
date: 2019-10-07 22:08:35
---
<sub>_[Source - Leetcode](https://leetcode.com/problems/convert-sorted-array-to-binary-search-tree/)_</sub>

### <span style="background-color: #FFFBCC"> Problem
Given an array where elements are sorted in ascending order, convert it to a height balanced BST.

For this problem, a height-balanced binary tree is defined as a binary tree in which the depth of the two subtrees of every node never differ by more than 1.

<!-- more --> 

__Example 1:__
```
Given the sorted array: [-10,-3,0,5,9],

One possible answer is: [0,-3,9,-10,null,5], which represents the following height balanced BST:

      0
     / \
   -3   9
   /   /
 -10  5
```

### <span style="background-color: #FFFBCC"> Attempt
- Tree problems can usually be solved by recursive / iterative approach.
- Since the BST takes lower number to the left of a node & higher number to the right, the number on the middle should be the most parent node.

__Recursive Solution__
```javascript
var sortedArrayToBST = function(nums) {
    //Corner case to break out of recursive calls
    if (!nums.length) return null;
    //Declarations 
    let n = nums.length
    let mid = Math.floor(nums.length/2)
    let node = new TreeNode(nums[mid])
    //Recursive calls
    node.left = sortedArrayToBST(nums.slice(0,mid)) //tasks the lower value
    node.right = sortedArrayToBST(nums.slice(mid+1)) //tasks the higher value
    return node
};
```