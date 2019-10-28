---
title: remove-duplicate-from-sorted-array
tags:
---

1st Attempt

```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var removeDuplicates = function(nums) {
  let i = 0
  while (i < nums.length) {
    if (nums[i] == nums[i + 1]) nums.splice(i, 1)
    else {
      i++
    }
  }
}
```

```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var removeDuplicates = function(nums) {
  let i = 0
  for (let j = 0; j < nums.length; j++) {
    if (nums[j] != nums[i]) nums[++i] = nums[j]
  }
  return ++i
}
```
