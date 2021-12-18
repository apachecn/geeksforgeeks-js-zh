# JavaScript Promise.race()方法

> 原文:[https://www . geesforgeks . org/JavaScript-promise-race-method/](https://www.geeksforgeeks.org/javascript-promise-race-method/)

**Promise.race()** 方法返回一个承诺，只要可重复的承诺中的一个兑现或拒绝，就兑现或拒绝该承诺，并给出该承诺的值或理由。

#### 语法:

```
Promise.race(iterable);
```

#### 参数:

*   **可迭代的:**可迭代的对象，如数组、映射、字符串等。

#### 例 1:

## java 描述语言

```
<script>
const promise1 = new Promise((resolve, reject) => {
  setTimeout(resolve, 600, "one");
});

const promise2 = new Promise((resolve, reject) => {
  setTimeout(resolve, 200, "two");
});

Promise.race([promise1, promise2]).then((value) => {
  console.log(value);
});
</script>
```

**输出:**正如所承诺的，2 打印速度更快，可以打印两个。

```
two
```

#### 例 2:

## java 描述语言

```
<script>
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => resolve("five"), 500);
});

const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => reject(new Error("six")), 100);
});

Promise.race([promise1, promise2]).then((value) => {
  console.log(value);
});
<script>
```

**输出:**

![](img/606c74dda27304da81d7a9a8b071d69e.png)

因为 promise2 比 promise1 快，所以它拒绝并不打印任何内容。

**支持的浏览器:**

*   谷歌 Chrome 6.0 及以上版本
*   Internet Explorer 9.0 及以上版本
*   Mozilla 4.0 及以上版本
*   Opera 11.1 及以上
*   Safari 5.0 及以上版本