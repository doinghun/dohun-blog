---
title: Permutations
tags:
  - leetcode
categories:
  - Data Structure & Algorithm
  - Backtracking
date: 2019-10-23 00:18:07
---

### <span style="background-color: #FFFBCC"> Problem

Given a collection of **distinct** integers, return all possible permutations.

<!-- more -->

Example:

```javascript
Input: [1, 2, 3];
Output: [[1, 2, 3], [1, 3, 2], [2, 1, 3], [2, 3, 1], [3, 1, 2], [3, 2, 1]];
```

### <span style="background-color: #FFFBCC"> Attempt

- https://leetcode.com/problems/permutations/discuss/293217/Javascript-Backtracking-with-Explanation-beats-99

```javascript
/**
 * @param {number[]} nums
 * @return {number[][]}
 */
const permute = function(nums) {
  const result = [];
  const temp = [];
  findPermutations(temp, nums, result);
  return result;
};

const findPermutations = (temp, nums, result) => {
  if (!nums.length) {
    result.push(temp.concat());
    return;
  }

  for (var i = 0; i < nums.length; i++) {
    const newNum = nums[i];
    temp.push(newNum);
    nums.splice(i, 1);
    findPermutations(temp, nums, result);
    temp.pop();
    nums.splice(i, 0, newNum);
  }
};
```

---

_[Question Source - Leetcode](https://leetcode.com/problems/permutations/)_
