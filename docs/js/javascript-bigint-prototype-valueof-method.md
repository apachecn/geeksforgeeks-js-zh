# JavaScript | Bigint . prototype . valueof()方法

> 原文:[https://www . geesforgeks . org/JavaScript-big int-prototype-value of-method/](https://www.geeksforgeeks.org/javascript-bigint-prototype-valueof-method/)

**BigInt . prototype . ToString()**方法是 JavaScript 中的一个内置方法，用于返回 BigInt 对象的包装基元值。
**语法:**

```
bigIntObj.valueOf()
```

**参数:**此方法不接受任何参数。
**返回值:**这个方法返回一个 BigInt，表示指定 BigInt 对象的基元值。
以下示例说明了 JavaScript 中的 BigInt.prototype.toString()方法:
**示例 1:**

## java 描述语言

```
console.log(typeof Object(1324n));
console.log(typeof Object(24324).valueOf());
```

**输出:**

```
"object"
"number"
```

**例 2:**

## java 描述语言

```
console.log(typeof Object("GeeksforGeeks"));
console.log(typeof Object("GeeksforGeeks").valueOf());
```

**输出:**

```
"object"
"string"
```

**支持的浏览器:**bigint . prototype . value of()方法支持的浏览器如下:

*   谷歌 Chrome 67 及以上
*   边缘 79 及以上
*   Firefox 68 及以上版本
*   歌剧 54 及以上
*   Safari 14 及以上