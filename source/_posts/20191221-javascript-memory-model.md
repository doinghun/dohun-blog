---
title: Memory Model
date: 2019-12-21 23:51:54
categories:
  - Programming
  - JavaScript
thumbnail: /2019/12/21/javascript-memory-model/js-memory-model.png
---

Using JavaScript, declaring variables, initializing them, and assigning them new values later on is something we do on a daily basis. So what actually happens in memory when we declare & assign value?

<!--more-->

### Variable declarations and assignments for JS primitives

```javascript
let myNumber = 23;
let newVar = myNumber;
myNumber = myNumber + 1;
```

 <center>{% asset_img 'js-memory-model1.jpeg' 400 %}</center>

> The call stack is where primitives are stored (in addition to function calls). While the heap is where non-primitives are stored. The key difference is that the heap can store unordered data that can grow dynamically—perfect for arrays and objects.

### Variable declarations and assignments for JS non-primitives

What actually happens in memory when we declare & assign value?

```javascript
let myArray = [];
```

 <center>{% asset_img 'js-memory-model2.jpeg' 400 %}</center>

### Let vs Const

> The correct way to interpret “change” is a change in memory address. Let allows you to change memory addresses. Const does not allow you to change memory addresses.

```javascript
let sum = 0;
sum = 1 + 2 + 3 + 4 + 5;
let numbers = []; // WRONG! Use const
numbers.push(1);
numbers.push(2);
numbers.push(3);
numbers.push(4);
numbers.push(5);
```

> Google, who has some of the best coders in the world, says in their JavaScript style guide, “Declare all local variables with either const or let. Use const by default, unless a variable needs to be reassigned. The var keyword must not be used”

---

_Reference_:

- https://medium.com/@ethannam/javascripts-memory-model-7c972cd2c239
