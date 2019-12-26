---
title: 238. Product of Array Except Self
tags:
  - leetcode
categories:
  - Data Structures & Algorithms
  - null
date: 2019-12-12 11:44:32
---


### <span style="background-color: #FFFBCC"> Problem

Given an array nums of n integers where n > 1, return an array output such that output[i] is equal to the product of all the elements of nums except nums[i].

<!-- more -->

Example:

```
Input:  [1,2,3,4]
Output: [24,12,8,6]
```

Note: Please solve it without division and in O(n).

Follow up:
Could you solve it with constant space complexity? (The output array does not count as extra space for the purpose of space complexity analysis.)

[Question Source - Leetcode](https://leetcode.com/problems/product-of-array-except-self/)

### <span style="background-color: #FFFBCC"> Solution

Break down of solution array

     [1, 2, 3, 4]
    -> [24, 12, 8, 6]
    =  [2*3*4, 1*3*4, 1*2*4, 1*2*3]
    =  [     , 1    , 1*2  , 1*2*3] (L)
      *[2*3*4,   3*4,     4,      ] (R)

```javascript
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var productExceptSelf = function(nums) {
  let n = nums.length
  let L = new Array(n)
  let R = new Array(n)
  let res = new Array(n)

  for (i = 1; i < n; i++) {
    L[0] = 1
    L[i] = L[i - 1] * nums[i - 1]
  }

  for (i = n - 2; i >= 0; i--) {
    R[n - 1] = 1
    R[i] = R[i + 1] * nums[i + 1]
  }

  for (i = 0; i < n; i++) {
    res[i] = L[i] * R[i]
  }
  return res
}
```

Time Complexity: O(3N) ≈ O(N)
Space Complexity: O(N)
