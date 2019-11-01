---
title: Grading Students
tags:
  - hacker rank
categories:
  - Data Structures & Algorithms
  - Array
date: 2019-10-15 09:25:52
---

### <span style="background-color: #FFFBCC"> Problem

HackerLand University has the following grading policy:

- Every student receives a `grade` in the inclusive range from `0` to `100`.
  Any `grade` less than `40` is a failing grade.

Sam is a professor at the university and likes to round each student's according to these rules:

- If the difference between the `grade` and the next multiple of `5` is less than `3`, round `grade` up to the next multiple of `5`.
- If the value of `grade` is less than `38`, no rounding occurs as the result will still be a failing grade.

<!-- more -->

**For example:**
Sample Input

```
4
73
67
38
33
```

Sample Output

```
75
67
40
33
```

### <span style="background-color: #FFFBCC"> Attempt

- Convert alphabet to integer

**Solution**

```javascript
let ans = []
for (let i = 0; i < grades.length; i++) {
  if (grades[i] < 38) {
    //failing grade
    ans.push(grades[i])
  } else if (grades[i] % 5 < 3) {
    //do not round up
    ans.push(grades[i])
  } else if (grades[i] % 5 >= 3) {
    //round up
    let roundUp = Math.ceil(grades[i] / 5) * 5
    ans.push(roundUp)
  }
}
return ans
```

---

_[Question Source - Hacker Rank](https://www.hackerrank.com/challenges/grading/problem)_
