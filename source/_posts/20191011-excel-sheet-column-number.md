---
title: Excel Sheet Column Number
tags:
  - leetcode
categories:
  - Data Structure & Algorithm
  - String
date: 2019-10-11 22:08:35
---
### <span style="background-color: #FFFBCC"> Problem
Given a column title as appear in an Excel sheet, return its corresponding column number.

<!-- more --> 

For example:
```
    A -> 1
    B -> 2
    C -> 3
    ...
    Z -> 26
    AA -> 27
    AB -> 28 
    ...
```

__Example 1:__
```
Input: "A"
Output: 1
```
__Example 2:__
```
Input: "AB"
Output: 28
```

### <span style="background-color: #FFFBCC"> Attempt
- Convert alphabet to integer

__Solution__
```javascript
var titleToNumber = function(s) {
    let sum = 0
    let n = s.length
    for(i=0;i<n;i++){
        let num = s.charCodeAt(i) - 64
        sum += Math.pow(26,n-1-i) * num
    }
    return sum
};
```
-----
_[Question Source - Leetcode](https://leetcode.com/problems/excel-sheet-column-number/)_