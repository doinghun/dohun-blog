---
title: missing-number
tags:
  - leetcode
categories:
  - Data Structure & Algorithm
  - Array
---

### <span style="background-color: #FFFBCC"> Problem

Given an array containing n distinct numbers taken from 0, 1, 2, ..., n, find the one that is missing from the array.

Example 1:

```
Input: [3,0,1]
Output: 2
```

Example 2:

```
Input: [9,6,4,2,3,5,7,0,1]
Output: 8
```

Note:
Your algorithm should run in linear runtime complexity. Could you implement it using only constant extra space complexity?

### <span style="background-color: #FFFBCC"> Attempt

1st Attempt

```javascript
var missingNumber = function(nums) {
  nums.sort((a, b) => a - b);
  for (i = 0; i <= nums.length; i++) {
    if (i !== nums[i]) {
      return i;
    }
  }
};
```

Improved

```javascript
var missingNumber = function(nums) {
  let n = nums.length;
  let sum = ((0 + n) * (n + 1)) / 2;
  for (i = 0; i < n; i++) {
    sum -= nums[i];
  }
  return sum;
};
```

Bitwise

```javascript
var missingNumber = function(nums) {
  let res = nums.length;
  for (i = 0; i < nums.length; i++) {
    res ^= i ^ nums[i];
  }
  return res;
};
```

---

_[Question Source - Leetcode](https://leetcode.com/problems/missing-number/)_
