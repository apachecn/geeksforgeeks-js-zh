# JavaScript | Atomics.notify()方法

> 原文:[https://www . geesforgeks . org/JavaScript-atomics-notify-method/](https://www.geeksforgeeks.org/javascript-atomics-notify-method/)

在原子操作中，JavaScript 中有一个内置的操作 Atomics.notify()，用于通知一些正在等待队列中睡眠的代理。方法返回一些被唤醒的代理。整数类型的数组、索引和计数作为参数传递给函数。
**语法:**

```
Atomics.notify(typedArray, index, count)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **typedarray:** 此参数指定共享整数类型数组 Int16Array。
*   **索引:**此参数指定数组中的位置，键入等待的时间。
*   **计数:**此参数统计要通知的休眠座席数。它的默认值是+Infinity。

**返回值:****atomics . notify()方法**返回被唤醒的座席数。
下面的程序说明了 JavaScript 中的 **Atomics.notify()方法:
**程序 1:**** 

## java 描述语言

```
const sab = new SharedArrayBuffer(1024);
const int32 = new Int32Array(sab);
int32[0] = 77;
console.log(int32[0]);
console.log(Atomics.store(int32, 0, 123));
console.log(Atomics.notify(int32, 0, 1));
```