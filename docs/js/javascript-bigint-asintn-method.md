# JavaScript | BigInt.asIntN()方法

> 原文:[https://www . geesforgeks . org/JavaScript-bigint-asitn-method/](https://www.geeksforgeeks.org/javascript-bigint-asintn-method/)

**BigInt . asitn()**方法是 JavaScript 中的一个内置方法，用于将 BigInt 值包装为-2 <sup>width-1</sup> 和 2 <sup>width-1</sup> -1 之间的有符号整数。
**语法:**

```
BigInt.asIntN(width, bigint);;
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **宽度:**此参数保存整数大小的可用位数。
*   **bigint:** 此参数保存要箝位的整数，以适合所提供的位。

**返回值:**该方法将 bigint 模 2 <sup>宽度</sup>的值作为有符号整数返回。
以下示例说明了 JavaScript 中的**bigint . asitn()方法**:
**示例 1:**

## java 描述语言

```
let maxlimit = 2n ** (64n - 1n) - 1n;

function GFG(num) {
  (num > maxlimit) ?
    console.log("Number exceed the limit of"+
                  " signed 64-bit integer!") :
    console.log(BigInt.asIntN(64, num));
}

GFG(2n ** 16n);
GFG(2n ** 32n);
GFG(2n ** 64n);     
```