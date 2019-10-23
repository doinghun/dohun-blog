---
title: reverse-string
tags:
---

leetcode

```javascript
/**
 * @param {character[]} s
 * @return {void} Do not return anything, modify s in-place instead.
 */
var reverseString = function(s) {
  let n = s.length;
  let temp = 0;
  for (let i = 0; i < n / 2; i++) {
    temp = s[i];
    s[i] = s[n - 1 - i];
    s[n - 1 - i] = temp;
  }
};
```
