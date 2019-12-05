---
title: 217. Contains Duplicate
tags:
  - leetcode
categories:
  - Data Structures & Algorithms
  - Array
date: 2019-11-12 10:08:23
---

### <span style="background-color: #FFFBCC"> Problem

Given an array of integers, find if the array contains any duplicates.

Your function should return true if any value appears at least twice in the array, and it should return false if every element is distinct.

<!-- more -->

Example 1:

```
Input: [1,2,3,1]
Output: true
```

Example 2:

```
Input: [1,2,3,4]
Output: false
```

Example 3:

```
Input: [1,1,1,3,3,4,3,2,4,2]
Output: true
```

### <span style="background-color: #FFFBCC"> Solution

#### Sort & Compare

```javascript
/**
 * @param {number[]} nums
 * @return {boolean}
 */
var containsDuplicate = function(nums) {
  var sorted = nums.sort();
  for (i = 1; i < sorted.length; i++) {
    if (sorted[i] == sorted[i - 1]) return true;
  }
  return false;
};
```

- Time Complexity: O(N lgN)
- Space Complexity: O(1)

#### Using Hashmap

```javascript
/**
 * @param {number[]} nums
 * @return {boolean}
 */
var containsDuplicate = function(nums) {
  let hashmap = {};
  for (i = 0; i < nums.length; i++) {
    let num = nums[i];
    hashmap[num] ? hashmap[num]++ : (hashmap[num] = 1);
    if (hashmap[num] !== 1) return true;
  }
  return false;
};
```

- Time Complexity: O(N)
- Space Complexity: O(N)

#### Using Hash Map

```javascript
/**
 * @param {number[]} nums
 * @return {boolean}
 */
var containsDuplicate = function(nums) {
  let hashmap = {};
  for (i = 0; i < nums.length; i++) {
    let num = nums[i];
    hashmap[num] ? hashmap[num]++ : (hashmap[num] = 1);
    if (hashmap[num] !== 1) return true;
  }
  return false;
};
```
