---
title: Reverse String
tags:
  - leetcode
categories:
  - Data Structures & Algorithms
  - String
date: 2019-10-31 16:35:50
---

### <span style="background-color: #FFFBCC"> Problem

Write a function that reverses a string. The input string is given as an array of characters char[].

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

You may assume all the characters consist of printable ascii characters.

<!-- more -->

Example 1:

```
Input: ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
```

Example 2:

```
Input: ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]
```

_[Question Source: LeetCode](https://leetcode.com/problems/reverse-string/)_

### <span style="background-color: #FFFBCC"> Solution

```javascript
/**
 * @param {character[]} s
 * @return {void} Do not return anything, modify s in-place instead.
 */
var reverseString = function(s) {
  let n = s.length
  let temp = 0
  // Iterate for half the number of string
  for (let i = 0; i < n / 2; i++) {
    // Store 1st half chars in dummy
    temp = s[i]
    // Swap 2nd half char with 1st half
    s[i] = s[n - 1 - i]
    // Release stored value to 2nd half chars
    s[n - 1 - i] = temp
  }
}
```

- Runtime: `O(n)`
- Space: `O(1)`
