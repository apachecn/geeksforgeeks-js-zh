# JavaScript Promise 构造函数

> 原文:[https://www . geesforgeks . org/JavaScript-promise-constructor/](https://www.geeksforgeeks.org/javascript-promise-constructor/)

JavaScript **承诺**用于处理 JavaScript 中的异步操作。当处理多个异步操作时，它们很容易管理，其中回调会创建回调地狱，导致无法管理的代码。

**JavaScript 中的 Promise 构造函数**主要用于包装已经不支持 Promise 的函数。

**语法:**

```
new Promise(executor)
```

**参数:**

*   **执行者:**执行者可以是将结果与承诺联系起来的自定义代码。你，程序员，写遗嘱执行人。

**返回值:**另一个承诺对象，在这种情况下，承诺被动态插入到链中。

**示例 1:** 仅创建一个承诺构造函数。

## java 描述语言

```
<script>
// Creating an new promise and resolving geeks for geeks
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('geeks for geeks');
  }, 100);
});

promise1.then((value) => {
  console.log(value);
 // output will be : geeks for geeks
});

// output will be : [object Promise]
console.log(promise1);
</script>
```

**输出:**

![](img/d88ada1223d7b98a5f24ab30db7a255d.png)

**示例 2:** 在这段代码中，我们将创建两个承诺构造函数。

## java 描述语言

```
<script>
// Creating first promise constructor
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('geeks for geeks');
  }, 100);
});

////creating second promise constructor
const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('computer science portal');
  }, 100);
});

promise2.then((value) => {
  console.log(value);
  // output: "computer science portal"
});

promise1.then((value) => {
  console.log(value);
  //  output: "geeks for geeks"
});
console.log(promise1);
// output: [object Promise]
</script>
```

**输出:**

![](img/0eda875095ff4819d2fd986a3eaae519.png)

**示例 3:** 显示值

## java 描述语言

```
<script>// Creating first promise constructor
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('geeks for geeks');
  }, 100);
});

// Creating second promise constructor
const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('computer science portal');
  }, 100);
});

promise2.then((value) => {
  console.log(value);
  // output: "computer science portal"
});

promise1.then((value) => {
  console.log(value);
  //  output: "geeks for geeks"
});
console.log(2+3);
// output: [object Promise]
</script>
```

**输出:**

![](img/9e2934742824e5823715ecb2b2b560ff.png)