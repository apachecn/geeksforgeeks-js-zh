# JavaScript | bigint . prototype . tostring()方法

> 原文:[https://www . geesforgeks . org/JavaScript-big int-prototype-tostring-method/](https://www.geeksforgeeks.org/javascript-bigint-prototype-tostring-method/)

**BigInt . prototype . ToString()**方法是 JavaScript 中的一个内置方法，用于返回表示指定 BigInt 对象的字符串。
**语法:**

```
bigIntObj.toString( radix )
```

**参数:**该功能接受单个参数，为可选参数。

*   **基数:**是 2 到 36 范围内的整数值。

**返回值:**这个方法返回一个代表指定 BigInt 对象的字符串。
**异常:** A ***范围错误*** 如果 toString()小于 2 或大于基数 36，则抛出。
以下示例说明了 JavaScript 中的 BigInt.prototype.toString()方法:
**示例 1:**

## java 描述语言

```
console.log(1023n.toString());

console.log(1023n.toString(2));

console.log(1023n.toString(9));

console.log((-0n).toString());  

console.log(BigInt(-0).toString());
```