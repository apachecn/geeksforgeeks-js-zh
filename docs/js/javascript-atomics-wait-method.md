# JavaScript | Atomics.wait()方法

> 原文:[https://www . geesforgeks . org/JavaScript-atomics-wait-method/](https://www.geeksforgeeks.org/javascript-atomics-wait-method/)

在原子操作中，有一个内置的操作 atomics。JavaScript 中的 wait()用于验证 **Int32Array** 中的给定位置是否仍包含给定值，如果包含，则休眠，等待唤醒或超时。 **Atomics.wait()** 操作返回一个字符串，该字符串为“ok”、“不相等”或“超时”。整数 typedarray、索引和值作为参数传递给函数，超时也是一个参数，但它是可选的。
**语法:**

```
Atomics.wait(typedArray, index, value, timeout)
```

**参数:**该方法接受上述四个参数，描述如下:

*   **typedarray:** 此参数指定共享整数类型数组 Int16Array。
*   **索引:**此参数指定数组中的位置，键入等待的时间。
*   **值:**该参数指定测试的期望值。
*   **超时:**该参数为可选参数。等待的时间是毫秒。

**返回值:****atomics . wait()**方法返回“正常”、“不相等”或“超时”的字符串。
**例:**

```
Input: arr[0] = 5
        Atomics.wait(arr, 0, 0, 1)
Output: not-equal

Input: arr[0] = 4
        Atomics.wait(arr, 1, 0, 1)
Output: time-out
```

下面的程序说明了 JavaScript 中的 **Atomics.wait()方法:
**程序 1:**** 

## java 描述语言

```
var buf = new SharedArrayBuffer(1024);
var arr = new Int32Array(buf);

arr[0] = 5;
console.log(Atomics.load(arr, 0));
console.log(Atomics.and(arr, 0, 9));
console.log(Atomics.wait(arr, 0, 0, 1));
console.log(Atomics.load(arr, 0));
```

**输出:**

```
5
5
not-equal
1
```

**节目 2:**

## java 描述语言

```
var buf = new SharedArrayBuffer(1024);
var arr = new Int32Array(buf);

arr[0] = 5;
console.log(Atomics.load(arr, 0));
console.log(Atomics.and(arr, 0, 9));
console.log(Atomics.wait(arr, 1, 0, 1));
console.log(Atomics.load(arr, 0));
```

**输出:**

```
5
5
time-out
1
```

**例外:**

*   如果 typedArray 不是共享的 Int32Array，那么 Atomics.wait()操作将引发 TypeError。
*   如果用作 Atomics.wait()操作参数的索引超出了 typedArray 中的界限，则 Atomics.store()操作将引发 RangeError。

**支持的浏览器:**

*   谷歌 Chrome
*   微软边缘
*   火狐浏览器