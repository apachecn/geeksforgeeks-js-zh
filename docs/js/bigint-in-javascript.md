# JavaScript 中的斑点

> 原文:[https://www.geeksforgeeks.org/bigint-in-javascript/](https://www.geeksforgeeks.org/bigint-in-javascript/)

BigInt 是 JavaScript 中的内置对象，提供了一种表示大于 2 <sup>53</sup> -1 的整数的方法。JavaScript 可以用 number 原语可靠表示的最大数字是 2 <sup>53</sup> -1，由 **MAX_SAFE_INTEGER** 常量表示。这在需要对大量数据进行操作的情况下有多种用途。

**语法:**

```
BigInt( number ) 
or
Appending n to end of an integer literal

```

**参数:**它接受单个整数文字作为字符串，需要表示为 BigInt。

**返回类型:**该方法返回给定值作为 BigInt 数据类型。

**示例:**本示例使用 BigInt()函数创建一个 BigInt。

## java 描述语言

```
// Parameter in decimal format
var bigNum = BigInt(
  "123422222222222222222222222222222222222");
console.log(bigNum);

// Parameter in hexadecimal format
var bigHex = BigInt("0x1ffffffeeeeeeeeef");
console.log(bigHex);

// Parameter in binary format
var bigBin = BigInt(
  "0b1010101001010101001111111111111111");
console.log(bigBin);
```

**输出:**

```
123422222222222222222222222222222222222n
36893488074118328047n
11430854655n

```

**示例:**本示例通过在数字末尾追加 n 来创建 BigInt。

## java 描述语言

```
// Decimal format
var bigNum = 123422222222222222222222222222222222222n
console.log(bigNum)

// Hexadecimal format
var bigHex = 0x1ffffffeeeeeeeeefn
console.log(bigHex)

// Binary format
var bigBin = 0b1010101001010101001111111111111111n
console.log(bigBin)
```

**输出:**

```
123422222222222222222222222222222222222n
36893488074118328047n
11430854655n

```

**比较 BigInt 其他类型:**BigInt 在某些方面类似于 Number，但是，它不能与内置 Math 对象的方法一起使用，也不能与 Number 的实例在操作中混合使用。

**示例:**将 BigInt 与数字进行比较。

```
typeof 100n === 100        // Returns false
typeof 100n ==  100        // Returns true due to coercion
typeof 100n === 'bigint'   // Returns true
100n < 101                 // Returns true due to coercion

```

**排序:**数组既可以保存基元数据类型，也可以保存 BigInts。这使得**排序()**方法可以在数组中同时存在正常的数字和大整数值时工作。

**示例:**

## java 描述语言

```
// Array consisting of both
// Number and BigInt
var arr = [4, 2, 5n, 2n]

// Sorting the array
arr.sort()

console.log(arr)  // [2, 2n, 4, 5n]
```

**输出:**

```
[2, 2n, 4, 5n]
```

**使用建议:**由于 BigInt 的实现，不建议将以下应用与 BigInt 一起使用:

1.  **强制:**Number 和 BigInt 之间强制会导致精度损失，建议只在合理预期值大于 253 时使用 BigInt，不要在两种类型之间强制。
2.  **密码学:**BigInt 上支持的操作不是时间常数。因此 BigInt 不适合用于密码学。

**支持的浏览器:**支持 BigInt 方法的浏览器如下:

*   铬
*   边缘
*   火狐浏览器
*   歌剧