---
title: Callbacks, Promises & Async Await
categories:
  - Programming
  - JavaScript
date: 2019-12-24 23:57:52
thumbnail: /2019/12/24/callback-promises-async-await/callback-hell-cover.png
---

There are different ways to execute asynchronous function in JavaScript.

<!-- more -->

To call a function that does following task:

- Print a string `A`, `B`, `C` in order
- After a random amount of time.

### Callbacks

```javascript
function printString(string, callback) {
  setTimeout(() => {
    console.log(string);
    callback();
  }, Math.floor(Math.random() * 100) + 1);
}

function printAll() {
  printString("A", () => {
    printString("B", () => {
      printString("C", () => {});
    });
  });
}
printAll();
```

Callback Hell

- Nesting functions within functions within functions
- Hard to read the code.

### Promises

```javascript
function printString(string) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log(string);
      resolve();
    }, Math.floor(Math.random() * 100) + 1);
  });
}

function printAll() {
  printString("A")
    .then(() => printString("B"))
    .then(() => printString("C"));
}
printAll();
```

The code is no longer nested but it still looks messy!

### Await

```javascript
function printString(string) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log(string);
      resolve();
    }, Math.floor(Math.random() * 100) + 1);
  });
}

async function printAll() {
  await printString("A");
  await printString("B");
  await printString("C");
}
printAll();
```

Await is basically syntactic sugar for Promises. It makes your asynchronous code look more like synchronous/procedural code, which is easier for humans to understand.

---

_Reference:_

- https://medium.com/front-end-weekly/callbacks-promises-and-async-await-ad4756e01d90
- https://medium.com/codebuddies/getting-to-know-asynchronous-javascript-callbacks-promises-and-async-await-17e0673281ee
