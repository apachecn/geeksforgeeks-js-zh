# JavaScript | bigint . asuint()方法

> 原文:[https://www . geesforgeks . org/JavaScript-bigint-ASU intn-method/](https://www.geeksforgeeks.org/javascript-bigint-asuintn-method/)

**BigInt . Asintn()**方法是 JavaScript 中的内置方法，用于将 Bigint 值包装为 0 到 2 之间的无符号整数<sup>宽度</sup> -1。
**语法:**

```
BigInt.asUintN (width, bigint);
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **宽度:**此参数保存整数大小的可用位数。
*   **bigint:** 此参数保存要箝位的整数，以适合所提供的位。

**返回值:**该方法以无符号整数形式返回 bigint 模 2 <sup>宽度</sup>的值。
以下示例说明了 JavaScript 中的 BigInt.asUintN()方法:
**示例 1:**

## java 描述语言

```
<script>
let maxlimit = 2n ** (64n - 1n) - 1n;

function GFG(num) {
  (num > maxlimit) ?
    console.log("Number exceed the limit "
           + "of signed 64-bit integer!");
    console.log(BigInt.asUintN(64, num));
}

GFG(2n ** 16n);
GFG(2n ** 32n);
GFG(2n ** 64n);
</script>    
```

**输出:**

```
65536n
4294967296n
"Number exceed the limit of signed 64-bit integer!"
```

**例 2:**

## java 描述语言

```
<script>
const max = 2n ** (64n - 1n) - 1n;

console.log(BigInt.asUintN(64, max));
console.log(BigInt.asUintN(64, max + 1n));
console.log(BigInt.asUintN(32, max));
</script>
```

**输出:**

```
9223372036854775807n
9223372036854775808n
4294967295n
```

**支持的浏览器:**bigint . asuint()方法支持的浏览器如下:

*   谷歌 Chrome 67 及以上
*   边缘 79 及以上
*   Firefox 68 及以上版本
*   歌剧 54 及以上
*   Safari 14 及以上